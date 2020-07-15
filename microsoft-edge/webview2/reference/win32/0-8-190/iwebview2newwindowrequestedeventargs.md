---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: a90727949fa9a64004527236e6c5f016afe018e0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878367"
---
# <span data-ttu-id="c7b38-104">0.8.355-Interface IWebView2NewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c7b38-104">0.8.355 - interface IWebView2NewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c7b38-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="c7b38-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="c7b38-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="c7b38-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="c7b38-107">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="c7b38-107">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="c7b38-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c7b38-108">Summary</span></span>

 <span data-ttu-id="c7b38-109">Участников</span><span class="sxs-lookup"><span data-stu-id="c7b38-109">Members</span></span>                        | <span data-ttu-id="c7b38-110">Описания</span><span class="sxs-lookup"><span data-stu-id="c7b38-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c7b38-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c7b38-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="c7b38-112">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c7b38-112">The target uri of the NewWindowRequest.</span></span>
[<span data-ttu-id="c7b38-113">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c7b38-113">put_NewWindow</span></span>](#put_newwindow) | <span data-ttu-id="c7b38-114">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c7b38-114">Sets a WebView as a result of the NewWindowRequest.</span></span>
[<span data-ttu-id="c7b38-115">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c7b38-115">get_NewWindow</span></span>](#get_newwindow) | <span data-ttu-id="c7b38-116">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="c7b38-116">Gets the new window.</span></span>
[<span data-ttu-id="c7b38-117">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c7b38-117">put_Handled</span></span>](#put_handled) | <span data-ttu-id="c7b38-118">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="c7b38-118">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="c7b38-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c7b38-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="c7b38-120">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="c7b38-120">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>
[<span data-ttu-id="c7b38-121">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c7b38-121">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="c7b38-122">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="c7b38-122">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="c7b38-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c7b38-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c7b38-124">Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="c7b38-124">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

<span data-ttu-id="c7b38-125">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (через Window. Open () и т. д.)</span><span class="sxs-lookup"><span data-stu-id="c7b38-125">The event is fired when content inside webview requested to a open a new window (through window.open() etc.)</span></span>

## <span data-ttu-id="c7b38-126">Участников</span><span class="sxs-lookup"><span data-stu-id="c7b38-126">Members</span></span>

#### <span data-ttu-id="c7b38-127">get_Uri</span><span class="sxs-lookup"><span data-stu-id="c7b38-127">get_Uri</span></span> 

<span data-ttu-id="c7b38-128">Целевой URI для NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c7b38-128">The target uri of the NewWindowRequest.</span></span>

> <span data-ttu-id="c7b38-129">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="c7b38-129">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="c7b38-130">put_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c7b38-130">put_NewWindow</span></span> 

<span data-ttu-id="c7b38-131">Задает WebView в качестве результата NewWindowRequest.</span><span class="sxs-lookup"><span data-stu-id="c7b38-131">Sets a WebView as a result of the NewWindowRequest.</span></span>

> <span data-ttu-id="c7b38-132">общедоступные значения HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="c7b38-132">public HRESULT [put_NewWindow](#put_newwindow)([IWebView2WebView](IWebView2WebView.md) \* newWindow)</span></span>

<span data-ttu-id="c7b38-133">Не следует перемещаться по целевому WebView.</span><span class="sxs-lookup"><span data-stu-id="c7b38-133">The target webview should not be navigated.</span></span> <span data-ttu-id="c7b38-134">Если задано значение NewWindow, окно верхнего уровня будет возвращено в виде открытой WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="c7b38-134">If the NewWindow is set, its top level window will return as the opened WindowProxy.</span></span>

#### <span data-ttu-id="c7b38-135">get_NewWindow</span><span class="sxs-lookup"><span data-stu-id="c7b38-135">get_NewWindow</span></span> 

<span data-ttu-id="c7b38-136">Получает новое окно.</span><span class="sxs-lookup"><span data-stu-id="c7b38-136">Gets the new window.</span></span>

> <span data-ttu-id="c7b38-137">общедоступные значения HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \* \* NewWindow)</span><span class="sxs-lookup"><span data-stu-id="c7b38-137">public HRESULT [get_NewWindow](#get_newwindow)([IWebView2WebView](IWebView2WebView.md) \*\* newWindow)</span></span>

#### <span data-ttu-id="c7b38-138">put_Handled</span><span class="sxs-lookup"><span data-stu-id="c7b38-138">put_Handled</span></span> 

<span data-ttu-id="c7b38-139">Определяет, будет ли NewWindowRequestedEvent обрабатываться узлом.</span><span class="sxs-lookup"><span data-stu-id="c7b38-139">Sets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="c7b38-140">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="c7b38-140">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

<span data-ttu-id="c7b38-141">Если это значение равно false и не задано значение NewWindow, WebView откроет всплывающее окно, и оно будет возвращено как открытое WindowProxy.</span><span class="sxs-lookup"><span data-stu-id="c7b38-141">If this is false and no NewWindow is set, the WebView will open a popup window and it will be returned as opened WindowProxy.</span></span> <span data-ttu-id="c7b38-142">Если установлено значение true, а для NewWindow Window. Open не задано значение "истина", то открытая WindowProxy будет использоваться для объекта-заглушки окна, а окно загрузится не будет.</span><span class="sxs-lookup"><span data-stu-id="c7b38-142">If set to true and no NewWindow is set for a window.open call, the opened WindowProxy will be for an dummy window object and no window will load.</span></span> <span data-ttu-id="c7b38-143">Значение по умолчанию — false.</span><span class="sxs-lookup"><span data-stu-id="c7b38-143">Default is false.</span></span>

#### <span data-ttu-id="c7b38-144">get_Handled</span><span class="sxs-lookup"><span data-stu-id="c7b38-144">get_Handled</span></span> 

<span data-ttu-id="c7b38-145">Возвращает значение, определяющее, обрабатывается ли NewWindowRequestedEvent узлом.</span><span class="sxs-lookup"><span data-stu-id="c7b38-145">Gets whether the NewWindowRequestedEvent is handled by host.</span></span>

> <span data-ttu-id="c7b38-146">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="c7b38-146">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

#### <span data-ttu-id="c7b38-147">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c7b38-147">get_IsUserInitiated</span></span> 

<span data-ttu-id="c7b38-148">IsUserInitiated имеет значение true, когда новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="c7b38-148">IsUserInitiated is true when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="c7b38-149">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="c7b38-149">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="c7b38-150">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c7b38-150">GetDeferral</span></span> 

<span data-ttu-id="c7b38-151">Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="c7b38-151">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="c7b38-152">общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="c7b38-152">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="c7b38-153">Вы можете использовать объект [IWebView2Deferral](IWebView2Deferral.md) , чтобы завершить запрос на открытие окна позже.</span><span class="sxs-lookup"><span data-stu-id="c7b38-153">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the window open request at a later time.</span></span> <span data-ttu-id="c7b38-154">Несмотря на то, что это событие отложено, окно opener вернет WindowProxy в окно unnavigateed, которое будет перемещаться по завершении отсрочки.</span><span class="sxs-lookup"><span data-stu-id="c7b38-154">While this event is deferred the opener window will be returned a WindowProxy to an unnavigated window, which will navigate when the deferral is complete.</span></span>

