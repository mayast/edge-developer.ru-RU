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
ms.openlocfilehash: 576f54f2a7ecc2e1e99758719e80cc589c5bc791
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699293"
---
# <span data-ttu-id="3b5bc-104">интерфейс ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="3b5bc-104">interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

> [!NOTE]
> <span data-ttu-id="3b5bc-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="3b5bc-106">Функции окна для всплывающего окна WebView.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-106">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="3b5bc-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3b5bc-107">Summary</span></span>

 <span data-ttu-id="3b5bc-108">Участников</span><span class="sxs-lookup"><span data-stu-id="3b5bc-108">Members</span></span>                        | <span data-ttu-id="3b5bc-109">Описания</span><span class="sxs-lookup"><span data-stu-id="3b5bc-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3b5bc-110">get_Height</span><span class="sxs-lookup"><span data-stu-id="3b5bc-110">get_Height</span></span>](#get_height) | <span data-ttu-id="3b5bc-111">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-111">The height of the window.</span></span>
[<span data-ttu-id="3b5bc-112">get_Left</span><span class="sxs-lookup"><span data-stu-id="3b5bc-112">get_Left</span></span>](#get_left) | <span data-ttu-id="3b5bc-113">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-113">The left position of the window.</span></span> <span data-ttu-id="3b5bc-114">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-114">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="3b5bc-115">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="3b5bc-115">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="3b5bc-116">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="3b5bc-117">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="3b5bc-117">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="3b5bc-118">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="3b5bc-119">get_Status</span><span class="sxs-lookup"><span data-stu-id="3b5bc-119">get_Status</span></span>](#get_status) | <span data-ttu-id="3b5bc-120">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="3b5bc-121">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="3b5bc-121">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="3b5bc-122">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="3b5bc-123">get_Top</span><span class="sxs-lookup"><span data-stu-id="3b5bc-123">get_Top</span></span>](#get_top) | <span data-ttu-id="3b5bc-124">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-124">The top position of the window.</span></span> <span data-ttu-id="3b5bc-125">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-125">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="3b5bc-126">get_Width</span><span class="sxs-lookup"><span data-stu-id="3b5bc-126">get_Width</span></span>](#get_width) | <span data-ttu-id="3b5bc-127">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-127">The width of the window.</span></span>
[<span data-ttu-id="3b5bc-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="3b5bc-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="3b5bc-129">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-129">Has specified left and top values.</span></span>
[<span data-ttu-id="3b5bc-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="3b5bc-130">HasSize</span></span>](#hassize) | <span data-ttu-id="3b5bc-131">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-131">Has specified height and width values.</span></span>

<span data-ttu-id="3b5bc-132">Эти поля соответствуют параметру "windowFeatures", передаваемому в Window. Open, как указано в[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-132">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="3b5bc-133">Участников</span><span class="sxs-lookup"><span data-stu-id="3b5bc-133">Members</span></span>

#### <span data-ttu-id="3b5bc-134">get_Height</span><span class="sxs-lookup"><span data-stu-id="3b5bc-134">get_Height</span></span> 

<span data-ttu-id="3b5bc-135">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-135">The height of the window.</span></span>

> <span data-ttu-id="3b5bc-136">общедоступные значения HRESULT [get_Height](#get_height)(UINT32 \* высота)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-136">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="3b5bc-137">Минимальное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-137">Minimum value is 100.</span></span> <span data-ttu-id="3b5bc-138">Если HasSize имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-138">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="3b5bc-139">get_Left</span><span class="sxs-lookup"><span data-stu-id="3b5bc-139">get_Left</span></span> 

<span data-ttu-id="3b5bc-140">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-140">The left position of the window.</span></span> <span data-ttu-id="3b5bc-141">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-141">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="3b5bc-142">общедоступные значения HRESULT [get_Left](#get_left)(UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-142">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="3b5bc-143">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="3b5bc-143">get_MenuBar</span></span> 

<span data-ttu-id="3b5bc-144">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-144">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="3b5bc-145">общедоступные значения HRESULT [get_MenuBar](#get_menubar)(bool \* MenuBar)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-145">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="3b5bc-146">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="3b5bc-146">get_ScrollBars</span></span> 

<span data-ttu-id="3b5bc-147">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-147">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="3b5bc-148">общедоступные значения HRESULT [get_ScrollBars](#get_scrollbars)(логические \* полосы прокрутки)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-148">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="3b5bc-149">get_Status</span><span class="sxs-lookup"><span data-stu-id="3b5bc-149">get_Status</span></span> 

<span data-ttu-id="3b5bc-150">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-150">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="3b5bc-151">общедоступные значения HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-151">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="3b5bc-152">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="3b5bc-152">get_Toolbar</span></span> 

<span data-ttu-id="3b5bc-153">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-153">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="3b5bc-154">общедоступные значения HRESULT [get_Toolbar](#get_toolbar)(bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-154">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="3b5bc-155">get_Top</span><span class="sxs-lookup"><span data-stu-id="3b5bc-155">get_Top</span></span> 

<span data-ttu-id="3b5bc-156">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-156">The top position of the window.</span></span> <span data-ttu-id="3b5bc-157">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-157">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="3b5bc-158">общедоступные значения HRESULT [get_Top](#get_top)(UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-158">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="3b5bc-159">get_Width</span><span class="sxs-lookup"><span data-stu-id="3b5bc-159">get_Width</span></span> 

<span data-ttu-id="3b5bc-160">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-160">The width of the window.</span></span>

> <span data-ttu-id="3b5bc-161">общедоступные значения HRESULT [get_Width](#get_width)(UINT32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-161">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="3b5bc-162">Минимальное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-162">Minimum value is 100.</span></span> <span data-ttu-id="3b5bc-163">Если HasSize имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-163">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="3b5bc-164">HasPosition</span><span class="sxs-lookup"><span data-stu-id="3b5bc-164">HasPosition</span></span> 

<span data-ttu-id="3b5bc-165">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-165">Has specified left and top values.</span></span>

> <span data-ttu-id="3b5bc-166">общедоступные значения HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-166">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="3b5bc-167">HasSize</span><span class="sxs-lookup"><span data-stu-id="3b5bc-167">HasSize</span></span> 

<span data-ttu-id="3b5bc-168">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="3b5bc-168">Has specified height and width values.</span></span>

> <span data-ttu-id="3b5bc-169">общедоступные значения HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="3b5bc-169">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

