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
# <span data-ttu-id="a7a9e-104">Поддержка подключения к Интернету и сети в прогрессивных веб-приложениях</span><span class="sxs-lookup"><span data-stu-id="a7a9e-104">Offline and network connectivity support in Progressive Web Apps</span></span>

<span data-ttu-id="a7a9e-105">В течение многих лет Организации были неохотно за незначительное количество инвестиций в веб-приложения по сравнению с машинным обеспечением, поскольку веб-приложение зависело от стабильных сетевых подключений.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-105">For many years organizations were reluctant to invest heavily in web-based software over native software because web applications depended on stable network connections.</span></span> <span data-ttu-id="a7a9e-106">На сегодняшний день веб-платформа теперь поддерживает надежные параметры, позволяющие пользователям продолжать работу, даже если сетевое подключение работает нестабильно или полностью выходит из сети.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-106">Today, the web platform now offers robust options that enable users to continue working, even if the network connection becomes unstable or goes completely offline.</span></span>

## <span data-ttu-id="a7a9e-107">Повышение производительности PWAs с помощью кэширования</span><span class="sxs-lookup"><span data-stu-id="a7a9e-107">Use the caching to improve performance of PWAs</span></span>

<span data-ttu-id="a7a9e-108">С введением [сотрудников обслуживания][MDNServiceWorker]веб-платформа добавила `Cache` API, чтобы предоставить доступ к управляемым кэшированным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-108">With the introduction of [Service Workers][MDNServiceWorker], the web platform added the `Cache` API to provide access to managed cached resources.</span></span> <span data-ttu-id="a7a9e-109">Этот API-интерфейс на основе обещаний позволяет разработчикам хранить и извлекать большое количество веб-ресурсов: HTML, CSS, JavaScript, изображений, JSON и т. д.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-109">This Promise-based API allows developers to store and retrieve many web resources—HTML, CSS, JavaScript, images, JSON, and so on.</span></span> <span data-ttu-id="a7a9e-110">Обычно API кэша используется в контексте сотрудника службы, но он также доступен в основном потоке `window` объекта.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-110">Usually, the Cache API is used within the context of a Service Worker, but it is also available in the main thread on the `window` object.</span></span>

<span data-ttu-id="a7a9e-111">Чаще всего API используется для `Cache` предварительного кэширования ресурсов при установке сотрудника службы, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-111">One common use for the `Cache` API is to pre-cache critical resources when a Service Worker is installed, as shown in the following code snippet.</span></span>  

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

<span data-ttu-id="a7a9e-112">Этот код, который запускается во время `install` события жизненного цикла рабочего процесса службы, открывает кэш с именем, `static-cache` а затем, когда он имеет указатель на кэш, добавляет в него четыре ресурса с помощью `addAll()` метода.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-112">This code, which runs during the Service Worker `install` life cycle event, opens a cache named `static-cache` and then, when it has a pointer to the cache, adds four resources to it using the `addAll()` method.</span></span>  <span data-ttu-id="a7a9e-113">Часто подход связан с извлечением кэша во время `fetch` события</span><span class="sxs-lookup"><span data-stu-id="a7a9e-113">Often the approach is coupled with cache retrieval during a `fetch` event</span></span>   

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

