---
title: Управление сетевыми запросами и Push-уведомлениями с помощью рабочих процессов служб
description: Служебные работники — это веб-роли, которые помогают улучшить производительность, реагировать на различные условия сети и улучшать связь с веб-приложением.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: прогрессивные веб-приложения, PWA, EDGE, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 9bf573b668ade351716b69965f653e05857c32ec
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659302"
---
# <span data-ttu-id="aab2c-104">Управление сетевыми запросами и Push-уведомлениями с помощью рабочих процессов служб</span><span class="sxs-lookup"><span data-stu-id="aab2c-104">Use Service Workers to manage network requests and push notifications</span></span>

<span data-ttu-id="aab2c-105">Служебные работники — это особый тип рабочего процесса, с помощью которого можно перехватывать, изменять и отвечать на все сетевые запросы, используя `Fetch` API-интерфейс.</span><span class="sxs-lookup"><span data-stu-id="aab2c-105">Service Workers are a special type of Web Worker with the ability to intercept, modify, and respond to all network requests using the `Fetch` API.</span></span>  <span data-ttu-id="aab2c-106">Работники служб могут получить доступ к `Cache` API и асинхронные хранилища данных на стороне клиента, например `IndexedDB` , для хранения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aab2c-106">Service Workers can access the `Cache` API, and asynchronous client-side data stores, such as `IndexedDB`, to store resources.</span></span>  

## <span data-ttu-id="aab2c-107">Регистрация сотрудника службы</span><span class="sxs-lookup"><span data-stu-id="aab2c-107">Registering a Service Worker</span></span>  

<span data-ttu-id="aab2c-108">Как и другие веб-работники, сотрудники служб должны находиться в отдельном файле.</span><span class="sxs-lookup"><span data-stu-id="aab2c-108">Similar to other Web Workers, Service Workers must exist in a separate file.</span></span> <span data-ttu-id="aab2c-109">Вы хотите сослаться на этот файл при регистрации сотрудника службы, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="aab2c-109">You reference this file when registering the Service Worker, as shown in the following code snippet.</span></span>  

```javascript
if ( "serviceWorker" in navigator ) {
    navigator.serviceWorker.register( "/serviceworker.min.js" );
}
```  

<span data-ttu-id="aab2c-110">Современные браузеры предоставляют разные уровни поддержки для сотрудников служб.</span><span class="sxs-lookup"><span data-stu-id="aab2c-110">Modern browsers provide different levels of support for Service Workers.</span></span> <span data-ttu-id="aab2c-111">Таким образом, `serviceWorker` перед выполнением любого кода, связанного с сервисными сотрудниками, рекомендуется проверить существование объекта.</span><span class="sxs-lookup"><span data-stu-id="aab2c-111">As such, it is a good practice to test for the existence of the `serviceWorker` object before running any Service Worker-related code.</span></span> <span data-ttu-id="aab2c-112">В приведенном выше фрагменте кода сотрудник службы зарегистрирован с помощью `serviceworker.min.js` файла, расположенного в корне сайта.</span><span class="sxs-lookup"><span data-stu-id="aab2c-112">In the above code snippet, a Service Worker is registered using the `serviceworker.min.js` file located at the root of the site.</span></span> <span data-ttu-id="aab2c-113">Убедитесь, что файл JavaScript, который определяет сотрудника службы, существует в каталоге верхнего уровня, который вы хотите использовать для управления \ (который называется областью действия сотрудника).</span><span class="sxs-lookup"><span data-stu-id="aab2c-113">Ensure that the JavaScript file that defines your Service Worker exists in the highest-level directory that you want it to manage \(which is referred to as the scope of the Service Worker\).</span></span>  <span data-ttu-id="aab2c-114">В приведенном выше фрагменте кода файл хранится в корневом каталоге, а рабочий процесс управляет всеми страницами в домене.</span><span class="sxs-lookup"><span data-stu-id="aab2c-114">In the above code snippet, the file is stored in the root, and the Service Worker manages all pages in the domain.</span></span> <span data-ttu-id="aab2c-115">Если рабочий файл службы хранился в `js` каталоге, областью обслуживания является `js` каталог и вложенные папки.</span><span class="sxs-lookup"><span data-stu-id="aab2c-115">If the Service Worker file was stored in a `js` directory, the scope of the Service Worker would be the `js` directory and any subdirectories.</span></span>  <span data-ttu-id="aab2c-116">Рекомендуется размещать файл рабочего процесса службы в корне сайта, если вам не нужно уменьшать область обслуживания.</span><span class="sxs-lookup"><span data-stu-id="aab2c-116">As a best practice, place the Service Worker file in the root of your site, unless you need to reduce the scope of your Service Worker.</span></span>  

## <span data-ttu-id="aab2c-117">Жизненный цикл обслуживания сотрудников</span><span class="sxs-lookup"><span data-stu-id="aab2c-117">The Service Worker lifecycle</span></span>  

