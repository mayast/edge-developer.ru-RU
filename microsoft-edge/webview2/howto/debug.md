---
description: Сведения об отладке элементов управления WebView2.
title: Отладка WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888588"
---
# <span data-ttu-id="123ba-104">Отладка с помощью WebView2</span><span class="sxs-lookup"><span data-stu-id="123ba-104">How to Debug with WebView2</span></span>  

<span data-ttu-id="123ba-105">Цель элемента управления Microsoft Edge WebView2 — объединение лучшей из функций разработки веб-приложений и собственного приложения, а также средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="123ba-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="123ba-106">На следующей странице описаны различные инструменты для разработки с помощью элементов управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="123ba-106">The following page outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="123ba-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="123ba-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="123ba-108">Используйте [средства разработчика Microsoft EDGE (Chromium)][DevtoolsMain] для отладки веб-содержимого, отображаемого в элементах управления WebView2, таким же образом, как и при использовании Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="123ba-108">Use [Microsoft Edge (Chromium) Developer Tools][DevtoolsMain] to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="123ba-109">Чтобы открыть DevTools, установите фокус в окне WebView, а затем выполните одно из указанных ниже действий.</span><span class="sxs-lookup"><span data-stu-id="123ba-109">To open the DevTools, set focus on the WebView window and then use any of the following actions.</span></span>  

*   <span data-ttu-id="123ba-110">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="123ba-110">Select `F12`.</span></span>  
*   <span data-ttu-id="123ba-111">Выберите `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="123ba-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="123ba-112">Откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите команду `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="123ba-112">Open the context menu \(right-click\) and select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   <span data-ttu-id="123ba-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="123ba-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!IMPORTANT]
> <span data-ttu-id="123ba-115">При отладке приложения в Visual Studio с присоединенным отладчиком машинного кода выбор `F12` может инициировать собственный отладчик вместо средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="123ba-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="123ba-116">Использование `Ctrl` + `Shift` + `I` или использование контекстного меню \ (щелкните правой кнопкой мыши, чтобы избежать ситуации).</span><span class="sxs-lookup"><span data-stu-id="123ba-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid the situation.</span></span>  

## <span data-ttu-id="123ba-117">VisualStudio</span><span class="sxs-lookup"><span data-stu-id="123ba-117">Visual Studio</span></span>  

<span data-ttu-id="123ba-118">Вы можете использовать Visual Studio для одновременной разработки кода приложения и сценариев отладки.</span><span class="sxs-lookup"><span data-stu-id="123ba-118">You may use Visual Studio to develop application code and debug scripts at the same time.</span></span>  

<span data-ttu-id="123ba-119">Учитывайте указанные ниже моменты.</span><span class="sxs-lookup"><span data-stu-id="123ba-119">Keep the following things in mind.</span></span>  

*   <span data-ttu-id="123ba-120">Visual Studio поддерживает сценарии отладки только при запуске приложения в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="123ba-120">Visual Studio only supports debugging scripts when the app is launched from within Visual Studio.</span></span>  <span data-ttu-id="123ba-121">\ (Подключение запущенного процесса для отладки не поддерживается. \)</span><span class="sxs-lookup"><span data-stu-id="123ba-121">\(Attaching a running process for debugging is not supported.\)</span></span>  
*   <span data-ttu-id="123ba-122">Конечный сценарий отладки WebView не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="123ba-122">The targeted WebView debugging scenario is not supported.</span></span>  

<span data-ttu-id="123ba-123">Используйте отладчик сценариев в Visual Studio 2019 версии 16,4 Preview 2 и более поздних версий для отладки сценария в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="123ba-123">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  

<span data-ttu-id="123ba-124">Настройте отладчик.</span><span class="sxs-lookup"><span data-stu-id="123ba-124">Set up the debugger.</span></span>  

*   <span data-ttu-id="123ba-125">Убедитесь, что компонент **диагностики JavaScript** установлен на **рабочем столе с** рабочей нагрузкой C++.</span><span class="sxs-lookup"><span data-stu-id="123ba-125">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  
    
    1.  <span data-ttu-id="123ba-126">Перейдите в раздел **приложения & параметры компонентов** в Windows.</span><span class="sxs-lookup"><span data-stu-id="123ba-126">Navigate to **Apps & features** settings in Windows.</span></span>  <span data-ttu-id="123ba-127">Найдите его с помощью панели задач Windows.</span><span class="sxs-lookup"><span data-stu-id="123ba-127">Search for it using the Windows task bar.</span></span>  
    1.  <span data-ttu-id="123ba-128">Нажмите кнопку **изменить**.</span><span class="sxs-lookup"><span data-stu-id="123ba-128">Choose **Modify**.</span></span>  
    1.  <span data-ttu-id="123ba-129">Убедитесь, что выбраны флажки **Диагностика** и **Разработка классической среды на C++** .</span><span class="sxs-lookup"><span data-stu-id="123ba-129">Verify the **Javascript diagnostics** and **Desktop Development in C++** checkboxes are selected.</span></span>  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Приложения и компоненты" lightbox="../media/appsandfeatures.png":::
           <span data-ttu-id="123ba-131">Приложения и компоненты</span><span class="sxs-lookup"><span data-stu-id="123ba-131">Apps & Features</span></span>  
        :::image-end:::  
        
