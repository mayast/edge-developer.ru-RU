---
description: Навигация
title: Навигация
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 0df8e12acb11824006515ac711250d776d276e36
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895580"
---
# <span data-ttu-id="e917e-104">События навигации</span><span class="sxs-lookup"><span data-stu-id="e917e-104">Navigation events</span></span>  

<span data-ttu-id="e917e-105">Нормальная последовательность событий навигации:,,,, `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` и затем `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="e917e-105">The normal sequence of navigation events is `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span>  <span data-ttu-id="e917e-106">Следующие события описывают состояние WebView2 во время каждой навигации.</span><span class="sxs-lookup"><span data-stu-id="e917e-106">The following events describe the state of WebView2 during each navigation.</span></span>  

| <span data-ttu-id="e917e-107">Sequence</span><span class="sxs-lookup"><span data-stu-id="e917e-107">Sequence</span></span> | <span data-ttu-id="e917e-108">Имя события</span><span class="sxs-lookup"><span data-stu-id="e917e-108">Event name</span></span> | <span data-ttu-id="e917e-109">Сведения</span><span class="sxs-lookup"><span data-stu-id="e917e-109">Details</span></span> |  
|:--- |:--- |:--- |  
| <span data-ttu-id="e917e-110">1,1</span><span class="sxs-lookup"><span data-stu-id="e917e-110">1</span></span> | `NavigationStarting`  |  <span data-ttu-id="e917e-111">WebView2 запускает навигацию и навигацию, что приводит к выполнению сетевого запроса.</span><span class="sxs-lookup"><span data-stu-id="e917e-111">WebView2 starts to navigate and the navigation results in a network request.</span></span>  <span data-ttu-id="e917e-112">Ведущее приложение может запретить запрос во время события.</span><span class="sxs-lookup"><span data-stu-id="e917e-112">The host is able to disallow the request during the event.</span></span>  |  
| <span data-ttu-id="e917e-113">2</span><span class="sxs-lookup"><span data-stu-id="e917e-113">2</span></span> | `SourceChanged`  |  <span data-ttu-id="e917e-114">Источник изменений WebView2 меняется на новый URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="e917e-114">The source of WebView2 changes to a new URL.</span></span>  <span data-ttu-id="e917e-115">Это событие может быть вызвано навигацией, которая не является причиной сетевого запроса, например Навигация по фрагменту.</span><span class="sxs-lookup"><span data-stu-id="e917e-115">The event may result from a navigation that does not cause a network request such as a fragment navigation.</span></span>  |  
| <span data-ttu-id="e917e-116">Трехконтактный</span><span class="sxs-lookup"><span data-stu-id="e917e-116">3</span></span> | `HistoryChanged`  |  <span data-ttu-id="e917e-117">История обновлений WebView2 в результате навигации.</span><span class="sxs-lookup"><span data-stu-id="e917e-117">The history of WebView2 updates as a result of the navigation.</span></span>  |  
| <span data-ttu-id="e917e-118">четырехпроцессорном</span><span class="sxs-lookup"><span data-stu-id="e917e-118">4</span></span> | `ContentLoading`  |  <span data-ttu-id="e917e-119">WebView загружает содержимое для новой страницы.</span><span class="sxs-lookup"><span data-stu-id="e917e-119">WebView starts loading content for the new page.</span></span>  |  
| <span data-ttu-id="e917e-120">5</span><span class="sxs-lookup"><span data-stu-id="e917e-120">5</span></span> | `NavigationCompleted`  |  <span data-ttu-id="e917e-121">WebView2 завершает загрузку содержимого на новой странице.</span><span class="sxs-lookup"><span data-stu-id="e917e-121">WebView2 completes loading content on the new page.</span></span>  |  