<span data-ttu-id="a7a9e-114">Фрагмент кода запускается в рамках сотрудника службы всякий раз, когда браузер выполняет `fetch` запрос для этого сайта.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-114">The code snippet runs within the Service Worker whenever the browser makes a `fetch` request for this site.</span></span> <span data-ttu-id="a7a9e-115">Внутри этого события есть условный оператор, который выполняется, если запрос предназначен для HTML-файла.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-115">Within that event, there is a conditional statement that runs if the request is for an HTML file.</span></span> <span data-ttu-id="a7a9e-116">Рабочий процесс пытается проверить, существует ли файл в каком-либо кэше \ (с помощью `match()` метода \).</span><span class="sxs-lookup"><span data-stu-id="a7a9e-116">The Service Worker checks to see if the file already exists in any cache \(using the `match()` method\).</span></span> <span data-ttu-id="a7a9e-117">Если запрос существует в кэше, возвращается этот кэшируемый результат.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-117">If the request exists in the cache, that cached result is returned.</span></span> <span data-ttu-id="a7a9e-118">Если это не так, `fetch` будет запущен новый ресурс, а копия ответа будет помещена в кэш для дальнейшего, и будет возвращен ответ.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-118">If not, a new `fetch` for that resource is run, a copy of the response is cached for later, and the response is returned.</span></span> <span data-ttu-id="a7a9e-119">Если это `fetch` не удается из-за того, что сеть недоступна, из кэша будет возвращена автономная страница.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-119">If the `fetch` fails because the network is unavailable, the offline page is returned from the cache.</span></span>

<span data-ttu-id="a7a9e-120">В этом простом вводе показано, как использовать кэширование в последовательном веб-приложении (PWA).</span><span class="sxs-lookup"><span data-stu-id="a7a9e-120">This simple introduction shows how to use caching in your progressive web app (PWA).</span></span> <span data-ttu-id="a7a9e-121">Каждый PWA отличается и может использовать различные стратегии кэширования.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-121">Each PWA is different and may use different caching strategies.</span></span> <span data-ttu-id="a7a9e-122">Код может выглядеть по-разному, и вы можете использовать различные стратегии кэширования для разных маршрутов в одном приложении.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-122">Your code may look different, and you may use different caching strategies for different routes within the same application.</span></span>

## <span data-ttu-id="a7a9e-123">Использование IndexedDB в PWA для хранения структурированных данных</span><span class="sxs-lookup"><span data-stu-id="a7a9e-123">Use IndexedDB in your PWA to store structured data</span></span>

`IndexedDB` <span data-ttu-id="a7a9e-124">— это API для хранения структурированных данных.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-124">is an API for storing structured data.</span></span> <span data-ttu-id="a7a9e-125">Аналогично `Cache` API-интерфейсом, он также является асинхронным, что означает, что вы можете использовать его в основном потоке или с веб-сотрудниками, например сотрудниками служб.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-125">Similar to the `Cache` API, it is also asynchronous, which means you may use it in the main thread or with Web Workers such as Service Workers.</span></span> <span data-ttu-id="a7a9e-126">Используйте `IndexedDB` API для хранения значительной структуры структурированных данных на клиентском компьютере, а также двоичных данных, таких как зашифрованные объекты мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-126">Use the `IndexedDB` API for storing a significant amount of structured data on the client, or binary data, such as encrypted media objects.</span></span> <span data-ttu-id="a7a9e-127">Дополнительные сведения можно найти [в разделе MDN основы использования IndexedDB][MDNIndexeddbApiUsing].</span><span class="sxs-lookup"><span data-stu-id="a7a9e-127">For more information, see [MDN primer on using IndexedDB][MDNIndexeddbApiUsing].</span></span>

## <span data-ttu-id="a7a9e-128">Общие сведения о параметрах хранения для PWAs</span><span class="sxs-lookup"><span data-stu-id="a7a9e-128">Understand storage options for PWAs</span></span>

<span data-ttu-id="a7a9e-129">Иногда вам может потребоваться хранить небольшие объемы данных для обеспечения более эффективной работы в автономном режиме для пользователей.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-129">Sometimes you may need to store small amounts of data in order to provide a better offline experience for your users.</span></span> <span data-ttu-id="a7a9e-130">Если это так, вы можете найти простоту системы пар "ключ-значение", соответствующей вашим потребностям.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-130">If that is the case, you may find the simplicity of the key-value pair system of web storage meets your needs.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="a7a9e-131">Веб-хранилище — это синхронный процесс, и его нельзя использовать в рабочих потоках, например сотрудниках служб.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-131">Web Storage is a synchronous process and is not available for use within worker threads such as Service Workers.</span></span> <span data-ttu-id="a7a9e-132">Использование трудовых ресурсов может привести к проблемам с производительностью приложения.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-132">Heavy usage may create performance issues for your application.</span></span> 


