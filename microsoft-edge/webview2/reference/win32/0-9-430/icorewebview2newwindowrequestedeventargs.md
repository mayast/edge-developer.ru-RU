---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2ea3500c5e230b543f75241c47c58163276942da
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654855"
---
# <span data-ttu-id="7e3b2-104">интерфейс ICoreWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7e3b2-104">interface ICoreWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7e3b2-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7e3b2-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="7e3b2-107">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="7e3b2-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7e3b2-108">Summary</span></span>

 <span data-ttu-id="7e3b2-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7e3b2-109">Members</span></span>                        | <span data-ttu-id="7e3b2-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7e3b2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7e3b2-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7e3b2-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="7e3b2-112">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-112">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="7e3b2-113">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="7e3b2-113">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="7e3b2-114">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-114">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="7e3b2-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="7e3b2-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="7e3b2-116">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-116">Gets the new window.</span></span>
[<span data-ttu-id="7e3b2-117">put_Handled</span><span class="sxs-lookup"><span data-stu-id="7e3b2-117">put_Handled</span></span>](#put_handled) | <span data-ttu-id="7e3b2-118">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-118">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="7e3b2-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="7e3b2-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="7e3b2-120">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-120">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="7e3b2-121">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7e3b2-121">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="7e3b2-122">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-122">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="7e3b2-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7e3b2-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="7e3b2-124">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-124">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="7e3b2-125">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (через Window. Open () и т. д.)</span><span class="sxs-lookup"><span data-stu-id="7e3b2-125">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="7e3b2-126">Участников</span><span class="sxs-lookup"><span data-stu-id="7e3b2-126">Members</span></span>

#### <span data-ttu-id="7e3b2-127">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7e3b2-127">get_Uri</span></span> 

<span data-ttu-id="7e3b2-128">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-128">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="7e3b2-129">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="7e3b2-129">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="7e3b2-130">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="7e3b2-130">put_NewWindow</span></span> 

<span data-ttu-id="7e3b2-131">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-131">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="7e3b2-132">общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="7e3b2-132">public HRESULT [put_NewWindow](#put_newwindow)([ICoreWebView2](ICoreWebView2.md) \* newWindow)</span></span>

<span data-ttu-id="7e3b2-133">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-133">The target webview should not be navigated.</span></span> <span data-ttu-id="7e3b2-134">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-134">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="7e3b2-135">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="7e3b2-135">get_NewWindow</span></span> 

<span data-ttu-id="7e3b2-136">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-136">Gets the new window.</span></span>

> <span data-ttu-id="7e3b2-137">общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="7e3b2-137">public HRESULT [get_NewWindow](#get_newwindow)([ICoreWebView2](ICoreWebView2.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="7e3b2-138">put_Handled</span><span class="sxs-lookup"><span data-stu-id="7e3b2-138">put_Handled</span></span> 

<span data-ttu-id="7e3b2-139">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-139">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="7e3b2-140">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="7e3b2-140">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="7e3b2-141">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-141">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="7e3b2-142">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-142">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="7e3b2-143">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-143">Default is false.</span></span>

#### <span data-ttu-id="7e3b2-144">get_Handled</span><span class="sxs-lookup"><span data-stu-id="7e3b2-144">get_Handled</span></span> 

<span data-ttu-id="7e3b2-145">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-145">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="7e3b2-146">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="7e3b2-146">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="7e3b2-147">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7e3b2-147">get_IsUserInitiated</span></span> 

<span data-ttu-id="7e3b2-148">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-148">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="7e3b2-149">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="7e3b2-149">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="7e3b2-150">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7e3b2-150">GetDeferral</span></span> 

<span data-ttu-id="7e3b2-151">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-151">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="7e3b2-152">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="7e3b2-152">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="7e3b2-153">Вы можете использовать объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) , чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-153">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="7e3b2-154">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="7e3b2-154">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

