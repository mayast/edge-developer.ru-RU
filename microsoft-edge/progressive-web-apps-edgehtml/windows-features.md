---
description: Расширение возможностей PWA для Windows с помощью собственных функций приложения
title: Адаптация PWA (EdgeHTML) для Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: прогрессивные веб-приложения, PWA, EDGE, Windows, WinRT, UWP, EdgeHTML
ms.openlocfilehash: 296ae0a65481edd312e06b83c1554813ec2bffae
ms.sourcegitcommit: 515522959f517e194f93a27f5d360690600edd9d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894719"
---
# <span data-ttu-id="578db-104">Адаптация PWA (EdgeHTML) для Windows</span><span class="sxs-lookup"><span data-stu-id="578db-104">Tailor your PWA (EdgeHTML) for Windows</span></span>  

<span data-ttu-id="578db-105">PWAs, установленный в Windows 10, обладает [всеми преимуществами][PwaIndexWindows10] работы в качестве приложений [универсальной платформы Windows (UWP)][WindowsUWPGetStartedGuide] , включая защиту через изолированную платформу приложения для Windows и полный доступ к API [среды выполнения Windows \ (WinRT \))][UwpApiIndex] , в том числе следующие:</span><span class="sxs-lookup"><span data-stu-id="578db-105">PWAs installed on Windows 10 enjoy [all the benefits][PwaIndexWindows10] of running as [Universal Windows Platform \(UWP\)][WindowsUWPGetStartedGuide] apps, including protection through Windows app sandboxing security and full access to [Windows Runtime \(WinRT\))][UwpApiIndex] APIs, including those for:</span></span>  

*   <span data-ttu-id="578db-106">Управление функциями устройства (например, Камера, микрофон, GPS)</span><span class="sxs-lookup"><span data-stu-id="578db-106">Controlling device features \(such as camera, microphone, GPS\)</span></span>  
*   <span data-ttu-id="578db-107">Доступ к пользовательским ресурсам \ (например, календарь, контакты, документы, музыка и т. д.)</span><span class="sxs-lookup"><span data-stu-id="578db-107">Accessing user resources \(such as calendar, contacts, documents, music\)</span></span>  
*   <span data-ttu-id="578db-108">Запуск и Навигация в приложении с помощью голосовых команд Кортаны</span><span class="sxs-lookup"><span data-stu-id="578db-108">Launching / navigating your app through Cortana voice commands</span></span>  
*   <span data-ttu-id="578db-109">Интеграция с ОС Windows \ (через центр уведомлений Windows, панель задач для настольных компьютеров и контекстные меню \)</span><span class="sxs-lookup"><span data-stu-id="578db-109">Integrating with the Windows OS \(through the Windows Action Center, desktop taskbar, and context menus\)</span></span>  

<span data-ttu-id="578db-110">Это лишь некоторые из добавленных возможностей для PWA \ (EdgeHTML \) в Windows.</span><span class="sxs-lookup"><span data-stu-id="578db-110">These are only a few of the added possibilities for your PWA \(EdgeHTML\) on Windows.</span></span>  

<span data-ttu-id="578db-111">В этой статье объясняется, как установить, запустить и усовершенствовать приложение PWA \ (EdgeHTML \) в Windows 10, а также обеспечить совместимость между браузерами и разными платформами.</span><span class="sxs-lookup"><span data-stu-id="578db-111">This article shows you how to install, run, and enhance your PWA \(EdgeHTML\) as a Windows 10 app, while still ensuring cross-browser and cross-platform compatibility.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="578db-112">Для примеров и шагов, описанных в этой статье, требуется Visual Studio 2017.</span><span class="sxs-lookup"><span data-stu-id="578db-112">The examples and steps in this article require Visual Studio 2017.</span></span> <span data-ttu-id="578db-113">В Visual Studio 2019 не входит шаблон, используемый в этой статье.</span><span class="sxs-lookup"><span data-stu-id="578db-113">Visual Studio 2019 does not include the template used in this article.</span></span> <span data-ttu-id="578db-114">Сведения о том, как скачать Visual Studio 2017, можно найти в разделе [загрузки Visual Studio — 2017, 2015 & предыдущие версии][PreviousVSDownloads]</span><span class="sxs-lookup"><span data-stu-id="578db-114">To download Visual Studio 2017, see [Visual Studio Downloads - 2017, 2015 & Previous Versions][PreviousVSDownloads]</span></span>  


## <span data-ttu-id="578db-115">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="578db-115">Prerequisites</span></span>  

*   <span data-ttu-id="578db-116">Существующий веб-сайт PWA \ (или размещенное приложение) — либо на сайте Live, либо на localhost.</span><span class="sxs-lookup"><span data-stu-id="578db-116">An existing PWA \(or hosted web app\), either a live or localhost site.</span></span>  <span data-ttu-id="578db-117">В этом руководстве для [начала работы с прогрессивными веб-приложениями][PwaGetStarted]используется образец PWA.</span><span class="sxs-lookup"><span data-stu-id="578db-117">This guide uses the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted].</span></span>  
*   <span data-ttu-id="578db-118">Скачайте (бесплатное) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span><span class="sxs-lookup"><span data-stu-id="578db-118">Download the \(free\) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].</span></span>  <span data-ttu-id="578db-119">Вы также можете использовать выпуски профессионального выпуска, Enterprise или [Preview][MicrosoftVisualStudioPreview] .</span><span class="sxs-lookup"><span data-stu-id="578db-119">You are also able to use the Professional, Enterprise, or [Preview][MicrosoftVisualStudioPreview] editions.</span></span>  <span data-ttu-id="578db-120">В установщике Visual Studio выберите указанные ниже рабочие нагрузки.</span><span class="sxs-lookup"><span data-stu-id="578db-120">From the Visual Studio Installer, choose the following Workloads:</span></span>  
    *   **<span data-ttu-id="578db-121">Разработка универсальной платформы Windows</span><span class="sxs-lookup"><span data-stu-id="578db-121">Universal Windows Platform development</span></span>**  

## <span data-ttu-id="578db-122">Настройка и выполнение универсального приложения для Windows</span><span class="sxs-lookup"><span data-stu-id="578db-122">Set up and run your Universal Windows app</span></span>  

<span data-ttu-id="578db-123">PWA \ (EdgeHTML \), установленный как приложение Windows 10, запускается независимо от браузера, в отдельном окне \ ( `WWAHost.exe` процесс).</span><span class="sxs-lookup"><span data-stu-id="578db-123">A PWA \(EdgeHTML\) installed as a Windows 10 app runs independently from the browser, in a standalone \(`WWAHost.exe` process\) window.</span></span>  <span data-ttu-id="578db-124">Для этого просто требуется упрощенная оболочка приложения, содержащая размещенное веб-приложение, которое вы можете быстро настроить с помощью `Progressive Web App (Universal Windows)` шаблона проекта Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="578db-124">Enabling this simply requires a lightweight app wrapper that contains your hosted web app, which you are able to quickly set up using the Visual Studio `Progressive Web App (Universal Windows)` project template.</span></span>  <span data-ttu-id="578db-125">\ (Все ваши логики приложения, включая отправку запросов API среды выполнения Windows, по-прежнему выполняются в исходном коде веб-приложения.)</span><span class="sxs-lookup"><span data-stu-id="578db-125">\(All your app logic, including sending native Windows Runtime API requests, still happens in your original web app code.\)</span></span>  

<span data-ttu-id="578db-126">Настройка среды разработки приложений для Windows в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="578db-126">Set up your Windows app development environment in Visual Studio.</span></span>  

