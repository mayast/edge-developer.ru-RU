---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 03c943c87f07344ab4e3d1a7c707a993a795cdba
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751851"
---
# <span data-ttu-id="8c5f0-104">интерфейс ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8c5f0-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="8c5f0-105">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="8c5f0-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8c5f0-106">Summary</span></span>

 <span data-ttu-id="8c5f0-107">Участников</span><span class="sxs-lookup"><span data-stu-id="8c5f0-107">Members</span></span>                        | <span data-ttu-id="8c5f0-108">Описания</span><span class="sxs-lookup"><span data-stu-id="8c5f0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8c5f0-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="8c5f0-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="8c5f0-110">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="8c5f0-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="8c5f0-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="8c5f0-112">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="8c5f0-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="8c5f0-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="8c5f0-114">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-114">Gets the new window.</span></span>
[<span data-ttu-id="8c5f0-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8c5f0-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="8c5f0-116">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="8c5f0-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8c5f0-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="8c5f0-118">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="8c5f0-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="8c5f0-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="8c5f0-120">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="8c5f0-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="8c5f0-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="8c5f0-122">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="8c5f0-123">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="8c5f0-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="8c5f0-124">Участников</span><span class="sxs-lookup"><span data-stu-id="8c5f0-124">Members</span></span>

#### <span data-ttu-id="8c5f0-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="8c5f0-125">get_Handled</span></span> 

<span data-ttu-id="8c5f0-126">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="8c5f0-127">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="8c5f0-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="8c5f0-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="8c5f0-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="8c5f0-129">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="8c5f0-130">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="8c5f0-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="8c5f0-131">Элементы управления WebView2 могут отображать всплывающие окна, так как блокирование всплывающих окон отключено.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-131">WebView2 controls may display pop-up windows because the Pop-Up blocker is turned off.</span></span> <span data-ttu-id="8c5f0-132">Чтобы заблокировать отображение всплывающих окон, не инициированных пользователем, используйте `get_IsUserInitiated` .</span><span class="sxs-lookup"><span data-stu-id="8c5f0-132">To block non-user initiated pop-up windows from being displayed, use `get_IsUserInitiated`.</span></span>

#### <span data-ttu-id="8c5f0-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="8c5f0-133">get_NewWindow</span></span> 

<span data-ttu-id="8c5f0-134">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-134">Gets the new window.</span></span>

> <span data-ttu-id="8c5f0-135">общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="8c5f0-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="8c5f0-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="8c5f0-136">get_Uri</span></span> 

<span data-ttu-id="8c5f0-137">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-137">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="8c5f0-138">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="8c5f0-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="8c5f0-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8c5f0-139">GetDeferral</span></span> 

<span data-ttu-id="8c5f0-140">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-140">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="8c5f0-141">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="8c5f0-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="8c5f0-142">Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) , чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-142">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="8c5f0-143">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-143">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="8c5f0-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="8c5f0-144">put_Handled</span></span> 

<span data-ttu-id="8c5f0-145">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-145">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="8c5f0-146">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="8c5f0-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="8c5f0-147">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-147">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="8c5f0-148">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-148">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="8c5f0-149">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-149">Default is false.</span></span>

#### <span data-ttu-id="8c5f0-150">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="8c5f0-150">put_NewWindow</span></span> 

<span data-ttu-id="8c5f0-151">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-151">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="8c5f0-152">общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="8c5f0-152">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="8c5f0-153">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-153">The target webview should not be navigated.</span></span> <span data-ttu-id="8c5f0-154">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="8c5f0-154">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>
