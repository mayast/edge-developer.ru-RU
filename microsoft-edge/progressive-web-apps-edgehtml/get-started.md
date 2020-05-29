---
description: В этом руководстве вы найдете общие сведения о базовых данных и средствах для создания последовательной веб-приложений для Windows.
title: Приступите к работе с прогрессивными веб-приложениями
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: прогрессивные веб-приложения, PWA, EDGE, Windows, PWABuilder, веб-манифест, специалист по обслуживанию, отправка
ms.openlocfilehash: 4d7b571b83048f9ce271f451a7537027bb92eebc
ms.sourcegitcommit: 9169d784485e3cb0b1987a8f395c4bb688bd9b2e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "10583786"
---
# Приступите к работе с прогрессивными веб-приложениями  

Прогрессивные веб-приложения \ (PWAs \) — это веб-приложения, которые [последовательно дополнены][WikiProgressiveEnhancement] функциями поддержки платформ и обработчиков браузеров, таких как установка из системы и работа с приложениями начальный экран, Автономная поддержка и Push-уведомления.  В Windows 10 с ядром Microsoft Edge \ (EdgeHTML \) PWAs наслаждайтесь дополнительным преимуществом работы независимо от окна браузера в качестве приложений [универсальной платформы Windows][WindowsUwpGetStartedWhat] .  

В этом руководстве вы найдете общие сведения об основных возможностях PWA, создав простое `localhost` веб-приложение в PWA с помощью Microsoft Visual Studio и некоторых служебных программ PWA.  Готовый продукт работает так же, как и любой браузер, поддерживающий PWAs.  

> [!TIP]
> Чтобы быстро преобразовать существующий веб-сайт в PWA и упаковать его для Windows 10 и других платформ приложений, ознакомьтесь с [построителем PWA][PwaBuilder].  

## Предварительные условия  

Вы можете создать PWAs с любой интегрированной средой разработки веб-приложений.  Ниже приведены только необходимые условия для этого руководства, в ходе которого вы переходите в службу поддержки средств на панели управления для Windows для разработчиков.  

*   Скачайте (бесплатное) [Visual Studio Community 2017][VisualStudioDownloads].  Вы также можете использовать выпуски профессионального выпуска, Enterprise или [Preview][VisualStudioPreview] .  В установщике Visual Studio выберите указанные ниже рабочие нагрузки.  
    
    *   **Разработка универсальной платформы Windows**  
    *   **Разработка приложений Node. js**  

## Настройка простого веб-приложения  

Для простоты используйте шаблон Visual Studio [node. js и Экспресс-приложение][VisualStudioNodeJsTutorial] , чтобы создать `localhost` приложение, которое будет служить `index.html` страницей.  Представьте это в качестве заполнителя для привлекательного полнофункционального веб-приложения, которое вы разрабатываете как PWA.  

1.  Запустите Visual Studio и начните новый проект.  
    *   **Файл**  >  **Новые**  >  **Проект...**  
    *   `Ctrl`+`Shift`+`N`  
