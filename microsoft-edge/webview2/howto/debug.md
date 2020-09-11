---
description: Сведения об отладке элементов управления WebView2.
title: Приступая к отладке приложений WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 15171147b847b1d41cd603efed1b8ee42185dc29
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010700"
---
# <span data-ttu-id="54cdb-104">Приступая к отладке приложений WebView2</span><span class="sxs-lookup"><span data-stu-id="54cdb-104">Get started debugging WebView2 applications</span></span>  

<span data-ttu-id="54cdb-105">Цель элемента управления Microsoft Edge WebView2 заключается в том, чтобы сочетать лучший из функций разработки веб-и собственных приложений, а также средств и инструментов.</span><span class="sxs-lookup"><span data-stu-id="54cdb-105">The goal of the Microsoft Edge WebView2 control is to combine the best of both the web and native application development features and tools.</span></span>  <span data-ttu-id="54cdb-106">Когда вы разрабатываете приложение WebView2, необходимо выполнить отладку приложения.</span><span class="sxs-lookup"><span data-stu-id="54cdb-106">When you develop your WebView2 application, you should debug your application.</span></span>  <span data-ttu-id="54cdb-107">В этой статье описаны различные инструменты для отладки вашего веб-и собственного кода в приложении WebView2.</span><span class="sxs-lookup"><span data-stu-id="54cdb-107">This article outlines the different tools to use to debug both your web and native code in your WebView2 application.</span></span>  

## [<span data-ttu-id="54cdb-108">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="54cdb-108">Microsoft Edge DevTools</span></span>](#tab/devtools)  

<span data-ttu-id="54cdb-109">Используйте [средства разработчика Microsoft EDGE (Chromium)][DevtoolsGuideChromiumMain] для отладки содержимого веб-страницы, отображаемого в элементах управления WebView2, таким же образом, как и при отладке на других страницах, отображаемых в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="54cdb-109">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you may debug for another webpage displayed in Microsoft Edge.</span></span>  <span data-ttu-id="54cdb-110">Чтобы открыть DevTools, установите фокус на элементе управления WebView, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="54cdb-110">To open the DevTools, set focus on the WebView control and then use one of the following actions.</span></span>  

*   <span data-ttu-id="54cdb-111">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="54cdb-111">Select `F12`.</span></span>  
*   <span data-ttu-id="54cdb-112">Выберите `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="54cdb-112">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="54cdb-113">Откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите команду `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="54cdb-113">Open the context menu \(right-click\) and choose `Inspect`.</span></span>  

<span data-ttu-id="54cdb-114">Дополнительные сведения можно найти в разделе [Общие сведения о DevTools][DevtoolsGuideChromiumMain].</span><span class="sxs-lookup"><span data-stu-id="54cdb-114">For more information, see [DevTools overview][DevtoolsGuideChromiumMain].</span></span>  

:::image type="complex" source="./media/f12.png" alt-text="Отладка DevTools" lightbox="./media/f12.png":::
   <span data-ttu-id="54cdb-116">Отладка DevTools</span><span class="sxs-lookup"><span data-stu-id="54cdb-116">DevTools debugging</span></span>  
:::image-end:::  

## [<span data-ttu-id="54cdb-117">VisualStudio</span><span class="sxs-lookup"><span data-stu-id="54cdb-117">Visual Studio</span></span>](#tab/visualstudio)  

