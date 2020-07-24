---
description: В этом руководстве вы найдете общие сведения о базовых данных и средствах для создания последовательной веб-приложений для Windows.
title: Приступая к работе с прогрессивными веб-приложениями (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
keywords: прогрессивные веб-приложения, PWA, EDGE, Windows, PWABuilder, веб-манифест, специалист по обслуживанию, отправка
ms.openlocfilehash: a9a0cad2d771e52b783053e36f0f23dec5d8e70c
ms.sourcegitcommit: 515522959f517e194f93a27f5d360690600edd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894712"
---
# <span data-ttu-id="6d10a-104">Приступая к работе с прогрессивными веб-приложениями (Chromium)</span><span class="sxs-lookup"><span data-stu-id="6d10a-104">Get started with Progressive Web Apps (Chromium)</span></span>  

<span data-ttu-id="6d10a-105">Прогрессивные веб-приложения \ (PWAs \) — это веб-приложения, которые [последовательно улучшены][WikiProgressiveEnhancement] с помощью таких функций, как установка, Автономная поддержка и Push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="6d10a-105">Progressive Web Apps \(PWAs\) are web apps that are [progressively enhanced][WikiProgressiveEnhancement] with app-like features, such as installation, offline support, and push notifications.</span></span>  <span data-ttu-id="6d10a-106">Кроме того, вы можете упаковать веб-приложения PWA для магазинов приложений, в том числе Microsoft Store, а также Google Play, Mac App Store и т. д.</span><span class="sxs-lookup"><span data-stu-id="6d10a-106">You may also packaged your PWA for app stores, including the Microsoft Store as well as Google Play, Mac App Store and more.</span></span>  <span data-ttu-id="6d10a-107">Microsoft Store — это коммерческое приложение, встроенное в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="6d10a-107">The Microsoft Store is the commercial app store built into Windows 10.</span></span>  

<span data-ttu-id="6d10a-108">В приведенном ниже руководстве представлен обзор основ PWA, создание простого веб-приложения и расширение его как PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-108">The following guide gives you an overview of PWA basics by creating a simple web app and extending it as a PWA.</span></span>  <span data-ttu-id="6d10a-109">Готовый проект работает в современных браузерах.</span><span class="sxs-lookup"><span data-stu-id="6d10a-109">The finished project works across modern browsers.</span></span>  

> [!TIP]
> <span data-ttu-id="6d10a-110">Вы можете использовать [PWABuilder][PwaBuilder] для создания нового PWA, улучшения существующего веб-приложения PWA или упаковки для магазина приложений PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-110">You may use [PWABuilder][PwaBuilder] to create a new PWA, enhance your existing PWA, or package your PWA for app stores.</span></span>  

## <span data-ttu-id="6d10a-111">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="6d10a-111">Prerequisites</span></span>  

*   <span data-ttu-id="6d10a-112">Использование [кода VS][VisualstudioCodeMain] для редактирования ИСХОДНОГО кода PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-112">Use [VS Code][VisualstudioCodeMain] to edit your PWA source code.</span></span>  
*   <span data-ttu-id="6d10a-113">Используйте [Node.js][NodejsMain] в качестве локального веб-сервера.</span><span class="sxs-lookup"><span data-stu-id="6d10a-113">Use [Node.js][NodejsMain] as your local web server.</span></span>  

## <span data-ttu-id="6d10a-114">Настройка простого веб-приложения</span><span class="sxs-lookup"><span data-stu-id="6d10a-114">Set up a basic web app</span></span>  

<span data-ttu-id="6d10a-115">Чтобы создать пустое веб-приложение, выполните действия, описанные в статье [генератор приложений для приложения Express][ExpressjsApplicationGenerator], и назовите свое приложение `MySamplePwa` .</span><span class="sxs-lookup"><span data-stu-id="6d10a-115">To create an empty web app, follow the steps in [Node Express App Generator][ExpressjsApplicationGenerator], and name your app `MySamplePwa`.</span></span>  

<span data-ttu-id="6d10a-116">В командной строке выполните указанные ниже команды.</span><span class="sxs-lookup"><span data-stu-id="6d10a-116">In the prompt, run the following commands.</span></span>  

```shell
npx express-generator --no-view
```  

```shell
npm install
```  

<span data-ttu-id="6d10a-117">Команды создают пустое веб-приложение и устанавливают все зависимости.</span><span class="sxs-lookup"><span data-stu-id="6d10a-117">The commands creates an empty web app and install any dependencies.</span></span>  

<span data-ttu-id="6d10a-118">Теперь у вас есть простое функциональное веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="6d10a-118">Now you have a simple, functional web app.</span></span>  <span data-ttu-id="6d10a-119">Чтобы запустить ее, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6d10a-119">To start it, run the following command.</span></span>  

```shell
npm start
```  

<span data-ttu-id="6d10a-120">Теперь можно перейти к `http://localhost:3000` просмотру нового веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="6d10a-120">Now browse to `http://localhost:3000` to view your new web app.</span></span>  

:::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="Выполнение нового PWA на localhost":::
   <span data-ttu-id="6d10a-122">Выполнение нового PWA на localhost</span><span class="sxs-lookup"><span data-stu-id="6d10a-122">Running your new PWA on localhost</span></span>
:::image-end:::

## <span data-ttu-id="6d10a-123">Начало создания PWA</span><span class="sxs-lookup"><span data-stu-id="6d10a-123">Get started building a PWA</span></span>  

<span data-ttu-id="6d10a-124">Теперь, когда у вас есть простое веб-приложение, расширьте его как PWA, добавив 3 требования для PWAs</span><span class="sxs-lookup"><span data-stu-id="6d10a-124">Now that you have a simple web app, extend it as a PWA by adding the 3 requirements for PWAs</span></span><!--[3 requirements for PWAs][PwaEdgehtmlIndexRequirements]--><span data-ttu-id="6d10a-125">: [HTTPS](#step-1---use-https), [Манифест веб-приложения](#step-2---create-a-web-app-manifest)и [сотрудник службы](#step-3---add-a-service-worker).</span><span class="sxs-lookup"><span data-stu-id="6d10a-125">: [HTTPS](#step-1---use-https), a [Web App Manifest](#step-2---create-a-web-app-manifest), and a [Service Worker](#step-3---add-a-service-worker).</span></span>  

### <span data-ttu-id="6d10a-126">Этап 1: использование HTTPS</span><span class="sxs-lookup"><span data-stu-id="6d10a-126">Step 1 - Use HTTPS</span></span>  

<span data-ttu-id="6d10a-127">Ключевые части платформы PWA, например [работники служб][MDNServiceWorkerApi], требуют использования HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6d10a-127">Key parts of the PWA platform, such as [Service Workers][MDNServiceWorkerApi], require the use of HTTPS.</span></span>  <span data-ttu-id="6d10a-128">Когда PWA разйдет в реальном времени, необходимо опубликовать его в URL-адресе HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6d10a-128">When your PWA goes live, you must publish it to an HTTPS URL.</span></span>  

<span data-ttu-id="6d10a-129">В целях отладки Microsoft EDGE также допускает `http://localhost` Использование API PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-129">For debugging purposes, Microsoft Edge also permits `http://localhost` to use the PWA APIs.</span></span>  

<span data-ttu-id="6d10a-130">Если вы [публикуете веб-приложение как активный сайт][VisualStudioNodejsTutorialPublishAzureAppService] (например, путем настройки [учетной записи Azure Free][AzureCreateFreeAccount]), необходимо убедиться, что сервер настроен для HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6d10a-130">If you [publish your web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="6d10a-131">Если вы используете [службу приложений Microsoft Azure][AzureWebApps] для размещения сайта, она по умолчанию обрабатывается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6d10a-131">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="6d10a-132">В следующем руководстве описано, `http://localhost` как выполнить СБОРКУ PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-132">The following guide, use `http://localhost` to build your PWA.</span></span>  

### <span data-ttu-id="6d10a-133">Шаг 2: создание манифеста веб-приложения</span><span class="sxs-lookup"><span data-stu-id="6d10a-133">Step 2 - Create a Web App Manifest</span></span>  

<span data-ttu-id="6d10a-134">[Манифест веб-приложения][MDNWebAppManifest] — это файл в формате JSON, содержащий метаданные вашего приложения, такие как имя, описание, значки и т. д.</span><span class="sxs-lookup"><span data-stu-id="6d10a-134">A [Web App Manifest][MDNWebAppManifest] is a JSON file containing metadata about your app, such as name, description, icons, and more.</span></span>  

<span data-ttu-id="6d10a-135">Чтобы добавить в веб-приложение манифест приложения, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6d10a-135">To add an app manifest to the web app:</span></span>  

1.  <span data-ttu-id="6d10a-136">В коде VS **File**  >  **откройте папку открыть** файл и выберите `MySamplePwa` каталог, созданный ранее.</span><span class="sxs-lookup"><span data-stu-id="6d10a-136">In VS Code, go **File** > **Open Folder** and choose the `MySamplePwa` directory you created earlier.</span></span>  
1.  <span data-ttu-id="6d10a-137">Нажмите кнопку `Ctrl` + `N` , чтобы создать новый файл, и вставьте его в следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="6d10a-137">Press `Ctrl`+`N` to create a new file, and paste in the following code snippet.</span></span>  
    
    ```json
    {
        "lang": "en-us",
        "name": "My Sample PWA",
        "short_name": "SamplePWA",
        "description": "A sample PWA for testing purposes",
        "start_url": "/",
        "background_color": "#2f3d58",
        "theme_color": "#2f3d58",        
        "orientation": "any",
        "display": "standalone",
        "icons": [
            {
                "src": "/icon512.png",
                "sizes": "512x512"
            }
        ]
    }
    ```  
    
1.  <span data-ttu-id="6d10a-138">Сохраните файл как `/MySamplePwa/public/manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="6d10a-138">Save the file as `/MySamplePwa/public/manifest.json`.</span></span>  
1.  <span data-ttu-id="6d10a-139">Добавление изображения значка приложения 512x512 с именем " `icon512.png` Кому" `/MySamplePwa/public/images` .</span><span class="sxs-lookup"><span data-stu-id="6d10a-139">Add a 512x512 app icon image named `icon512.png` to `/MySamplePwa/public/images`.</span></span>  <span data-ttu-id="6d10a-140">[Образец изображения][ImagePwa] можно использовать в целях тестирования.</span><span class="sxs-lookup"><span data-stu-id="6d10a-140">You may use the [sample image][ImagePwa] for testing purposes.</span></span>  
1.  <span data-ttu-id="6d10a-141">В коде VS откройте `/public/index.html` и добавьте следующий фрагмент кода в `<head>` тег.</span><span class="sxs-lookup"><span data-stu-id="6d10a-141">In VS Code, open `/public/index.html`, and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <link rel="manifest" href="/manifest.json">
    ```   
    
### <span data-ttu-id="6d10a-142">Шаг 3: Добавление сотрудника службы</span><span class="sxs-lookup"><span data-stu-id="6d10a-142">Step 3 - Add a Service Worker</span></span>  

<span data-ttu-id="6d10a-143">ИТ – это ключевая технология для PWAs, позволяющая выполнять сценарии, такие как поддержка в автономном режиме, дополнительное кэширование и выполнение фоновых задач, которые ранее были ограничены собственными приложениями.</span><span class="sxs-lookup"><span data-stu-id="6d10a-143">Service workers are the key technology behind PWAs, enabling scenarios like offline support, advanced caching, and running background tasks previously limited to native apps.</span></span>  

<span data-ttu-id="6d10a-144">Служебные работники — это фоновые задачи, которые перехватывают сетевые запросы из вашего веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="6d10a-144">Service workers are background tasks that intercept network requests from your web app.</span></span>  <span data-ttu-id="6d10a-145">Они выполняют задачи, даже если приложение PWA не запущено, например, помещение запрошенных ресурсов из кэша, отправка push-уведомлений, выполнение задач фоновой выборки, индикаторах событий значки и т. д.</span><span class="sxs-lookup"><span data-stu-id="6d10a-145">They perform tasks, even when your PWA is not running, such as serving requested resources from a cache, sending push notifications, running background fetch tasks, badging icons, and so on.</span></span>  <span data-ttu-id="6d10a-146">Служебные сотрудники определяются в специальном файле JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6d10a-146">Service workers are defined in a special JavaScript file.</span></span>  <span data-ttu-id="6d10a-147">Дополнительные сведения можно найти [в разделе Использование служебных служб][MDNUsingServiceWorkers] и [API обслуживания рабочих процессов служб][MDNServiceWorkerApi].</span><span class="sxs-lookup"><span data-stu-id="6d10a-147">For more information, see [Using Service Workers][MDNUsingServiceWorkers] and [Service Worker API][MDNServiceWorkerApi].</span></span>  

<span data-ttu-id="6d10a-148">Чтобы создать сотрудника службы в проекте, используйте рецепт роли " **первый из кэша** " в [построителе PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="6d10a-148">To build a service worker in your project, use the **Cache-first network** service worker recipe from [PWA Builder][PwaBuilderServiceWorker].</span></span>  

1.  <span data-ttu-id="6d10a-149">Перейдите к [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], выберите сотрудника, который является **первым из кэша** , и нажмите кнопку **скачать** .</span><span class="sxs-lookup"><span data-stu-id="6d10a-149">Navigate to [pwabuilder.com/serviceworker][PwaBuilderServiceWorker], select the **Cache-first network** service worker, and select the **Download** button.</span></span>  <span data-ttu-id="6d10a-150">Загруженный файл включает следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="6d10a-150">The downloaded file contains the following files:</span></span>
    
    *   `pwabuilder-sw-register.js`  
    *   `pwabuilder-sw.js`  
    
1.  <span data-ttu-id="6d10a-151">Скопируйте Скачанные файлы в `public` папку в проекте веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="6d10a-151">Copy the downloaded files to the `public` folder in your web app project.</span></span>  
    
1.  <span data-ttu-id="6d10a-152">В коде VS откройте `/public/index.html` и добавьте следующий фрагмент кода в `<head>` тег.</span><span class="sxs-lookup"><span data-stu-id="6d10a-152">In VS Code, open `/public/index.html` and add the following code snippet inside the `<head>` tag.</span></span>  
    
    ```html
    <script type="module" src="/pwabuilder-sw-register.js"></script>
    ```  
    
<span data-ttu-id="6d10a-153">У вашего веб-приложения теперь есть сотрудник службы, который использует стратегию первого кэша, которая сначала извлекает такие ресурсы, как изображения, JS, CSS и HTML из кэша, и при необходимости возвращается к сети.</span><span class="sxs-lookup"><span data-stu-id="6d10a-153">Your web app now has a service worker that uses the cache-first strategy, which fetches resources like images, JS, CSS, and HTML from the cache first, and falls back to the network as needed.</span></span>  

<span data-ttu-id="6d10a-154">Выполните указанные ниже действия, чтобы подтвердить выполнение рабочего процесса службы.</span><span class="sxs-lookup"><span data-stu-id="6d10a-154">Use the following steps to confirm that your service worker runs.</span></span>  

1.  <span data-ttu-id="6d10a-155">Перейдите к веб-приложению с помощью `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="6d10a-155">Navigate to your web app using `http://localhost:3000`.</span></span>  <span data-ttu-id="6d10a-156">Если веб-приложение недоступно, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="6d10a-156">If your web app is not available, run the following command.</span></span>   
    
    ```shell
    npm start
    ```
    
1.  <span data-ttu-id="6d10a-157">В Microsoft Edge щелкните, `F12` чтобы открыть Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="6d10a-157">In Microsoft Edge, select `F12` to open the Microsoft Edge DevTools.</span></span>  <span data-ttu-id="6d10a-158">Выберите **приложение**, а затем — **сотрудники службы** , чтобы просмотреть сотрудников службы.</span><span class="sxs-lookup"><span data-stu-id="6d10a-158">Select **Application**, then **Service Workers** to view the service workers.</span></span>  <span data-ttu-id="6d10a-159">Если вы не видите сотрудника службы, вам может потребоваться обновить страницу.</span><span class="sxs-lookup"><span data-stu-id="6d10a-159">If you do not see the service worker, you may need to refresh the page.</span></span>  
     
    :::image type="complex" source="./media/devtools-sw-overview.png" alt-text="Общие сведения о рабочем процессе службы Microsoft Edge DevTools":::
       <span data-ttu-id="6d10a-161">Общие сведения о рабочем процессе службы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6d10a-161">Microsoft Edge DevTools Service Worker overview</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="6d10a-162">Просмотрите кэш рабочих процессов службы, развернув **хранилище кэша** , и выберите **pwabuilder — предварительный кэш**.</span><span class="sxs-lookup"><span data-stu-id="6d10a-162">View the service worker cache by expanding **Cache Storage** and select **pwabuilder-precache**.</span></span>  <span data-ttu-id="6d10a-163">Будут видны все ресурсы, кэшируемые сотрудником службы, такие как значок приложения, манифест приложения, CSS и файлы JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6d10a-163">You should see all the resources cached by the service worker, such as the app icon, app manifest, CSS and JavaScript files.</span></span>  
    
    :::image type="complex" source="./media/devtools-cache.png" alt-text="Кэш рабочих процессов службы в Microsoft Edge DevTools":::
       <span data-ttu-id="6d10a-165">Кэш рабочих процессов службы в Microsoft Edge DevTools (F12)</span><span class="sxs-lookup"><span data-stu-id="6d10a-165">Service Worker cache in Microsoft Edge DevTools (F12)</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="6d10a-166">Попробуйте использование PWA в качестве автономного приложения.</span><span class="sxs-lookup"><span data-stu-id="6d10a-166">Try your PWA as an offline app.</span></span>  <span data-ttu-id="6d10a-167">В Microsoft Edge DevTools \ ( `F12` \) выберите **Network (сеть** ) и измените сетевой статус **Offline**на "не в сети". **Online**</span><span class="sxs-lookup"><span data-stu-id="6d10a-167">In Microsoft Edge DevTools \(`F12`\), choose **Network** then change the **Online** status to **Offline**.</span></span>  
    
    :::image type="complex" source="./media/devtools-offline.png" alt-text="Установка автономного режима приложения в Microsoft Edge DevTools":::
       <span data-ttu-id="6d10a-169">Установка автономного режима приложения в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="6d10a-169">Setting app to offline mode in Microsoft Edge DevTools</span></span>
    :::image-end:::
    
1.  <span data-ttu-id="6d10a-170">Обновите приложение, и вы увидите, что оно работает в автономном режиме, с помощью ресурсов приложения из кэша.</span><span class="sxs-lookup"><span data-stu-id="6d10a-170">Refresh your app and you should see it working offline by serving the resources of your app from the cache.</span></span>  
    
    :::image type="complex" source="./media/vs-nodejs-express-index.png" alt-text="PWA работает в автономном режиме":::
       <span data-ttu-id="6d10a-172">PWA работает в автономном режиме</span><span class="sxs-lookup"><span data-stu-id="6d10a-172">PWA running offline</span></span>
    :::image-end:::
    
## <span data-ttu-id="6d10a-173">Добавление push-уведомлений к PWA</span><span class="sxs-lookup"><span data-stu-id="6d10a-173">Add push notifications to your PWA</span></span>  

<span data-ttu-id="6d10a-174">Вы можете создать PWAs, поддерживающий push-уведомления, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="6d10a-174">You may create PWAs that support push notifications by completing the following tasks.</span></span>  

1.  <span data-ttu-id="6d10a-175">Подписка на службу сообщений с помощью [API push-уведомлений][MDNPushApi]</span><span class="sxs-lookup"><span data-stu-id="6d10a-175">Subscribe to a messaging service using the [Push API][MDNPushApi]</span></span>  
1.  <span data-ttu-id="6d10a-176">Показывать всплывающие сообщения при получении сообщения от службы с помощью [API уведомлений][MDNNotificationsApi]</span><span class="sxs-lookup"><span data-stu-id="6d10a-176">Display a toast messages when a message is received from the service using the [Notifications API][MDNNotificationsApi]</span></span>  

<span data-ttu-id="6d10a-177">Как и в случае с сотрудниками служб, это основанные на стандартах API, которые работают в разных браузерах, поэтому вам нужно написать код только один раз для того, чтобы он работал везде, где они PWAs поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="6d10a-177">As with Service Workers, these are standards-based APIs that work across browsers, so you only have to write the code once for it to work everywhere that PWAs are supported.</span></span>  <span data-ttu-id="6d10a-178">Дополнительные сведения о том, как отправлять push-сообщения в другие браузеры на сервере, можно получить с помощью [веб-][NPMWebPush] библиотеки Open Source.</span><span class="sxs-lookup"><span data-stu-id="6d10a-178">For more information on delivering push messages to different browsers on your server, use the [Web-Push][NPMWebPush] open-source library.</span></span>  

<span data-ttu-id="6d10a-179">Описанные ниже действия были адаптированы с помощью демона "Push-Cookbook" в [службе обслуживания сотрудников][ServiceWorkerCookbookPushRichDemo] , предоставляемой Mozilla, которая имеет ряд других полезных рецептов для отправки по Интернету и обслуживания рабочих процессов.</span><span class="sxs-lookup"><span data-stu-id="6d10a-179">The following steps have been adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which has a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="6d10a-180">Шаг 1. Создание VAPIDных ключей</span><span class="sxs-lookup"><span data-stu-id="6d10a-180">Step 1 - Generate VAPID keys</span></span>  

<span data-ttu-id="6d10a-181">Для отправки push-сообщений в клиент PWA требуется VAPID \ (код добровольного сервера приложений) с помощью извещающих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6d10a-181">Push notifications require VAPID \(Voluntary Application Server Identification\) keys in order to send push messages to the PWA client.</span></span>  <span data-ttu-id="6d10a-182">Доступно несколько VAPIDных генераторов ключей в Интернете (например, [vapidkeys.com][VapidkeysMain]\).</span><span class="sxs-lookup"><span data-stu-id="6d10a-182">There are several VAPID key generators available online \(for example, [vapidkeys.com][VapidkeysMain]\).</span></span>  <span data-ttu-id="6d10a-183">После создания необходимо получить объект JSON, содержащий открытый и закрытый ключи.</span><span class="sxs-lookup"><span data-stu-id="6d10a-183">After generation, you should get a JSON object containing a public and private key.</span></span>  <span data-ttu-id="6d10a-184">Сохраните клавиши для дальнейших действий, описанных в следующем учебнике.</span><span class="sxs-lookup"><span data-stu-id="6d10a-184">Save the keys for subsequent steps in the following tutorial.</span></span>  <span data-ttu-id="6d10a-185">Сведения о том, как работают VAPID и VAPID, приведены в разделе Отправка поступающих [извещений о событиях через службу push-уведомлений Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush].</span><span class="sxs-lookup"><span data-stu-id="6d10a-185">For information on how VAPID and WebPush works, see [Sending VAPID identified WebPush Notifications via Mozilla's Push Service][MozillaServicesSendingVapidWebPushNotificationsPush].</span></span>  

### <span data-ttu-id="6d10a-186">Шаг 2: подписаться на push-уведомления</span><span class="sxs-lookup"><span data-stu-id="6d10a-186">Step 2 - Subscribe to push notifications</span></span>  

<span data-ttu-id="6d10a-187">Работники обслуживания обрабатывают события push-уведомлений и взаимодействие с всплывающими уведомлениями в PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-187">Service workers handle push events and toast notification interactions in your PWA.</span></span>  <span data-ttu-id="6d10a-188">Чтобы оформить подписку на push-уведомления сервера PWA, убедитесь, что выполнены указанные ниже условия.</span><span class="sxs-lookup"><span data-stu-id="6d10a-188">To subscribe the PWA to server push notifications, ensure the following conditions are met.</span></span>  

*   <span data-ttu-id="6d10a-189">Приложение PWA установлено, активно и зарегистрировано</span><span class="sxs-lookup"><span data-stu-id="6d10a-189">Your PWA is installed, active and registered</span></span>  
*   <span data-ttu-id="6d10a-190">Код, выполняющий задачу по подписке, находится в основном потоке пользовательского интерфейса PWA</span><span class="sxs-lookup"><span data-stu-id="6d10a-190">Your code that performs the subscription task is on the main UI thread of the PWA</span></span>  
*   <span data-ttu-id="6d10a-191">Вы подключены к сети</span><span class="sxs-lookup"><span data-stu-id="6d10a-191">You have network connectivity</span></span>  

<span data-ttu-id="6d10a-192">Перед созданием новой принудительной подписки Microsoft Edge проверяет, предоставил ли пользователь разрешение на получение уведомлений в PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-192">Before a new push subscription is created, Microsoft Edge checks if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="6d10a-193">В противном случае пользователю будет предложено разрешить браузеру.</span><span class="sxs-lookup"><span data-stu-id="6d10a-193">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="6d10a-194">Если разрешение закрыто, запрос `registration.pushManager.subscribe` генерирует исключение `DOMException` , которое должно быть обработано.</span><span class="sxs-lookup"><span data-stu-id="6d10a-194">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, which must be handled.</span></span>  <span data-ttu-id="6d10a-195">Дополнительные сведения об управлении разрешениями можно найти [в разделе push-уведомления в Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="6d10a-195">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="6d10a-196">Добавьте в `pwabuilder-sw-register.js` файл следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="6d10a-196">In your `pwabuilder-sw-register.js` file, append the following code snippet.</span></span>  

```javascript
// Ask the user for permission to send push notifications.
navigator.serviceWorker.ready
    .then(function (registration) {
        // Check if the user has an existing subscription
        return registration.pushManager.getSubscription()
            .then(function (subscription) {
                if (subscription) {
                    return subscription;
                }
                
                const vapidPublicKey = "PASTE YOUR PUBLIC VAPID KEY HERE";             
                return registration.pushManager.subscribe({
                    userVisibleOnly: true,
                    applicationServerKey: urlBase64ToUint8Array(vapidPublicKey)
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

<span data-ttu-id="6d10a-197">Дополнительные сведения можно найти в разделе [PushManager][MDNPushManager] и [Отправка по Интернету][NPMWebPushUsage].</span><span class="sxs-lookup"><span data-stu-id="6d10a-197">For more information, see [PushManager][MDNPushManager] and [Web-Push][NPMWebPushUsage].</span></span>  

### <span data-ttu-id="6d10a-198">Шаг 3: прослушивание push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="6d10a-198">Step 3 - Listen for push notifications</span></span>  

<span data-ttu-id="6d10a-199">Теперь, когда вы настроили подписку на веб-сервере PWA, добавьте обработчики для этого сотрудника, чтобы реагировать на события push-уведомлений (отправленные с сервера), чтобы отобразить всплывающие уведомления с данными полученного сообщения.</span><span class="sxs-lookup"><span data-stu-id="6d10a-199">Now that a subscription is set up in your PWA, add handlers to the service worker to respond to push events \(sent from the server\) to display toast notifications with the data of a received message.</span></span>  <span data-ttu-id="6d10a-200">Чтобы выполнить любое из перечисленных ниже действий, необходимо добавить обработчик нажатия.</span><span class="sxs-lookup"><span data-stu-id="6d10a-200">You must add a click handler to perform the any of the following tasks.</span></span>  
*   <span data-ttu-id="6d10a-201">закрыть всплывающее уведомление</span><span class="sxs-lookup"><span data-stu-id="6d10a-201">dismiss the toast notification</span></span>  
*   <span data-ttu-id="6d10a-202">открыть, сфокусировать или открыть и сфокусировать любые открытые окна</span><span class="sxs-lookup"><span data-stu-id="6d10a-202">open, focus, or open and focus any open windows</span></span>  
*   <span data-ttu-id="6d10a-203">Открытие нового окна и фокусирование для отображения страницы клиента PWA</span><span class="sxs-lookup"><span data-stu-id="6d10a-203">open and focus a new window to display a PWA client page</span></span>  

<span data-ttu-id="6d10a-204">В `pwabuilder-sw.js` файле добавьте следующие обработчики.</span><span class="sxs-lookup"><span data-stu-id="6d10a-204">In your `pwabuilder-sw.js` file, add the following handlers.</span></span>  

```javascript
// Respond to a server push with a user notification.
self.addEventListener('push', function (event) {
    if (Notification.permission === "granted") {
        const notificationText = event.data.text();
        const showNotification = self.registration.showNotification('Sample PWA', {
            body: notificationText,
            icon: 'images/icon512.png'
        });
        // Ensure the toast notification is displayed before exiting the function.
        event.waitUntil(showNotification);
    }
});

// Respond to the user selecting the toast notification.
self.addEventListener('notificationclick', function (event) {
    console.log('On notification click: ', event.notification.tag);
    event.notification.close();
    
    // This looks to see if the current notification is already open and focuses it.
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

### <span data-ttu-id="6d10a-205">Шаг 4: попробуйте.</span><span class="sxs-lookup"><span data-stu-id="6d10a-205">Step 4 - Try it out</span></span>  

<span data-ttu-id="6d10a-206">Выполните указанные ниже действия, чтобы проверить push-уведомления в PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-206">Perform the following steps to test push notifications in your PWA.</span></span>  

1.  <span data-ttu-id="6d10a-207">Перейдите на веб – PWA по адресу `http://localhost:3000` .</span><span class="sxs-lookup"><span data-stu-id="6d10a-207">Navigate to your PWA at `http://localhost:3000`.</span></span>  <span data-ttu-id="6d10a-208">Когда сотрудник службы активируется и пытается оформить подписку на PWA для push-уведомлений, Microsoft Edge предлагает вам разрешить просмотр уведомлений на PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-208">When your service worker activates and attempts to subscribe your PWA to push notifications, Microsoft Edge prompts you to allow your PWA to show notifications.</span></span>  <span data-ttu-id="6d10a-209">Нажмите кнопку **Разрешить**.</span><span class="sxs-lookup"><span data-stu-id="6d10a-209">Select **Allow**.</span></span>  
    
    :::image type="complex" source="./media/notification-permission.png" alt-text="Диалоговое окно разрешений для включения уведомлений":::
       <span data-ttu-id="6d10a-211">Диалоговое окно разрешений для включения уведомлений</span><span class="sxs-lookup"><span data-stu-id="6d10a-211">Permission dialog for enabling notifications</span></span>
    :::image-end:::
    
    
1.  <span data-ttu-id="6d10a-212">Имитировать push-уведомление на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="6d10a-212">Simulate a server-side push notification.</span></span>  <span data-ttu-id="6d10a-213">Откройте веб – приложение Project Web App `http://localhost:3000` в браузере и нажмите кнопку, `F12` чтобы открыть DevTools.</span><span class="sxs-lookup"><span data-stu-id="6d10a-213">With your PWA opened at `http://localhost:3000` in your browser, select `F12` to open the DevTools.</span></span>  <span data-ttu-id="6d10a-214">Нажмите **кнопку**отправить,  >  **Service Worker**  >  **Push** чтобы отправить тестовое push-уведомление на PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-214">Choose **Application** > **Service Worker** > **Push** to send a test push notification to your PWA.</span></span>  <span data-ttu-id="6d10a-215">Рядом с панелью задач появится push-уведомление.</span><span class="sxs-lookup"><span data-stu-id="6d10a-215">You should see a push notification appear near the taskbar.</span></span>  
    
    :::image type="complex" source="./media/devtools-push.png" alt-text="Отправка уведомления из DevTools":::
       <span data-ttu-id="6d10a-217">Отправка уведомления из DevTools</span><span class="sxs-lookup"><span data-stu-id="6d10a-217">Push a notification from DevTools</span></span>
    :::image-end:::
     
    <span data-ttu-id="6d10a-218">Если вы не выберете параметр \ (или активировать) всплывающее уведомление, оно будет закрыто через несколько секунд и помещается в очередь в центре уведомлений Windows.</span><span class="sxs-lookup"><span data-stu-id="6d10a-218">If you do not select \(or activate\) a toast notification, it is dismissed after several seconds and queues up in your Windows Action Center.</span></span>  
    
    :::image type="complex" source="./media/windows-action-center.png" alt-text="Уведомления в центре уведомлений Windows":::
       <span data-ttu-id="6d10a-220">Уведомления в центре уведомлений Windows</span><span class="sxs-lookup"><span data-stu-id="6d10a-220">Notifications in Windows Action Center</span></span>
    :::image-end:::
    
    
## <span data-ttu-id="6d10a-221">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6d10a-221">Next steps</span></span>  

<span data-ttu-id="6d10a-222">Ниже приведен список дополнительных задач, с помощью которых можно ознакомиться с созданием реальных PWAs:</span><span class="sxs-lookup"><span data-stu-id="6d10a-222">The following is a list of additional tasks to learn when building real-world PWAs:</span></span>  

*  <span data-ttu-id="6d10a-223">Управление принудительными подписками и их хранение</span><span class="sxs-lookup"><span data-stu-id="6d10a-223">Manage and store push subscriptions</span></span>  
*  <span data-ttu-id="6d10a-224">[Шифрование][NPMWebPushEncrypt] полезных данных</span><span class="sxs-lookup"><span data-stu-id="6d10a-224">[Encrypt][NPMWebPushEncrypt] payload data</span></span>  
*  <span data-ttu-id="6d10a-225">Адаптивный дизайн</span><span class="sxs-lookup"><span data-stu-id="6d10a-225">Responsive design</span></span>  
*  <span data-ttu-id="6d10a-226">Глубокая связь</span><span class="sxs-lookup"><span data-stu-id="6d10a-226">Deep-linking</span></span>  
*  [<span data-ttu-id="6d10a-227">Тестирование в нескольких браузерах</span><span class="sxs-lookup"><span data-stu-id="6d10a-227">Cross-browser testing</span></span>][BrowserStackTestEdgeBrowser]  
*  <span data-ttu-id="6d10a-228">Реализация рекомендаций, таких как " [Совет][Webhint] "</span><span class="sxs-lookup"><span data-stu-id="6d10a-228">Implement best practices such as [Webhint][Webhint]</span></span>  

## <span data-ttu-id="6d10a-229">См. также</span><span class="sxs-lookup"><span data-stu-id="6d10a-229">See also</span></span>  

*   <span data-ttu-id="6d10a-230">[Прогрессивные веб-приложения на MDN веб-документах][MDNProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="6d10a-230">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps].</span></span>  
*   <span data-ttu-id="6d10a-231">[Прогрессивные веб-приложения на Web. dev][WebDevProgressiveWebApps].</span><span class="sxs-lookup"><span data-stu-id="6d10a-231">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps].</span></span>  
*   <span data-ttu-id="6d10a-232">[Средства чтения новостей, такие как прогрессивные веб-приложения,][HackerNewsProgressiveWebApps] сравнивают различные платформы и шаблоны производительности для реализации примера \ (средство чтения новостей с помощью хакеров \) PWA.</span><span class="sxs-lookup"><span data-stu-id="6d10a-232">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

<!-- image links -->  

[ImagePwa]: ./media/pwa.png  

<!-- links -->  

<!--[PwaEdgehtmlIndexRequirements]: ../progressive-web-apps-edgehtml/index.md#requirements "Requirements - Progressive Web Apps \(EdgeHTML\) on Windows | Microsoft Docs"  -->  

[VisualStudioNodejsTutorialPublishAzureAppService]: /azure/javascript/tutorial-vscode-azure-app-service-node-03 "Развертывание Node.js приложения в Azure с помощью кода VS | Документы Microsoft"  

[AzureCreateFreeAccount]: https://azure.microsoft.com/free "Создать бесплатную учетную запись Azure | Microsoft Azure"  
[AzureWebApps]: https://azure.microsoft.com/services/app-service/web "Веб-приложения | Microsoft Azure"  

[WindowsBlogsWebNotificationsEdge]: https://blogs.windows.com/msedgedev/2016/05/16/web-notifications-microsoft-edge#UAbvU2ymUlHO8EUV.97 "Веб-уведомления в Microsoft Edge | Блоги Windows"  

[VisualstudioCodeMain]: https://code.visualstudio.com "Код Visual Studio"  

[BrowserStackTestEdgeBrowser]: https://www.browserstack.com/test-on-microsoft-edge-browser "Бесплатное тестирование браузера Microsoft EDGE в Windows 10 | BrowserStack"  

[ExpressjsApplicationGenerator]: https://expressjs.com/starter/generator.html "Генератор приложений для Экспресс | Предоставлен" 

[HackerNewsProgressiveWebApps]: https://hnpwa.com "Средства чтения новостей от хакеров в виде последовательного веб-приложения"  

[MDNDedicatedWorkerGlobalScopePostMessage]: https://developer.mozilla.org/docs/Web/API/
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNProgressiveWebApps]: https://developer.mozilla.org/Apps/Progressive "Прогрессивные веб-приложения \ (PWAs) | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push-уведомлений | MDN"  
[MDNPushManager]: https://developer.mozilla.org/docs/Web/API/PushManager "PushManager | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочего процесса службы | MDN"  
[MDNUsingServiceWorkers]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API/Using_Service_Workers "Работа с сотрудниками службы | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[MozillaServicesSendingVapidWebPushNotificationsPush]: https://blog.mozilla.org/services/2016/08/23/sending-vapid-identified-webpush-notifications-via-mozillas-push-service "Отправка VAPID идентифицированных уведомлений о событиях через службу Push-сообщений для Mozilla | Службы Mozilla"  

[NodejsMain]: https://nodejs.org "Node.js"  

[NPMWebPush]: https://www.npmjs.com/package/web-push "веб-отправка | NPM"  
[NPMWebPushEncrypt]: https://www.npmjs.com/package/web-push#encryptuserpublickey-userauth-payload-contentencoding "Encrypt (userPublicKey, userAuth, полезные данные, contentEncoding) — веб-отправка | NPM"  
[NPMWebPushUsage]: https://www.npmjs.com/package/web-push#usage "Использование-веб-Push | NPM"  

[ProgressiveWebApps]: https://pwa.rocks "Прогрессивные веб-приложения"  

[PwaBuilder]: https://www.pwabuilder.com "Конструктор PWA"  
[PwaBuilderServiceWorker]: https://www.pwabuilder.com/serviceworker "Сервисный сотрудник | Конструктор PWA"  

[ServiceWorkerCookbookPushRichDemo]: https://serviceworke.rs/push-rich_demo.html "Push-ролик с богатыми возможностями | ServiceWorker Cookbook"  

[VapidkeysMain]: https://vapidkeys.com "VAPID Secure Key | VapidKeys" 

[Webhint]: https://sonarwhal.com "Подсказка, подсистема подсказок для веб-рекомендаций"  

[WebDevProgressiveWebApps]: https://developers.google.com/web/progressive-web-apps "Прогрессивные веб-приложения | Web. dev"  

[WikiProgressiveEnhancement]: https://en.wikipedia.org/wiki/Progressive_enhancement "Улучшенное последовательное расширение | Википедии"  