<span data-ttu-id="a7a9e-133">Существует два типа веб-хранилищ: `localStorage` и `sessionStorage` .</span><span class="sxs-lookup"><span data-stu-id="a7a9e-133">There are 2 types of Web Storage: `localStorage` and `sessionStorage`.</span></span> <span data-ttu-id="a7a9e-134">Каждый из них хранится в отдельном хранилище данных, изолированном с доменом, в котором он был создан.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-134">Each is maintained as a separate data store isolated to the domain that created it.</span></span> `sessionStorage` <span data-ttu-id="a7a9e-135">сохраняются только в течение сеанса просмотра (например, при открытии браузера, который включает в себя обновление и восстановление).</span><span class="sxs-lookup"><span data-stu-id="a7a9e-135">persists only for the duration of the browsing session (for example, while the browser is open, which includes refresh and restores).</span></span> `localStorage` <span data-ttu-id="a7a9e-136">повторяется до тех пор, пока данные не будут удалены кодом, пользователем или браузером (например, если доступно ограниченное хранилище).</span><span class="sxs-lookup"><span data-stu-id="a7a9e-136">persists until the data is removed by the code, the user, or the browser (for example, when there is limited storage available).</span></span> <span data-ttu-id="a7a9e-137">В приведенном ниже фрагменте кода показано, как использовать этот метод `localStorage` , который аналогичен тому, как `sessionStorage` он используется.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-137">The following code snippet shows how to use `localStorage`, which is similar to how `sessionStorage` is used.</span></span>

```javascript
var data = {
    title: document.querySelector("[property='og:title']").getAttribute("content"),
    description: document.querySelector( "meta[name='description']" ).getAttribute("content")
};
localStorage.setItem( window.location, JSON.stringify(data) );
```  

<span data-ttu-id="a7a9e-138">Этот фрагмент кода извлекает метаданные о текущей странице и сохраняет его в объекте JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-138">This code snippet grabs metadata about the current page and stores it in a JavaScript object.</span></span> <span data-ttu-id="a7a9e-139">Затем он сохраняет это значение как JSON в `localStorage` `setItem()` методе и назначает ключ, равный текущему `window.location` URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-139">Then it stores that value as JSON in `localStorage` using the `setItem()` method, and assigns a key equal to the current `window.location` URL.</span></span> <span data-ttu-id="a7a9e-140">Вы можете получить информацию с `localStorage` помощью этого `getItem()` метода.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-140">You may retrieve the information from `localStorage` using the `getItem()` method.</span></span> 

<span data-ttu-id="a7a9e-141">В следующем фрагменте кода показано, как использовать кэширование с `localstorage` целью перечисления кэшированных страниц и извлечения метаданных для выполнения задачи, например для создания списка ссылок.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-141">The following code snippet shows how to use caching with `localstorage` to enumerate cached pages and extract metadata to perform a task, such as building a list of links.</span></span>

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

<span data-ttu-id="a7a9e-142">`insertOfflineLink()`Метод передает URL-адрес запроса в `localStorage.getItem()` метод для получения всех сохраненных метаданных.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-142">The `insertOfflineLink()` method passes the URL of the request into the `localStorage.getItem()` method to retrieve any stored metadata.</span></span> <span data-ttu-id="a7a9e-143">Извлеченные данные проверяются на предмет их существования, и, если это так, для их отображения можно выполнить действие с данными, такие как создание и вставка разметки.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-143">The retrieved data is checked to see if it exists, and if it does, an action can be taken on the data, such as building and inserting the markup to display it.</span></span>

## <span data-ttu-id="a7a9e-144">Проверка сетевых подключений в PWA</span><span class="sxs-lookup"><span data-stu-id="a7a9e-144">Test for network connections in your PWA</span></span>

