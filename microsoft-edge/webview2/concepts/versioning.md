---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 3862576134d1179fb24b2ce865f705b2bf1db8a6
ms.sourcegitcommit: de171a8e7ccd9f23846f3cd06519e4a0104f1c52
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757608"
---
# <span data-ttu-id="c3467-104">Общие сведения о версиях SDK для WebView2</span><span class="sxs-lookup"><span data-stu-id="c3467-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="c3467-105">WebView2 зависит от Microsoft Edge для функционирования.</span><span class="sxs-lookup"><span data-stu-id="c3467-105">WebView2 depends on Microsoft Edge to function.</span></span> <span data-ttu-id="c3467-106">Для каждого WebView2 SDK требуется, чтобы была установлена минимальная версия браузера.</span><span class="sxs-lookup"><span data-stu-id="c3467-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="c3467-107">Минимальная версия отражается в версии пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="c3467-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="c3467-108">Например, если вы используете этот параметр `SDK package version 0.9.488` , необходимо установить Microsoft Edge с номером сборки 488 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="c3467-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span> <span data-ttu-id="c3467-109">Версия браузера также указывается в [заметках о выпуске][Webview2Releasenotes]WebView2.</span><span class="sxs-lookup"><span data-stu-id="c3467-109">The browser version is also specified in the WebView2 [Release Notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="c3467-110">Дополнительные сведения о последних выпусках браузера можно найти в разделе [каналы браузера][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="c3467-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="c3467-111">WebView2 в настоящее время является предварительной версией.</span><span class="sxs-lookup"><span data-stu-id="c3467-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="c3467-112">Несмотря на то, что группа Microsoft Edge WebView гарантирует обратную совместимость между версиями браузеров и пакетами SDK, это не гарантирует, что некоторые более поздние версии браузера могут не поддерживать старые версии SDK.</span><span class="sxs-lookup"><span data-stu-id="c3467-112">While, the Microsoft Edge WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed as some newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="c3467-113">Если между версиями браузеров и пакетами SDK есть коренные изменения, группа Microsoft Edge WebView указывает изменения в [заметках о выпуске][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="c3467-113">If there are breaking changes between browser versions and SDKs, the Microsoft Edge WebView team specifies the changes in the [release notes][Webview2Releasenotes].</span></span>  

<span data-ttu-id="c3467-114">В будущем модель распределения для WebView2 приложений изменится.</span><span class="sxs-lookup"><span data-stu-id="c3467-114">In the future, the distribution model for WebView2 applications will change.</span></span> <span data-ttu-id="c3467-115">Дополнительные сведения можно найти в разделе [Среда выполнения WebView2][Webview2IndexEdgeRuntime].</span><span class="sxs-lookup"><span data-stu-id="c3467-115">For more information, see [WebView2 Runtime][Webview2IndexEdgeRuntime].</span></span>  
 
## <span data-ttu-id="c3467-116">Пакет для выпуска и предварительной версии</span><span class="sxs-lookup"><span data-stu-id="c3467-116">Release and pre-release package</span></span>  

<span data-ttu-id="c3467-117">В предварительной версии пакет выпусков включает указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="c3467-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="c3467-118">[API C/C++ для Win32][Webview2ReferenceWin3209538]: API в SDK, которые должны оставаться прежними.</span><span class="sxs-lookup"><span data-stu-id="c3467-118">[Win32 C/C++ APIs][Webview2ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span> 

<span data-ttu-id="c3467-119">В предварительной версии пакет предварительной версии включает указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="c3467-119">In preview, the pre-release package contains the following.</span></span>  

*   <span data-ttu-id="c3467-120">API-интерфейсы .NET: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515]и [ядро][Webview2ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="c3467-120">.NET APIs: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515], and [Core][Webview2ReferenceDotnet09538]</span></span>
*   <span data-ttu-id="c3467-121">Экспериментальные API.</span><span class="sxs-lookup"><span data-stu-id="c3467-121">Experimental APIs.</span></span>  <span data-ttu-id="c3467-122">Дополнительные сведения можно найти в разделе [API Experimantal](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="c3467-122">For more information, see the [Experimantal APIs](#experimental-apis) section.</span></span>  

### <span data-ttu-id="c3467-123">Экспериментальные API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="c3467-123">Experimental APIs</span></span>  

<span data-ttu-id="c3467-124">Группа WebView тестирует API-интерфейсы, которые представляют собой будущие функции, названные экспериментальными API.</span><span class="sxs-lookup"><span data-stu-id="c3467-124">The WebView Team is testing APIs that represent future functionality named Experimental APIs.</span></span>  <span data-ttu-id="c3467-125">Экспериментальные API-интерфейсы помечены как `experimental` в SDK.</span><span class="sxs-lookup"><span data-stu-id="c3467-125">The Experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="c3467-126">Некоторые экспериментальные API-интерфейсы могут поставляться в пакете выпуска как полностью стабильные API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="c3467-126">Some Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="c3467-127">Вы должны ожидать, что все экспериментальные API будут изменяться перед выпуском.</span><span class="sxs-lookup"><span data-stu-id="c3467-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="c3467-128">Пожалуйста, оцените экспериментальные API-интерфейсы и поделитесь отзывами с помощью [WebViewа обратной связи][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="c3467-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="c3467-129">Старайтесь не использовать экспериментальные API в производственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="c3467-129">Avoid using the experimental APIs in production applications.</span></span>  

### <span data-ttu-id="c3467-130">Стратегия</span><span class="sxs-lookup"><span data-stu-id="c3467-130">Roadmap</span></span>  

<span data-ttu-id="c3467-131">После того как WebView2 пойдет в устойчивое общее доступное состояние, пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++ и .NET.</span><span class="sxs-lookup"><span data-stu-id="c3467-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="c3467-132">Пакет предварительной версии включает экспериментальные API-интерфейсы, которые изменяются на основе отзывов и общих аналитических приложений.</span><span class="sxs-lookup"><span data-stu-id="c3467-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--links -->

[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2-распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Webview2ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Webview2ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
