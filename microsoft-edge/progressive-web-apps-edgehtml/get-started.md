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
# <span data-ttu-id="af2eb-104">Приступите к работе с прогрессивными веб-приложениями</span><span class="sxs-lookup"><span data-stu-id="af2eb-104">Get started with Progressive Web Apps</span></span>  

<span data-ttu-id="af2eb-105">Прогрессивные веб-приложения \ (PWAs \) — это веб-приложения, которые [последовательно дополнены][WikiProgressiveEnhancement] функциями поддержки платформ и обработчиков браузеров, таких как установка из системы и работа с приложениями начальный экран, Автономная поддержка и Push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="af2eb-105">Progressive Web Apps \(PWAs\) are simply web apps that are [progressively enhanced][WikiProgressiveEnhancement] with native app-like features on supporting platforms and browser engines, such as launch-from-homescreen installation, offline support, and push notifications.</span></span>  <span data-ttu-id="af2eb-106">В Windows 10 с ядром Microsoft Edge \ (EdgeHTML \) PWAs наслаждайтесь дополнительным преимуществом работы независимо от окна браузера в качестве приложений [универсальной платформы Windows][WindowsUwpGetStartedWhat] .</span><span class="sxs-lookup"><span data-stu-id="af2eb-106">On Windows 10 with the Microsoft Edge \(EdgeHTML\) engine, PWAs enjoy the added advantage of running independently of the browser window as [Universal Windows Platform][WindowsUwpGetStartedWhat] apps.</span></span>  

<span data-ttu-id="af2eb-107">В этом руководстве вы найдете общие сведения об основных возможностях PWA, создав простое `localhost` веб-приложение в PWA с помощью Microsoft Visual Studio и некоторых служебных программ PWA.</span><span class="sxs-lookup"><span data-stu-id="af2eb-107">This guide gives you an overview of PWA basics by building a simple `localhost` web app as a PWA using Microsoft Visual Studio and some PWA Builder utilities.</span></span>  <span data-ttu-id="af2eb-108">Готовый продукт работает так же, как и любой браузер, поддерживающий PWAs.</span><span class="sxs-lookup"><span data-stu-id="af2eb-108">The finished product works similarly across any browser that supports PWAs.</span></span>  

> [!TIP]
> <span data-ttu-id="af2eb-109">Чтобы быстро преобразовать существующий веб-сайт в PWA и упаковать его для Windows 10 и других платформ приложений, ознакомьтесь с [построителем PWA][PwaBuilder].</span><span class="sxs-lookup"><span data-stu-id="af2eb-109">For a quick way to convert an existing site to a PWA and package it for Windows 10 and other app platforms, review [PWA Builder][PwaBuilder].</span></span>  

## <span data-ttu-id="af2eb-110">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="af2eb-110">Prerequisites</span></span>  

<span data-ttu-id="af2eb-111">Вы можете создать PWAs с любой интегрированной средой разработки веб-приложений.</span><span class="sxs-lookup"><span data-stu-id="af2eb-111">You may build PWAs with any web development IDE.</span></span>  <span data-ttu-id="af2eb-112">Ниже приведены только необходимые условия для этого руководства, в ходе которого вы переходите в службу поддержки средств на панели управления для Windows для разработчиков.</span><span class="sxs-lookup"><span data-stu-id="af2eb-112">The following are only prerequisites for this guide, which walks you through PWA tooling support in the Windows developer ecosystem.</span></span>  

*   <span data-ttu-id="af2eb-113">Скачайте (бесплатное) [Visual Studio Community 2017][VisualStudioDownloads].</span><span class="sxs-lookup"><span data-stu-id="af2eb-113">Download the \(free\) [Visual Studio Community 2017][VisualStudioDownloads].</span></span>  <span data-ttu-id="af2eb-114">Вы также можете использовать выпуски профессионального выпуска, Enterprise или [Preview][VisualStudioPreview] .</span><span class="sxs-lookup"><span data-stu-id="af2eb-114">You may also use the Professional, Enterprise, or [Preview][VisualStudioPreview] editions.</span></span>  <span data-ttu-id="af2eb-115">В установщике Visual Studio выберите указанные ниже рабочие нагрузки.</span><span class="sxs-lookup"><span data-stu-id="af2eb-115">From the Visual Studio Installer, choose the following Workloads.</span></span>  
    
    *   **<span data-ttu-id="af2eb-116">Разработка универсальной платформы Windows</span><span class="sxs-lookup"><span data-stu-id="af2eb-116">Universal Windows Platform development</span></span>**  
    *   **<span data-ttu-id="af2eb-117">Разработка приложений Node. js</span><span class="sxs-lookup"><span data-stu-id="af2eb-117">Node.js development</span></span>**  

## <span data-ttu-id="af2eb-118">Настройка простого веб-приложения</span><span class="sxs-lookup"><span data-stu-id="af2eb-118">Set up a basic web app</span></span>  

<span data-ttu-id="af2eb-119">Для простоты используйте шаблон Visual Studio [node. js и Экспресс-приложение][VisualStudioNodeJsTutorial] , чтобы создать `localhost` приложение, которое будет служить `index.html` страницей.</span><span class="sxs-lookup"><span data-stu-id="af2eb-119">For the sake of simplicity, use the Visual Studio [Node.js and Express app][VisualStudioNodeJsTutorial] template to create `localhost` web app that serves up an `index.html` page.</span></span>  <span data-ttu-id="af2eb-120">Представьте это в качестве заполнителя для привлекательного полнофункционального веб-приложения, которое вы разрабатываете как PWA.</span><span class="sxs-lookup"><span data-stu-id="af2eb-120">Imagine this as a placeholder for the compelling, full-featured web app that you are developing as a PWA.</span></span>  

1.  <span data-ttu-id="af2eb-121">Запустите Visual Studio и начните новый проект.</span><span class="sxs-lookup"><span data-stu-id="af2eb-121">Launch Visual Studio, and start a new project.</span></span>  
    *   <span data-ttu-id="af2eb-122">**Файл**  >  **Новые**  >  **Проект...**</span><span class="sxs-lookup"><span data-stu-id="af2eb-122">**File** > **New** > **Project...**</span></span>  
    *   `Ctrl`+`Shift`+`N`  
1.  <span data-ttu-id="af2eb-123">В разделе **JavaScript**выберите **базовый приложение Node. js Express 4**.</span><span class="sxs-lookup"><span data-stu-id="af2eb-123">Under **JavaScript**, select **Basic Node.js Express 4 Application**.</span></span>  <span data-ttu-id="af2eb-124">Укажите имя и расположение и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="af2eb-124">Set the name and location and choose **OK**.</span></span>  
    
    ![Выбор шаблона проекта Node. js Express 4 в Visual Studio][ImageVsNodejsExpressTemplate]  
    
1.  <span data-ttu-id="af2eb-126">После загрузки нового проекта выберите команду **построить** \ ( `Ctrl` + `Shift` + `B` \) и **начать отладку** \ ( `F5` \).</span><span class="sxs-lookup"><span data-stu-id="af2eb-126">Once your new project loads, choose **Build** \(`Ctrl`+`Shift`+`B`\) and **Start Debugging** \(`F5`\).</span></span>  <span data-ttu-id="af2eb-127">Убедитесь в том, что `index.html` файл загружается при просмотре `http://localhost:1337` .</span><span class="sxs-lookup"><span data-stu-id="af2eb-127">Verify that your `index.html` file loads when you browse to `http://localhost:1337`.</span></span>  
    
    ![Выполнение нового сайта на localhost][ImageVsNodejsExpressIndex]  