1.  В разделе **JavaScript**выберите **базовый приложение Node. js Express 4**.  Укажите имя и расположение и нажмите кнопку **ОК**.  
    
    ![Выбор шаблона проекта Node. js Express 4 в Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  После загрузки нового проекта выберите команду **построить** \ ( `Ctrl` + `Shift` + `B` \) и **начать отладку** \ ( `F5` \).  Убедитесь в том, что `index.html` файл загружается при просмотре `http://localhost:1337` .  
    
    ![Выполнение нового сайта на localhost][ImageVsNodejsExpressIndex]  

## Преобразование приложения в PWA  

Теперь пришло время связать базовые [требования PWA][PwaEdgehtmlIndexRequirements] для вашего веб-приложения: *Манифест веб-приложения*, *HTTPS* и *сотрудников службы*.  

### Манифест веб-приложения  

[Манифест веб-приложения][MDNWebAppManifest] — это файл метаданных JSON, описывающий ваше приложение, включая имя, автора, URL-адрес страницы ввода и один или несколько значков.  Поскольку она используется в [соответствии со стандартными схемами][W3cWebAppManifest], необходимо предоставить только один манифест веб-приложения для PWA, который устанавливается на любую ПЛАТФОРМУ, ОС и устройство, поддерживающее PWAs.  В экосистеме Windows манифест веб-приложения передает веб-индексатору Bing о том, что ваш PWA является кандидатом на автоматическое включение в [Microsoft Store][PwaEdgehtmlMicrosoftStore], где он может достигать почти 700 000 000 активных ежемесячных пользователей как приложение Windows 10.  

Если это существующий активный сайт, вы можете создать манифест веб-приложения с помощью [построителя PWA][PwaBuilder].  Так как он по-прежнему является неопубликованным проектом, скопируйте пример манифеста.  

1.  В *обозревателе решений*Visual Studio щелкните *общедоступную* папку правой кнопкой мыши и выберите команду **добавить**  >  **новый файл...**, указав в `manifest.json` качестве имени элемента.  
1.  `manifest.json`Скопируйте следующий код в файле.  

    ```json
    {
        "dir": "ltr",
        "lang": "en-us",
        "name": "My Sample PWA",
        "scope": "/",
        "display": "browser",
        "start_url": "https://PLACEHOLDER-FOR-PWA-URL",
        "short_name": "SamplePWA",
        "theme_color": "transparent",
        "description": "A sample PWA for testing purposes",
        "orientation": "any",
        "background_color": "transparent",
        "related_applications": [],
        "prefer_related_applications": false,
        "icons": []
    }
    ```  
    
    В реальном времени на веб-странице PWA следует настроить *имя*, *start_url*, *short_name*, *Описание*и *значки* \ (значки описаны на следующем шаге).  
    
    Чтобы узнать больше о различных значениях элементов и связанных целях, ознакомьтесь со статьей ссылка на [Манифест веб-приложения][MDNWebAppManifest] .  
    
1.  Затем заполните пустой `icons` массив фактическими путями изображений с помощью генератора изображений приложения PWA Builder.  
    
    1.  С помощью веб-браузера скачайте этот [образец 512x512ного образа PWA][ImagePwa].  
    1.  Перейдите к средству [создания изображений приложения][PwaBuilderAppImageGenerator]PWA Builder и выберите `pwa.png` изображение, которое вы только что сохранили, а затем нажмите кнопку **загрузить** . **Input Image**  
    1.  **Откройте** и **Извлеките** ZIP-файл.  
    1.  В обозревателе решений Visual Studio щелкните правой кнопкой мыши `public` папку и **откройте папку проводник**.  Создайте **новую папку** с именем `images` .  
    1.  Скопируйте все папки платформы \ ( `android` , `chrome` , `windows10` и т. д.) из извлеченного Zip- `images` файла в папку и закройте окно проводника.  Добавьте папки в проект Visual Studio \ (в обозревателе решений щелкните правой кнопкой мыши `images` папку и выберите команду **Добавить**  >  **существующую папку...** для каждой папки \).  
    1.  Откройте документ \ (в Visual Studio или любом из редакторов), `icons.json` а затем скопируйте `"icons": [...]` массив в `manifest.json` файл проекта.  

1.  Теперь вы должны связать свой манифест веб-приложения с вашим приложением.  Откройте `layout.pug` файл \ (в `views` папке \) для редактирования и добавьте эту строку сразу после ссылки на таблицу стилей.  \ (Это просто краткий шаблон узла [pug][PugAttributes] для `<link rel='manifest' href='/manifest.json'>` \).  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
Теперь, когда веб-приложение размещается на своем месте, в нем сомещаются манифесты и значки приложений, готовые к начальный экран!  Попробуйте запустить приложение \ ( `F5` \) и загрузить манифест.  

![Загрузка манифеста веб-приложения из localhost][ImageVsNodejsExpressManifest]  

И один из значков.  

![Загрузка логотипа приложения Square71x71Logo с localhost][ImageVsNodejsExpressIcon]  

Если опубликовать приложение в режиме реального времени \ (с фактическим данными `start_url` \), средство поиска Bing теперь будет определять его как кандидат на [автоматическую упаковку и отправку в Microsoft Store][PwaEdgehtmlMicrosoftStore] как приложение Windows 10 с возможностью установки.  Убедитесь в том, что файл manifest. JSON включает [сигналы качества для последовательного веб-приложения][WindowsBlogsPwaEdge] , в которых проверяются результаты поиска Bing, включая перечисленные ниже элементы.   

*   `name`  
*   `description`  
*   По крайней мере один значок 512px квадратную или крупную фигуру, чтобы убедиться, что источник изображения подходит для автоматического создания экрана-заставки вашего приложения, описания в магазине, мозаичного изображения и т. д.  

Кроме того, можно использовать [протокол HTTPS](#https), [рабочие процессы обслуживания](#service-workers)и соблюдать [политики Microsoft Store][LegalWindowsAgrementsMicrosoftStorePolicies].  

### HTTPS  

[Сотрудники служб][MDNServiceWorkerApi] и другие ключевые технологии PWA, которые работают с сотрудниками служб (например, [Cache][MDNCache], [Push][MDNPushApi]и API [фоновой синхронизации][MDNSyncManager] ), работают только в безопасных соединениях, то есть [HTTPS][WikiHttps] для активных сайтов или `localhost` для целей отладки.  

Если вы [публикуете это веб-приложение в рамках действующего сайта][VisualStudioNodejsTutorialPublishAzureAppService] (например, при настройке [учетной записи Azure Free][AzureCreateFreeAccount]), необходимо убедиться, что сервер настроен для HTTPS.  Если вы используете [службу приложений Microsoft Azure][AzureWebApps] для размещения сайта, она по умолчанию обрабатывается по протоколу HTTPS.  

Для этого руководства продолжайте использовать `http://localhost` в качестве заполнителя для активного сайта, обслуживаемого активным `https://` .  

### Обслуживание сотрудников  

Специалистами службы является ключевая технология, PWAs. Служебные работники выполняют роль прокси между PWA и сетью, чтобы обеспечить работу вашего веб-сайта в качестве установленного собственного приложения, обслуживающего сценарии в автономном режиме, реагируя на принудительные уведомления сервера и запускающего фоновые задачи.  Работники служб также открывают новые стратегии обеспечения производительности.  Вы не обязаны реализовывать все веб-приложения, чтобы использовать кэш рабочих процессов службы для точной настройки производительности загрузки страниц для вашего веб-сайта.  

Служебные работники — это управляемые событиями фоновые потоки, которые выполняются из файлов JavaScript вместе с обычными сценариями, которые используются для включения в веб-приложение.  Поскольку работники служб не работают в основном потоке пользовательского интерфейса, у сотрудников служб нет доступа DOM, хотя [поток пользовательского интерфейса][MDNWorkerPrototypePostMessage] и [Рабочий поток][MDNDedicatedWorkerGlobalScopePostMessage] может взаимодействовать с помощью `postMessage()` `onmessage` обработчиков событий.  

Вы связываете сотрудника службы с вашим приложением, регистрируя его в источнике URL-адреса сайта (или в указанном месте).  После регистрации файл рабочего процесса службы загружается, устанавливается и активируется на компьютере пользователя.  Более того, MDN веб-документы имеет исчерпывающее руководство по [работе с сотрудниками служб][MDNUsingServiceWorkers] и подробным справочником по [API рабочего процесса службы][MDNServiceWorkerApi] .  

В этом учебнике используйте сценарий рабочего процесса службы автономной обработки страниц в [конструкторе PWA][PwaBuilderServiceWorker].  Начните с настройки сценария с большим набором функциональных возможностей в соответствии с требованиями к производительности, пропускной способностью сети и т. д.  Изучите [Cookbook рабочего процесса][ServiceWorkerCookbook] , предоставленный Mozilla, для ряда полезных идей по кэшированию рабочих процессов служб.  

1.  Откройте [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] и выберите рабочий процесс **автономной работы со страницей** \ (по умолчанию \) и нажмите кнопку " **загрузить сотрудник службы** ".  
1.  Откройте папку download и скопируйте следующие два файла  

    *   ServiceWorker1\pwabuilder-sw-register.js  
    *   ServiceWorker1\pwabuilder-sw.js  
    
    Сохраните файлы в `public` папке проекта Visual Studio Web App.  \ (В Visual Studio `Ctrl` + `O` откройте проводник для проекта и перейдите в `public` папку \).  
    
    Рекомендуется проанализировать этот код в обоих файлах, чтобы получить сведения о том, как зарегистрировать сотрудника службы, который кэширует указанную страницу \ ( `offline.html` \) и выполняет ее в случае сбоя при выборке из сети.  Затем создайте простую `offline.html` страницу в качестве заполнителя для автономной работы приложения.  
    
1.  В обозревателе решений откройте `views/layout.pug` файл и добавьте следующую строку под тегами ссылки.  
    
    ```html
    script(src='/pwabuilder-sw-register.js')
    ```  
    
    Ваш сайт загрузит и запустит сценарий регистрации рабочего процесса службы.  
    
1.  В обозревателе решений щелкните папку правой кнопкой мыши `public` и выберите команду **Добавить**  >  **новый файл..**..  Присвойте ему имя `offline.html` , а затем добавьте `<title>` и часть основного содержимого, например приведенный ниже код.  
    
    ```html
    <!DOCTYPE html>
    
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title>Offline mode</title>
    </head>
    <body>
        You are now offline.
    </body>
    </html>
    ```  
    
    На этом этапе у вашей `public` папки должны быть три новых файла.  
    
    ![Файлы, добавленные в общую папку решения][ImageVsNodejsExpressPublic]  
    
1.  В обозревателе решений откройте `routes\index.js` файл и добавьте следующий код непосредственно перед последней командой \ ( `module.exports = router;` \).  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    Это указывает приложению на необходимость обслуживания `offline.html` файла \ (когда ваш сотрудник службы извлекает ее для автономного кэша).  
    
1.  Протестируйте веб-приложение PWA!  `Ctrl` + `Shift` + `B` `F5` Чтобы запустить Microsoft EDGE и открыть страницу, выполните сборку \ (\) и запустите "["] веб-приложение `localhost` .  Затем выполните указанные ниже действия.  
    
    1.  Откройте вкладку **Edge DevTools (** `Ctrl` + `Shift` + `J` \) и убедитесь, что сотрудник службы зарегистрирован.  
    1.  На панели **отладчик** разверните элемент Управление **сотрудниками службы** и щелкните на своем источнике.  В **обзоре сотрудника службы**убедитесь, что сотрудник службы активирован и запущен.  
        
        ![Общие сведения о сотруднике службы Edge DevTools][ImageDevtoolsSwOverview]  
        
    1.  Разверните элемент управления **кэшем** и убедитесь, что `offline.html` страница кэширована.  
        
        ![Кэш рабочего процесса службы Edge DevTools][ImageDevtoolsSwCache]  
        
1.  Время, когда вы можете попробовать приложение PWA в автономном режиме!  В Visual Studio **отключите отладку** ( `Shift` + `F5` \) веб-приложение, а затем откройте Microsoft Edge \ (или обновите \) на адрес localhost вашего веб-сайта.  Теперь оно должно загрузить `offline.html` страницу \ (благодаря своему сотруднику службы и автономному кэшу)!  
    
    ![offline. HTML из http://localhost:1337 загруженного в Microsoft Edge][ImageOfflineHtml]  

## Добавление push-уведомлений  

Сделайте этот веб-сайт более похожим, добавив поддержку на стороне клиента для отправки push- [уведомлений в службу][MDNPushApi] сообщений и [API уведомлений][MDNNotificationsApi] для отображения всплывающего сообщения при получении сообщения.  Как и в случае с сотрудниками служб, они являются стандартными API, которые работают в разных браузерах, поэтому вам нужно написать код только для того, чтобы он работал везде, где бы они ни наPWAsись.  На стороне сервера используйте [веб-извещающую][NPMWebPush] библиотеку с открытым исходным кодом для обработки различий, связанных с предоставлением Push-сообщений для различных браузеров.  

Ниже приведено множество полезных демонстрационных роликов, посвященных [специалистам службы Cookbook][ServiceWorkerCookbookPushRichDemo] , предоставляемым Mozilla, что стоит делать, чтобы получить доступ к другим полезным рецептам веб-внедрения и обслуживания.  

### Шаг 1: Установка веб-библиотеки NPM  

В обозревателе решений Visual Studio щелкните проект правой кнопкой мыши и **откройте интерактивное окно Node. js..**..  Введите следующий код.  

```javascript
.npm install web-push
```  

Будет установлено [веб-принудительная][NPMWebPush] библиотека.  Затем откройте `index.js` файл и добавьте следующую строку в начало файла после других операторов требования.  

```javascript
var webpush = require('web-push');
```  

### Шаг 2. Создание VAPIDных ключей для сервера  

Затем для отправки push-сообщений в клиент PWA необходимо создать для сервера ключи VAPID \ (код добровольного сервера приложений).  Это нужно сделать только один раз \ (то есть для вашего сервера требуется только одна пара ключей VAPID).  В интерактивном окне Node. js введите следующий код.  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

Результат должен привести к тому, что объект JSON содержит открытый и закрытый ключи, которые вы копируете в логику сервера.  

В `index.js` файле перед последней `module.exports = router` строкой \ (\) добавьте следующий код.  

```javascript
const vapidKeys = {
    publicKey: '',
    privateKey: ''
};

webpush.setVapidDetails(
    'mailto:pwa@example.com',
    vapidKeys.publicKey,
    vapidKeys.privateKey
);
```  

Скопируйте `publicKey` `privateKey` только что созданные значения.  Вы можете настроить адрес так же, `mailto` как если бы он ни запускался для выполнения этого примера \.  

В [блоге по проектированию служб Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush] вы узнаете о том, как VAPID и веб-извещающую, если вы заинтересованы в том, как это работает за сценой.  

### Шаг 3: обработка запросов сервера, связанных с принудительной отправкой  

Теперь настройте маршруты для обработки запросов push-уведомлений от клиента PWA, в том числе для предоставления открытого ключа VAPID и регистрации клиента для приема pushs.  

В реальной ситуации push-уведомление, как правило, является событием в логике сервера.  Чтобы упростить это, необходимо добавить кнопку Push- **уведомлений** на нашу ДОМАШНЮЮ страницу PWA, чтобы создать push-уведомления с нашего сервера, и `/sendNotification` конечную точку \ (серверный маршрут \) для обработки запросов.  

В `index.js` файле добавьте следующие маршруты сразу после кода инициализации VAPID, добавленного в [Step 2] [#step-2---Generate-VAPID-Keys-для вашего сервера].  

```javascript
router.get('/vapidPublicKey', function (req, res) {
    res.send(vapidKeys.publicKey);
});

router.post('/register', function (req, res) {
    // A real world application stores the subscription info.
    res.sendStatus(201);
});

router.post('/sendNotification', function (req, res) {
    const subscription = req.body.subscription;
    const payload = 'payload';
    const options = null;
    
    webpush.sendNotification(subscription, payload, options)
        .then(function () {
            res.sendStatus(201);
        })
        .catch(function (error) {
            res.sendStatus(500);
            console.log(error);
        });
});
```  

С помощью серверного кода на месте в push-уведомлениях на клиенте PWA.  

### Шаг 4: Подписка на push-уведомления  

Как часть роли прокси-сервера PWA, сотрудники служб обрабатывают события push-уведомлений и взаимодействие с всплывающими уведомлениями.  Тем не менее, так как при первой настройке (или регистрации) сотрудник службы подписаться на push-уведомления PWA в главном потоке пользовательского интерфейса PWA и требуется сетевое подключение.  Для подписки на push-уведомления требуется активная регистрация рабочего процесса службы, поэтому сначала необходимо убедиться, что ваш сотрудник службы установлен и активен, прежде чем пытаться подписаться на push-уведомления.  

Перед созданием новой принудительной подписки Microsoft Edge проверяет, предоставил ли пользователь разрешение на получение уведомлений в PWA.  В противном случае пользователю будет предложено разрешить браузеру.  Если разрешение на доступ отклонено, запрос `registration.pushManager.subscribe` вызывает исключение a `DOMException` , поэтому необходимо обработать его.  Дополнительные сведения об управлении разрешениями можно найти [в разделе push-уведомления в Microsoft Edge][WindowsBlogsWebNotificationsEdge].  

В `pwabuilder-sw-register.js` файле добавьте следующий код.  

```javascript
// Subscribe this PWA to push notifications from the server
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(async function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                // Otherwise subscribe with the server public key
                const response = await fetch('./vapidPublicKey');
                const vapidPublicKey = await response.text();
                const convertedVapidKey = urlBase64ToUint8Array(vapidPublicKey);
                
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: convertedVapidKey
                });
            });
    }).then(function (subscription) {
        // Send the subscription details to the server
        fetch('./register', {
            method: 'post',
            headers: {
                'Content-type': 'application/json'
            },
            body: JSON.stringify({
                subscription: subscription
            }),
        });
        
        // Create a button to mimic server pushes for testing purposes
        var button = document.createElement('input');
        button.type = 'button';
        button.id = 'notify';
        button.value = 'Send Notification';
        document.body.appendChild(button);
        document.getElementById('notify').addEventListener('click', function () {
            fetch('./sendNotification', {
                method: 'post',
                headers: {
                    'Content-type': 'application/json'
                },
                body: JSON.stringify({
                    subscription: subscription
                }),
            });
        });
    });

// Utility function for browser interoperability
function urlBase64ToUint8Array(base64String) {
    var padding = '='.repeat((4 - base64String.length % 4) % 4);
    var base64 = (base64String + padding)
        .replace(/\-/g, '+')
        .replace(/_/g, '/');
        
    var rawData = window.atob(base64);
    var outputArray = new Uint8Array(rawData.length);
    
    for (var i = 0; i < rawData.length; ++i) {
        outputArray[i] = rawData.charCodeAt(i);
    }
    return outputArray;
}
```  

Ознакомьтесь с документацией по MDN на интерфейсе [PushManager][MDNPushManager] и NPM документами в [Интернет-библиотеке Push][NPMWebPushUsage] -данных для получения дополнительных сведений о работе API и различных связанных параметрах.  

### Шаг 5: Настройка обработчиков событий push-уведомлений и notificationclick  

При настройке принудительной подписки оставшаяся часть работы в сервисном работнике выполняется.  Сначала необходимо настроить обработчик для извещающих событий, отправленных сервером, и ответить с помощью всплывающего уведомления \ (если предоставлено разрешение), отображая полезные данные push-данных.  Затем вы добавите обработчик Click для всплывающего уведомления, чтобы отклонить уведомление и отсортировать список открытых в данный момент окон, которые нужно открыть, сосредоточиться или открыть, а также сосредоточиться на странице клиента Project Web App.  

В `pwabuilder-sw.js` файле добавьте следующие обработчики.  

```javascript
//Respond to a server push with a user notification
self.addEventListener('push', function (event) {
    if ("granted" === Notification.permission) {
        var payload = event.data ? event.data.text() : 'no payload';
        const promiseChain = self.registration.showNotification('Sample PWA', {
            body: payload,
            icon: 'images/windows10/Square44x44Logo.scale-100.png'
        });
        //Ensure the toast notification is displayed before exiting this function
        event.waitUntil(promiseChain);
    }
});
    
//Respond to the user clicking the toast notification
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current is already open and focuses it
    event.waitUntil(clients.matchAll({
        type: 'window'
    }).then(function (clientList) {
        for (var i = 0; i < clientList.length; i++) {
            var client = clientList[i];
            if (client.url == 'http://localhost:1337/' && 'focus' in client)
                return client.focus();
        }
        if (clients.openWindow)
            return clients.openWindow('/');
    }));
});
```  

### Шаг 6: попробовать  

Время на тестирование push-уведомлений в PWA!  

1.  Запустите `F5` в браузере веб-приложение Project Web App.  Так как вы изменили код сервисного рабочего процесса \ ( `pwabuilder-sw.js` \), необходимо открыть отладчик DevTools \ ( `F12` \) на панели **обзора рабочих процессов** и **отменить регистрацию** рабочего процесса и повторно загрузить \ ( `F5` \) страницы, чтобы заново ее зарегистрировать (или нажать кнопку **Обновить**).  В рабочем сценарии браузер проверяет регулярную проверку наличия обновлений для рабочего процесса обслуживания и устанавливает обновления в фоновом режиме.  Для немедленного поиска необходимо принудительно выполнить эту программу.  
    
    Когда сотрудник службы активируется и пытается оформить подписку на PWA для отправки уведомлений, вы увидите диалоговое окно с разрешениями в нижней части страницы.  
    
    ![Диалоговое окно разрешений для включения уведомлений][ImageNotificationPermission]  
    
    Нажмите кнопку **Да** , чтобы включить всплывающие уведомления для PWA.  
    
1.  На панели Общие сведения о рабочем процессе попробуйте нажать кнопку " **Отправить** ".  На экран будет отображено всплывающее уведомление с "\" с жестко заданным тестовым Push-сообщением из DevTools "\".  
    
    ![Отправка уведомления из DevTools][ImageDevtoolsPush]  
    
1.  Затем попробуйте нажать кнопку **Отправить уведомление** на домашней странице PWA.  На этот раз появится всплывающее уведомление с полезной нагрузкой на сервере.  
    
    ![Отправка уведомления с сервера PWA][ImagePwaPush]  
    
    Если вы не нажимайте кнопку \ (или активируете) всплывающее уведомление, оно будет закрыто через несколько секунд и помещается в очередь в центре уведомлений Windows.  
    
    ![Уведомления в центре уведомлений Windows][ImageWindowsActionCenter]  
    
    У вас есть основы push-уведомлений PWA.  В реальном приложении описанные ниже действия реализованы таким образом, чтобы управлять принудительными подписками и хранить их, а также для правильного [шифрования][NPMWebPushEncrypt] данных, передаваемых по сети.  
    
## Дальнейшая работа  

В этом руководстве показано, как создать прогрессивное веб-приложение и средства разработки для Microsoft PWA, в том числе Visual Studio, конструктор PWA и DevTools Edge.  

Разумеется, вы можете сделать так, чтобы выпустить веб-приложение [Project Web][PwaEdgehtmlIndexRequirements] App, помимо того, что вы прочитали здесь, в том числе разработку, глубокое связывание и [тестирование в разных браузерах][BrowserStackTestEdgeBrowser] , а также другие [Советы и рекомендации][Webhint] , но мы надеемся, что в этом руководстве предоставлено вам полное представление о концепциях PWA и идеи для начала работы.  Если у вас возникли вопросы по разработке PWA в Windows или Visual Studio, оставьте комментарий.  

Ознакомьтесь с другими руководствами по Project Web App, чтобы узнать о том, как повысить эффективность работы с клиентами и обеспечить более простое и интегрированное приложение для операционной системы.  

*   [Адаптация Windows][PwaEdgehtmlWindowsFeatures]. Благодаря функциям простого обнаружения функций вы можете последовательно усовершенствовать пользователей PWA для Windows 10 с помощью встроенных API среды выполнения Windows (WinRT), например для настройки уведомлений на плитке меню " **Пуск** " Windows и Jumplists, а также \ (при разрешении) для работы с пользовательскими ресурсами, такими как фотографии, музыка и календарь.  
*   [PWAs в Microsoft Store][PwaEdgehtmlMicrosoftStore].  Узнайте больше о преимуществах распространения магазина приложений и о том, как отправить PWA.  

## См. также  

*   [Прогрессивные веб-приложения в MDN веб-документах][MDNProgressiveWebApps] — отличное руководство по прогрессивным веб-приложениям.  
*   [Прогрессивные веб-приложения на веб-сайте Web. dev][WebDevProgressiveWebApps] -превосходное руководство по прогрессивным веб-приложениям.  
*   [Прогрессивные веб-приложения Rocks][ProgressiveWebApps] — наглядные примеры PWAs.  
*   [Средства чтения новостей, такие как прогрессивные веб-приложения,][HackerNewsProgressiveWebApps] сравнивают различные платформы и шаблоны производительности для реализации примера \ (средство чтения новостей с помощью хакеров \) PWA.  

<!-- image links -->  

[ImageDevtoolsPush]: ./media/devtools-push.png  
[ImageDevtoolsSwCache]: ./media/devtools-cache.png  
[ImageDevtoolsSwOverview]: ./media/devtools-sw-overview.png  
[ImageNotificationPermission]: ./media/notification-permission.png  
[ImageOfflineHtml]: ./media/offline-html.png  
[ImagePwa]: ./media/pwa.png  
[ImagePwaPush]: ./media/pwa-push.png  
[ImageVsNodejsExpressIcon]: ./media/vs-nodejs-express-icon.png  
[ImageVsNodejsExpressIndex]: ./media/vs-nodejs-express-index.png  
[ImageVsNodejsExpressManifest]: ./media/vs-nodejs-express-manifest.png  
[ImageVsNodejsExpressPublic]: ./media/vs-nodejs-express-public.png  
[ImageVsNodejsExpressTemplate]: ./media/vs-nodejs-express-template.png  
[ImageWindowsActionCenter]: ./media/windows-action-center.png  

<!-- links -->  

[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Требования к веб-приложениям с последовательностью \ (EdgeHTML \) в Windows"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Прогрессивные веб-приложения \ (EdgeHTML \) в Microsoft Store"  
[PwaEdgehtmlWindowsFeatures]: ../progressive-web-apps-edgehtml/windows-features.md "Настройка PWA \ (EdgeHTML \) для Windows"  

[LegalWindowsAgrementsMicrosoftStorePolicies]: /legal/windows/agreements/store-policies "Политики Microsoft Store | Документы Microsoft"  

[VisualStudioNodeJsTutorial]: /visualstudio/nodejs/tutorial-nodejs "Учебник: создание приложения Node. js и Экспресс-представления в Visual Studio | Документы Microsoft"  
[VisualStudioNodejsTutorialPublishAzureAppService]: /visualstudio/nodejs/tutorial-nodejs#optional-publish-to-azure-app-service "Публикация в службе приложений Azure — создание приложения Node. js и Экспресс-представления в Visual Studio | Документы Microsoft"  

[WindowsUwpGetStartedWhat]: /windows/uwp/get-started/whats-a-uwp "Что такое приложение универсальной платформы Windows (UWP)?  | Документы Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Создать бесплатную учетную запись Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Веб-приложения | Microsoft Azure"  

<!--[DeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote/ "page not found"  -->  

[WindowsBlogsPwaEdge]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#4UOdrDJj3124VIkc.97 "Welcoming последовательного веб-приложения в Microsoft EDGE и Windows 10 | Блоги Windows"  
[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Веб-уведомления в Microsoft Edge | Блоги Windows"  

[VisualStudioDownloads]: https://www.visualstudio.com/downloads "Загрузки | Visual Studio"  
[VisualStudioFree]: https://visualstudio.microsoft.com/free-developer-offers "Бесплатные приложения для разработчиков & службы | Visual Studio"  
[VisualStudioPreview]: https://www.visualstudio.com/vs/preview "Предварительная версия Visual Studio"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Бесплатное тестирование браузера Microsoft EDGE в Windows 10 | BrowserStack"  

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Средства чтения новостей от хакеров в виде последовательного веб-приложения"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/DedicatedWorkerGlobalScope/postMessage "DedicatedWorkerGlobalScope. i \ (\) | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Прогрессивные веб-приложения \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push-уведомлений | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочего процесса службы | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Работа с сотрудниками службы | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  
[MDNWorkerPrototypePostMessage]: https://developer.mozilla.org/docs/Web/API/Worker/postMessage "Worker. prototype. i сообщение \ (\) | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Отправка VAPID идентифицированных уведомлений о событиях через службу Push-сообщений для Mozilla | Службы Mozilla"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "веб-отправка | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, полезные данные, contentEncoding) — веб-отправка | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Использование-веб-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Прогрессивные веб-приложения"  

[PugAttributes]: https://pugjs.org/language/attributes.html "Атрибуты | Pug"  

[PwaBuilder]: https://www.pwabuilder.com "Конструктор PWA"  
[PwaBuilderAppImageGenerator]: https://www.pwabuilder.com/imageGenerator "Генератор изображений приложений"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Сервисный сотрудник | Конструктор PWA"  

[ServiceWorkerCookbook]: https://serviceworke.rs "ServiceWorker Cookbook"  
[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push-ролик с богатыми возможностями | ServiceWorker Cookbook"  

[W3cWebAppManifest]: https://www.w3.org/TR/appmanifest "Манифест веб-приложения | PNG"  

[Webhint]: https://sonarwhal.com "Подсказка, подсистема подсказок для веб-рекомендаций" 
 
[MDNWebWorkers]: https://developer.mozilla.org/docs/Web/API/Web_Workers_API/Using_web_workers "Использование веб-сотрудников" 

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Прогрессивные веб-приложения | Web. dev"  

[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS | Википедии"  
[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Улучшенное последовательное расширение | Википедии"  
