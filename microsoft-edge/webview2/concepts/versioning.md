---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: acf3103f39d33586ee0614aeb0f10de0ab71c89a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894314"
---
# <span data-ttu-id="0a487-104">Общие сведения о версиях SDK для WebView2</span><span class="sxs-lookup"><span data-stu-id="0a487-104">Understand WebView2 SDK versions</span></span>  

<span data-ttu-id="0a487-105">WebView2 зависит от Microsoft Edge для функционирования.</span><span class="sxs-lookup"><span data-stu-id="0a487-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="0a487-106">Для каждого WebView2 SDK требуется, чтобы была установлена минимальная версия браузера.</span><span class="sxs-lookup"><span data-stu-id="0a487-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="0a487-107">Минимальная версия отражается в версии пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="0a487-107">The minimum version is reflected in the package version of the SDK.</span></span>  <span data-ttu-id="0a487-108">Например, если вы используете этот параметр `SDK package version 0.9.488` , необходимо установить Microsoft Edge с номером сборки 488 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="0a487-108">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="0a487-109">Версия браузера также указывается в [заметках о выпуске][Releasenotes]WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a487-109">The browser version is also specified in the WebView2 [Release Notes][Releasenotes].</span></span>  <span data-ttu-id="0a487-110">Дополнительные сведения о последних выпусках браузера можно найти в разделе [каналы браузера][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="0a487-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="0a487-111">WebView2 в настоящее время является предварительной версией.</span><span class="sxs-lookup"><span data-stu-id="0a487-111">WebView2 is currently in preview.</span></span>  <span data-ttu-id="0a487-112">Несмотря на то, что группа WebView стремится обеспечить обратную совместимость между версиями браузеров и пакетами SDK, она не гарантируется, так как более поздние версии браузера могут не поддерживать предыдущие версии SDK.</span><span class="sxs-lookup"><span data-stu-id="0a487-112">While the WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed because newer versions of the browser may not support previous SDK versions.</span></span>  <span data-ttu-id="0a487-113">Если между версиями браузеров и пакетами SDK есть коренные изменения, мы указываем изменения в [заметках о выпуске][Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="0a487-113">If there are breaking changes between browser versions and SDKs, we specify the changes in the [Release Notes][Releasenotes].</span></span>  

<span data-ttu-id="0a487-114">В будущем мы планируем изменить модель распределения для приложений WebView2.</span><span class="sxs-lookup"><span data-stu-id="0a487-114">In the future, we plan to change the distribution model for WebView2 applications.</span></span>  <span data-ttu-id="0a487-115">Дополнительные сведения можно найти в разделе [Режим распространения Evergreen][DistributionEvergreenMode].</span><span class="sxs-lookup"><span data-stu-id="0a487-115">For more information, see [Evergreen distribution mode][DistributionEvergreenMode].</span></span>  
 
## <span data-ttu-id="0a487-116">Пакет для выпуска и предварительной версии</span><span class="sxs-lookup"><span data-stu-id="0a487-116">Release and pre-release package</span></span>  

<span data-ttu-id="0a487-117">В предварительной версии пакет выпусков включает указанные ниже.</span><span class="sxs-lookup"><span data-stu-id="0a487-117">In preview, the release package contains the following.</span></span>  

*   <span data-ttu-id="0a487-118">[API C/C++ для Win32][ReferenceWin3209538]: API в SDK, которые должны оставаться прежними.</span><span class="sxs-lookup"><span data-stu-id="0a487-118">[Win32 C/C++ APIs][ReferenceWin3209538]: APIs in the SDK that are expected to remain the same at GA.</span></span>  

<span data-ttu-id="0a487-119">В предварительной версии пакет предварительной версии включает следующие компоненты:</span><span class="sxs-lookup"><span data-stu-id="0a487-119">In preview, the pre-release package contains the following components.</span></span>  

*   <span data-ttu-id="0a487-120">API-интерфейсы .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]и [ядро][ReferenceDotnet09538]</span><span class="sxs-lookup"><span data-stu-id="0a487-120">.NET APIs: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515], and [Core][ReferenceDotnet09538]</span></span>  
*   <span data-ttu-id="0a487-121">Экспериментальные API.</span><span class="sxs-lookup"><span data-stu-id="0a487-121">Experimental APIs.</span></span>  <span data-ttu-id="0a487-122">Дополнительные сведения можно найти в разделе [экспериментальные API-интерфейсы](#experimental-apis) .</span><span class="sxs-lookup"><span data-stu-id="0a487-122">For more information, see the [Experimental APIs](#experimental-apis) section.</span></span>  

## <span data-ttu-id="0a487-123">Экспериментальные API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="0a487-123">Experimental APIs</span></span>  

<span data-ttu-id="0a487-124">Мы тестируем экспериментальные API, которые могут представлять будущие функции.</span><span class="sxs-lookup"><span data-stu-id="0a487-124">We are testing experimental APIs that may represent future functionality.</span></span>  <span data-ttu-id="0a487-125">Экспериментальные API-интерфейсы помечены как `experimental` в SDK.</span><span class="sxs-lookup"><span data-stu-id="0a487-125">The experimental APIs are marked as `experimental` in the SDK.</span></span>  <span data-ttu-id="0a487-126">Экспериментальные API-интерфейсы могут поставляться в пакете выпуска как полностью стабильные API-интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="0a487-126">Experimental APIs may ship as fully stable APIs in the release package.</span></span>  <span data-ttu-id="0a487-127">Вы должны ожидать, что все экспериментальные API будут изменяться перед выпуском.</span><span class="sxs-lookup"><span data-stu-id="0a487-127">You should expect all experimental APIs to change before release.</span></span>  <span data-ttu-id="0a487-128">Пожалуйста, оцените экспериментальные API-интерфейсы и поделитесь отзывами с помощью [WebViewа обратной связи][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="0a487-128">Please evaluate the Experimental APIs and share feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>   

> [!CAUTION]
> <span data-ttu-id="0a487-129">Старайтесь не использовать экспериментальные API в производственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="0a487-129">Avoid using the experimental APIs in production applications.</span></span>  

## <span data-ttu-id="0a487-130">Стратегия</span><span class="sxs-lookup"><span data-stu-id="0a487-130">Roadmap</span></span>  

<span data-ttu-id="0a487-131">После того как WebView2 пойдет в устойчивое общее доступное состояние, пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++ и .NET.</span><span class="sxs-lookup"><span data-stu-id="0a487-131">After WebView2 reaches a stable general available state, the release package contains all of the stable, supported Win32 C/C++ and .NET APIs.</span></span>  <span data-ttu-id="0a487-132">Пакет предварительной версии включает экспериментальные API-интерфейсы, которые изменяются на основе отзывов и общих аналитических приложений.</span><span class="sxs-lookup"><span data-stu-id="0a487-132">The pre-release package contains experimental APIs that are subject to change based upon developer feedback and shared insights.</span></span>  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Режим распространения Evergreen — распространение приложений с помощью WebView2 | Документы Microsoft"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
