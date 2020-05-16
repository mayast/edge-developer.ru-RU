---
title: Поддержка подключения к Интернету и сети в прогрессивных веб-приложениях
description: Сведения о том, как использовать поддерживающие технологии для создания отказоустойчивых интерфейсов для различных условий сети.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: прогрессивные веб-приложения, PWA, EDGE, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 58ffb8e9ae596dec4b99143a3061995a6598ce44
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659309"
---
# Поддержка подключения к Интернету и сети в прогрессивных веб-приложениях

В течение многих лет Организации были неохотно за незначительное количество инвестиций в веб-приложения по сравнению с машинным обеспечением, поскольку веб-приложение зависело от стабильных сетевых подключений. На сегодняшний день веб-платформа теперь поддерживает надежные параметры, позволяющие пользователям продолжать работу, даже если сетевое подключение работает нестабильно или полностью выходит из сети.

## Повышение производительности PWAs с помощью кэширования

С введением [сотрудников обслуживания][MDNServiceWorker]веб-платформа добавила `Cache` API, чтобы предоставить доступ к управляемым кэшированным ресурсам. Этот API-интерфейс на основе обещаний позволяет разработчикам хранить и извлекать большое количество веб-ресурсов: HTML, CSS, JavaScript, изображений, JSON и т. д. Обычно API кэша используется в контексте сотрудника службы, но он также доступен в основном потоке `window` объекта.

Чаще всего API используется для `Cache` предварительного кэширования ресурсов при установке сотрудника службы, как показано в следующем фрагменте кода.  

```javascript
self.addEventListener( "install", function( event ){
    event.waitUntil(
        caches.open( "static-cache" )
              .then(function( cache ){
            return cache.addAll([
                "/css/main.css",
                "/js/main.js",
                "/img/favicon.png",
                "/offline/"
            ]);
        })
    );
});
```  

Этот код, который запускается во время `install` события жизненного цикла рабочего процесса службы, открывает кэш с именем, `static-cache` а затем, когда он имеет указатель на кэш, добавляет в него четыре ресурса с помощью `addAll()` метода.  Часто подход связан с извлечением кэша во время `fetch` события   

```javascript
self.addEventListener( "fetch", event => {
    const request = event.request,
                    url = request.url;
    
    // If we are requesting an HTML page.
    if ( request.headers.get("Accept").includes("text/html") ) {
        event.respondWith(
            // Check the cache first to see if the asset exists, and if it does, return the cached asset.
            caches.match( request )
                  .then( cached_result => {
                if ( cached_result ) {
                    return cached_result;
                }
                // If the asset is not in the cache, fallback to a network request for the asset, and proceed to cache the result.
                return fetch( request )
                       .then( response => {
                    const copy = response.clone();
                    // Wait until the response we received is added to the cache.
                    event.waitUntil(
                        caches.open( "pages" )
                              .then( cache => {
                            return cache.put( request, response );
                        });
                    );
                    return response;
                })
                // If the network is unavailable to make a request, pull the offline page out of the cache.
                .catch(() => caches.match( "/offline/" ));
            })
        ); // end respondWith
    } // end if HTML
});
```  

Фрагмент кода запускается в рамках сотрудника службы всякий раз, когда браузер выполняет `fetch` запрос для этого сайта. Внутри этого события есть условный оператор, который выполняется, если запрос предназначен для HTML-файла. Рабочий процесс пытается проверить, существует ли файл в каком-либо кэше \ (с помощью `match()` метода \). Если запрос существует в кэше, возвращается этот кэшируемый результат. Если это не так, `fetch` будет запущен новый ресурс, а копия ответа будет помещена в кэш для дальнейшего, и будет возвращен ответ. Если это `fetch` не удается из-за того, что сеть недоступна, из кэша будет возвращена автономная страница.

В этом простом вводе показано, как использовать кэширование в последовательном веб-приложении (PWA). Каждый PWA отличается и может использовать различные стратегии кэширования. Код может выглядеть по-разному, и вы можете использовать различные стратегии кэширования для разных маршрутов в одном приложении.

## Использование IndexedDB в PWA для хранения структурированных данных

`IndexedDB` — это API для хранения структурированных данных. Аналогично `Cache` API-интерфейсом, он также является асинхронным, что означает, что вы можете использовать его в основном потоке или с веб-сотрудниками, например сотрудниками служб. Используйте `IndexedDB` API для хранения значительной структуры структурированных данных на клиентском компьютере, а также двоичных данных, таких как зашифрованные объекты мультимедиа. Дополнительные сведения можно найти [в разделе MDN основы использования IndexedDB][MDNIndexeddbApiUsing].

## Общие сведения о параметрах хранения для PWAs

Иногда вам может потребоваться хранить небольшие объемы данных для обеспечения более эффективной работы в автономном режиме для пользователей. Если это так, вы можете найти простоту системы пар "ключ-значение", соответствующей вашим потребностям.  