## <span data-ttu-id="af2eb-129">Преобразование приложения в PWA</span><span class="sxs-lookup"><span data-stu-id="af2eb-129">Turn your app into a PWA</span></span>  

<span data-ttu-id="af2eb-130">Теперь пришло время связать базовые [требования PWA][PwaEdgehtmlIndexRequirements] для вашего веб-приложения: *Манифест веб-приложения*, *HTTPS* и *сотрудников службы*.</span><span class="sxs-lookup"><span data-stu-id="af2eb-130">Now it is time to wire up the basic [PWA requirements][PwaEdgehtmlIndexRequirements] for your web app: a *Web App Manifest*, *HTTPS* and *Service Workers*.</span></span>  

### <span data-ttu-id="af2eb-131">Манифест веб-приложения</span><span class="sxs-lookup"><span data-stu-id="af2eb-131">Web App Manifest</span></span>  

<span data-ttu-id="af2eb-132">[Манифест веб-приложения][MDNWebAppManifest] — это файл метаданных JSON, описывающий ваше приложение, включая имя, автора, URL-адрес страницы ввода и один или несколько значков.</span><span class="sxs-lookup"><span data-stu-id="af2eb-132">A [Web App Manifest][MDNWebAppManifest] is a JSON metadata file describing your app, including the name, author, entry page URL, and one or more icons.</span></span>  <span data-ttu-id="af2eb-133">Поскольку она используется в [соответствии со стандартными схемами][W3cWebAppManifest], необходимо предоставить только один манифест веб-приложения для PWA, который устанавливается на любую ПЛАТФОРМУ, ОС и устройство, поддерживающее PWAs.</span><span class="sxs-lookup"><span data-stu-id="af2eb-133">Because it follows a [standards-based schema][W3cWebAppManifest], you must only supply a single web app manifest for the PWA that you are installing on any platform, OS, and device combination that supports PWAs.</span></span>  <span data-ttu-id="af2eb-134">В экосистеме Windows манифест веб-приложения передает веб-индексатору Bing о том, что ваш PWA является кандидатом на автоматическое включение в [Microsoft Store][PwaEdgehtmlMicrosoftStore], где он может достигать почти 700 000 000 активных ежемесячных пользователей как приложение Windows 10.</span><span class="sxs-lookup"><span data-stu-id="af2eb-134">In the Windows ecosystem, your web app manifest signals to the Bing web indexer that your PWA is a candidate for automatic inclusion in the [Microsoft Store][PwaEdgehtmlMicrosoftStore], where it may reach nearly 700 million active monthly users as a Windows 10 app.</span></span>  

<span data-ttu-id="af2eb-135">Если это существующий активный сайт, вы можете создать манифест веб-приложения с помощью [построителя PWA][PwaBuilder].</span><span class="sxs-lookup"><span data-stu-id="af2eb-135">If this were an existing live site, you may generate a web app manifest using [PWA Builder][PwaBuilder].</span></span>  <span data-ttu-id="af2eb-136">Так как он по-прежнему является неопубликованным проектом, скопируйте пример манифеста.</span><span class="sxs-lookup"><span data-stu-id="af2eb-136">Since it is still an unpublished project, copy a sample manifest.</span></span>  

1.  <span data-ttu-id="af2eb-137">В *обозревателе решений*Visual Studio щелкните *общедоступную* папку правой кнопкой мыши и выберите команду **добавить**  >  **новый файл...**, указав в `manifest.json` качестве имени элемента.</span><span class="sxs-lookup"><span data-stu-id="af2eb-137">In the Visual Studio *Solution Explorer*, right-click the *public* folder and select **Add** > **New File...**, specifying `manifest.json` as the item name.</span></span>  
1.  <span data-ttu-id="af2eb-138">`manifest.json`Скопируйте следующий код в файле.</span><span class="sxs-lookup"><span data-stu-id="af2eb-138">In the `manifest.json` file, copy the following code.</span></span>  

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
    
    <span data-ttu-id="af2eb-139">В реальном времени на веб-странице PWA следует настроить *имя*, *start_url*, *short_name*, *Описание*и *значки* \ (значки описаны на следующем шаге).</span><span class="sxs-lookup"><span data-stu-id="af2eb-139">In a real PWA, the next step is to customize *name*, *start_url*, *short_name*, *description*, and *icons* \(icons are covered in the next step\).</span></span>  
    
    <span data-ttu-id="af2eb-140">Чтобы узнать больше о различных значениях элементов и связанных целях, ознакомьтесь со статьей ссылка на [Манифест веб-приложения][MDNWebAppManifest] .</span><span class="sxs-lookup"><span data-stu-id="af2eb-140">To learn more about the different member values and associated purposes, see the [Web App Manifest][MDNWebAppManifest] reference.</span></span>  
    
1.  <span data-ttu-id="af2eb-141">Затем заполните пустой `icons` массив фактическими путями изображений с помощью генератора изображений приложения PWA Builder.</span><span class="sxs-lookup"><span data-stu-id="af2eb-141">Next, fill in the empty `icons` array with actual image paths by using the PWA Builder App Image Generator.</span></span>  
    
    1.  <span data-ttu-id="af2eb-142">С помощью веб-браузера скачайте этот [образец 512x512ного образа PWA][ImagePwa].</span><span class="sxs-lookup"><span data-stu-id="af2eb-142">Using a web browser, download this [sample 512x512 PWA image][ImagePwa].</span></span>  
    1.  <span data-ttu-id="af2eb-143">Перейдите к средству [создания изображений приложения][PwaBuilderAppImageGenerator]PWA Builder и выберите `pwa.png` изображение, которое вы только что сохранили, а затем нажмите кнопку **загрузить** . **Input Image**</span><span class="sxs-lookup"><span data-stu-id="af2eb-143">Go to the PWA Builder [App Image Generator][PwaBuilderAppImageGenerator], and select the `pwa.png` image you just saved as the **Input Image** and then choose the **Download** button.</span></span>  
    1.  <span data-ttu-id="af2eb-144">**Откройте** и **Извлеките** ZIP-файл.</span><span class="sxs-lookup"><span data-stu-id="af2eb-144">**Open** and **Extract** the zip file.</span></span>  
    1.  <span data-ttu-id="af2eb-145">В обозревателе решений Visual Studio щелкните правой кнопкой мыши `public` папку и **откройте папку проводник**.</span><span class="sxs-lookup"><span data-stu-id="af2eb-145">In the Visual Studio Solution Explorer, right-click the `public` folder and **Open Folder in File Explorer**.</span></span>  <span data-ttu-id="af2eb-146">Создайте **новую папку** с именем `images` .</span><span class="sxs-lookup"><span data-stu-id="af2eb-146">Create a **New folder** named `images`.</span></span>  
    1.  <span data-ttu-id="af2eb-147">Скопируйте все папки платформы \ ( `android` , `chrome` , `windows10` и т. д.) из извлеченного Zip- `images` файла в папку и закройте окно проводника.</span><span class="sxs-lookup"><span data-stu-id="af2eb-147">Copy all of the platform folders \(`android`, `chrome`, `windows10`, and so on\) from your extracted zip to the `images` folder and close the file explorer window.</span></span>  <span data-ttu-id="af2eb-148">Добавьте папки в проект Visual Studio \ (в обозревателе решений щелкните правой кнопкой мыши `images` папку и выберите команду **Добавить**  >  **существующую папку...** для каждой папки \).</span><span class="sxs-lookup"><span data-stu-id="af2eb-148">Add the folders to your Visual Studio project \(in Solution Explorer, right-click `images` folder and select **Add** > **Existing folder...** for each of the folders\).</span></span>  
    1.  <span data-ttu-id="af2eb-149">Откройте документ \ (в Visual Studio или любом из редакторов), `icons.json` а затем скопируйте `"icons": [...]` массив в `manifest.json` файл проекта.</span><span class="sxs-lookup"><span data-stu-id="af2eb-149">Open \(with Visual Studio or any editor\) the `icons.json` file from the extracted zip and copy the `"icons": [...]` array into the `manifest.json` file of your project.</span></span>  