<span data-ttu-id="e917e-122">Отслеживайте `navigations` каждый новый документ с помощью идентификатора навигации \ ( `NavigationId` \).</span><span class="sxs-lookup"><span data-stu-id="e917e-122">Track `navigations` to each new document using the navigation ID \(`NavigationId`\).</span></span>  <span data-ttu-id="e917e-123">`NavigationId`WebView меняется каждый раз при успешном переходе на новый документ.</span><span class="sxs-lookup"><span data-stu-id="e917e-123">The `NavigationId` of WebView changes every time there is a successful navigation to a new document.</span></span>

:::image type="complex" source="../media/navigation-graph.png" alt-text="События навигации Microsoft Edge WebView2" lightbox="../media/navigation-graph.png":::
   <span data-ttu-id="e917e-125">События навигации Microsoft Edge WebView2</span><span class="sxs-lookup"><span data-stu-id="e917e-125">The Microsoft Edge WebView2 Navigation Events</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="e917e-126">Предыдущий рисунок представляет события навигации с тем же `NavigationId` свойством для соответствующего события arg.</span><span class="sxs-lookup"><span data-stu-id="e917e-126">The previous figure represents navigation events with the same `NavigationId` property on the respective event arg.</span></span>  

 `Navigations` <span data-ttu-id="e917e-127">события с разными экземплярами `NavigationId` события могут перекрываться.</span><span class="sxs-lookup"><span data-stu-id="e917e-127">events with different instances of `NavigationId` event may overlap.</span></span>  <span data-ttu-id="e917e-128">Например, при запуске навигации необходимо дождаться связанного `NavigationStarting` события.</span><span class="sxs-lookup"><span data-stu-id="e917e-128">For instance when you start a navigation, you have to wait for the related `NavigationStarting` event.</span></span>  <span data-ttu-id="e917e-129">Если затем вы запустите другую навигацию, вы увидите `NavigationStarting` событие для первого перехода, за которым следует событие `NavigationStarting` для первой навигации, затем событие, `NavigationCompleted` а затем все остальные события навигации для второй навигации.</span><span class="sxs-lookup"><span data-stu-id="e917e-129">If you then start another navigation, you should see the `NavigationStarting` event for the first navigate followed by the `NavigationStarting` event for the second navigate, followed by the `NavigationCompleted` event for the first navigation and then all the rest of the appropriate navigation events for the second navigation.</span></span>  
 
 <span data-ttu-id="e917e-130">В случае ошибок может возникнуть или не быть `ContentLoading` событием в зависимости от того, продолжает ли переход страница ошибки.</span><span class="sxs-lookup"><span data-stu-id="e917e-130">In error cases there may or may not be a `ContentLoading` event depending on whether the navigation is continued to an error page.</span></span>  
 
 <span data-ttu-id="e917e-131">В случае переадресации HTTP `NavigationStarting` в строке есть несколько событий, в которых для последующего события `IsRedirect` задано свойство, но оно остается прежним `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="e917e-131">In the case of an HTTP redirect, there are multiple `NavigationStarting` events in a row, where subsequent event args have the `IsRedirect` property set, however the `NavigationId` remains the same.</span></span>  
 
 <span data-ttu-id="e917e-132">Тот же документ `navigations` , например переход к фрагменту, не приводит к `NavigationStarting` событию, и его нельзя увеличить `NavigationId` .</span><span class="sxs-lookup"><span data-stu-id="e917e-132">Same document `navigations`, such as navigating to a fragment, do not result in the `NavigationStarting` event and do not increment the `NavigationId`.</span></span>  

<span data-ttu-id="e917e-133">Для контроля и отмены `navigations` внутри подкадров в WebView используйте `FrameNavigationStarting` события and, `FrameNavigationCompleted` которые действуют так же, как эквивалентные события, не связанные с кадрами.</span><span class="sxs-lookup"><span data-stu-id="e917e-133">To monitor or cancel `navigations` inside subframes in the WebView, use the `FrameNavigationStarting` and the `FrameNavigationCompleted` events which act just like the equivalent non-frame counterpart events.</span></span>  

<!-- links -->  