> [!IMPORTANT]
> Веб-хранилище — это синхронный процесс, и его нельзя использовать в рабочих потоках, например сотрудниках служб. Использование трудовых ресурсов может привести к проблемам с производительностью приложения. 


Существует два типа веб-хранилищ: `localStorage` и `sessionStorage` . Каждый из них хранится в отдельном хранилище данных, изолированном с доменом, в котором он был создан. `sessionStorage` сохраняются только в течение сеанса просмотра (например, при открытии браузера, который включает в себя обновление и восстановление). `localStorage` повторяется до тех пор, пока данные не будут удалены кодом, пользователем или браузером (например, если доступно ограниченное хранилище). В приведенном ниже фрагменте кода показано, как использовать этот метод `localStorage` , который аналогичен тому, как `sessionStorage` он используется.

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

Этот фрагмент кода извлекает метаданные о текущей странице и сохраняет его в объекте JavaScript. Затем он сохраняет это значение как JSON в `localStorage` `setItem()` методе и назначает ключ, равный текущему `window.location` URL-адресу. Вы можете получить информацию с `localStorage` помощью этого `getItem()` метода. 

В следующем фрагменте кода показано, как использовать кэширование с `localstorage` целью перечисления кэшированных страниц и извлечения метаданных для выполнения задачи, например для создания списка ссылок.

```javascript
caches.open( "pages" )
      .then( cache => {
    cache.keys()
         .then( keys => {
        if ( keys.length )
        {
            keys.forEach( insertOfflineLink );
        }
    })
});

function insertOfflineLink( request ) {
    var data = JSON.parse( localStorage.getItem( request.url ) );
    // If data exists and this page is not an offline page, assuming that offline pages have the word offline in the URL.
    if ( data && request.url.indexOf('offline') < 0  )
    {
        // Build a link and insert it into the page.
    }
}
```  

`insertOfflineLink()`Метод передает URL-адрес запроса в `localStorage.getItem()` метод для получения всех сохраненных метаданных. Извлеченные данные проверяются на предмет их существования, и, если это так, для их отображения можно выполнить действие с данными, такие как создание и вставка разметки.

## Проверка сетевых подключений в PWA

Помимо хранения сведений для автономного использования, полезно знать, когда доступно сетевое подключение для синхронизации данных или информировать пользователей о том, что состояние сети изменилось. Используйте следующие параметры для проверки подключения к сети.

### Навигатор. онлайн  

`navigator.onLine`Свойство является логическим значением, которое позволяет узнать текущее состояние сети. Если задано значение `true` , пользователь находится в сети, в противном случае пользователь не в сети.

### События в Интернете и в автономном режиме  

Сведения о том, доступна ли сеть, но может потребоваться при изменении сетевого подключения. В этой ситуации может возникнуть необходимость в ответе на события сети и принимать меры. События доступны для `window` элементов, которые `document` `document.body` отображаются в следующем фрагменте кода.

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## См. также  

Дополнительные сведения об управлении автономными сценариями можно найти на следующих страницах.  

*   [Кэш][MDNCache]  
*   [IndexedDB][MDNIndexeddbApi]  
*   [Сервисный работник][MDNServiceWorker]  
*   [Веб-хранилище][MDNWebStorageApi]  
*   [Навигатор. онлайн][MDNNavigatoronline]  
*   [События в Интернете и в автономном режиме][MDNNavigatoronlineOfflineEvents]  
*   [Запрос с намерением: стратегии кэширования в возраст PWAs][AlistapartRequestIntentCachingStrategiesAgePwas]

<!-- links -->  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNIndexeddbApi]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNIndexeddbApiUsing]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Использование API IndexDb-IndexDB | MDN"  
[MDNServiceWorker]: https://developer.mozilla.org/docs/Web/API/ServiceWorker "ServiceWorker | MDN"  
[MDNWebStorageApi]: https://developer.mozilla.org/docs/Web/API/Web_Storage_API "API веб-хранилища | MDN"  
[MDNNavigatoronline]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine "NavigatorOnLine | MDN"  
[MDNNavigatoronlineOfflineEvents]: https://developer.mozilla.org/docs/Web/API/NavigatorOnLine/Online_and_offline_events "События в сети и в автономном режиме — NavigatorOnLine | MDN"  

[AbookapartGoingOffline]: https://abookapart.com/products/going-offline "Перейти в автономный режим с помощью Джереми Кит | Отдельное руководство"  

[AlistapartRequestIntentCachingStrategiesAgePwas]: https://alistapart.com/article/request-with-intent-caching-strategies-in-the-age-of-pwas "Запрос с намерением: стратегии кэширования в возраст PWAs с «Екатерина Gustafson | Разделение списка"  