*   <span data-ttu-id="123ba-132">Включите отладку сценариев WebView2.</span><span class="sxs-lookup"><span data-stu-id="123ba-132">Enable WebView2 script debugging.</span></span>  
    1.  <span data-ttu-id="123ba-133">Наведите указатель мыши на проект, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="123ba-133">Hover on your project, open the context menu \(right-click\), and select **Properties**.</span></span>  
    1.  <span data-ttu-id="123ba-134">На вкладке **Свойства конфигурации**выберите пункт **Отладка**.</span><span class="sxs-lookup"><span data-stu-id="123ba-134">On **Configuration Properties**, select **Debugging**.</span></span>  
    1.  <span data-ttu-id="123ba-135">В свойстве **Тип отладчика** выполните поиск в списке параметров и выберите **JavaScript (WebView2)**.</span><span class="sxs-lookup"><span data-stu-id="123ba-135">On the **Debugger Type** property, search the the list of options, and select **JavaScript (WebView2)**.</span></span>  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Отладчик JavaScript для Visual Studio" lightbox="../media/enbjs.png":::
           <span data-ttu-id="123ba-137">Отладчик JavaScript для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="123ba-137">Visual Studio JavaScript Debugger</span></span>  
        :::image-end:::  
        
<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="123ba-138">Все настроено и готово к отладке.</span><span class="sxs-lookup"><span data-stu-id="123ba-138">You are all set up and ready to debug.</span></span>  

<span data-ttu-id="123ba-139">Чтобы выполнить отладку, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="123ba-139">To Debug, complete the following actions.</span></span>  

1.  <span data-ttu-id="123ba-140">Установка точек останова</span><span class="sxs-lookup"><span data-stu-id="123ba-140">Set Breakpoints</span></span>  
    *   <span data-ttu-id="123ba-141">Откройте файл сценария и установите точку останова в нужном месте.</span><span class="sxs-lookup"><span data-stu-id="123ba-141">Open the script file and set the breakpoint where you want it.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="123ba-142">Адаптеры отладки JS/TS не выполняют сопоставление исходного пути.</span><span class="sxs-lookup"><span data-stu-id="123ba-142">The JS/TS debug adapter does not do source path mapping.</span></span><span data-ttu-id="123ba-143">Вы должны открыть именно тот же путь, связанный с вашим WebView2.</span><span class="sxs-lookup"><span data-stu-id="123ba-143">  You must open the exact same path associated with your WebView2.</span></span>  
        
1.  <span data-ttu-id="123ba-144">Выполнение кода</span><span class="sxs-lookup"><span data-stu-id="123ba-144">Run Code</span></span>  
    *   <span data-ttu-id="123ba-145">Выберите соответствующую версию сборки и среду выполнения, а затем запустите локальный отладчик Windows.</span><span class="sxs-lookup"><span data-stu-id="123ba-145">Select your appropriate build flavor and runtime environment and then start the local windows debugger.</span></span>  
1.  <span data-ttu-id="123ba-146">Просмотр консоли отладки</span><span class="sxs-lookup"><span data-stu-id="123ba-146">View Debug Console</span></span>  
    *   <span data-ttu-id="123ba-147">Вы запускаете приложение, и отладчик подключается после создания первого webview2.</span><span class="sxs-lookup"><span data-stu-id="123ba-147">You application runs and the debugger connects after the first webview2 is created.</span></span><span data-ttu-id="123ba-148">На экране появятся все ожидающие результаты отладки.</span><span class="sxs-lookup"><span data-stu-id="123ba-148">  Any pending debug output is displayed.</span></span>  
        
        > [!NOTE]
        > <span data-ttu-id="123ba-149">Этот метод отладки в настоящее время ограничен приложениями Win32 и надстройками Office.</span><span class="sxs-lookup"><span data-stu-id="123ba-149">This method of debugging is currently restricted to Win32 applications and Office add-ins.</span></span>  
        
## <span data-ttu-id="123ba-150">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="123ba-150">Visual Studio Code</span></span>  

<span data-ttu-id="123ba-151">Код Visual Studio можно использовать для отладки сценариев, которые выполняются в элементах управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="123ba-151">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="123ba-152">Дополнительные сведения можно найти в разделе [приложения Microsoft EDGE (Chromium) WebView][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span><span class="sxs-lookup"><span data-stu-id="123ba-152">For more information, see [Microsoft Edge (Chromium) WebView Applications][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="123ba-153">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="123ba-153">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="123ba-154">Помогите вам создать более WebView2ную работу, отправив свой отзыв.</span><span class="sxs-lookup"><span data-stu-id="123ba-154">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="123ba-155">Чтобы отправить запросы на функции или отчеты об ошибках, посетите [репозиторий обратной связи][GithubMicrosoftedgeWebviewfeedback] .</span><span class="sxs-lookup"><span data-stu-id="123ba-155">Visit the [feedback repo][GithubMicrosoftedgeWebviewfeedback] to submit feature requests or bug reports.</span></span>  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-VS-Debugger для Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
