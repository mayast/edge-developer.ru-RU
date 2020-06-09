---
description: Сведения об отладке элементов управления WebView2.
title: Отладка WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 7e3ee11de443713a14684023fcd90de3cb1d265a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697751"
---
# <span data-ttu-id="20d99-104">Отладка при разработке с помощью элементов управления WebView2</span><span class="sxs-lookup"><span data-stu-id="20d99-104">How to debug when developing with WebView2 controls</span></span>  

<span data-ttu-id="20d99-105">Цель элемента управления Microsoft Edge WebView2 — объединение лучшей из функций разработки веб-приложений и собственного приложения, а также средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="20d99-105">The goal of the Microsoft Edge WebView2 control is combining the best of both the web and native application development features and developer tools.</span></span>  <span data-ttu-id="20d99-106">В этой статье описываются различные инструменты, которые следует использовать при разработке с помощью элементов управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="20d99-106">This article outlines the different tools to use when developing with WebView2 controls.</span></span>  

## <span data-ttu-id="20d99-107">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="20d99-107">Microsoft Edge DevTools</span></span>  

<span data-ttu-id="20d99-108">Используйте [средства разработчика Microsoft EDGE (Chromium)](/microsoft-edge/devtools-guide-chromium) для отладки веб-содержимого, отображаемого в элементах управления WebView2, таким же образом, как и при использовании Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="20d99-108">Use [Microsoft Edge (Chromium) Developer Tools](/microsoft-edge/devtools-guide-chromium) to debug web content displayed in WebView2 controls, in the same way that you would if you were using Microsoft Edge.</span></span>  <span data-ttu-id="20d99-109">Чтобы открыть DevTools, установите фокус в окне WebView и воспользуйтесь одним из указанных ниже способов.</span><span class="sxs-lookup"><span data-stu-id="20d99-109">To open the DevTools, set focus on the WebView window and then use any of the following options.</span></span>  
*   <span data-ttu-id="20d99-110">Выберите `F12` .</span><span class="sxs-lookup"><span data-stu-id="20d99-110">Select `F12`.</span></span>  
*   <span data-ttu-id="20d99-111">Выберите `Ctrl` + `Shift` + `I` .</span><span class="sxs-lookup"><span data-stu-id="20d99-111">Select `Ctrl`+`Shift`+`I`.</span></span>  
*   <span data-ttu-id="20d99-112">Откройте контекстное меню \ (щелкните правой кнопкой мыши, > выбрать `Inspect` .</span><span class="sxs-lookup"><span data-stu-id="20d99-112">Open the context menu \(right-click\) > select `Inspect`.</span></span>  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools":::
   <span data-ttu-id="20d99-114">Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="20d99-114">Microsoft Edge DevTools</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="20d99-115">При отладке приложения в Visual Studio с присоединенным отладчиком машинного кода выбор `F12` может инициировать собственный отладчик вместо средств разработчика.</span><span class="sxs-lookup"><span data-stu-id="20d99-115">When you debug your application in Visual Studio with the native debugger attached, selecting `F12` may trigger the native debugger instead of Developer Tools.</span></span>  <span data-ttu-id="20d99-116">Использование `Ctrl` + `Shift` + `I` или использование контекстного меню \ (щелкните правой кнопкой мыши, чтобы избежать такой ситуации).</span><span class="sxs-lookup"><span data-stu-id="20d99-116">Use `Ctrl`+`Shift`+`I`, or use the context menu \(right-click\) to avoid this situation.</span></span>  

## <span data-ttu-id="20d99-117">VisualStudio</span><span class="sxs-lookup"><span data-stu-id="20d99-117">Visual Studio</span></span>  

<span data-ttu-id="20d99-118">Используйте отладчик сценариев в Visual Studio 2019 версии 16,4 Preview 2 и более поздних версий для отладки сценария в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="20d99-118">Use the script debugger in Visual Studio 2019 version 16.4 Preview 2 or later to debug your script in Visual Studio.</span></span>  <span data-ttu-id="20d99-119">Убедитесь, что компонент **диагностики JavaScript** установлен на **рабочем столе с** рабочей нагрузкой C++.</span><span class="sxs-lookup"><span data-stu-id="20d99-119">Verify the **JavaScript diagnostics** component in **Desktop development with C++** workload is installed.</span></span>  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Диагностика JavaScript в Visual Studio":::
   <span data-ttu-id="20d99-121">Диагностика JavaScript в Visual Studio</span><span class="sxs-lookup"><span data-stu-id="20d99-121">Visual Studio JavaScript diagnostics</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

<span data-ttu-id="20d99-122">Чтобы включить отладку сценариев WebView2, откройте контекстное меню в проекте, а затем щелкните правой кнопкой мыши > выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="20d99-122">To enable WebView2 script debugging, open the context menu \(right-click\) on your project > select **Properties**.</span></span>  <span data-ttu-id="20d99-123">На вкладке **Свойства конфигурации**выберите пункт **Отладка**.</span><span class="sxs-lookup"><span data-stu-id="20d99-123">On **Configuration Properties**, select **Debugging**.</span></span>  <span data-ttu-id="20d99-124">В свойстве **Type Debugger (тип отладчика** **) выберите JavaScript (WebView2)** в списке параметров.</span><span class="sxs-lookup"><span data-stu-id="20d99-124">On the **Debugger Type** property, choose **JavaScript (WebView2)** from the list of options.</span></span> 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Отладчик JavaScript для Visual Studio":::
   <span data-ttu-id="20d99-126">Отладчик JavaScript для Visual Studio</span><span class="sxs-lookup"><span data-stu-id="20d99-126">Visual Studio JavaScript Debugger</span></span>  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## <span data-ttu-id="20d99-127">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="20d99-127">Visual Studio Code</span></span>  

<span data-ttu-id="20d99-128">Код Visual Studio можно использовать для отладки сценариев, которые выполняются в элементах управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="20d99-128">You may use Visual Studio Code to debug scripts that run in WebView2 controls.</span></span>  <span data-ttu-id="20d99-129">Дополнительные сведения можно найти в разделе [приложения Microsoft EDGE (Chromium) WebView](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span><span class="sxs-lookup"><span data-stu-id="20d99-129">For more information, see [Microsoft Edge (Chromium) WebView Applications](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).</span></span>  

<!--todo:  add See also heading  -->  

## <span data-ttu-id="20d99-130">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="20d99-130">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="20d99-131">Помогите вам создать более WebView2ную работу, отправив свой отзыв.</span><span class="sxs-lookup"><span data-stu-id="20d99-131">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="20d99-132">Чтобы отправить запросы на функции или отчеты об ошибках, посетите [репозиторий обратной связи](https://aka.ms/webviewfeedback) .</span><span class="sxs-lookup"><span data-stu-id="20d99-132">Visit the [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>  