<span data-ttu-id="a7a9e-145">Помимо хранения сведений для автономного использования, полезно знать, когда доступно сетевое подключение для синхронизации данных или информировать пользователей о том, что состояние сети изменилось.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-145">In addition to storing information for offline use, it is helpful to know when a network connection is available in order to synchronize data or inform users that the network status has changed.</span></span> <span data-ttu-id="a7a9e-146">Используйте следующие параметры для проверки подключения к сети.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-146">Use the following options to test for network connectivity.</span></span>

### <span data-ttu-id="a7a9e-147">Навигатор. онлайн</span><span class="sxs-lookup"><span data-stu-id="a7a9e-147">navigator.onLine</span></span>  

<span data-ttu-id="a7a9e-148">`navigator.onLine`Свойство является логическим значением, которое позволяет узнать текущее состояние сети.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-148">The `navigator.onLine` property is a boolean that lets you know the current status of the network.</span></span> <span data-ttu-id="a7a9e-149">Если задано значение `true` , пользователь находится в сети, в противном случае пользователь не в сети.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-149">If the value is `true`, the user is online, otherwise the user is offline.</span></span>

### <span data-ttu-id="a7a9e-150">События в Интернете и в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="a7a9e-150">Online and Offline Events</span></span>  

<span data-ttu-id="a7a9e-151">Сведения о том, доступна ли сеть, но может потребоваться при изменении сетевого подключения.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-151">Knowing whether the network is available is helpful, but you may want to take action  when your network connectivity changes.</span></span> <span data-ttu-id="a7a9e-152">В этой ситуации может возникнуть необходимость в ответе на события сети и принимать меры.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-152">In this situation, you may want to listen and take action in response to network events.</span></span> <span data-ttu-id="a7a9e-153">События доступны для `window` элементов, которые `document` `document.body` отображаются в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-153">The events are available on the `window`, `document`, and `document.body` elements as displayed in the following code snippet.</span></span>

```javascript
window.addEventListener("online",  function(){
    console.log("You are online!");
});
window.addEventListener("offline", function(){
    console.log("Oh no, you lost your network connection.");
});
```  

## <span data-ttu-id="a7a9e-154">См. также</span><span class="sxs-lookup"><span data-stu-id="a7a9e-154">See also</span></span>  

<span data-ttu-id="a7a9e-155">Дополнительные сведения об управлении автономными сценариями можно найти на следующих страницах.</span><span class="sxs-lookup"><span data-stu-id="a7a9e-155">To learn more about managing offline scenarios, see the following pages.</span></span>  

*   [<span data-ttu-id="a7a9e-156">Кэш</span><span class="sxs-lookup"><span data-stu-id="a7a9e-156">Cache</span></span>][MDNCache]  
*   [<span data-ttu-id="a7a9e-157">IndexedDB</span><span class="sxs-lookup"><span data-stu-id="a7a9e-157">IndexedDB</span></span>][MDNIndexeddbApi]  
*   [<span data-ttu-id="a7a9e-158">Сервисный работник</span><span class="sxs-lookup"><span data-stu-id="a7a9e-158">Service Worker</span></span>][MDNServiceWorker]  
*   [<span data-ttu-id="a7a9e-159">Веб-хранилище</span><span class="sxs-lookup"><span data-stu-id="a7a9e-159">Web Storage</span></span>][MDNWebStorageApi]  
*   [<span data-ttu-id="a7a9e-160">Навигатор. онлайн</span><span class="sxs-lookup"><span data-stu-id="a7a9e-160">navigator.onLine</span></span>][MDNNavigatoronline]  
*   [<span data-ttu-id="a7a9e-161">События в Интернете и в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="a7a9e-161">Online and Offline Events</span></span>][MDNNavigatoronlineOfflineEvents]  
*   [<span data-ttu-id="a7a9e-162">Запрос с намерением: стратегии кэширования в возраст PWAs</span><span class="sxs-lookup"><span data-stu-id="a7a9e-162">Request with Intent: Caching Strategies in the Age of PWAs</span></span>][AlistapartRequestIntentCachingStrategiesAgePwas]

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
