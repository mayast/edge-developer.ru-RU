---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: cc924a146057a3c8c578ccea187e1dd63dedcbe6
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697219"
---
# <span data-ttu-id="65f65-104">Сведения о версиях браузеров и WebView2</span><span class="sxs-lookup"><span data-stu-id="65f65-104">Understanding browser versions and WebView2</span></span>  

<span data-ttu-id="65f65-105">WebView2 зависит от Microsoft Edge для функционирования.</span><span class="sxs-lookup"><span data-stu-id="65f65-105">WebView2 depends on Microsoft Edge to function.</span></span>  <span data-ttu-id="65f65-106">Для каждого WebView2 SDK требуется, чтобы была установлена минимальная версия браузера.</span><span class="sxs-lookup"><span data-stu-id="65f65-106">Each WebView2 SDK requires that a minimum browser version is installed.</span></span>  <span data-ttu-id="65f65-107">Эта версия браузера указана в [заметках о выпуске][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="65f65-107">This browser version is specified in our [Release Notes][Webview2Releasenotes].</span></span>  <span data-ttu-id="65f65-108">Минимальная версия может отображаться в версии пакета SDK.</span><span class="sxs-lookup"><span data-stu-id="65f65-108">You may see the minimum version reflected in the package version of the SDK.</span></span>  <span data-ttu-id="65f65-109">Например, если вы используете этот параметр `SDK package version 0.9.488` , необходимо установить Microsoft Edge с номером сборки 488 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="65f65-109">For example, if you use the `SDK package version 0.9.488`, then you must install Microsoft Edge with a build number of 488 or later.</span></span>  <span data-ttu-id="65f65-110">Дополнительные сведения о последних выпусках браузера можно найти в разделе [каналы браузера][DeployedgeChannels].</span><span class="sxs-lookup"><span data-stu-id="65f65-110">For more information on the latest releases of the browser, see [Browser Channels][DeployedgeChannels].</span></span>  

> [!NOTE]
> <span data-ttu-id="65f65-111">WebView2 в настоящее время является предварительной версией.</span><span class="sxs-lookup"><span data-stu-id="65f65-111">WebView2 is currently in Preview.</span></span>  <span data-ttu-id="65f65-112">Несмотря на то, что группа Microsoft Edge WebView гарантирует обратную совместимость между версиями браузеров и пакетами SDK, это не гарантирует, что некоторые более поздние версии браузера могут не поддерживать старые версии SDK.</span><span class="sxs-lookup"><span data-stu-id="65f65-112">While, the Microsoft Edge WebView team strives to ensure backward compatibility between browser versions and SDKs, it is not guaranteed as some newer versions of the browser may not support older SDK versions.</span></span>  <span data-ttu-id="65f65-113">Если между версиями браузеров и пакетами SDK есть коренные изменения, группа Microsoft Edge WebView указывает изменения в [заметках о выпуске][Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="65f65-113">If there are breaking changes between browser versions and SDKs, the Microsoft Edge WebView team indicates the changes in the [release notes][Webview2Releasenotes].</span></span>  

<span data-ttu-id="65f65-114">В будущем группа Microsoft Edge WebViews планирует изменить модель распространения.</span><span class="sxs-lookup"><span data-stu-id="65f65-114">In the future, the Microsoft Edge WebView team plans to change the distribution model.</span></span>  <span data-ttu-id="65f65-115">Microsoft Edge WebView Teams, чтобы удалить прямую зависимость в браузере Microsoft Edge из WebView2.</span><span class="sxs-lookup"><span data-stu-id="65f65-115">The Microsoft Edge WebView team plans to remove the direct dependency on the Microsoft Edge browser from WebView2.</span></span>  <span data-ttu-id="65f65-116">Дополнительные сведения можно найти в разделе [распространение][Webview2Distibution] [среды выполнения WebView2][Webview2IndexEdgeRuntime] .</span><span class="sxs-lookup"><span data-stu-id="65f65-116">To learn more, see [WebView2 Runtime][Webview2IndexEdgeRuntime] in the [Distribution][Webview2Distibution] section.</span></span>  

## <span data-ttu-id="65f65-117">Экспериментальные API-интерфейсы</span><span class="sxs-lookup"><span data-stu-id="65f65-117">Experimental APIs</span></span>  

<span data-ttu-id="65f65-118">Несмотря на то, что WebView2 является предварительным просмотром, для API в пакете SDK должны оставаться одинаковыми.</span><span class="sxs-lookup"><span data-stu-id="65f65-118">While WebView2 is a preview, the APIs in the SDK are expected to remain the same at GA.</span></span>  <span data-ttu-id="65f65-119">В пакет SDK включены [экспериментальные API][Webview2ReferenceWin3209538Experimental] .</span><span class="sxs-lookup"><span data-stu-id="65f65-119">There are [experimental APIs][Webview2ReferenceWin3209538Experimental] included in the SDK.</span></span>  <span data-ttu-id="65f65-120">Пожалуйста, оцените экспериментальные API-интерфейсы и отправьте отзыв с помощью [репозитория обратной связи WebView][GithubMicrosoftedgeWebviewfeedback].</span><span class="sxs-lookup"><span data-stu-id="65f65-120">Please evaluate the experimental APIs and send your feedback using the [WebView feedback repo][GithubMicrosoftedgeWebviewfeedback].</span></span>  

### <span data-ttu-id="65f65-121">Стратегия</span><span class="sxs-lookup"><span data-stu-id="65f65-121">Roadmap</span></span>  

<span data-ttu-id="65f65-122">После того как WebView2 пойдет в устойчивое общее состояние, и мы выпустим пакет 1.0.0 SDK, планы Microsoft Edge WebView Teams, чтобы переместить все экспериментальные API в предварительную версию пакета.</span><span class="sxs-lookup"><span data-stu-id="65f65-122">After WebView2 reaches a stable general available state and we release the 1.0.0 SDK, the Microsoft Edge WebView team plans to move all experimental APIs to a pre-release package.</span></span>  <span data-ttu-id="65f65-123">Предварительная версия пакета продолжает разрешать отзыв и сведения о новейших функциях, в то время как в стабильном выпуске поддерживается обратная совместимость.</span><span class="sxs-lookup"><span data-stu-id="65f65-123">The pre-release package continues to allow for feedback and insight into the latest features, while the stable release version maintains backward compatibility.</span></span>  

<!--links -->

[Webview2Distibution]: ./distribution.md "Распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2-распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ReferenceWin3209538Experimental]: ../reference/win32/0-9-538-reference-webview2.md#experimental "Экспериментальный справочник (WebView2) | Документы Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