<span data-ttu-id="54cdb-118">Visual Studio предоставляет различные инструменты отладки для веб-и машинного кода в приложениях WebView2.</span><span class="sxs-lookup"><span data-stu-id="54cdb-118">Visual Studio provides various debugging tools for web and native code in WebView2 applications.</span></span>  <span data-ttu-id="54cdb-119">В разделе Visual Studio главным фокусом является Отладка элементов управления WebView, однако другие методы отладки в Visual Studio можно использовать в обычном режиме.</span><span class="sxs-lookup"><span data-stu-id="54cdb-119">In the Visual Studio section, the primarily focus is debugging WebView controls, however the other methods of debugging in Visual Studio are available as usual.</span></span>  <span data-ttu-id="54cdb-120">Используйте следующий процесс для отладки веб-и машинного кода в приложениях Win32 или только для надстроек Office.</span><span class="sxs-lookup"><span data-stu-id="54cdb-120">Use the following process to debug web and native code in Win32 applications or Office add-ins only.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="54cdb-121">При отладке приложения в Visual Studio с присоединенным отладчиком машинного кода выбор `F12` может инициировать собственный отладчик вместо средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="54cdb-121">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="54cdb-122">`Ctrl` + `Shift` + `I` Чтобы избежать ситуации, выберите или используйте контекстное меню \ (щелкните правой кнопкой мыши).</span><span class="sxs-lookup"><span data-stu-id="54cdb-122">Select `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

<span data-ttu-id="54cdb-123">Прежде чем начать, убедитесь, что выполнены следующие требования.</span><span class="sxs-lookup"><span data-stu-id="54cdb-123">Before you begin, ensure the following requirements are met.</span></span>  

*   <span data-ttu-id="54cdb-124">Для отладки скриптов приложение должно быть запущено в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="54cdb-124">To debug scripts, the app must be launched from within Visual Studio.</span></span>  
*   <span data-ttu-id="54cdb-125">Вы не можете прикрепить отладчик к выполняющемуся процессу WebView2.</span><span class="sxs-lookup"><span data-stu-id="54cdb-125">You cannot attach a debugger to a running WebView2 process.</span></span>  
*   <span data-ttu-id="54cdb-126">Установите Visual Studio 2019 версии 16,4 Preview 2 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="54cdb-126">Install Visual Studio 2019 version 16.4 Preview 2 or later.</span></span>  

<span data-ttu-id="54cdb-127">Установка и настройка средств отладки сценариев в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="54cdb-127">Install and set up the script debugger tools in Visual Studio.</span></span>  

1.  <span data-ttu-id="54cdb-128">Выполните указанные ниже действия, чтобы установить компонент **диагностики JavaScript** в **классических разработках с + +**.</span><span class="sxs-lookup"><span data-stu-id="54cdb-128">Complete the following actions to install the **JavaScript diagnostics** component in **Desktop development with C++**.</span></span>  

    1. <span data-ttu-id="54cdb-129">На панели проводника Windows введите `Visual Studio Installer` .</span><span class="sxs-lookup"><span data-stu-id="54cdb-129">In the Windows Explorer bar, type `Visual Studio Installer`.</span></span>  
    1. <span data-ttu-id="54cdb-130">Щелкните **Установщик Visual Studio** , чтобы открыть его.</span><span class="sxs-lookup"><span data-stu-id="54cdb-130">Choose **Visual Studio Installer** to open it.</span></span>  
    1. <span data-ttu-id="54cdb-131">В установщике Visual Studio на установленной версии нажмите кнопку **Дополнительно** , а затем выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="54cdb-131">In the Visual Studio Installer, on the installed version, choose the **More** button, and then choose **Modify**.</span></span>  
    1. <span data-ttu-id="54cdb-132">В Visual Studio в разделе **рабочие нагрузки**выберите параметр **Разработка классической среды на C++** .</span><span class="sxs-lookup"><span data-stu-id="54cdb-132">In Visual Studio, under **Workloads**, choose the **Desktop Development in C++** setting.</span></span>  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Экран изменения рабочей нагрузки в Visual Studio" lightbox="./media/workloads.png":::
            <span data-ttu-id="54cdb-134">Экран изменения рабочей нагрузки в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54cdb-134">Visual Studio Modifying Workloads Screen</span></span> :::image-end:::  
        
    1.  <span data-ttu-id="54cdb-135">Выберите **отдельные компоненты**.</span><span class="sxs-lookup"><span data-stu-id="54cdb-135">Choose **Individual components**.</span></span>  
    1.  <span data-ttu-id="54cdb-136">В поле поиска введите `JavaScript diagnostics` .</span><span class="sxs-lookup"><span data-stu-id="54cdb-136">In the search box, enter `JavaScript diagnostics`.</span></span>  
    1.  <span data-ttu-id="54cdb-137">Выберите параметр **диагностики JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="54cdb-137">Choose the **JavaScript diagnostics** setting.</span></span>  
    1.  <span data-ttu-id="54cdb-138">Нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="54cdb-138">Choose **Modify**.</span></span> 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Вкладка "изменение отдельных компонентов" в Visual Studio" lightbox="./media/indivcomp.png":::
           <span data-ttu-id="54cdb-140">Вкладка "изменение отдельных компонентов" в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54cdb-140">Visual Studio Modifying Individual Components Tab</span></span>  
        :::image-end:::  
        
1.  <span data-ttu-id="54cdb-141">Включите отладку сценариев для приложений WebView2.</span><span class="sxs-lookup"><span data-stu-id="54cdb-141">Enable script debugging for WebView2 applications.</span></span>  
    1.  <span data-ttu-id="54cdb-142">В проекте WebView2 откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="54cdb-142">In your WebView2 project, open the context menu \(right-click\), and choose **Properties**.</span></span>  
    1.  <span data-ttu-id="54cdb-143">В разделе **Свойства конфигурации**выберите пункт **Отладка**.</span><span class="sxs-lookup"><span data-stu-id="54cdb-143">Under the **Configuration Properties**, choose **Debugging**.</span></span>  
    1.  <span data-ttu-id="54cdb-144">В разделе **Тип отладчика**выберите **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="54cdb-144">Under the **Debugger Type**, choose **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Свойство конфигурации отладки в Visual Studio" lightbox="./media/enbjs.png":::
           <span data-ttu-id="54cdb-146">Свойство конфигурации **отладки** в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54cdb-146">Visual Studio **Debugging** Configuration Property</span></span>  
        :::image-end:::  
        
<span data-ttu-id="54cdb-147">Выполните указанные ниже действия, чтобы выполнить отладку приложения WebView2.</span><span class="sxs-lookup"><span data-stu-id="54cdb-147">Complete the following actions to debug your WebView2 application.</span></span>  

1.  <span data-ttu-id="54cdb-148">Чтобы задать точку останова в исходном коде, наведите указатель мыши на левый номер строки и выберите точку останова.</span><span class="sxs-lookup"><span data-stu-id="54cdb-148">To set a breakpoint in your source code, hover to the left of the line number, and choose to set a breakpoint.</span></span>  <span data-ttu-id="54cdb-149">Адаптеры отладки JS-и ст не выполняют сопоставление исходного пути.</span><span class="sxs-lookup"><span data-stu-id="54cdb-149">The JS/TS debug adapter does not perform source path mapping.</span></span>  <span data-ttu-id="54cdb-150">Вы должны открыть именно тот же путь, связанный с вашим WebView2.</span><span class="sxs-lookup"><span data-stu-id="54cdb-150">You must open the exact same path associated with your WebView2.</span></span>  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Добавление точки останова в Visual Studio" lightbox="./media/breakpoint.png"::: 
       <span data-ttu-id="54cdb-152">Добавление точки останова в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54cdb-152">Visual Studio add breakpoint</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="54cdb-153">Чтобы запустить отладчик, выберите битовый Размер платформы, а затем нажмите зеленую кнопку воспроизведения рядом с **местным отладчиком Windows**.</span><span class="sxs-lookup"><span data-stu-id="54cdb-153">To run the debugger, choose the bit size of the platform, and then choose the green play button next to **Local Windows Debugger**.</span></span>  <span data-ttu-id="54cdb-154">Приложение запустится, и отладчик подключится к первому процессу WebView2, который вы создали.</span><span class="sxs-lookup"><span data-stu-id="54cdb-154">The application runs and the debugger connects to the first WebView2 process that is created.</span></span>  
    
    :::image type="complex" source="./media/run.png" alt-text=" Локальный отладчик Windows для Visual Studio" lightbox="./media/run.png"::: 
       <span data-ttu-id="54cdb-156">**Локальный отладчик Windows** для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54cdb-156">Visual Studio **Local Windows Debugger**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="54cdb-157">В **консоли отладки**найдите выходные данные отладчика.</span><span class="sxs-lookup"><span data-stu-id="54cdb-157">In the **Debug Console**, find the output from the debugger.</span></span>  
    
    :::image type="complex" source="./media/console.png" alt-text=" Консоль отладки Visual Studio" lightbox="./media/console.png"::: 
       <span data-ttu-id="54cdb-159">**Консоль отладки** Visual Studio</span><span class="sxs-lookup"><span data-stu-id="54cdb-159">Visual Studio **Debug Console**</span></span>  
    :::image-end:::  
    
* * *  

## <span data-ttu-id="54cdb-160">Статьи по теме</span><span class="sxs-lookup"><span data-stu-id="54cdb-160">See also</span></span>  

*   <span data-ttu-id="54cdb-161">Чтобы приступить к работе с WebView2, ознакомьтесь со статьей [руководства Приступая к работе с WebView2][Webview2MainGettingStarted].</span><span class="sxs-lookup"><span data-stu-id="54cdb-161">To get started using WebView2, see [WebView2 Getting Started Guides][Webview2MainGettingStarted].</span></span>  
*   <span data-ttu-id="54cdb-162">Полный пример возможностей WebView2 можно найти в репозитории [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.</span><span class="sxs-lookup"><span data-stu-id="54cdb-162">For a comprehensive example of WebView2 capabilities, see the [WebView2Samples][GithubMicrosoftedgeWebview2samples] repo on GitHub.</span></span>
*   <span data-ttu-id="54cdb-163">Более подробную информацию об API WebView2 можно найти в [справочнике API][Webview2ApiReference].</span><span class="sxs-lookup"><span data-stu-id="54cdb-163">For more detailed information about WebView2 APIs, see [API reference][Webview2ApiReference].</span></span>
*   <span data-ttu-id="54cdb-164">Дополнительные сведения о WebView2ах можно найти в статьях [ресурсы WebView2][Webview2MainNextSteps].</span><span class="sxs-lookup"><span data-stu-id="54cdb-164">For more information about WebView2, see [WebView2 Resources][Webview2MainNextSteps].</span></span>

## <span data-ttu-id="54cdb-165">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="54cdb-165">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium)"  

[Webview2ReferenceDotnet09628MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-628/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "Класс AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions | Документы Microsoft"  
[Webview2ReferenceWin3209622Webview2IdlParameters]: ../reference/win32/0-9-622/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Документы Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности -Отладчик JavaScript для Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-Debugger (код Visual Studio) — отладчик для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