<span data-ttu-id="aab2c-118">Жизненный цикл сотрудника службы состоит из нескольких шагов, каждый из которых инициирует событие.</span><span class="sxs-lookup"><span data-stu-id="aab2c-118">The lifecycle of a Service Worker consists of multiple steps, with each step triggering an event.</span></span> <span data-ttu-id="aab2c-119">Вы можете добавлять прослушиватели для этих событий, чтобы выполнить код для выполнения действия.</span><span class="sxs-lookup"><span data-stu-id="aab2c-119">You can add listeners to these events to run code to perform an action.</span></span> <span data-ttu-id="aab2c-120">В приведенном ниже списке представлено общее представление жизненного цикла и связанных событий сотрудников служб.</span><span class="sxs-lookup"><span data-stu-id="aab2c-120">The following list presents a high-level view of the lifecycle and related events of service workers.</span></span> 

1. <span data-ttu-id="aab2c-121">Зарегистрируйте сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="aab2c-121">Register the Service Worker.</span></span>  
1.  <span data-ttu-id="aab2c-122">Браузер загружает файл JavaScript, устанавливает сотрудника службы и инициирует `install` событие.</span><span class="sxs-lookup"><span data-stu-id="aab2c-122">The browser downloads the JavaScript file, installs the Service Worker, and triggers the `install` event.</span></span> <span data-ttu-id="aab2c-123">Вы можете использовать `install` событие для предварительного кэширования важных и длительных файлов, таких как CSS-файлы, файлы JavaScript, изображения логотипов, автономные страницы и т. д.</span><span class="sxs-lookup"><span data-stu-id="aab2c-123">You can use the `install` event to pre-cache any important and long-lived files, such as CSS files, JavaScript files, logo images, offline pages, and so on from your website.</span></span>  
    
    ```javascript
    self.addEventListener( "install", function( event ){
        console.log( "WORKER: install event in progress." );
    });
    ```  
    
1.  <span data-ttu-id="aab2c-124">Активируется сотрудник службы, который запускает `activate` событие.</span><span class="sxs-lookup"><span data-stu-id="aab2c-124">The Service Worker is activated, which triggers the `activate` event.</span></span>  <span data-ttu-id="aab2c-125">Это событие используется для очистки устаревших кэшей.</span><span class="sxs-lookup"><span data-stu-id="aab2c-125">Use this event to clean up outdated caches.</span></span>  
    
    ```javascript
    self.addEventListener( "activate", event => {
        console.log('WORKER: activate event in progress.');
    });
    ```  
    
1.  <span data-ttu-id="aab2c-126">Сотрудник службы готов к выполнению при обновлении страницы или при переходе пользователя на новую страницу сайта.</span><span class="sxs-lookup"><span data-stu-id="aab2c-126">The Service Worker is ready to run when the page is refreshed or when the user navigates to a new page on the site.</span></span> <span data-ttu-id="aab2c-127">Если вы хотите запустить сервисный сотрудник без ожидания, используйте `self.skipWaiting()` метод во время `install` события.</span><span class="sxs-lookup"><span data-stu-id="aab2c-127">If you want to run the Service Worker without waiting, use the `self.skipWaiting()` method during the `install` event.</span></span>  
    
    ```javascript
    self.addEventListener( "install", event => {
        self.skipWaiting();
        // …
    });
    ```
    
1.  <span data-ttu-id="aab2c-128">Рабочий процесс обслуживания сейчас выполняется.</span><span class="sxs-lookup"><span data-stu-id="aab2c-128">The Service Worker is now running.</span></span>     
    
## <span data-ttu-id="aab2c-129">Использование fetch в рабочих работниках служб</span><span class="sxs-lookup"><span data-stu-id="aab2c-129">Using fetch in Service Workers</span></span>  

<span data-ttu-id="aab2c-130">Основное событие, используемое в качестве сотрудника службы, — это `fetch` событие.</span><span class="sxs-lookup"><span data-stu-id="aab2c-130">The main event that you use in a Service Worker is the `fetch` event.</span></span>  <span data-ttu-id="aab2c-131">`fetch`Событие выполняется каждый раз, когда браузер пытается получить доступ к содержимому в области действия сотрудника службы.</span><span class="sxs-lookup"><span data-stu-id="aab2c-131">The `fetch` event runs every time the browser attempts to access content within the scope of the Service Worker.</span></span> <span data-ttu-id="aab2c-132">В следующем фрагменте кода показано, как добавить прослушиватель в событие FETCH.</span><span class="sxs-lookup"><span data-stu-id="aab2c-132">The following code snippet shows how to add a listener to the fetch event.</span></span>  

```javascript
self.addEventListener( "fetch", event => {
  console.log('WORKER: Fetching', event.request);
});
```  

