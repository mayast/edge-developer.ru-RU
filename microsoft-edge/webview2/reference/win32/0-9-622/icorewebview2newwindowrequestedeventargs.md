---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: d1cf39fe71c4b00f10a14da8a65428eb24daa71f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012516"
---
# <span data-ttu-id="cb760-104">интерфейс ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="cb760-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="cb760-105">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="cb760-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="cb760-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="cb760-106">Summary</span></span>

 <span data-ttu-id="cb760-107">Участников</span><span class="sxs-lookup"><span data-stu-id="cb760-107">Members</span></span>                        | <span data-ttu-id="cb760-108">Описания</span><span class="sxs-lookup"><span data-stu-id="cb760-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cb760-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="cb760-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="cb760-110">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="cb760-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="cb760-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="cb760-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="cb760-112">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="cb760-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="cb760-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="cb760-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="cb760-114">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="cb760-114">Gets the new window.</span></span>
[<span data-ttu-id="cb760-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="cb760-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="cb760-116">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="cb760-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="cb760-117">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="cb760-117">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="cb760-118">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="cb760-118">Window features specified by the window.open call.</span></span>
[<span data-ttu-id="cb760-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cb760-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="cb760-120">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="cb760-120">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="cb760-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="cb760-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="cb760-122">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="cb760-122">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="cb760-123">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="cb760-123">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="cb760-124">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="cb760-124">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="cb760-125">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="cb760-125">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="cb760-126">Участников</span><span class="sxs-lookup"><span data-stu-id="cb760-126">Members</span></span>

#### <span data-ttu-id="cb760-127">get_Handled</span><span class="sxs-lookup"><span data-stu-id="cb760-127">get_Handled</span></span> 

<span data-ttu-id="cb760-128">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="cb760-128">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="cb760-129">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="cb760-129">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="cb760-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="cb760-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="cb760-131">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="cb760-131">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="cb760-132">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="cb760-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="cb760-133">Заблокированный блочный блок "Edge" отключен для WebView, поэтому приложение может использовать этот флаг, чтобы заблокировать всплывающие окна, не инициированные пользователем.</span><span class="sxs-lookup"><span data-stu-id="cb760-133">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="cb760-134">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="cb760-134">get_NewWindow</span></span> 

<span data-ttu-id="cb760-135">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="cb760-135">Gets the new window.</span></span>

> <span data-ttu-id="cb760-136">общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="cb760-136">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="cb760-137">get_Uri</span><span class="sxs-lookup"><span data-stu-id="cb760-137">get_Uri</span></span> 

<span data-ttu-id="cb760-138">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="cb760-138">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="cb760-139">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="cb760-139">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="cb760-140">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="cb760-140">get_WindowFeatures</span></span> 

<span data-ttu-id="cb760-141">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="cb760-141">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="cb760-142">общедоступные значения HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2WindowFeatures](icorewebview2windowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="cb760-142">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2WindowFeatures](icorewebview2windowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="cb760-143">Эти функции можно учитывать при размещении и изменении размера новых окон WebView.</span><span class="sxs-lookup"><span data-stu-id="cb760-143">These features can be considered for positioning and sizing of new webview windows.</span></span>

#### <span data-ttu-id="cb760-144">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="cb760-144">GetDeferral</span></span> 

<span data-ttu-id="cb760-145">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="cb760-145">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="cb760-146">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="cb760-146">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="cb760-147">Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) , чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="cb760-147">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="cb760-148">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="cb760-148">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="cb760-149">put_Handled</span><span class="sxs-lookup"><span data-stu-id="cb760-149">put_Handled</span></span> 

<span data-ttu-id="cb760-150">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="cb760-150">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="cb760-151">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="cb760-151">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="cb760-152">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="cb760-152">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="cb760-153">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="cb760-153">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="cb760-154">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="cb760-154">Default is false.</span></span>

#### <span data-ttu-id="cb760-155">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="cb760-155">put_NewWindow</span></span> 

<span data-ttu-id="cb760-156">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="cb760-156">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="cb760-157">общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="cb760-157">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="cb760-158">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="cb760-158">The target WebView should not be navigated.</span></span> <span data-ttu-id="cb760-159">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="cb760-159">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

