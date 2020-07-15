---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 798c3ce0a3eeddad651668124d6a263d0672a391
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877842"
---
# <span data-ttu-id="2a639-104">0.9.430-Interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2a639-104">0.9.430 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="2a639-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="2a639-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="2a639-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="2a639-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="2a639-107">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="2a639-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="2a639-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2a639-108">Summary</span></span>

 <span data-ttu-id="2a639-109">Участников</span><span class="sxs-lookup"><span data-stu-id="2a639-109">Members</span></span>                        | <span data-ttu-id="2a639-110">Описания</span><span class="sxs-lookup"><span data-stu-id="2a639-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2a639-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2a639-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2a639-112">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="2a639-112">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="2a639-113">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="2a639-113">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="2a639-114">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="2a639-114">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="2a639-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="2a639-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="2a639-116">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="2a639-116">Gets the new window.</span></span>
[<span data-ttu-id="2a639-117">put_Handled</span><span class="sxs-lookup"><span data-stu-id="2a639-117">put_Handled</span></span>](#put_handled) | <span data-ttu-id="2a639-118">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="2a639-118">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="2a639-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="2a639-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="2a639-120">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="2a639-120">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="2a639-121">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2a639-121">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="2a639-122">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="2a639-122">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="2a639-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2a639-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2a639-124">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="2a639-124">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="2a639-125">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (через Window. Open () и т. д.)</span><span class="sxs-lookup"><span data-stu-id="2a639-125">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="2a639-126">Участников</span><span class="sxs-lookup"><span data-stu-id="2a639-126">Members</span></span>

#### <span data-ttu-id="2a639-127">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2a639-127">get_Uri</span></span> 

<span data-ttu-id="2a639-128">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="2a639-128">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="2a639-129">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2a639-129">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2a639-130">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="2a639-130">put_NewWindow</span></span> 

<span data-ttu-id="2a639-131">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="2a639-131">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="2a639-132">общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="2a639-132">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* newWindow)</span></span>

<span data-ttu-id="2a639-133">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="2a639-133">The target webview should not be navigated.</span></span> <span data-ttu-id="2a639-134">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="2a639-134">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="2a639-135">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="2a639-135">get_NewWindow</span></span> 

<span data-ttu-id="2a639-136">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="2a639-136">Gets the new window.</span></span>

> <span data-ttu-id="2a639-137">общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="2a639-137">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="2a639-138">put_Handled</span><span class="sxs-lookup"><span data-stu-id="2a639-138">put_Handled</span></span> 

<span data-ttu-id="2a639-139">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="2a639-139">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="2a639-140">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="2a639-140">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="2a639-141">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="2a639-141">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="2a639-142">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="2a639-142">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="2a639-143">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="2a639-143">Default is false.</span></span>

#### <span data-ttu-id="2a639-144">get_Handled</span><span class="sxs-lookup"><span data-stu-id="2a639-144">get_Handled</span></span> 

<span data-ttu-id="2a639-145">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="2a639-145">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="2a639-146">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="2a639-146">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="2a639-147">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2a639-147">get_IsUserInitiated</span></span> 

<span data-ttu-id="2a639-148">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="2a639-148">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="2a639-149">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="2a639-149">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="2a639-150">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2a639-150">GetDeferral</span></span> 

<span data-ttu-id="2a639-151">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="2a639-151">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="2a639-152">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="2a639-152">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2a639-153">Вы можете использовать объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) , чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="2a639-153">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="2a639-154">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="2a639-154">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

