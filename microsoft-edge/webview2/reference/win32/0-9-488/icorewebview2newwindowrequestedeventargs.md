---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d99c05026257116dd5c6c7119325e00227d9a6d0
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697814"
---
# <span data-ttu-id="52da3-104">интерфейс ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="52da3-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="52da3-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="52da3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="52da3-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="52da3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="52da3-107">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="52da3-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="52da3-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="52da3-108">Summary</span></span>

 <span data-ttu-id="52da3-109">Участников</span><span class="sxs-lookup"><span data-stu-id="52da3-109">Members</span></span>                        | <span data-ttu-id="52da3-110">Описания</span><span class="sxs-lookup"><span data-stu-id="52da3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="52da3-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="52da3-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="52da3-112">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="52da3-112">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="52da3-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="52da3-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="52da3-114">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="52da3-114">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="52da3-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="52da3-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="52da3-116">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="52da3-116">Gets the new window.</span></span>
[<span data-ttu-id="52da3-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="52da3-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="52da3-118">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="52da3-118">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="52da3-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="52da3-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="52da3-120">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="52da3-120">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="52da3-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="52da3-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="52da3-122">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="52da3-122">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="52da3-123">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="52da3-123">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="52da3-124">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="52da3-124">Sets a WebView as a result of the NewWindowRequest.</span></span>

<span data-ttu-id="52da3-125">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="52da3-125">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="52da3-126">Участников</span><span class="sxs-lookup"><span data-stu-id="52da3-126">Members</span></span>

#### <span data-ttu-id="52da3-127">get_Handled</span><span class="sxs-lookup"><span data-stu-id="52da3-127">get_Handled</span></span> 

<span data-ttu-id="52da3-128">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="52da3-128">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="52da3-129">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="52da3-129">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="52da3-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="52da3-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="52da3-131">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="52da3-131">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="52da3-132">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="52da3-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="52da3-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="52da3-133">get_NewWindow</span></span> 

<span data-ttu-id="52da3-134">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="52da3-134">Gets the new window.</span></span>

> <span data-ttu-id="52da3-135">общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="52da3-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](icorewebview2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="52da3-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="52da3-136">get_Uri</span></span> 

<span data-ttu-id="52da3-137">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="52da3-137">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="52da3-138">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="52da3-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="52da3-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="52da3-139">GetDeferral</span></span> 

<span data-ttu-id="52da3-140">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="52da3-140">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="52da3-141">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="52da3-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="52da3-142">Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) , чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="52da3-142">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="52da3-143">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="52da3-143">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

#### <span data-ttu-id="52da3-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="52da3-144">put_Handled</span></span> 

<span data-ttu-id="52da3-145">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="52da3-145">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="52da3-146">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="52da3-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="52da3-147">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="52da3-147">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="52da3-148">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="52da3-148">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="52da3-149">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="52da3-149">Default is false.</span></span>

#### <span data-ttu-id="52da3-150">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="52da3-150">put_NewWindow</span></span> 

<span data-ttu-id="52da3-151">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="52da3-151">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="52da3-152">общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="52da3-152">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](icorewebview2.md) \* newWindow)</span></span>

<span data-ttu-id="52da3-153">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="52da3-153">The target webview should not be navigated.</span></span> <span data-ttu-id="52da3-154">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="52da3-154">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