<span data-ttu-id="aab2c-133">Внутри `fetch` обработчика вы можете указать, будет ли запрос переноситься в сеть, отвлекать из кэша и т. д.</span><span class="sxs-lookup"><span data-stu-id="aab2c-133">Within the `fetch` handler, you may control whether a request goes to the network, pulls from the cache, and so on.</span></span>  <span data-ttu-id="aab2c-134">Подход, который вы будете использовать, зависит от типа запрашиваемого ресурса, частоты его обновления и других бизнес-логики, уникальных для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="aab2c-134">The approach you take likely varies based upon the type of resource being requested, how frequently it is updated, and other business logic unique to your application.</span></span>  <span data-ttu-id="aab2c-135">Вот несколько примеров того, что можно сделать:</span><span class="sxs-lookup"><span data-stu-id="aab2c-135">Here are a few examples of what you may do:</span></span>  

*   <span data-ttu-id="aab2c-136">Если это возможно, возвращайте ответ из кэша, в противном случае — откат, чтобы запросить ресурс по сети.</span><span class="sxs-lookup"><span data-stu-id="aab2c-136">If available, return a response from the cache, otherwise fallback to request the resource over the network.</span></span>  
*   <span data-ttu-id="aab2c-137">Получение ресурса из сети, кэширование копии и возврат ответа.</span><span class="sxs-lookup"><span data-stu-id="aab2c-137">Fetch a resource from the network, cache a copy, and return the response.</span></span>
*   <span data-ttu-id="aab2c-138">Разрешить пользователю указывать параметр, позволяющий сохранить данные.</span><span class="sxs-lookup"><span data-stu-id="aab2c-138">Allow user's to specify a preference to save data.</span></span> 
*   <span data-ttu-id="aab2c-139">Укажите изображение заполнителя для определенных запросов изображений.</span><span class="sxs-lookup"><span data-stu-id="aab2c-139">Supply a placeholder image for certain image requests.</span></span>  
*   <span data-ttu-id="aab2c-140">Создание ответа непосредственно в сотруднике службы.</span><span class="sxs-lookup"><span data-stu-id="aab2c-140">Generate a response directly in the Service Worker.</span></span>  

## <span data-ttu-id="aab2c-141">Push-уведомления</span><span class="sxs-lookup"><span data-stu-id="aab2c-141">Push Notifications</span></span>  

<span data-ttu-id="aab2c-142">Работники обслуживания могут отправлять уведомления пользователям.</span><span class="sxs-lookup"><span data-stu-id="aab2c-142">Service workers can push notifications to users.</span></span> <span data-ttu-id="aab2c-143">Push-уведомления полезны для запроса пользователей на повторное взаимодействие с приложением после того, как прошло какое-то время.</span><span class="sxs-lookup"><span data-stu-id="aab2c-143">Push Notifications are helpful to prompt users to re-engage with your application after some time has elapsed.</span></span> <span data-ttu-id="aab2c-144">Дополнительные сведения можно найти в разделе [Пошаговые инструкции и демонстрация push-уведомлений][AzurewebsitesWebpushdemo].</span><span class="sxs-lookup"><span data-stu-id="aab2c-144">For more information, see [Push Notifications walkthrough and demo][AzurewebsitesWebpushdemo].</span></span>  

## <span data-ttu-id="aab2c-145">См. также</span><span class="sxs-lookup"><span data-stu-id="aab2c-145">See also</span></span>  

<span data-ttu-id="aab2c-146">Дополнительные сведения о сотрудниках служб можно найти в приведенном ниже списке соответствующих тем.</span><span class="sxs-lookup"><span data-stu-id="aab2c-146">To learn more about Service Workers, see the following list of related topics.</span></span>  

*   [<span data-ttu-id="aab2c-147">PWAs автономной работы с сотрудниками служб</span><span class="sxs-lookup"><span data-stu-id="aab2c-147">Making PWAs work offline with Service workers</span></span>][MDNPwasMakingOfflineServiceWorkers]  
*   [<span data-ttu-id="aab2c-148">Как сделать так, чтобы PWAs повторно привлекать с помощью уведомлений и Push</span><span class="sxs-lookup"><span data-stu-id="aab2c-148">How to make PWAs re-engageable using Notifications and Push</span></span>][MDNPwasMakeReengageablesingNotificationsPush]  

<!-- links -->  

[AzurewebsitesWebpushdemo]: https://webpushdemo.azurewebsites.net "Push-уведомления в Интернете |  Демонстрации Microsoft Edge"  

[MDNPwasMakingOfflineServiceWorkers]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Offline_Service_workers "Как сделать PWAs работать автономно с сотрудниками служб — PWAs | MDN"  
[MDNPwasMakeReengageablesingNotificationsPush]: https://developer.mozilla.org/docs/Web/Progressive_web_apps/Re-engageable_Notifications_Push "Как сделать так, чтобы PWAs повторной подписаться с помощью уведомлений и Push-PWAs | MDN"  