1.  <span data-ttu-id="af2eb-150">Теперь вы должны связать свой манифест веб-приложения с вашим приложением.</span><span class="sxs-lookup"><span data-stu-id="af2eb-150">Now you must associate your web app manifest with your app.</span></span>  <span data-ttu-id="af2eb-151">Откройте `layout.pug` файл \ (в `views` папке \) для редактирования и добавьте эту строку сразу после ссылки на таблицу стилей.</span><span class="sxs-lookup"><span data-stu-id="af2eb-151">Open the `layout.pug` file \(in `views` folder\) for editing, and add this line right after the stylesheet link.</span></span>  <span data-ttu-id="af2eb-152">\ (Это просто краткий шаблон узла [pug][PugAttributes] для `<link rel='manifest' href='/manifest.json'>` \).</span><span class="sxs-lookup"><span data-stu-id="af2eb-152">\(It is simply the Node [pug][PugAttributes] template shorthand for `<link rel='manifest' href='/manifest.json'>`\).</span></span>  
    
    ```html
    link(rel='manifest', href='/manifest.json')
    ```  
    
<span data-ttu-id="af2eb-153">Теперь, когда веб-приложение размещается на своем месте, в нем сомещаются манифесты и значки приложений, готовые к начальный экран!</span><span class="sxs-lookup"><span data-stu-id="af2eb-153">With all that in place, your web app is now serving up a manifest and homescreen-ready app icons!</span></span>  <span data-ttu-id="af2eb-154">Попробуйте запустить приложение \ ( `F5` \) и загрузить манифест.</span><span class="sxs-lookup"><span data-stu-id="af2eb-154">Try running your app \(`F5`\) and loading up the manifest.</span></span>  

![Загрузка манифеста веб-приложения из localhost][ImageVsNodejsExpressManifest]  

<span data-ttu-id="af2eb-156">И один из значков.</span><span class="sxs-lookup"><span data-stu-id="af2eb-156">And one of your icons.</span></span>  

![Загрузка логотипа приложения Square71x71Logo с localhost][ImageVsNodejsExpressIcon]  

<span data-ttu-id="af2eb-158">Если опубликовать приложение в режиме реального времени \ (с фактическим данными `start_url` \), средство поиска Bing теперь будет определять его как кандидат на [автоматическую упаковку и отправку в Microsoft Store][PwaEdgehtmlMicrosoftStore] как приложение Windows 10 с возможностью установки.</span><span class="sxs-lookup"><span data-stu-id="af2eb-158">If you publish the app live \(with an actual `start_url`\), the Bing search engine now identifies it as a candidate for [automatic packaging and submission to the Microsoft Store][PwaEdgehtmlMicrosoftStore] as an installable Windows 10 app.</span></span>  <span data-ttu-id="af2eb-159">Убедитесь в том, что файл manifest. JSON включает [сигналы качества для последовательного веб-приложения][WindowsBlogsPwaEdge] , в которых проверяются результаты поиска Bing, включая перечисленные ниже элементы.</span><span class="sxs-lookup"><span data-stu-id="af2eb-159">Ensure that your manifest.json file includes the [Quality signals for Progressive Web Apps][WindowsBlogsPwaEdge] for which Bing scans including the following items.</span></span>   

*   `name`  
*   `description`  
*   <span data-ttu-id="af2eb-160">По крайней мере один значок 512px квадратную или крупную фигуру, чтобы убедиться, что источник изображения подходит для автоматического создания экрана-заставки вашего приложения, описания в магазине, мозаичного изображения и т. д.</span><span class="sxs-lookup"><span data-stu-id="af2eb-160">At least one icon 512px square or larger \(to ensure an image source of sufficient resolution for auto-generating the splash screen of your app, store listing, tile image, and so on\).</span></span>  

