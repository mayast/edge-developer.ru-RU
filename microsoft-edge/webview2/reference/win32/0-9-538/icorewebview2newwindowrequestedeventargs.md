---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: af8df8ff67a0fbe7fd4ec9308b1562b9ef987933
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699287"
---
# <span data-ttu-id="f2138-104">интерфейс ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f2138-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="f2138-105">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f2138-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="f2138-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f2138-106">Summary</span></span>

 <span data-ttu-id="f2138-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f2138-107">Members</span></span>                        | <span data-ttu-id="f2138-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f2138-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f2138-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="f2138-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="f2138-110">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="f2138-110">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="f2138-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f2138-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="f2138-112">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="f2138-112">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="f2138-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f2138-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="f2138-114">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="f2138-114">Gets the new window.</span></span>
[<span data-ttu-id="f2138-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f2138-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="f2138-116">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f2138-116">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="f2138-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f2138-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f2138-118">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="f2138-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="f2138-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="f2138-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="f2138-120">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="f2138-120">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="f2138-121">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f2138-121">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="f2138-122">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f2138-122">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="f2138-123">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f2138-123">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="f2138-124">Участников</span><span class="sxs-lookup"><span data-stu-id="f2138-124">Members</span></span>

#### <span data-ttu-id="f2138-125">get_Handled</span><span class="sxs-lookup"><span data-stu-id="f2138-125">get_Handled</span></span> 

<span data-ttu-id="f2138-126">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="f2138-126">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="f2138-127">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="f2138-127">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="f2138-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f2138-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="f2138-129">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="f2138-129">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="f2138-130">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="f2138-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="f2138-131">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f2138-131">get_NewWindow</span></span> 

<span data-ttu-id="f2138-132">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="f2138-132">Gets the new window.</span></span>

> <span data-ttu-id="f2138-133">общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="f2138-133">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="f2138-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f2138-134">get_Uri</span></span> 

<span data-ttu-id="f2138-135">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f2138-135">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="f2138-136">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="f2138-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="f2138-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f2138-137">GetDeferral</span></span> 

<span data-ttu-id="f2138-138">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="f2138-138">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="f2138-139">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="f2138-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="f2138-140">Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) , чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="f2138-140">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="f2138-141">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="f2138-141">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="f2138-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="f2138-142">put_Handled</span></span> 

<span data-ttu-id="f2138-143">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="f2138-143">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="f2138-144">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="f2138-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="f2138-145">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="f2138-145">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="f2138-146">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="f2138-146">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="f2138-147">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="f2138-147">Default is false.</span></span>

#### <span data-ttu-id="f2138-148">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="f2138-148">put_NewWindow</span></span> 

<span data-ttu-id="f2138-149">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="f2138-149">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="f2138-150">общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="f2138-150">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="f2138-151">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="f2138-151">The target webview should not be navigated.</span></span> <span data-ttu-id="f2138-152">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="f2138-152">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

