---
description: Сведения об отладке элементов управления WebView2.
title: Отладка WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6b2cc65e5cb368c29efec2eb3638f0c1772000d9
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926479"
---
# <span data-ttu-id="70324-104">Отладка с помощью WebView2</span><span class="sxs-lookup"><span data-stu-id="70324-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="70324-105">Цель элемента управления Microsoft Edge WebView2 — объединение лучшей из функций разработки веб-приложений и собственного приложения, а также средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="70324-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="70324-106">На следующей странице описаны различные инструменты для разработки с помощью элементов управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="70324-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="70324-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="70324-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="70324-108">Используйте [средства разработчика Microsoft EDGE (Chromium)][DevtoolsGuideChromiumMain] для отладки веб-содержимого, отображаемого в элементах управления WebView2, таким же образом, как и при использовании Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="70324-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsGuideChromiumMain] to debug web content displayed in WebView2 controls, in the same way that you use Microsoft Edge.</span></span>  <span data-ttu-id="70324-109">Чтобы открыть DevTools, установите фокус в окне WebView, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="70324-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  
*   <span data-ttu-id="70324-110">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="70324-110">Select `F12`.</span></span>  
*   <span data-ttu-id="70324-111">Выберите `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="70324-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="70324-112">Откройте контекстное меню \ (щелкните правой кнопкой мыши, > выбрать `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="70324-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   <span data-ttu-id="70324-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="70324-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="70324-115">При отладке приложения в Visual Studio с прикрепленным отладчиком машинного кода `F12` вместо средств разработчика может возникнуть нажатие клавиш отладчика машинного кода.</span><span class="sxs-lookup"><span data-stu-id="70324-115">When you debug your application in Visual Studio with the native debugger attached, pressing `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="70324-116">`Ctrl` + `Shift` + `I` Чтобы избежать такой ситуации, нажмите или используйте контекстное меню (щелкните правой кнопкой мыши).</span><span class="sxs-lookup"><span data-stu-id="70324-116">Press `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

> [!NOTE]
> <span data-ttu-id="70324-117">Вы можете использовать `--auto-open-devtools-for-tabs` аргумент командной строки, чтобы открыть новое окно DevTools при первом создании WebView.</span><span class="sxs-lookup"><span data-stu-id="70324-117">You may use the `--auto-open-devtools-for-tabs` command-line argument to open a new DevTools window when you first create a WebView.</span></span>  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## <span data-ttu-id="70324-118">VisualStudio</span><span class="sxs-lookup"><span data-stu-id="70324-118">Visual Studio</span></span>  

<span data-ttu-id="70324-119">Используйте отладчик сценариев в Visual Studio 2019 версии 16,4 Preview 2 и более поздних версий для отладки сценария в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="70324-119">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="70324-120">Убедитесь, что компонент **диагностики JavaScript** установлен на **рабочем столе с** рабочей нагрузкой C++.</span><span class="sxs-lookup"><span data-stu-id="70324-120">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Диагностика JavaScript в Visual Studio":::
   <span data-ttu-id="70324-122">Диагностика JavaScript в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="70324-122">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="70324-123">Чтобы включить отладку сценариев WebView2, откройте контекстное меню в проекте, а затем щелкните правой кнопкой мыши > выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="70324-123">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  

*   <span data-ttu-id="70324-124">На вкладке **Свойства конфигурации**выберите пункт **Отладка**.</span><span class="sxs-lookup"><span data-stu-id="70324-124">On **Configuration Properties**, select **Debugging**.</span></span>  
*   <span data-ttu-id="70324-125">В свойстве **Type Debugger (тип отладчика** **) выберите JavaScript (WebView2)** в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="70324-125">On the **Debugger Type** property, select **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Отладчик JavaScript для Visual Studio":::
   <span data-ttu-id="70324-127">Отладчик JavaScript для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="70324-127">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="70324-128">Все настроено и готово к отладке.</span><span class="sxs-lookup"><span data-stu-id="70324-128">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="70324-129">Чтобы выполнить отладку, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="70324-129">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="70324-130">Установка точек останова</span><span class="sxs-lookup"><span data-stu-id="70324-130">Set Breakpoints</span></span>  
    *   <span data-ttu-id="70324-131">Откройте файл сценария и установите точку останова в нужном месте.</span><span class="sxs-lookup"><span data-stu-id="70324-131">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="70324-132">Адаптеры отладки JS/TS не выполняют сопоставление исходного пути.</span><span class="sxs-lookup"><span data-stu-id="70324-132">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="70324-133">Вы должны открыть именно тот же путь, связанный с вашим WebView2.</span><span class="sxs-lookup"><span data-stu-id="70324-133">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="70324-134">Выполнение кода</span><span class="sxs-lookup"><span data-stu-id="70324-134">Run Code</span></span>  
    *   <span data-ttu-id="70324-135">Выберите соответствующую версию сборки и среду выполнения, а затем запустите локальный отладчик Windows.</span><span class="sxs-lookup"><span data-stu-id="70324-135">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="70324-136">Просмотр консоли отладки</span><span class="sxs-lookup"><span data-stu-id="70324-136">View Debug Console</span></span>  
    *   <span data-ttu-id="70324-137">Вы запускаете приложение, и отладчик подключается после создания первого webview2.</span><span class="sxs-lookup"><span data-stu-id="70324-137">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="70324-138">На экране появятся все ожидающие результаты отладки.</span><span class="sxs-lookup"><span data-stu-id="70324-138">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="70324-139">Этот метод отладки в настоящее время ограничен приложениями Win32 и надстройками Office.</span><span class="sxs-lookup"><span data-stu-id="70324-139">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="70324-140">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="70324-140">Visual Studio Code</span></span>  

<span data-ttu-id="70324-141">Код Visual Studio можно использовать для отладки сценариев, которые выполняются в элементах управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="70324-141">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="70324-142">Дополнительные сведения можно найти в разделе [приложения Microsoft EDGE (Chromium) WebView][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="70324-142">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="70324-143">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="70324-143">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium)"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-VS-Debugger для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