<span data-ttu-id="af2eb-161">Кроме того, можно использовать [протокол HTTPS](#https), [рабочие процессы обслуживания](#service-workers)и соблюдать [политики Microsoft Store][LegalWindowsAgrementsMicrosoftStorePolicies].</span><span class="sxs-lookup"><span data-stu-id="af2eb-161">In addition, use [HTTPS](#https), [service workers](#service-workers), and comply with [Microsoft Store Policies][LegalWindowsAgrementsMicrosoftStorePolicies].</span></span>  

### <span data-ttu-id="af2eb-162">HTTPS</span><span class="sxs-lookup"><span data-stu-id="af2eb-162">HTTPS</span></span>  

<span data-ttu-id="af2eb-163">[Сотрудники служб][MDNServiceWorkerApi] и другие ключевые технологии PWA, которые работают с сотрудниками служб (например, [Cache][MDNCache], [Push][MDNPushApi]и API [фоновой синхронизации][MDNSyncManager] ), работают только в безопасных соединениях, то есть [HTTPS][WikiHttps] для активных сайтов или `localhost` для целей отладки.</span><span class="sxs-lookup"><span data-stu-id="af2eb-163">[Service Workers][MDNServiceWorkerApi] and other key PWA technologies that work with service workers \(such as the [Cache][MDNCache], [Push][MDNPushApi], and [Background Sync][MDNSyncManager] APIs\) only work across secure connections, which means [HTTPS][WikiHttps] for live sites or `localhost` for debugging purposes.</span></span>  

<span data-ttu-id="af2eb-164">Если вы [публикуете это веб-приложение в рамках действующего сайта][VisualStudioNodejsTutorialPublishAzureAppService] (например, при настройке [учетной записи Azure Free][AzureCreateFreeAccount]), необходимо убедиться, что сервер настроен для HTTPS.</span><span class="sxs-lookup"><span data-stu-id="af2eb-164">If you [publish this web app as a live site][VisualStudioNodejsTutorialPublishAzureAppService] \(for example, by setting up an [Azure free account][AzureCreateFreeAccount]\), you must ensure your server is configured for HTTPS.</span></span>  <span data-ttu-id="af2eb-165">Если вы используете [службу приложений Microsoft Azure][AzureWebApps] для размещения сайта, она по умолчанию обрабатывается по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="af2eb-165">If you use the [Microsoft Azure App Service][AzureWebApps] to host your site, it is served over HTTPS by default.</span></span>  

<span data-ttu-id="af2eb-166">Для этого руководства продолжайте использовать `http://localhost` в качестве заполнителя для активного сайта, обслуживаемого активным `https://` .</span><span class="sxs-lookup"><span data-stu-id="af2eb-166">For this guide, continue using `http://localhost` as a placeholder for a live site served over `https://`.</span></span>  

### <span data-ttu-id="af2eb-167">Обслуживание сотрудников</span><span class="sxs-lookup"><span data-stu-id="af2eb-167">Service Workers</span></span>  

<span data-ttu-id="af2eb-168">Специалистами службы является ключевая технология, PWAs.</span><span class="sxs-lookup"><span data-stu-id="af2eb-168">Service Workers is the key technology behind PWAs.</span></span> <span data-ttu-id="af2eb-169">Служебные работники выполняют роль прокси между PWA и сетью, чтобы обеспечить работу вашего веб-сайта в качестве установленного собственного приложения, обслуживающего сценарии в автономном режиме, реагируя на принудительные уведомления сервера и запускающего фоновые задачи.</span><span class="sxs-lookup"><span data-stu-id="af2eb-169">Service Workers act as a proxy between your PWA and the network to enable your website to function as an installed native app that serves up offline scenarios, responds to server push notifications, and runs background tasks.</span></span>  <span data-ttu-id="af2eb-170">Работники служб также открывают новые стратегии обеспечения производительности.</span><span class="sxs-lookup"><span data-stu-id="af2eb-170">Service workers also open up new performance strategies.</span></span>  <span data-ttu-id="af2eb-171">Вы не обязаны реализовывать все веб-приложения, чтобы использовать кэш рабочих процессов службы для точной настройки производительности загрузки страниц для вашего веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="af2eb-171">You are not required to implement a full web app to use the service worker cache for fine-tuned page load performance for your website.</span></span>  

<span data-ttu-id="af2eb-172">Служебные работники — это управляемые событиями фоновые потоки, которые выполняются из файлов JavaScript вместе с обычными сценариями, которые используются для включения в веб-приложение.</span><span class="sxs-lookup"><span data-stu-id="af2eb-172">Service workers are event-driven background threads that run from JavaScript files served up alongside the regular scripts that power your web app.</span></span>  <span data-ttu-id="af2eb-173">Поскольку работники служб не работают в основном потоке пользовательского интерфейса, у сотрудников служб нет доступа DOM, хотя [поток пользовательского интерфейса][MDNWorkerPrototypePostMessage] и [Рабочий поток][MDNDedicatedWorkerGlobalScopePostMessage] может взаимодействовать с помощью `postMessage()` `onmessage` обработчиков событий.</span><span class="sxs-lookup"><span data-stu-id="af2eb-173">Because Service workers do not run on the main UI thread, service workers do not have DOM access, though the [UI thread][MDNWorkerPrototypePostMessage] and a [worker thread][MDNDedicatedWorkerGlobalScopePostMessage] is able to communicate using `postMessage()` and `onmessage` event handlers.</span></span>  

<span data-ttu-id="af2eb-174">Вы связываете сотрудника службы с вашим приложением, регистрируя его в источнике URL-адреса сайта (или в указанном месте).</span><span class="sxs-lookup"><span data-stu-id="af2eb-174">You associate a service worker with your app by registering it to the URL origin of your site \(or a specified path within it\).</span></span>  <span data-ttu-id="af2eb-175">После регистрации файл рабочего процесса службы загружается, устанавливается и активируется на компьютере пользователя.</span><span class="sxs-lookup"><span data-stu-id="af2eb-175">Once registered, the service worker file is then downloaded, installed, and activated on the user machine.</span></span>  <span data-ttu-id="af2eb-176">Более того, MDN веб-документы имеет исчерпывающее руководство по [работе с сотрудниками служб][MDNUsingServiceWorkers] и подробным справочником по [API рабочего процесса службы][MDNServiceWorkerApi] .</span><span class="sxs-lookup"><span data-stu-id="af2eb-176">For more, MDN web docs has a comprehensive guide on [Using Service Workers][MDNUsingServiceWorkers] and a detailed [Service Worker API][MDNServiceWorkerApi] reference.</span></span>  

<span data-ttu-id="af2eb-177">В этом учебнике используйте сценарий рабочего процесса службы автономной обработки страниц в [конструкторе PWA][PwaBuilderServiceWorker].</span><span class="sxs-lookup"><span data-stu-id="af2eb-177">For this tutorial, use the Offline page service worker script on [PWA Builder][PwaBuilderServiceWorker].</span></span>  <span data-ttu-id="af2eb-178">Начните с настройки сценария с большим набором функциональных возможностей в соответствии с требованиями к производительности, пропускной способностью сети и т. д.</span><span class="sxs-lookup"><span data-stu-id="af2eb-178">Start by customizing the script with more functionality according to your performance requirements, network bandwidth, and so on.</span></span>  <span data-ttu-id="af2eb-179">Изучите [Cookbook рабочего процесса][ServiceWorkerCookbook] , предоставленный Mozilla, для ряда полезных идей по кэшированию рабочих процессов служб.</span><span class="sxs-lookup"><span data-stu-id="af2eb-179">Review the [Service Worker Cookbook][ServiceWorkerCookbook]  provided by Mozilla for a number of useful service worker caching ideas.</span></span>  

1.  <span data-ttu-id="af2eb-180">Откройте [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] и выберите рабочий процесс **автономной работы со страницей** \ (по умолчанию \) и нажмите кнопку " **загрузить сотрудник службы** ".</span><span class="sxs-lookup"><span data-stu-id="af2eb-180">Open [https://www.pwabuilder.com/serviceworker][PwaBuilderServiceWorker] and select the \(default\) **Offline page** service worker and click the **Download service worker** button.</span></span>  
1.  <span data-ttu-id="af2eb-181">Откройте папку download и скопируйте следующие два файла</span><span class="sxs-lookup"><span data-stu-id="af2eb-181">Open the download folder and copy the following two files</span></span>  

    *   <span data-ttu-id="af2eb-182">ServiceWorker1\pwabuilder-sw-register.js</span><span class="sxs-lookup"><span data-stu-id="af2eb-182">ServiceWorker1\pwabuilder-sw-register.js</span></span>  
    *   <span data-ttu-id="af2eb-183">ServiceWorker1\pwabuilder-sw.js</span><span class="sxs-lookup"><span data-stu-id="af2eb-183">ServiceWorker1\pwabuilder-sw.js</span></span>  
    
    <span data-ttu-id="af2eb-184">Сохраните файлы в `public` папке проекта Visual Studio Web App.</span><span class="sxs-lookup"><span data-stu-id="af2eb-184">Save the files to the `public` folder of your Visual Studio web app project.</span></span>  <span data-ttu-id="af2eb-185">\ (В Visual Studio `Ctrl` + `O` откройте проводник для проекта и перейдите в `public` папку \).</span><span class="sxs-lookup"><span data-stu-id="af2eb-185">\(From Visual Studio, use `Ctrl`+`O` to open file explorer to your project and navigate to the `public` folder\).</span></span>  
    
    <span data-ttu-id="af2eb-186">Рекомендуется проанализировать этот код в обоих файлах, чтобы получить сведения о том, как зарегистрировать сотрудника службы, который кэширует указанную страницу \ ( `offline.html` \) и выполняет ее в случае сбоя при выборке из сети.</span><span class="sxs-lookup"><span data-stu-id="af2eb-186">It is worth reviewing the code in both of these files, to get the gist of how to register a service worker that caches a designated page \(`offline.html`\) and serves it when a network fetch fails.</span></span>  <span data-ttu-id="af2eb-187">Затем создайте простую `offline.html` страницу в качестве заполнителя для автономной работы приложения.</span><span class="sxs-lookup"><span data-stu-id="af2eb-187">Next, create a simple `offline.html` page as a placeholder for the offline functionality of your app.</span></span>  
    
1.  <span data-ttu-id="af2eb-188">В обозревателе решений откройте `views/layout.pug` файл и добавьте следующую строку под тегами ссылки.</span><span class="sxs-lookup"><span data-stu-id="af2eb-188">In Solution Explorer, open the `views/layout.pug` file, and add the following line below your link tags.</span></span>  
    
    ```html
    script(src='/pwabuilder-sw-register.js')
    ```  
    
    <span data-ttu-id="af2eb-189">Ваш сайт загрузит и запустит сценарий регистрации рабочего процесса службы.</span><span class="sxs-lookup"><span data-stu-id="af2eb-189">Your site loads and runs your service worker registration script.</span></span>  
    
1.  <span data-ttu-id="af2eb-190">В обозревателе решений щелкните папку правой кнопкой мыши `public` и выберите команду **Добавить**  >  **новый файл..**..  Присвойте ему имя `offline.html` , а затем добавьте `<title>` и часть основного содержимого, например приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="af2eb-190">In Solution Explorer, right-click on the `public` folder and select **Add** > **New File...**.  Name it `offline.html`, and add a `<title>` and some body content, for example the following code.</span></span>  
    
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
    
    <span data-ttu-id="af2eb-191">На этом этапе у вашей `public` папки должны быть три новых файла.</span><span class="sxs-lookup"><span data-stu-id="af2eb-191">At this point, your `public` folder should have three new files.</span></span>  
    
    ![Файлы, добавленные в общую папку решения][ImageVsNodejsExpressPublic]  
    
1.  <span data-ttu-id="af2eb-193">В обозревателе решений откройте `routes\index.js` файл и добавьте следующий код непосредственно перед последней командой \ ( `module.exports = router;` \).</span><span class="sxs-lookup"><span data-stu-id="af2eb-193">In Solution Explorer, open the `routes\index.js` file, and add the following code just before the final command \(`module.exports = router;`\).</span></span>  
    
    ```javascript
    router.get('/offline.html', function (req, res) {
        res.sendFile('public/offline.html');
    });
    ```  
    
    <span data-ttu-id="af2eb-194">Это указывает приложению на необходимость обслуживания `offline.html` файла \ (когда ваш сотрудник службы извлекает ее для автономного кэша).</span><span class="sxs-lookup"><span data-stu-id="af2eb-194">This instructs your app to serve the `offline.html` file \(when your service worker fetches it for the offline cache\).</span></span>  
    
1.  <span data-ttu-id="af2eb-195">Протестируйте веб-приложение PWA!</span><span class="sxs-lookup"><span data-stu-id="af2eb-195">Test out your PWA!</span></span>  <span data-ttu-id="af2eb-196">`Ctrl` + `Shift` + `B` `F5` Чтобы запустить Microsoft EDGE и открыть страницу, выполните сборку \ (\) и запустите "["] веб-приложение `localhost` .</span><span class="sxs-lookup"><span data-stu-id="af2eb-196">Build \(`Ctrl`+`Shift`+`B`\) and Run \(`F5`\) your web app to launch Microsoft Edge and open your `localhost` page.</span></span>  <span data-ttu-id="af2eb-197">Затем выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="af2eb-197">Then complete the following steps.</span></span>  
    
    1.  <span data-ttu-id="af2eb-198">Откройте вкладку **Edge DevTools (** `Ctrl` + `Shift` + `J` \) и убедитесь, что сотрудник службы зарегистрирован.</span><span class="sxs-lookup"><span data-stu-id="af2eb-198">Open the Edge DevTools **Console** \(`Ctrl`+`Shift`+`J`\) and verify the Service worker was registered.</span></span>  
    1.  <span data-ttu-id="af2eb-199">На панели **отладчик** разверните элемент Управление **сотрудниками службы** и щелкните на своем источнике.</span><span class="sxs-lookup"><span data-stu-id="af2eb-199">In the **Debugger** panel, expand the **Service Workers** control and click on your origin.</span></span>  <span data-ttu-id="af2eb-200">В **обзоре сотрудника службы**убедитесь, что сотрудник службы активирован и запущен.</span><span class="sxs-lookup"><span data-stu-id="af2eb-200">In the **Service Worker Overview**, verify your service worker is activated and running.</span></span>  
        
        ![Общие сведения о сотруднике службы Edge DevTools][ImageDevtoolsSwOverview]  
        
    1.  <span data-ttu-id="af2eb-202">Разверните элемент управления **кэшем** и убедитесь, что `offline.html` страница кэширована.</span><span class="sxs-lookup"><span data-stu-id="af2eb-202">Expand the **Cache** control and verify that the `offline.html` page is cached.</span></span>  
        
        ![Кэш рабочего процесса службы Edge DevTools][ImageDevtoolsSwCache]  
        
1.  <span data-ttu-id="af2eb-204">Время, когда вы можете попробовать приложение PWA в автономном режиме!</span><span class="sxs-lookup"><span data-stu-id="af2eb-204">Time to try your PWA as an offline app!</span></span>  <span data-ttu-id="af2eb-205">В Visual Studio **отключите отладку** ( `Shift` + `F5` \) веб-приложение, а затем откройте Microsoft Edge \ (или обновите \) на адрес localhost вашего веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="af2eb-205">In Visual Studio, **Stop Debugging** \(`Shift`+`F5`\) your web app, then open Microsoft Edge \(or refresh\) to the localhost address of your website.</span></span>  <span data-ttu-id="af2eb-206">Теперь оно должно загрузить `offline.html` страницу \ (благодаря своему сотруднику службы и автономному кэшу)!</span><span class="sxs-lookup"><span data-stu-id="af2eb-206">It should now load the `offline.html` page \(thanks to your service worker and offline cache\)!</span></span>  
    
    ![offline. HTML из http://localhost:1337 загруженного в Microsoft Edge][ImageOfflineHtml]  

## <span data-ttu-id="af2eb-208">Добавление push-уведомлений</span><span class="sxs-lookup"><span data-stu-id="af2eb-208">Add push notifications</span></span>  

<span data-ttu-id="af2eb-209">Сделайте этот веб-сайт более похожим, добавив поддержку на стороне клиента для отправки push- [уведомлений в службу][MDNPushApi] сообщений и [API уведомлений][MDNNotificationsApi] для отображения всплывающего сообщения при получении сообщения.</span><span class="sxs-lookup"><span data-stu-id="af2eb-209">Make your PWA more app-like by adding client-side support for push notifications using the [Push API][MDNPushApi] to subscribe to a messaging service and the [Notifications API][MDNNotificationsApi] to display a toast message upon receiving a message.</span></span>  <span data-ttu-id="af2eb-210">Как и в случае с сотрудниками служб, они являются стандартными API, которые работают в разных браузерах, поэтому вам нужно написать код только для того, чтобы он работал везде, где бы они ни наPWAsись.</span><span class="sxs-lookup"><span data-stu-id="af2eb-210">As with Service Workers, these are standards-based APIs that work cross-browser, so you only have to write the code once for it to work everywhere PWAs are supported.</span></span>  <span data-ttu-id="af2eb-211">На стороне сервера используйте [веб-извещающую][NPMWebPush] библиотеку с открытым исходным кодом для обработки различий, связанных с предоставлением Push-сообщений для различных браузеров.</span><span class="sxs-lookup"><span data-stu-id="af2eb-211">On the server side, use the [Web-Push][NPMWebPush] open-source library to handle the differences involved in delivering push messages to various browsers.</span></span>  

<span data-ttu-id="af2eb-212">Ниже приведено множество полезных демонстрационных роликов, посвященных [специалистам службы Cookbook][ServiceWorkerCookbookPushRichDemo] , предоставляемым Mozilla, что стоит делать, чтобы получить доступ к другим полезным рецептам веб-внедрения и обслуживания.</span><span class="sxs-lookup"><span data-stu-id="af2eb-212">The following is adapted from the Push Rich Demo in [Service Worker Cookbook][ServiceWorkerCookbookPushRichDemo] provided by Mozilla, which is worth checking out for a number of other useful Web Push and service worker recipes.</span></span>  

### <span data-ttu-id="af2eb-213">Шаг 1: Установка веб-библиотеки NPM</span><span class="sxs-lookup"><span data-stu-id="af2eb-213">Step 1 - Install the NPM web-push library</span></span>  

<span data-ttu-id="af2eb-214">В обозревателе решений Visual Studio щелкните проект правой кнопкой мыши и **откройте интерактивное окно Node. js..**..  Введите следующий код.</span><span class="sxs-lookup"><span data-stu-id="af2eb-214">In Visual Studio Solution Explorer, right-click your project and **Open Node.js Interactive Window...**.  In it, type the following code.</span></span>  

```javascript
.npm install web-push
```  

<span data-ttu-id="af2eb-215">Будет установлено [веб-принудительная][NPMWebPush] библиотека.</span><span class="sxs-lookup"><span data-stu-id="af2eb-215">This installs the [Web-Push][NPMWebPush] library.</span></span>  <span data-ttu-id="af2eb-216">Затем откройте `index.js` файл и добавьте следующую строку в начало файла после других операторов требования.</span><span class="sxs-lookup"><span data-stu-id="af2eb-216">Then, open up your `index.js` file, and add the following line to the top of your file after the other requirement statements.</span></span>  

```javascript
var webpush = require('web-push');
```  

### <span data-ttu-id="af2eb-217">Шаг 2. Создание VAPIDных ключей для сервера</span><span class="sxs-lookup"><span data-stu-id="af2eb-217">Step 2 - Generate VAPID keys for your server</span></span>  

<span data-ttu-id="af2eb-218">Затем для отправки push-сообщений в клиент PWA необходимо создать для сервера ключи VAPID \ (код добровольного сервера приложений).</span><span class="sxs-lookup"><span data-stu-id="af2eb-218">Next you must generate VAPID \(Voluntary Application Server Identification\) keys for your server to send push messages to the PWA client.</span></span>  <span data-ttu-id="af2eb-219">Это нужно сделать только один раз \ (то есть для вашего сервера требуется только одна пара ключей VAPID).</span><span class="sxs-lookup"><span data-stu-id="af2eb-219">You only have to do this once \(that is, your server only requires a single pair of VAPID keys\).</span></span>  <span data-ttu-id="af2eb-220">В интерактивном окне Node. js введите следующий код.</span><span class="sxs-lookup"><span data-stu-id="af2eb-220">In the Node.js Interactive Window, type the following code.</span></span>  

```javascript
var webpush = require('web-push');
webpush.generateVAPIDKeys();
```  

<span data-ttu-id="af2eb-221">Результат должен привести к тому, что объект JSON содержит открытый и закрытый ключи, которые вы копируете в логику сервера.</span><span class="sxs-lookup"><span data-stu-id="af2eb-221">The output should result in a JSON object containing a public and private key, which you copy into your server logic.</span></span>  

<span data-ttu-id="af2eb-222">В `index.js` файле перед последней `module.exports = router` строкой \ (\) добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="af2eb-222">In your `index.js` file, just before the final  \(`module.exports = router`\) line, add the following code.</span></span>  

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

<span data-ttu-id="af2eb-223">Скопируйте `publicKey` `privateKey` только что созданные значения.</span><span class="sxs-lookup"><span data-stu-id="af2eb-223">Copy the `publicKey` and `privateKey` values that you just generated.</span></span>  <span data-ttu-id="af2eb-224">Вы можете настроить адрес так же, `mailto` как если бы он ни запускался для выполнения этого примера \.</span><span class="sxs-lookup"><span data-stu-id="af2eb-224">Feel free to customize the `mailto` address as well \(though it is not required in order to run this sample\).</span></span>  

<span data-ttu-id="af2eb-225">В [блоге по проектированию служб Mozilla][MozillaServicesSendingVapidWebPushNotificationsPush] вы узнаете о том, как VAPID и веб-извещающую, если вы заинтересованы в том, как это работает за сценой.</span><span class="sxs-lookup"><span data-stu-id="af2eb-225">The [Mozilla Services engineering blog][MozillaServicesSendingVapidWebPushNotificationsPush] has a nice explainer on VAPID and WebPush if you are interested in the details of how it works behind the scenes.</span></span>  

### <span data-ttu-id="af2eb-226">Шаг 3: обработка запросов сервера, связанных с принудительной отправкой</span><span class="sxs-lookup"><span data-stu-id="af2eb-226">Step 3 - Handle push-related server requests</span></span>  

<span data-ttu-id="af2eb-227">Теперь настройте маршруты для обработки запросов push-уведомлений от клиента PWA, в том числе для предоставления открытого ключа VAPID и регистрации клиента для приема pushs.</span><span class="sxs-lookup"><span data-stu-id="af2eb-227">Now set up routes for handling push-related requests from the PWA client, including serving up the VAPID public key and registering the client to receive pushes.</span></span>  

<span data-ttu-id="af2eb-228">В реальной ситуации push-уведомление, как правило, является событием в логике сервера.</span><span class="sxs-lookup"><span data-stu-id="af2eb-228">In a real scenario, a push notification likely originates from an event in your server logic.</span></span>  <span data-ttu-id="af2eb-229">Чтобы упростить это, необходимо добавить кнопку Push- **уведомлений** на нашу ДОМАШНЮЮ страницу PWA, чтобы создать push-уведомления с нашего сервера, и `/sendNotification` конечную точку \ (серверный маршрут \) для обработки запросов.</span><span class="sxs-lookup"><span data-stu-id="af2eb-229">To simplify things here, you must add a **Push Notification** button to our PWA homepage for generating pushes from our server, and a `/sendNotification` endpoint \(server route\)for handling those requests.</span></span>  

<span data-ttu-id="af2eb-230">В `index.js` файле добавьте следующие маршруты сразу после кода инициализации VAPID, добавленного в [Step 2] [#step-2---Generate-VAPID-Keys-для вашего сервера].</span><span class="sxs-lookup"><span data-stu-id="af2eb-230">In your `index.js` file, append the following routes just after the VAPID initialization code you added in [Step 2][#step-2---generate-vapid-keys-for-your-server].</span></span>  

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

<span data-ttu-id="af2eb-231">С помощью серверного кода на месте в push-уведомлениях на клиенте PWA.</span><span class="sxs-lookup"><span data-stu-id="af2eb-231">With the server-side code in place, plumb in push notifications on the PWA client.</span></span>  

### <span data-ttu-id="af2eb-232">Шаг 4: Подписка на push-уведомления</span><span class="sxs-lookup"><span data-stu-id="af2eb-232">Step 4 - Subscribe to push notifications</span></span>  

<span data-ttu-id="af2eb-233">Как часть роли прокси-сервера PWA, сотрудники служб обрабатывают события push-уведомлений и взаимодействие с всплывающими уведомлениями.</span><span class="sxs-lookup"><span data-stu-id="af2eb-233">As part of their role as PWA network proxies, service workers handle push events and toast notification interactions.</span></span>  <span data-ttu-id="af2eb-234">Тем не менее, так как при первой настройке (или регистрации) сотрудник службы подписаться на push-уведомления PWA в главном потоке пользовательского интерфейса PWA и требуется сетевое подключение.</span><span class="sxs-lookup"><span data-stu-id="af2eb-234">However, as it is with first setting up \(or registering\) a service worker, subscribing the PWA to server push notifications happens on the main UI thread of the PWA and requires network connectivity.</span></span>  <span data-ttu-id="af2eb-235">Для подписки на push-уведомления требуется активная регистрация рабочего процесса службы, поэтому сначала необходимо убедиться, что ваш сотрудник службы установлен и активен, прежде чем пытаться подписаться на push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="af2eb-235">Subscribing to push notifications requires an active service worker registration, so you must first verify that your service worker is installed and active before trying to subscribe it to push notifications.</span></span>  

<span data-ttu-id="af2eb-236">Перед созданием новой принудительной подписки Microsoft Edge проверяет, предоставил ли пользователь разрешение на получение уведомлений в PWA.</span><span class="sxs-lookup"><span data-stu-id="af2eb-236">Before a new push subscription is created, Microsoft Edge check if the user granted the PWA permission to receive notifications.</span></span>  <span data-ttu-id="af2eb-237">В противном случае пользователю будет предложено разрешить браузеру.</span><span class="sxs-lookup"><span data-stu-id="af2eb-237">If not, the user is prompted by the browser for permission.</span></span>  <span data-ttu-id="af2eb-238">Если разрешение на доступ отклонено, запрос `registration.pushManager.subscribe` вызывает исключение a `DOMException` , поэтому необходимо обработать его.</span><span class="sxs-lookup"><span data-stu-id="af2eb-238">If the permission is denied, the request to `registration.pushManager.subscribe` throws a `DOMException`, so you must handle it.</span></span>  <span data-ttu-id="af2eb-239">Дополнительные сведения об управлении разрешениями можно найти [в разделе push-уведомления в Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span><span class="sxs-lookup"><span data-stu-id="af2eb-239">For more on permission management, see [Push Notifications in Microsoft Edge][WindowsBlogsWebNotificationsEdge].</span></span>  

<span data-ttu-id="af2eb-240">В `pwabuilder-sw-register.js` файле добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="af2eb-240">In your `pwabuilder-sw-register.js` file, append the following code.</span></span>  

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

<span data-ttu-id="af2eb-241">Ознакомьтесь с документацией по MDN на интерфейсе [PushManager][MDNPushManager] и NPM документами в [Интернет-библиотеке Push][NPMWebPushUsage] -данных для получения дополнительных сведений о работе API и различных связанных параметрах.</span><span class="sxs-lookup"><span data-stu-id="af2eb-241">Review the MDN documentation on the [PushManager][MDNPushManager] interface and NPM docs on the [Web-Push][NPMWebPushUsage] library for more details on how the APIs work and various related options.</span></span>  

### <span data-ttu-id="af2eb-242">Шаг 5: Настройка обработчиков событий push-уведомлений и notificationclick</span><span class="sxs-lookup"><span data-stu-id="af2eb-242">Step 5 - Set up push and notificationclick event handlers</span></span>  

<span data-ttu-id="af2eb-243">При настройке принудительной подписки оставшаяся часть работы в сервисном работнике выполняется.</span><span class="sxs-lookup"><span data-stu-id="af2eb-243">With our push subscription set up, the remainder of the work happens in the service worker.</span></span>  <span data-ttu-id="af2eb-244">Сначала необходимо настроить обработчик для извещающих событий, отправленных сервером, и ответить с помощью всплывающего уведомления \ (если предоставлено разрешение), отображая полезные данные push-данных.</span><span class="sxs-lookup"><span data-stu-id="af2eb-244">First you must set up a handler for server-sent push events, and respond with a toast notification \(if permission was granted\) displaying the push data payload.</span></span>  <span data-ttu-id="af2eb-245">Затем вы добавите обработчик Click для всплывающего уведомления, чтобы отклонить уведомление и отсортировать список открытых в данный момент окон, которые нужно открыть, сосредоточиться или открыть, а также сосредоточиться на странице клиента Project Web App.</span><span class="sxs-lookup"><span data-stu-id="af2eb-245">Next you add a click handler for the toast to dismiss the notification and sort through a list of currently open windows to open, focus, or open and focus the intended PWA client page.</span></span>  

<span data-ttu-id="af2eb-246">В `pwabuilder-sw.js` файле добавьте следующие обработчики.</span><span class="sxs-lookup"><span data-stu-id="af2eb-246">In your `pwabuilder-sw.js` file, append the following handlers.</span></span>  

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

### <span data-ttu-id="af2eb-247">Шаг 6: попробовать</span><span class="sxs-lookup"><span data-stu-id="af2eb-247">Step 6 - Try it out</span></span>  

<span data-ttu-id="af2eb-248">Время на тестирование push-уведомлений в PWA!</span><span class="sxs-lookup"><span data-stu-id="af2eb-248">Time to test push notifications in your PWA!</span></span>  

1.  <span data-ttu-id="af2eb-249">Запустите `F5` в браузере веб-приложение Project Web App.</span><span class="sxs-lookup"><span data-stu-id="af2eb-249">Run \(`F5`\) your PWA in the browser.</span></span>  <span data-ttu-id="af2eb-250">Так как вы изменили код сервисного рабочего процесса \ ( `pwabuilder-sw.js` \), необходимо открыть отладчик DevTools \ ( `F12` \) на панели **обзора рабочих процессов** и **отменить регистрацию** рабочего процесса и повторно загрузить \ ( `F5` \) страницы, чтобы заново ее зарегистрировать (или нажать кнопку **Обновить**).</span><span class="sxs-lookup"><span data-stu-id="af2eb-250">Because you modified the service worker code \(`pwabuilder-sw.js`\), you must open the DevTools Debugger \(`F12`\) to the **Service Worker Overview** panel and **Unregister** the service worker and reload \(`F5`\) the page to re-register it \(or you click **Update**\).</span></span>  <span data-ttu-id="af2eb-251">В рабочем сценарии браузер проверяет регулярную проверку наличия обновлений для рабочего процесса обслуживания и устанавливает обновления в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="af2eb-251">In a production scenario, the browser checks regularly check for service worker updates and install the updates in the background.</span></span>  <span data-ttu-id="af2eb-252">Для немедленного поиска необходимо принудительно выполнить эту программу.</span><span class="sxs-lookup"><span data-stu-id="af2eb-252">You should force it here for immediate results.</span></span>  
    
    <span data-ttu-id="af2eb-253">Когда сотрудник службы активируется и пытается оформить подписку на PWA для отправки уведомлений, вы увидите диалоговое окно с разрешениями в нижней части страницы.</span><span class="sxs-lookup"><span data-stu-id="af2eb-253">As your service worker activates and attempts to subscribe your PWA to push notifications, you should see a permission dialog at the bottom of the page.</span></span>  
    
    ![Диалоговое окно разрешений для включения уведомлений][ImageNotificationPermission]  
    
    <span data-ttu-id="af2eb-255">Нажмите кнопку **Да** , чтобы включить всплывающие уведомления для PWA.</span><span class="sxs-lookup"><span data-stu-id="af2eb-255">Choose **Yes** to enable toast notifications for your PWA.</span></span>  
    
1.  <span data-ttu-id="af2eb-256">На панели Общие сведения о рабочем процессе попробуйте нажать кнопку " **Отправить** ".</span><span class="sxs-lookup"><span data-stu-id="af2eb-256">From the Service Worker Overview pane, try choosing the  **Push** button.</span></span>  <span data-ttu-id="af2eb-257">На экран будет отображено всплывающее уведомление с "\" с жестко заданным тестовым Push-сообщением из DevTools "\".</span><span class="sxs-lookup"><span data-stu-id="af2eb-257">A toast notification with the \(hard-coded "Test push message from DevTools"\) payload should appear.</span></span>  
    
    ![Отправка уведомления из DevTools][ImageDevtoolsPush]  
    
1.  <span data-ttu-id="af2eb-259">Затем попробуйте нажать кнопку **Отправить уведомление** на домашней странице PWA.</span><span class="sxs-lookup"><span data-stu-id="af2eb-259">Next try choosing the **Send Notification** button on the homepage of your PWA.</span></span>  <span data-ttu-id="af2eb-260">На этот раз появится всплывающее уведомление с полезной нагрузкой на сервере.</span><span class="sxs-lookup"><span data-stu-id="af2eb-260">This time a toast with the payload from your server appears.</span></span>  
    
    ![Отправка уведомления с сервера PWA][ImagePwaPush]  
    
    <span data-ttu-id="af2eb-262">Если вы не нажимайте кнопку \ (или активируете) всплывающее уведомление, оно будет закрыто через несколько секунд и помещается в очередь в центре уведомлений Windows.</span><span class="sxs-lookup"><span data-stu-id="af2eb-262">If you do not click \(or activate\) a toast notification, it is dismissed after several seconds and queue up in your Windows Action Center.</span></span>  
    
    ![Уведомления в центре уведомлений Windows][ImageWindowsActionCenter]  
    
    <span data-ttu-id="af2eb-264">У вас есть основы push-уведомлений PWA.</span><span class="sxs-lookup"><span data-stu-id="af2eb-264">You have the basics of PWA push notifications.</span></span>  <span data-ttu-id="af2eb-265">В реальном приложении описанные ниже действия реализованы таким образом, чтобы управлять принудительными подписками и хранить их, а также для правильного [шифрования][NPMWebPushEncrypt] данных, передаваемых по сети.</span><span class="sxs-lookup"><span data-stu-id="af2eb-265">In a real app, the next steps are implemented in a way to manage and store push subscriptions and to properly [encrypt][NPMWebPushEncrypt] payload data being sent across the wire.</span></span>  
    
## <span data-ttu-id="af2eb-266">Дальнейшая работа</span><span class="sxs-lookup"><span data-stu-id="af2eb-266">Going further</span></span>  

<span data-ttu-id="af2eb-267">В этом руководстве показано, как создать прогрессивное веб-приложение и средства разработки для Microsoft PWA, в том числе Visual Studio, конструктор PWA и DevTools Edge.</span><span class="sxs-lookup"><span data-stu-id="af2eb-267">This guide demonstrated the basic anatomy of a Progressive Web App and Microsoft PWA development tools including Visual Studio, PWA Builder, and Edge DevTools.</span></span>  

<span data-ttu-id="af2eb-268">Разумеется, вы можете сделать так, чтобы выпустить веб-приложение [Project Web][PwaEdgehtmlIndexRequirements] App, помимо того, что вы прочитали здесь, в том числе разработку, глубокое связывание и [тестирование в разных браузерах][BrowserStackTestEdgeBrowser] , а также другие [Советы и рекомендации][Webhint] , но мы надеемся, что в этом руководстве предоставлено вам полное представление о концепциях PWA и идеи для начала работы.</span><span class="sxs-lookup"><span data-stu-id="af2eb-268">Of course, there is a lot more that goes into [making a great PWA][PwaEdgehtmlIndexRequirements] beyond what you read here, including responsive design, deep-linking, [cross-browser testing][BrowserStackTestEdgeBrowser] and other [best practices][Webhint] \(not to mention your app functionality!\), but hopefully this guide gave you a solid introduction of PWA basics and some ideas on getting started.</span></span>  <span data-ttu-id="af2eb-269">Если у вас возникли вопросы по разработке PWA в Windows или Visual Studio, оставьте комментарий.</span><span class="sxs-lookup"><span data-stu-id="af2eb-269">If you have further questions on PWA development with Windows or with Visual Studio, please leave a comment!</span></span>  

<span data-ttu-id="af2eb-270">Ознакомьтесь с другими руководствами по Project Web App, чтобы узнать о том, как повысить эффективность работы с клиентами и обеспечить более простое и интегрированное приложение для операционной системы.</span><span class="sxs-lookup"><span data-stu-id="af2eb-270">Review the other PWA guides to learn how to increase customer engagement and provide a more seamless, OS-integrated app experience.</span></span>  

*   <span data-ttu-id="af2eb-271">[Адаптация Windows][PwaEdgehtmlWindowsFeatures].</span><span class="sxs-lookup"><span data-stu-id="af2eb-271">[Windows tailoring][PwaEdgehtmlWindowsFeatures].</span></span> <span data-ttu-id="af2eb-272">Благодаря функциям простого обнаружения функций вы можете последовательно усовершенствовать пользователей PWA для Windows 10 с помощью встроенных API среды выполнения Windows (WinRT), например для настройки уведомлений на плитке меню " **Пуск** " Windows и Jumplists, а также \ (при разрешении) для работы с пользовательскими ресурсами, такими как фотографии, музыка и календарь.</span><span class="sxs-lookup"><span data-stu-id="af2eb-272">Using simple feature detection, you may progressively enhance your PWA for Windows 10 customers through native Windows Runtime \(WinRT\) APIs, such as those for customizing Windows **Start** menu tile notifications and taskbar jumplists, and \(upon permission\) working with user resources, such as photos, music, and calendar.</span></span>  
*   <span data-ttu-id="af2eb-273">[PWAs в Microsoft Store][PwaEdgehtmlMicrosoftStore].</span><span class="sxs-lookup"><span data-stu-id="af2eb-273">[PWAs in the Microsoft Store][PwaEdgehtmlMicrosoftStore].</span></span>  <span data-ttu-id="af2eb-274">Узнайте больше о преимуществах распространения магазина приложений и о том, как отправить PWA.</span><span class="sxs-lookup"><span data-stu-id="af2eb-274">Learn more about the benefits of app store distribution and how to submit your PWA.</span></span>  

## <span data-ttu-id="af2eb-275">См. также</span><span class="sxs-lookup"><span data-stu-id="af2eb-275">See also</span></span>  

*   <span data-ttu-id="af2eb-276">[Прогрессивные веб-приложения в MDN веб-документах][MDNProgressiveWebApps] — отличное руководство по прогрессивным веб-приложениям.</span><span class="sxs-lookup"><span data-stu-id="af2eb-276">[Progressive Web Apps on MDN web docs][MDNProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="af2eb-277">[Прогрессивные веб-приложения на веб-сайте Web. dev][WebDevProgressiveWebApps] -превосходное руководство по прогрессивным веб-приложениям.</span><span class="sxs-lookup"><span data-stu-id="af2eb-277">[Progressive Web Apps on web.dev][WebDevProgressiveWebApps] - Excellent guide on Progressive Web Apps.</span></span>  
*   <span data-ttu-id="af2eb-278">[Прогрессивные веб-приложения Rocks][ProgressiveWebApps] — наглядные примеры PWAs.</span><span class="sxs-lookup"><span data-stu-id="af2eb-278">[Progressive Web Apps rocks][ProgressiveWebApps] - Showcases real-world examples of PWAs.</span></span>  
*   <span data-ttu-id="af2eb-279">[Средства чтения новостей, такие как прогрессивные веб-приложения,][HackerNewsProgressiveWebApps] сравнивают различные платформы и шаблоны производительности для реализации примера \ (средство чтения новостей с помощью хакеров \) PWA.</span><span class="sxs-lookup"><span data-stu-id="af2eb-279">[Hacker News readers as Progressive Web Apps][HackerNewsProgressiveWebApps] - Compares different frameworks and performance patterns for implementing a sample \(Hacker News reader\) PWA.</span></span>  

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