1.  <span data-ttu-id="578db-127">В параметрах Windows включите [режим разработчика][WindowsUWPGetStartedEnable].</span><span class="sxs-lookup"><span data-stu-id="578db-127">In your Windows Settings, turn on [Developer mode][WindowsUWPGetStartedEnable].</span></span>  <span data-ttu-id="578db-128">\ (Введите `developer mode` в searchbar Windows, чтобы найти его. \)</span><span class="sxs-lookup"><span data-stu-id="578db-128">\(Type `developer mode` in the Windows searchbar to find it.\)</span></span>  
1.  <span data-ttu-id="578db-129">Запустите Visual Studio и **Создайте новый проект..** .</span><span class="sxs-lookup"><span data-stu-id="578db-129">Launch Visual Studio and **Create a new project...**</span></span>  
1.  <span data-ttu-id="578db-130">Выберите шаблон **проект упаковки приложений для Windows** на C#.</span><span class="sxs-lookup"><span data-stu-id="578db-130">Select the C# **Windows Application Packaging Project** template.</span></span>  <span data-ttu-id="578db-131">Если вы используете предыдущую версию Visual Studio, найдите соответствующий шаблон в разделе **размещенное веб-приложение (универсальные приложения для Windows)** или **прогрессивное веб-приложение (универсальные приложения для Windows)**.</span><span class="sxs-lookup"><span data-stu-id="578db-131">If you are using a previous version of Visual Studio, find the equivalent template under **Hosted Web App (Universal Windows)** or **Progressive Web App (Universal Windows)**.</span></span>  
1.  <span data-ttu-id="578db-132">Выберите по умолчанию Windows 10 `Target version` \ (самый последний выпуск \) и `Minimum version` \ (сборка 10586 или более поздняя) и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="578db-132">Select the default Windows 10 `Target version` \(most recent release\) and `Minimum version` \(build 10586 or higher\) and click **OK**.</span></span>  

    ![Диалоговое окно "выбор" в Visual Studio для сборок целевых объектов проекта UWP](media/vs-target-min-version.png)  

    <span data-ttu-id="578db-134">Новый проект загружается с открытым конструктором Package. appxmanifest.</span><span class="sxs-lookup"><span data-stu-id="578db-134">Your new project loads with the package.appxmanifest designer open.</span></span>  <span data-ttu-id="578db-135">Здесь вы настраиваете сведения о приложении, в том числе удостоверение пакета, зависимости пакетов, необходимые возможности, визуальные элементы и точки расширения.</span><span class="sxs-lookup"><span data-stu-id="578db-135">This is where you configure the details of your app, including package identity, package dependencies, required capabilities, visual elements, and extensibility points.</span></span>  <span data-ttu-id="578db-136">Это легко настраиваемая временная версия манифеста пакета приложения, используемая во время разработки приложения.</span><span class="sxs-lookup"><span data-stu-id="578db-136">This is an easily configurable, temporary version of the app package manifest used during app development.</span></span>  
    <span data-ttu-id="578db-137">При построении проекта приложения [Visual Studio создает файл AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] из этих метаданных, которые используются для установки и запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="578db-137">When you build your app project, [Visual Studio generates an AppxManifest.xml][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] file from this metadata, which is used to install and run your app.</span></span>  <span data-ttu-id="578db-138">Когда вы обновляете `package.appxmanifest` файл, не забудьте перестроить проект, чтобы оба были отражены во `AppxManifest.xml` время выполнения.</span><span class="sxs-lookup"><span data-stu-id="578db-138">Whenever you update your `package.appxmanifest` file, be sure to rebuild the project so both are reflected in your `AppxManifest.xml` at runtime.</span></span>  

1.  <span data-ttu-id="578db-139">На панели **приложения** в конструкторе манифестов введите URL-адрес PWA `Start page` .</span><span class="sxs-lookup"><span data-stu-id="578db-139">In the manifest designer **Application** panel, enter the URL of your PWA as the `Start page`.</span></span>

    > [!NOTE]
    > <span data-ttu-id="578db-140">Сотрудники служб поддерживаются для всех URL-адресов HTTPS \ (Secure, Remote), указанных в `StartPage` .</span><span class="sxs-lookup"><span data-stu-id="578db-140">Service workers are supported for all https \(secure, remote\) urls specified as the `StartPage`.</span></span>  <span data-ttu-id="578db-141">Сотрудники служб не поддерживаются по умолчанию для веб-приложений, задающих локальную начальную страницу.</span><span class="sxs-lookup"><span data-stu-id="578db-141">Service workers are not supported by default for web apps that specify a local start page.</span></span>  <span data-ttu-id="578db-142">Чтобы включить поддержку обслуживания сотрудников для этих случаев, добавьте в манифест явную запись [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) , например:</span><span class="sxs-lookup"><span data-stu-id="578db-142">To enable service worker support for these cases, add an explicit [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) entry to the manifest, for example:</span></span> `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Панель приложения в конструкторе Package. appxmanifest](media/vs-manifest-application.png)  
    
    <span data-ttu-id="578db-144">Вы можете изменить и то, `Display name` и другое `Description` .</span><span class="sxs-lookup"><span data-stu-id="578db-144">You are able to also modify the `Display name` and `Description` as you like.</span></span>  
1.  <span data-ttu-id="578db-145">Сохраните этот файл \ (или другой 512x512 изображение вашего выбора \) на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="578db-145">Save this file \(or another 512x512 image of your choosing\) to your desktop.</span></span>  
    <span data-ttu-id="578db-146">Затем на панели **визуальные ресурсы** конструктора манифестов нажмите кнопку `Source` поле **...** , выберите ее в качестве исходного файла и нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="578db-146">Then, in the manifest designer **Visual Assets** panel, click on the `Source` field **...** button, select it as your source file, and click **Generate**.</span></span>  <span data-ttu-id="578db-147">\ (Затем нажмите кнопку **ОК** , чтобы перезаписать изображения заполнителей по умолчанию \).</span><span class="sxs-lookup"><span data-stu-id="578db-147">\(Then click **OK** to overwrite the default placeholder images\).</span></span>  
    
    ![Панель "визуальные ресурсы" в конструкторе Package. appxmanifest](media/vs-manifest-visual-assets.png)  
    
    <span data-ttu-id="578db-149">Это создаст основные визуальные ресурсы для установки, запуска, запуска и распространения вашего приложения в магазине.</span><span class="sxs-lookup"><span data-stu-id="578db-149">This generates the basic visual assets for installing, running, launching, and distributing your app in the store.</span></span>  
    <span data-ttu-id="578db-150">Если отображаются красные ошибки \ ( `X` \), указывающие на отсутствие изображений, вы можете нажать кнопку ". **..** ", чтобы вручную выбрать файл из созданных изображений.</span><span class="sxs-lookup"><span data-stu-id="578db-150">If you see any red \(`X`\) errors indicating missing images, you are able to click on the **...** buttons to manually select a file from the generated images.</span></span>  
1.  <span data-ttu-id="578db-151">На панели **URI содержимого** конструктора манифестов замените на `http://example.com` расположение вашего PWA (например, `Rule`  =  `include` `WinRT Access`  =  `All` "\").</span><span class="sxs-lookup"><span data-stu-id="578db-151">In the manifest designer **Content URIs** panel, replace `http://example.com` with the location of your PWA \(such that `Rule` = `include` and `WinRT Access` = `All`\).</span></span>  
    <span data-ttu-id="578db-152">Таким образом, вы предоставляете разрешение на доступ к приложению PWA для отправки запросов API для встроенной среды выполнения Windows (WinRT) при запуске в качестве приложения Windows 10, которое рассматривается чуть позже.</span><span class="sxs-lookup"><span data-stu-id="578db-152">This grants your PWA permission to send native Windows Runtime \(WinRT\) API requests when running as a Windows 10 app, which is covered a bit later.</span></span>   <span data-ttu-id="578db-153">Если для вашего фактического доступа к приложению PWA не требуется доступ WinRT, вы можете переключить `WinRT Access` значение на `None` .</span><span class="sxs-lookup"><span data-stu-id="578db-153">If your actual PWA does not require WinRT access, you are able to switch the `WinRT Access` value to `None`.</span></span>  <span data-ttu-id="578db-154">В обоих случаях не забудьте вывести строку по умолчанию `http://example.com` с URI для PWA или ваше приложение не сможет правильно загрузиться во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="578db-154">Either way, be sure to sub out the default `http://example.com` string with the URI of your PWA, or your app is not able to properly load at runtime.</span></span>  
    <span data-ttu-id="578db-155">Вы готовы запускать и отлаживать PWA как приложение для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="578db-155">You are ready to run and debug your PWA as a Windows 10 app.</span></span>  <span data-ttu-id="578db-156">Если вы используете сайт localhost для перехода по этому руководству, убедитесь, что он запущен.</span><span class="sxs-lookup"><span data-stu-id="578db-156">If you are using a localhost site to step through this guide, make sure it is running.</span></span>  <span data-ttu-id="578db-157">Затем</span><span class="sxs-lookup"><span data-stu-id="578db-157">Then,</span></span>  
