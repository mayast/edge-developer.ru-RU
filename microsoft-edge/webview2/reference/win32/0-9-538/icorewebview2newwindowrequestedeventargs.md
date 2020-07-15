---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NewWindowRequestedEventArgs
ms.openlocfilehash: bb18b6662fd5921406e19b3c333c97f8a1cd0dbc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879438"
---
# <span data-ttu-id="4614a-104">интерфейс ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4614a-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="4614a-105">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="4614a-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="4614a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4614a-106">Summary</span></span>

 <span data-ttu-id="4614a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="4614a-107">Members</span></span>                        | <span data-ttu-id="4614a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="4614a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4614a-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="4614a-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="4614a-110">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="4614a-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="4614a-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4614a-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="4614a-112">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="4614a-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="4614a-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="4614a-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="4614a-114">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="4614a-114">Gets the new window.</span></span>
[<span data-ttu-id="4614a-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4614a-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="4614a-116">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="4614a-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="4614a-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4614a-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4614a-118">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="4614a-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="4614a-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="4614a-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="4614a-120">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="4614a-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="4614a-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="4614a-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="4614a-122">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="4614a-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="4614a-123">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="4614a-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="4614a-124">Участников</span><span class="sxs-lookup"><span data-stu-id="4614a-124">Members</span></span>

#### <span data-ttu-id="4614a-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="4614a-125">get_Handled</span></span> 

<span data-ttu-id="4614a-126">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="4614a-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="4614a-127">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="4614a-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="4614a-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="4614a-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="4614a-129">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="4614a-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="4614a-130">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="4614a-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="4614a-131">Заблокированный блочный блок "Edge" отключен для WebView, поэтому приложение может использовать этот флаг, чтобы заблокировать всплывающие окна, не инициированные пользователем.</span><span class="sxs-lookup"><span data-stu-id="4614a-131">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="4614a-132">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="4614a-132">get_NewWindow</span></span> 

<span data-ttu-id="4614a-133">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="4614a-133">Gets the new window.</span></span>

> <span data-ttu-id="4614a-134">общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="4614a-134">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="4614a-135">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4614a-135">get_Uri</span></span> 

<span data-ttu-id="4614a-136">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="4614a-136">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="4614a-137">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="4614a-137">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="4614a-138">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4614a-138">GetDeferral</span></span> 

<span data-ttu-id="4614a-139">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="4614a-139">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="4614a-140">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="4614a-140">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="4614a-141">Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) , чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="4614a-141">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="4614a-142">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="4614a-142">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="4614a-143">put_Handled</span><span class="sxs-lookup"><span data-stu-id="4614a-143">put_Handled</span></span> 

<span data-ttu-id="4614a-144">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="4614a-144">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="4614a-145">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="4614a-145">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="4614a-146">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="4614a-146">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="4614a-147">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="4614a-147">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="4614a-148">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="4614a-148">Default is false.</span></span>

#### <span data-ttu-id="4614a-149">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="4614a-149">put_NewWindow</span></span> 

<span data-ttu-id="4614a-150">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="4614a-150">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="4614a-151">общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="4614a-151">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="4614a-152">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="4614a-152">The target webview should not be navigated.</span></span> <span data-ttu-id="4614a-153">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="4614a-153">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

