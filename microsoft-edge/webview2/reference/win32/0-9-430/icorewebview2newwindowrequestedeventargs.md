---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 73f62e7130d50028b527353c6ba1a238f694dcda
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885683"
---
# <span data-ttu-id="d7d78-104">0.9.430-Interface ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="d7d78-104">0.9.430 - interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="d7d78-105">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="d7d78-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="d7d78-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d7d78-106">Summary</span></span>

 <span data-ttu-id="d7d78-107">Участников</span><span class="sxs-lookup"><span data-stu-id="d7d78-107">Members</span></span>                        | <span data-ttu-id="d7d78-108">Описания</span><span class="sxs-lookup"><span data-stu-id="d7d78-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d7d78-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="d7d78-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="d7d78-110">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d7d78-110">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="d7d78-111">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="d7d78-111">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="d7d78-112">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d7d78-112">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="d7d78-113">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="d7d78-113">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="d7d78-114">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="d7d78-114">Gets the new window.</span></span>
[<span data-ttu-id="d7d78-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d7d78-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="d7d78-116">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="d7d78-116">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="d7d78-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d7d78-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="d7d78-118">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="d7d78-118">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="d7d78-119">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d7d78-119">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="d7d78-120">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="d7d78-120">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="d7d78-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d7d78-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="d7d78-122">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="d7d78-122">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="d7d78-123">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (через Window. Open () и т. д.)</span><span class="sxs-lookup"><span data-stu-id="d7d78-123">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="d7d78-124">Участников</span><span class="sxs-lookup"><span data-stu-id="d7d78-124">Members</span></span>

#### <span data-ttu-id="d7d78-125">get_Uri</span><span class="sxs-lookup"><span data-stu-id="d7d78-125">get_Uri</span></span> 

<span data-ttu-id="d7d78-126">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d7d78-126">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="d7d78-127">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="d7d78-127">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="d7d78-128">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="d7d78-128">put_NewWindow</span></span> 

<span data-ttu-id="d7d78-129">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="d7d78-129">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="d7d78-130">общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="d7d78-130">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* newWindow)</span></span>

<span data-ttu-id="d7d78-131">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="d7d78-131">The target webview should not be navigated.</span></span> <span data-ttu-id="d7d78-132">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="d7d78-132">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="d7d78-133">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="d7d78-133">get_NewWindow</span></span> 

<span data-ttu-id="d7d78-134">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="d7d78-134">Gets the new window.</span></span>

> <span data-ttu-id="d7d78-135">общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="d7d78-135">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="d7d78-136">put_Handled</span><span class="sxs-lookup"><span data-stu-id="d7d78-136">put_Handled</span></span> 

<span data-ttu-id="d7d78-137">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="d7d78-137">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="d7d78-138">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="d7d78-138">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="d7d78-139">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="d7d78-139">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="d7d78-140">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="d7d78-140">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="d7d78-141">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="d7d78-141">Default is false.</span></span>

#### <span data-ttu-id="d7d78-142">get_Handled</span><span class="sxs-lookup"><span data-stu-id="d7d78-142">get_Handled</span></span> 

<span data-ttu-id="d7d78-143">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="d7d78-143">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="d7d78-144">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="d7d78-144">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="d7d78-145">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="d7d78-145">get_IsUserInitiated</span></span> 

<span data-ttu-id="d7d78-146">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="d7d78-146">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="d7d78-147">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="d7d78-147">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="d7d78-148">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="d7d78-148">GetDeferral</span></span> 

<span data-ttu-id="d7d78-149">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="d7d78-149">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="d7d78-150">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="d7d78-150">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="d7d78-151">Вы можете использовать объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) , чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="d7d78-151">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="d7d78-152">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="d7d78-152">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