1.  <span data-ttu-id="578db-158">Выполните сборку \ ( `Ctrl` + `Shift` + `F5` \) и запустите \ ( `F5` \) проект PWA.</span><span class="sxs-lookup"><span data-stu-id="578db-158">Build \(`Ctrl`+`Shift`+`F5`\) and Run \(`F5`\) your PWA project.</span></span>  <span data-ttu-id="578db-159">После этого ваш веб-сайт должен быть запущен в отдельном окне приложения.</span><span class="sxs-lookup"><span data-stu-id="578db-159">Your website should now launch in a standalone app window.</span></span>  <span data-ttu-id="578db-160">Это размещенное веб-приложение. оно запущено в виде последовательного веб-приложения, установленного в Windows 10!</span><span class="sxs-lookup"><span data-stu-id="578db-160">Not only is it a hosted web app; it is running as a Progressive Web App installed on Windows 10!</span></span>  

    ![Работа PWA в окне WWAHost.exe](media/wwahost.png)  

## <span data-ttu-id="578db-162">Отладка PWA \ (EdgeHTML \) как приложение для Windows</span><span class="sxs-lookup"><span data-stu-id="578db-162">Debug your PWA \(EdgeHTML\) as a Windows app</span></span>  

<span data-ttu-id="578db-163">Поскольку PWA \ (EdgeHTML \) — это просто последовательное, а размещенное веб-приложение, вы можете выполнять отладку кода на стороне сервера так же, как и любое веб-приложение, используя обычную среду IDE и рабочий процесс.</span><span class="sxs-lookup"><span data-stu-id="578db-163">Because a PWA \(EdgeHTML\) is simply a progressively enhanced hosted web app, you are able to debug your server-side code the same as any web app, using your usual IDE and workflow.</span></span>  <span data-ttu-id="578db-164">Изменения, которые вы разработали в режиме реального времени, будут отражены в установленном приложении Project Web App при следующем запуске (не требуется повторное развертывание универсального пакета приложения для Windows).</span><span class="sxs-lookup"><span data-stu-id="578db-164">The changes you deploy live are reflected in your installed PWA the next time you launch it \(no need to redeploy your Universal Windows app package\).</span></span>

<span data-ttu-id="578db-165">Для отладки на стороне клиента в приложении для Windows 10 необходимо `Microsoft Edge DevTools Preview` приложение.</span><span class="sxs-lookup"><span data-stu-id="578db-165">For client-side debugging within your Windows 10 app, you must have the `Microsoft Edge DevTools Preview` app.</span></span>  <span data-ttu-id="578db-166">Это автономное приложение включает все возможности исходного браузера [Microsoft Edge DevTools][DevToolsGuide] \ (в том числе [средств PWA][DevToolsGuideServiceWorkers]), а также основную поддержку [удаленной отладки][DevToolsProtocol01ClientsEdgePreview] и средство [выбора отладочной][DevToolsGuideMicrosoftStoreApp] версии для присоединения к любому запущенному экземпляру обработчика EdgeHTML, в том числе надстроек для Office, кортаны, веб-представлений приложений и, конечно же, PWAs запущено в Windows.</span><span class="sxs-lookup"><span data-stu-id="578db-166">This standalone app includes all the functionality of the original in-browser [Microsoft Edge DevTools][DevToolsGuide] \(including [PWA tools][DevToolsGuideServiceWorkers]\), plus basic [remote debugging][DevToolsProtocol01ClientsEdgePreview] support and a [Debug Target chooser][DevToolsGuideMicrosoftStoreApp] for attaching to any running instance of the EdgeHTML engine, including add-ins for Office, Cortana, app webviews, and of course, PWAs running on Windows.</span></span>  

<span data-ttu-id="578db-167">Вот как можно настроить отладку для PWA \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="578db-167">Here is how to set up debugging for your PWA \(EdgeHTML\).</span></span>  

1.  <span data-ttu-id="578db-168">Установите приложение [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] из магазина Microsoft Store, если оно еще не установлено.</span><span class="sxs-lookup"><span data-stu-id="578db-168">Install the [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] app from the Microsoft Store if you do not already have it.</span></span>  
1.  <span data-ttu-id="578db-169">Запустив веб-сайт PWA и запускайте приложение DevTools.</span><span class="sxs-lookup"><span data-stu-id="578db-169">With your PWA site up and running, launch the DevTools app.</span></span>  
1.  <span data-ttu-id="578db-170">В Visual Studio запустите приложение Windows 10 с помощью `Start Without Debugging` `Ctrl` + `F5` команды ().</span><span class="sxs-lookup"><span data-stu-id="578db-170">From Visual Studio, launch your Windows 10 app with the `Start Without Debugging` (`Ctrl`+`F5`) command.</span></span>  <span data-ttu-id="578db-171">\ (Приложение DevTools не прикрепляется должным образом, если активен отладчик Visual Studio. \)</span><span class="sxs-lookup"><span data-stu-id="578db-171">\(The DevTools app does not attach properly if the Visual Studio debugger is active.\)</span></span>  
1.  <span data-ttu-id="578db-172">В приложении DevTools нажмите кнопку **Обновить** в локальной версии средства выбора целевых объектов отладки.</span><span class="sxs-lookup"><span data-stu-id="578db-172">In the DevTools app, click the **Refresh** button in the Local debug target chooser.</span></span>  <span data-ttu-id="578db-173">Теперь должен быть указан сайт PWA \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="578db-173">Your PWA \(EdgeHTML\) site should now be listed.</span></span>  <span data-ttu-id="578db-174">\ (Если он также работает в окне браузера, это последний экземпляр этого сайта в списке. \)</span><span class="sxs-lookup"><span data-stu-id="578db-174">\(If it is also running in a browser window, it is the last instance of that site in the list.\)</span></span>  
1.  <span data-ttu-id="578db-175">Щелкните ссылку на веб-сайт PWA \ (EdgeHTML \), чтобы открыть новую вкладку экземпляра DevTools и начать отладку.</span><span class="sxs-lookup"><span data-stu-id="578db-175">Click on your PWA \(EdgeHTML\) site listing to open a new DevTools instance tab and start debugging.</span></span>  
    
    ![Средство выбора локальных целей отладки в приложении Microsoft Edge DevTools](media/devtools-local.png)  
    
1.  <span data-ttu-id="578db-177">Вы можете проверить, что DevTools присоединен к веб-приложению PWA, запущенному под управлением Windows.</span><span class="sxs-lookup"><span data-stu-id="578db-177">You are able to verify that DevTools is attached to your PWA-running-as-Windows-app.</span></span>  <span data-ttu-id="578db-178">На **консоли**DevTools введите:</span><span class="sxs-lookup"><span data-stu-id="578db-178">In the DevTools **Console**, type:</span></span>  
    
    ```shell
    window.Windows
    ```  
    
    <span data-ttu-id="578db-179">Это возвращает глобальный `Windows Runtime` объект, содержащий все [пространства имен WinRT верхнего уровня](#find-windows-runtime-winrt-apis).</span><span class="sxs-lookup"><span data-stu-id="578db-179">This returns the global `Windows Runtime` object containing all of the [top-level WinRT namespaces](#find-windows-runtime-winrt-apis).</span></span>  <span data-ttu-id="578db-180">Это ваша входная точка PWA \ (EdgeHTML \) для [универсальной платформы Windows][WindowsUWPIndex], доступная только для веб-приложений, которые выполняются в приложениях Windows 10 (в процессе, запущенном за пределами браузера `WWAHost.exe` ).</span><span class="sxs-lookup"><span data-stu-id="578db-180">This is your PWA \(EdgeHTML\) entrypoint to the [Universal Windows Platform][WindowsUWPIndex], and only exposed to web apps that run as Windows 10 apps (running outside the browser, in a `WWAHost.exe` process).</span></span>  
    
## <span data-ttu-id="578db-181">Поиск API-интерфейсов среды выполнения Windows \ (WinRT \)</span><span class="sxs-lookup"><span data-stu-id="578db-181">Find Windows Runtime \(WinRT\) APIs</span></span>  

<span data-ttu-id="578db-182">Как установленное приложение для Windows, класс [PWA \ (EdgeHTML \) имеет полный доступ к встроенным API среды выполнения Windows][WindowsRuntime]. Определение необходимых данных, получение разрешений для реквизитов и использование функции обнаружения функций для отправки запроса API в поддерживаемых средах.</span><span class="sxs-lookup"><span data-stu-id="578db-182">As an installed Windows app, your [PWA \(EdgeHTML\) has full access to native Windows Runtime APIs][WindowsRuntime]; identify what you need to use, obtain the requisite permissions, and employ feature detection to send that API request on supported environments.</span></span>  <span data-ttu-id="578db-183">Пошаговые инструкции по добавлению последовательного расширения для пользователей классического приложения для Windows для настольных систем.</span><span class="sxs-lookup"><span data-stu-id="578db-183">Walk through this process to add a progressive enhancement for Windows desktop users of your PWA.</span></span>  

<span data-ttu-id="578db-184">Существует несколько способов идентификации API универсальной платформы Windows, необходимых для работы с Windows PWA, в том числе поиск в обширных [документах UWP в центре разработки для Windows] [UWP/API/], скачивание и запуск [примеров кода UWP](#uwp-code-samples) в Visual Studio, а также просмотр фрагментов кода для распространенных задач для PWAs в Windows.</span><span class="sxs-lookup"><span data-stu-id="578db-184">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for PWAs on Windows.</span></span>

<span data-ttu-id="578db-185">Существует несколько способов идентификации API универсальной платформы Windows, которые необходимы для работы с Windows PWA, в том числе поиск в обширных [документах UWP в центре разработки для Windows] [UWP/API/], скачивание и запуск [примеров кода UWP](#uwp-code-samples) в Visual Studio, а также просмотр фрагментов кода для распространенных задач для [PWAs в Windows 10 (EdgeHTML)][PwaIndexWindows10].</span><span class="sxs-lookup"><span data-stu-id="578db-185">There are a number of ways to identify the Universal Windows Platform APIs you need for your Windows PWA, including searching the comprehensive [UWP docs on Windows Dev Center][uwp/api/], downloading and running [UWP code samples](#uwp-code-samples) with Visual Studio, and browsing code snippets for common tasks for [PWAs on Windows 10 (EdgeHTML)][PwaIndexWindows10].</span></span>  

<span data-ttu-id="578db-186">Общие API-интерфейсы WinRT работают в JavaScript так же, как и в C#, поэтому вы можете использовать общие сведения о [платформе универсальной платформы Windows][WindowsUWPIndex] и [Справочник по API-интерфейсам][UwpApiIndex] для использования.</span><span class="sxs-lookup"><span data-stu-id="578db-186">Overall, WinRT APIs work in JavaScript the same way they do in C#, so you may follow the general [Universal Windows Platform documentation][WindowsUWPIndex] and [API Reference][UwpApiIndex] for usage.</span></span>  <span data-ttu-id="578db-187">Однако обратите внимание на указанные ниже отличия.</span><span class="sxs-lookup"><span data-stu-id="578db-187">However, please note the following differences:</span></span>  

*   <span data-ttu-id="578db-188">Для функций WinRT в JavaScript используются [различные соглашения о регистре][ScriptingJsinrtUsingWinRTCasingConventions]</span><span class="sxs-lookup"><span data-stu-id="578db-188">WinRT features in JavaScript use  [different casing conventions][ScriptingJsinrtUsingWinRTCasingConventions]</span></span>  
*   <span data-ttu-id="578db-189">[События представлены в виде строковых идентификаторов][ScriptingJsinrtHandlingWinRTEvents] , передаваемых `addEventListener` / `removeEventListener` методам класса.</span><span class="sxs-lookup"><span data-stu-id="578db-189">[Events are represented as string identifiers][ScriptingJsinrtHandlingWinRTEvents] passed to class `addEventListener`/`removeEventListener` methods</span></span>  
*   <span data-ttu-id="578db-190">[Асинхронные методы][ScriptingJsinrtUsingWinRT] используют модель Promise для JavaScript</span><span class="sxs-lookup"><span data-stu-id="578db-190">[Asynchronous methods][ScriptingJsinrtUsingWinRT] use the JavaScript Promise model</span></span>  
*   <span data-ttu-id="578db-191">API-интерфейсы в `Windows.UI.Xaml` пространстве имен не поддерживаются для приложений JavaScript, которые вместо этого используют стек [EdgeHTML][DevGuideWhatsNew] модуля подготовки к просмотру \ (HTML, CSS \).</span><span class="sxs-lookup"><span data-stu-id="578db-191">APIs in the `Windows.UI.Xaml` namespace are not supported for JavaScript apps, which instead use the [EdgeHTML][DevGuideWhatsNew] engine web rendering stack \(HTML, CSS\)</span></span>  

<span data-ttu-id="578db-192">Дополнительные сведения можно найти [в разделе Использование среды выполнения Windows в JavaScript][WindowRuntimeUsingJavascript].</span><span class="sxs-lookup"><span data-stu-id="578db-192">For more details, see [Using the Windows Runtime in JavaScript][WindowRuntimeUsingJavascript].</span></span>  

### <span data-ttu-id="578db-193">Примеры кода UWP</span><span class="sxs-lookup"><span data-stu-id="578db-193">UWP code samples</span></span>  

<span data-ttu-id="578db-194">В репозитории [примеров универсальной платформы Windows (UWP)][MicrosoftDeveloperWindowsSamples] можно найти примеры кода JavaScript для распространенных сценариев приложений для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="578db-194">Check out the [Universal Windows Platform \(UWP\) Code Samples][MicrosoftDeveloperWindowsSamples] repo to browse JavaScript examples for common Windows 10 app scenarios.</span></span>  <span data-ttu-id="578db-195">Несмотря на то, что в JS-версиях этих примеров используется библиотека [WinJS][GithubWinjsWinjs] для структурирования шаблона, WinJS не требуется для отправки запросов API WinRT, которые демонстрируются в этих примерах.</span><span class="sxs-lookup"><span data-stu-id="578db-195">Although the JS versions of these samples use the [WinJS][GithubWinjsWinjs] library to structure the sample template, WinJS is not required for sending the WinRT API requests demonstrated in these samples.</span></span>  

> [!NOTE]
> <span data-ttu-id="578db-196">Если необходимо прослушать [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] событие для приложения, вы можете сделать это с помощью следующего собственного API WinRT.</span><span class="sxs-lookup"><span data-stu-id="578db-196">If you need to listen for the [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] event for the app, you are able to do this using the following native WinRT API:</span></span>  
> 
> **<span data-ttu-id="578db-197">Используйте этот</span><span class="sxs-lookup"><span data-stu-id="578db-197">Use this</span></span>**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> <span data-ttu-id="578db-198">... в отличие от этого типа WinJS запроса, используемого в примерах:</span><span class="sxs-lookup"><span data-stu-id="578db-198">... as opposed this type of WinJS request used in the samples:</span></span>  
> 
> **<span data-ttu-id="578db-199">Это не так</span><span class="sxs-lookup"><span data-stu-id="578db-199">Not this</span></span>**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## <span data-ttu-id="578db-200">Отправка запросов API WinRT из PWA (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="578db-200">Send WinRT API requests from your PWA (EdgeHTML)</span></span>  

<span data-ttu-id="578db-201">На этом этапе вы хотите добавить настраиваемое контекстное меню для пользователей Windows на веб-странице PWA \ (EdgeHTML \) и определить необходимые API в пространстве имен [Windows. UI. popups][UwpApiWindowsUiPopups] .</span><span class="sxs-lookup"><span data-stu-id="578db-201">At this point, pretend you want to add a custom context menu for Windows users of our PWA \(EdgeHTML\) and have identified the APIs you need in the [Windows.UI.Popups][UwpApiWindowsUiPopups] namespace.</span></span>  

<span data-ttu-id="578db-202">Чтобы отправить любые запросы API WinRT из нашего PWA \ (EdgeHTML \), необходимо сначала [установить разрешения реквизитов](#set-application-content-uri-rules-acurs) \ (или правила URI содержимого приложения \) в файле манифеста пакета приложения Windows \ ( `.appxmanifest` \).</span><span class="sxs-lookup"><span data-stu-id="578db-202">In order to send any WinRT APIs requests from our PWA \(EdgeHTML\), you first need to [establish the requisite permissions](#set-application-content-uri-rules-acurs) \(or, Application Content URI Rules\) in your Windows app package manifest \(`.appxmanifest`\) file.</span></span>  

<span data-ttu-id="578db-203">Если какой-либо из этих запросов API включает доступ к пользовательским ресурсам, например изображениям и музыке, или к функциям устройств, таким как камера или микрофон, необходимо также добавить [объявления возможностей приложения](#app-capability-declarations) в манифест пакета приложения, чтобы Windows предложит пользователю разрешение.</span><span class="sxs-lookup"><span data-stu-id="578db-203">If any of these API requests involve access to user resources like pictures or music, or to device features like the camera or microphone, you also need to add [app capability declarations](#app-capability-declarations) to the app package manifest in order for Windows to prompt the user for permission.</span></span>  <span data-ttu-id="578db-204">Если позже вы опубликуете PWA \ (EdgeHTML \) в Microsoft Store, такие разрешения на [доступ к приложениям][MicrosoftSupportWindowsAppPermissions] также будут указаны в вашем списке в магазине.</span><span class="sxs-lookup"><span data-stu-id="578db-204">If you later publish your PWA \(EdgeHTML\) to the Microsoft Store, these required [App permissions][MicrosoftSupportWindowsAppPermissions] are also noted in your store listing.</span></span>  

#### <span data-ttu-id="578db-205">Настройка правил URI содержимого приложения (Acur)</span><span class="sxs-lookup"><span data-stu-id="578db-205">Set Application Content URI Rules (ACURs)</span></span>  

<span data-ttu-id="578db-206">С помощью Acur, в противном случае называемого списком разрешенных URL-адресов, вы можете предоставить URL-адреса для прямого доступа к API PWA \ (EdgeHTML \) в интерфейсах среды выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="578db-206">Through ACURs, otherwise known as a URL allow list, you are able to give the URLs of your PWA \(EdgeHTML\) direct access to Windows Runtime APIs.</span></span>  <span data-ttu-id="578db-207">На уровне операционной системы Windows права на доступ к интерфейсу API платформы разрешаются с помощью кода, размещенного на веб-сервере.</span><span class="sxs-lookup"><span data-stu-id="578db-207">At the Windows OS level, the right policy bounds are set to allow code hosted on your web server to directly send platform API requests.</span></span>  <span data-ttu-id="578db-208">Вы определяете эти границы в файле манифеста пакета приложения, когда вы указываете URL-адреса PWA как `ApplicationContentUriRules` .</span><span class="sxs-lookup"><span data-stu-id="578db-208">You define these bounds in the app package manifest file when you specify your PWA URLs as `ApplicationContentUriRules`.</span></span>  

<span data-ttu-id="578db-209">Правила должны включать начальную страницу для вашего приложения и другие страницы, которые нужно добавить в качестве страниц приложения.</span><span class="sxs-lookup"><span data-stu-id="578db-209">Your rules should include the start page for your app and any other pages you want included as app pages.</span></span>  <span data-ttu-id="578db-210">Если пользователь переходит по URL-адресу, который не входит в правила, Windows открывает целевой URL-адрес в браузере Microsoft EDGE, а не в отдельном окне PWA \ ( `WWAHost.exe` процесс \).</span><span class="sxs-lookup"><span data-stu-id="578db-210">If your user navigates to a URL that is not included in your rules, Windows opens the target URL in the Microsoft Edge browser rather than your standalone PWA \(EdgeHTML\) window \(`WWAHost.exe` process\).</span></span>  <span data-ttu-id="578db-211">Вы также можете исключить конкретные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="578db-211">You may also exclude specific URLs.</span></span>  

<span data-ttu-id="578db-212">Указать URL-адрес `Match` в правилах можно несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="578db-212">There are several ways to specify a URL `Match` in your rules:</span></span>  

*   <span data-ttu-id="578db-213">Точное имя узла</span><span class="sxs-lookup"><span data-stu-id="578db-213">An exact hostname</span></span>  
*   <span data-ttu-id="578db-214">Имя узла, для которого включен или исключен универсальный код ресурса (URI) со всеми поддоменами этого имени узла</span><span class="sxs-lookup"><span data-stu-id="578db-214">A hostname for which a URI with any subdomain of that hostname is included or excluded</span></span>  
*   <span data-ttu-id="578db-215">Точный URI</span><span class="sxs-lookup"><span data-stu-id="578db-215">An exact URI</span></span>  
*   <span data-ttu-id="578db-216">Точный URI, содержащий свойство запроса</span><span class="sxs-lookup"><span data-stu-id="578db-216">An exact URI containing a query property</span></span>  
*   <span data-ttu-id="578db-217">Частичный путь и подстановочный знак для указания конкретного расширения файлов</span><span class="sxs-lookup"><span data-stu-id="578db-217">A partial path and a wildcard to indicate a particular file extension for an include rule</span></span>  
*   <span data-ttu-id="578db-218">Относительные пути для правил исключения</span><span class="sxs-lookup"><span data-stu-id="578db-218">Relative paths for exclude rules</span></span>  

<span data-ttu-id="578db-219">Вот несколько примеров Acur в `.appxmanifest` файле:</span><span class="sxs-lookup"><span data-stu-id="578db-219">Here are a few examples of ACURs in a `.appxmanifest` file:</span></span>  

```xml
<Application
Id="App"
StartPage="https://contoso.com/home">
<uap:ApplicationContentUriRules>
    <uap:Rule Type="include" Match="https://contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="include" Match="https://*.contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="exclude" Match="https://contoso.com/excludethispage.aspx" />
</uap:ApplicationContentUriRules>
```  

<span data-ttu-id="578db-220">URL-адреса, определенные в Acur для вашего приложения, могут предоставлять доступ к среде выполнения Windows с помощью `WindowsRuntimeAccess` атрибута, принимающего следующие значения:</span><span class="sxs-lookup"><span data-stu-id="578db-220">URLs defined within the ACURs for your app are able to be granted permission to the Windows Runtime through the `WindowsRuntimeAccess` attribute, which accepts the following values:</span></span>  

*   `all`<span data-ttu-id="578db-221">: Удаленный код JavaScript имеет доступ ко всем API-интерфейсам WinRT и локальным пакетным компонентам.</span><span class="sxs-lookup"><span data-stu-id="578db-221">: Remote JavaScript code has access to all WinRT APIs and any local packaged components.</span></span>  <span data-ttu-id="578db-222">В обработчике сценария будет вставлено пространство имен [Windows \ (WinRT \))][UwpApiIndex] .</span><span class="sxs-lookup"><span data-stu-id="578db-222">The [Windows \(WinRT\))][UwpApiIndex] namespace is injected and present in the script engine.</span></span>  
*   `allowForWeb`<span data-ttu-id="578db-223">: Удаленный доступ к коду JavaScript ограничен локальными пакетными компонентами, включая пользовательские компоненты C++/C #.</span><span class="sxs-lookup"><span data-stu-id="578db-223">: Remote JavaScript code access is limited to local packaged components, including custom C++/C# components.</span></span>  
*   `none`<span data-ttu-id="578db-224">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="578db-224">: Default.</span></span>  <span data-ttu-id="578db-225">Указанный URL-адрес не получает доступ к платформе.</span><span class="sxs-lookup"><span data-stu-id="578db-225">The specified URL has no platform access.</span></span>  

<span data-ttu-id="578db-226">В этом учебнике вы уже задали единственный ACUR, который вам нужен (шаг 6 предыдущей [настройки и запуск вашего раздела приложения](#set-up-and-run-your-universal-windows-app) ) для вашего приложения на основе одной страницы.</span><span class="sxs-lookup"><span data-stu-id="578db-226">In this tutorial, you already set the only ACUR that you need \(Step 6 of the previous [Set up and run your app](#set-up-and-run-your-universal-windows-app) section\) for your single-page app.</span></span>  <span data-ttu-id="578db-227">Вы можете подтвердить это с помощью панели **URI содержимого** в `package.appxmanifest` конструкторе Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="578db-227">You are able to confirm this from the **Content URIs** panel of the Visual Studio `package.appxmanifest` designer.</span></span>  

![Панель URI содержимого в конструкторе appxmanifest Visual Studio](media/vs-appxmanifest-editor-acurs.png)  

<span data-ttu-id="578db-229">Вы также можете просмотреть необработанный XML-файл манифеста, щелкнув его правой кнопкой мыши `package.appxmanifest` в обозревателе решений Visual Studio и выбрав команду **Просмотреть код** \ ( `F7` \).</span><span class="sxs-lookup"><span data-stu-id="578db-229">You are also able to view the raw XML of your manifest by right-clicking your `package.appxmanifest` file in Visual Studio Solution Explorer and selecting **View Code** \(`F7`\).</span></span>  <span data-ttu-id="578db-230">Чтобы вернуться в режим конструктора, нажмите кнопку **Конструктор представлений** \ ( `Shift` + `F7` \).</span><span class="sxs-lookup"><span data-stu-id="578db-230">To toggle back to the Designer view, select **View Designer** \(`Shift`+`F7`\).</span></span>  

#### <span data-ttu-id="578db-231">Объявления возможностей приложения</span><span class="sxs-lookup"><span data-stu-id="578db-231">App capability declarations</span></span>  

<span data-ttu-id="578db-232">Если вашему приложению требуется программный доступ к пользовательским ресурсам, например изображениям и музыке, или к устройствам, таким как камера или микрофон, необходимо включить соответствующие [объявления возможностей приложения][WindowsUwpPackagingAppCapabilities] в файл манифеста пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="578db-232">If your app needs programmatic access to user resources like pictures or music, or to devices like a camera or a microphone, you must include the corresponding [App capability declarations][WindowsUwpPackagingAppCapabilities] in your app package manifest file.</span></span>  <span data-ttu-id="578db-233">Ниже приводятся три категории объявления возможностей приложения.</span><span class="sxs-lookup"><span data-stu-id="578db-233">There are three app capability declaration categories:</span></span>  

*   <span data-ttu-id="578db-234">[Возможности общего применения][WindowsUwpPackagingAppCapabilitiesGeneralUse], которые используются в большей части сценариев приложений.</span><span class="sxs-lookup"><span data-stu-id="578db-234">[General-use capabilities][WindowsUwpPackagingAppCapabilitiesGeneralUse] that apply to most common app scenarios.</span></span>  
*   <span data-ttu-id="578db-235">[Возможности устройства][WindowsUwpPackagingAppCapabilitiesDevice], которые позволяют вашему приложению получать доступ к периферийным и внутренним устройствам.</span><span class="sxs-lookup"><span data-stu-id="578db-235">[Device capabilities][WindowsUwpPackagingAppCapabilitiesDevice] that allow your app to access peripheral and internal devices.</span></span>  
*   <span data-ttu-id="578db-236">[Специальные возможности][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] , поддерживающие сценарии предприятий и требующие использования учетной записи компании Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="578db-236">[Special-use capabilities][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] that support enterprise scenarios and require a Microsoft Store company account.</span></span>  <span data-ttu-id="578db-237">Подробнее об учетных записях компаний см. в разделе [Типы, доступность и стоимость учетных записей][WindowsUwpPublishAccountTypesLocationsFees].</span><span class="sxs-lookup"><span data-stu-id="578db-237">For more info about company accounts, see [Account types, locations, and fees][WindowsUwpPublishAccountTypesLocationsFees].</span></span>

<span data-ttu-id="578db-238">На странице приложения Microsoft Store перечислены все возможности, объявленные в манифесте пакета приложения, поэтому не забудьте указать только те возможности, которые используются приложением в действительности.</span><span class="sxs-lookup"><span data-stu-id="578db-238">Your Microsoft Store app page lists all the capabilities you declare in your app package manifest, so be sure to only specify the capabilities that your app actually uses.</span></span>

<span data-ttu-id="578db-239">Некоторые возможности предоставляют приложениям доступ к конфиденциальным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="578db-239">Some capabilities provide apps access to sensitive resources.</span></span>  <span data-ttu-id="578db-240">Эти ресурсы считаются конфиденциальными, так как каждый из них может получить доступ к личным данным пользователя или стоить пользователю денег.</span><span class="sxs-lookup"><span data-stu-id="578db-240">These resources are considered sensitive because each is able to access the user's personal data or cost the user money.</span></span>  <span data-ttu-id="578db-241">Параметры конфиденциальности, управляемые приложением " [Параметры][BingResultsWindows10Settings] " для Windows 10, позволяют пользователю динамически управлять доступом к конфиденциальным ресурсам.</span><span class="sxs-lookup"><span data-stu-id="578db-241">Privacy settings, managed by the Windows 10 [Settings][BingResultsWindows10Settings] app, let the user dynamically control access to sensitive resources.</span></span>  <span data-ttu-id="578db-242">Таким образом, важно, чтобы приложение не считало конфиденциальные ресурсы всегда доступными.</span><span class="sxs-lookup"><span data-stu-id="578db-242">Thus, it is important that your app does not assume a sensitive resource is always available.</span></span>  <span data-ttu-id="578db-243">Подробнее о доступе к конфиденциальным ресурсам см. в разделе [Руководство по приложениям, учитывающим требования конфиденциальности][WindowsUwp|::ref2::|Index].</span><span class="sxs-lookup"><span data-stu-id="578db-243">For more info about accessing sensitive resources, see [Guidelines for privacy-aware apps][WindowsUwp|::ref2::|Index].</span></span>  

<span data-ttu-id="578db-244">Вы запрашиваете доступ, объявляя возможности в манифесте пакета для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="578db-244">You request access by declaring capabilities in the package manifest for your app.</span></span>  <span data-ttu-id="578db-245">В Visual Studio вы можете сделать это на панели " **возможности** " конструктора Package. appxmanifest.</span><span class="sxs-lookup"><span data-stu-id="578db-245">In Visual Studio, you are able to do this from the **Capabilities** panel of the package.appxmanifest designer.</span></span>  

![Панель "возможности" в конструкторе appxmanifest Visual Studio](media/vs-appxmanifest-editor-capabilities.png)  

<span data-ttu-id="578db-247">В этом учебнике требуется только возможность использования по умолчанию для Интернет-(клиент \), поэтому дальнейших действий не требуется.</span><span class="sxs-lookup"><span data-stu-id="578db-247">In this tutorial, only the default Internet \(Client\) capability is required, so no further action is needed.</span></span>  

### <span data-ttu-id="578db-248">Использование функции обнаружения компонентов для вызова WinRT</span><span class="sxs-lookup"><span data-stu-id="578db-248">Use feature detection to invoke WinRT</span></span>  

<span data-ttu-id="578db-249">Чтобы обеспечить оптимальное качество для аудитории PWA на всех платформах, вы можете усовершенствовать интерфейс PWA в Windows с помощью обнаружения компонентов WinRT.</span><span class="sxs-lookup"><span data-stu-id="578db-249">To ensure a quality baseline experience for your PWA audience across all platforms, you progressively enhance your PWA experience on Windows using WinRT feature detection.</span></span>  <span data-ttu-id="578db-250">Таким образом, вы можете убедиться, что ваш код для Windows работает только в контексте, в котором доступны и применимы API-интерфейсы WinRT.</span><span class="sxs-lookup"><span data-stu-id="578db-250">This way, you are able to be sure your Windows-specific code is only run in a context where WinRT APIs are available and applicable.</span></span>  

<span data-ttu-id="578db-251">Обнаружение компонентов может быть таким же простым, как поиск `Windows` объекта \ (точка входа в [пространство имен WinRT][UwpApiIndex]\), как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="578db-251">Feature detection may be as simple as looking for the `Windows` object \(the entrypoint to the [WinRT namespace][UwpApiIndex]\) as below:</span></span>  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="578db-252">Тем не менее, если все интерфейсы API Windows доступны не на всех [типах устройств Windows 10][UwpExtensionSdkDeviceFamiliesOverview], лучше квалифицировать пространство имен запроса API, которое вы отправляете, с помощью более детального определения функций.</span><span class="sxs-lookup"><span data-stu-id="578db-252">However, given that not all Windows APIs are available on all [Windows 10 device types][UwpExtensionSdkDeviceFamiliesOverview], it is generally useful to use more specific feature detection to further qualify the namespace of the API request you are sending:</span></span>  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

<span data-ttu-id="578db-253">С помощью этого фона вы можете добавить некоторый код WinRT для реализации настраиваемого контекстного меню.</span><span class="sxs-lookup"><span data-stu-id="578db-253">With that background, you are ready to add some WinRT code to implement a custom context menu.</span></span>  <span data-ttu-id="578db-254">Если вы используете образец PWA [для начала работы с прогрессивными веб-приложениями][PwaGetStarted], выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="578db-254">If you are using the sample PWA from [Get started with Progressive Web Apps][PwaGetStarted]:</span></span>

1.  <span data-ttu-id="578db-255">Откройте Visual Studio для проекта сайта PWA.</span><span class="sxs-lookup"><span data-stu-id="578db-255">Open Visual Studio to your PWA site project.</span></span>

1.  <span data-ttu-id="578db-256">В обозревателе решений откройте `views\layout.pug` файл и добавьте следующую строку прямо ниже `script` ссылки для сотрудника службы:</span><span class="sxs-lookup"><span data-stu-id="578db-256">In Solution Explorer, open the `views\layout.pug` file and add the following line, right below the `script` reference for your service worker:</span></span>
    
    ```xml
    script(src='/javascripts/site.js')
    ```  

1.  <span data-ttu-id="578db-257">В обозревателе решений щелкните правой кнопкой мыши `javascripts` папку и выберите команду **Добавить**  >  **новый файл..**..</span><span class="sxs-lookup"><span data-stu-id="578db-257">In Solution Explorer, right-click on the `javascripts` folder and **Add** > **New File...**.</span></span>

1.  <span data-ttu-id="578db-258">Присвойте файлу имя: `site.js` и скопируйте его в следующем коде:</span><span class="sxs-lookup"><span data-stu-id="578db-258">Name your file: `site.js`, and copy in the following code:</span></span>
    
    ```javascript
    if (window.Windows && Windows.UI.Popups) {
        document.addEventListener('contextmenu', function (e) {

            // Build the context menu
            var menu = new Windows.UI.Popups.PopupMenu();
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 1", null, 1));
            menu.commands.append(new Windows.UI.Popups.UICommandSeparator);
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 2", null, 2));

            // Convert from webpage to WinRT coordinates
            function pageToWinRT(pageX, pageY) {
                var zoomFactor = document.documentElement.msContentZoomFactor;
                return {
                    x: (pageX - window.pageXOffset) * zoomFactor,
                    y: (pageY - window.pageYOffset) * zoomFactor
                };
            }

            // When the menu is invoked, execute the requested command
            menu.showAsync(pageToWinRT(e.pageX, e.pageY)).done(function (invokedCommand) {
                if (invokedCommand !== null) {
                    switch (invokedCommand.id) {
                        case 1:
                            console.log('Option 1 selected');
                            // Invoke code for option 1
                            break;
                        case 2:
                            console.log('Option 2 selected');
                            // Invoke code for option 2
                            break;
                        default:
                            break;
                    }
                } else {
                    // The command is null if no command was invoked.
                    console.log("Context menu dismissed");
                }
            });
        }, false);
    }
    ```

1.  <span data-ttu-id="578db-259">Сравните поведение контекстного меню при запуске PWA в браузере \ ( `F5` из проекта сайта PWA) и в окне приложения Windows \ ( `F5` из проекта универсального приложения для Windows).</span><span class="sxs-lookup"><span data-stu-id="578db-259">Compare the context menu behavior when you run your PWA in the browser \(`F5` from your PWA site project\) versus from inside the Windows app window \(`F5` from your Universal Windows app project\).</span></span>  <span data-ttu-id="578db-260">При щелчке правой кнопкой мыши в браузере появляется контекстное меню Microsoft Edge по умолчанию, в то время как в `WWAHost.exe` процессе вы можете открыть свое пользовательское меню.</span><span class="sxs-lookup"><span data-stu-id="578db-260">In the browser, right-clicking gives you the Microsoft Edge default context menu, whereas in the `WWAHost.exe` process, your custom menu now appears.</span></span>  

    | <span data-ttu-id="578db-261">Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="578db-261">Microsoft Edge</span></span> | <span data-ttu-id="578db-262">Приложение для Windows 10</span><span class="sxs-lookup"><span data-stu-id="578db-262">Windows 10 app</span></span> |  
    |:--- |:---- |  
    | ![Контекстное меню браузера по умолчанию](media/browser-context-menu.png) | ![Настраиваемое контекстное меню приложения](media/app-context-menu.png) |  

<span data-ttu-id="578db-265">Будем надеяться, что теперь у вас есть надежная основа для постепенного совершенствования PWAs в Windows.</span><span class="sxs-lookup"><span data-stu-id="578db-265">Hopefully you now have a solid foundation for progressively enhancing your PWAs on Windows.</span></span>  <span data-ttu-id="578db-266">Если вы столкнулись с вопросами или что-то еще не понятно, пожалуйста, отправьте комментарий.</span><span class="sxs-lookup"><span data-stu-id="578db-266">If you run into questions or anything is unclear, please send a comment!</span></span>  

## <span data-ttu-id="578db-267">Дальнейшая работа</span><span class="sxs-lookup"><span data-stu-id="578db-267">Going further</span></span>

<span data-ttu-id="578db-268">[Центр разработки для Windows][MicrosoftDeveloperWindowsApps] — это полный справочник по всем этапам здания приложений для Windows, от [начала работы][MicrosoftDeveloperWindowsAppsGetStarted]до [проектирования][MicrosoftDeveloperWindowsAppsDesign], [разработки][MicrosoftDeveloperWindowsAppsDevelop]и [публикации][MicrosoftDeveloperStorePublishApps] в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="578db-268">The [Windows Dev Center][MicrosoftDeveloperWindowsApps] is your complete reference for all stages of Windows app building, from [getting started][MicrosoftDeveloperWindowsAppsGetStarted], to [designing][MicrosoftDeveloperWindowsAppsDesign], [developing][MicrosoftDeveloperWindowsAppsDevelop], and [publishing][MicrosoftDeveloperStorePublishApps] to the Microsoft Store.</span></span>  

<span data-ttu-id="578db-269">Общие сведения о платформе универсальной платформы Windows (UWP) и о том, как ориентироваться на различные семейства устройств для Windows 10, приведены в статье [Введение для универсальной платформы Windows][WindowsUWPGetStartedGuide].</span><span class="sxs-lookup"><span data-stu-id="578db-269">For a general overview on the Universal Windows Platform \(UWP\) and how to target different Windows 10 device families, see [Intro to the Universal Windows Platform][WindowsUWPGetStartedGuide].</span></span>  

<span data-ttu-id="578db-270">Когда вы будете готовы, вот как \ (и почему! \) можно [Отправить PWA в Microsoft Store](./microsoft-store.md).</span><span class="sxs-lookup"><span data-stu-id="578db-270">And when you are ready, here is how \(and why!\) to [Submit your PWA to the Microsoft Store](./microsoft-store.md).</span></span>  

<!-- image links -->  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Приступите к работе с прогрессивными веб-приложениями"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs в Windows 10 (EdgeHTML) — прогрессивные веб-приложения для Windows"  
[DevToolsGuide]: ../devtools-guide.md "Инструменты разработчика Microsoft EDGE (EdgeHTML)"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide.md#microsoft-store-app "Microsoft Store App-Microsoft EDGE (EdgeHTML) Tools Developer"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Служебные сценарии"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Предварительный просмотр Средств разработчика в Microsoft Edge — Клиенты протокола средств разработчика"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "Новые возможности EdgeHTML"  
[WindowsRuntime]: ../windows-runtime/index.md "Среда выполнения Windows (WinRT) для JavaScript"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Использование среды выполнения Windows в JavaScript"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Обработка событий среды выполнения Windows в JavaScript"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Использование асинхронных методов среды выполнения Windows"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Соглашения с прописными буквами в функциях среды выполнения Windows — использование среды выполнения Windows в JavaScript"  
[UwpApiIndex]: /uwp/api/index "Пространства имен Windows UWP"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Пространство имен Windows. UI. popups"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "Событие WebUIApplication. Activated"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Общие сведения о семействах устройств"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "Создание манифеста пакета приложения в Visual Studio"  
[WindowsUWPIndex]: /windows/uwp/index "Документация по универсальной платформе Windows"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "Что такое приложение универсальной платформы Windows (UWP)?"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Активация устройства для разработки"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Разрешения"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Типы счетов, места и сборы"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Ограниченные возможности"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Возможности устройства"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "Возможности общего использования"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "Объявления возможностей приложения"  

[BingResultsWindows10Settings]: https://binged.it/2lOGSH0 "Параметры Windows 10 — Bing"  
[GithubWinjsWinjs]: https://github.com/winjs/winjs "WinJS/WinJS | GitHub"  
[MicrosoftDeveloperStorePublishApps]: https://developer.microsoft.com/store/publish-apps/index "Публикация приложений и игр для Windows"  
[MicrosoftDeveloperWindowsApps]: https://developer.microsoft.com/windows/apps/index "Документация по универсальной платформе Windows"  
[MicrosoftDeveloperWindowsAppsDesign]: https://developer.microsoft.com/windows/apps/design/index "Проектирование и кодирование приложений для Windows"  
[MicrosoftDeveloperWindowsAppsDevelop]: https://developer.microsoft.com/windows/apps/develop/index "Разработка приложений UWP"  
[MicrosoftDeveloperWindowsAppsGetStarted]: https://developer.microsoft.com/windows/apps/getstarted/index "Начало работы с приложениями для Windows 10"  
[MicrosoftDeveloperWindowsSamples]: https://developer.microsoft.com/windows/samples "Примеры кода"  
[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Предварительная версия DevTools Microsoft Edge"  
[MicrosoftSupportWindowsAppPermissions]: https://support.microsoft.com/help/10557/windows-10-app-permissions "Разрешения для приложений"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Загрузки"  
[MicrosoftVisualStudioPreview]: https://visualstudio.microsoft.com/vs/preview "Предварительная версия Visual Studio"  
[PreviousVSDownloads]: https://visualstudio.microsoft.com/vs/older-downloads/ "Загружаемые файлы для Visual Studio"