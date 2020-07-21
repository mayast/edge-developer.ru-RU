---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: 2672f2aac842fd475f6148c439dbecdacd7793ee
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885405"
---
# <span data-ttu-id="843cd-104">интерфейс ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="843cd-104">interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="843cd-105">Функции окна для всплывающего окна WebView.</span><span class="sxs-lookup"><span data-stu-id="843cd-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="843cd-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="843cd-106">Summary</span></span>

 <span data-ttu-id="843cd-107">Участников</span><span class="sxs-lookup"><span data-stu-id="843cd-107">Members</span></span>                        | <span data-ttu-id="843cd-108">Описания</span><span class="sxs-lookup"><span data-stu-id="843cd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="843cd-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="843cd-109">get_Height</span></span>](#get_height) | <span data-ttu-id="843cd-110">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="843cd-110">The height of the window.</span></span>
[<span data-ttu-id="843cd-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="843cd-111">get_Left</span></span>](#get_left) | <span data-ttu-id="843cd-112">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="843cd-112">The left position of the window.</span></span> <span data-ttu-id="843cd-113">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="843cd-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="843cd-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="843cd-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="843cd-115">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="843cd-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="843cd-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="843cd-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="843cd-117">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="843cd-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="843cd-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="843cd-118">get_Status</span></span>](#get_status) | <span data-ttu-id="843cd-119">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="843cd-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="843cd-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="843cd-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="843cd-121">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="843cd-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="843cd-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="843cd-122">get_Top</span></span>](#get_top) | <span data-ttu-id="843cd-123">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="843cd-123">The top position of the window.</span></span> <span data-ttu-id="843cd-124">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="843cd-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="843cd-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="843cd-125">get_Width</span></span>](#get_width) | <span data-ttu-id="843cd-126">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="843cd-126">The width of the window.</span></span>
[<span data-ttu-id="843cd-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="843cd-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="843cd-128">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="843cd-128">Has specified left and top values.</span></span>
[<span data-ttu-id="843cd-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="843cd-129">HasSize</span></span>](#hassize) | <span data-ttu-id="843cd-130">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="843cd-130">Has specified height and width values.</span></span>

<span data-ttu-id="843cd-131">Эти поля соответствуют параметру "windowFeatures", передаваемому в Window. Open, как указано в[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="843cd-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="843cd-132">Участников</span><span class="sxs-lookup"><span data-stu-id="843cd-132">Members</span></span>

#### <span data-ttu-id="843cd-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="843cd-133">get_Height</span></span> 

<span data-ttu-id="843cd-134">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="843cd-134">The height of the window.</span></span>

> <span data-ttu-id="843cd-135">общедоступные значения HRESULT [get_Height](#get_height)(UINT32 \* высота)</span><span class="sxs-lookup"><span data-stu-id="843cd-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="843cd-136">Минимальное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="843cd-136">Minimum value is 100.</span></span> <span data-ttu-id="843cd-137">Если HasSize имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="843cd-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="843cd-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="843cd-138">get_Left</span></span> 

<span data-ttu-id="843cd-139">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="843cd-139">The left position of the window.</span></span> <span data-ttu-id="843cd-140">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="843cd-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="843cd-141">общедоступные значения HRESULT [get_Left](#get_left)(UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="843cd-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="843cd-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="843cd-142">get_MenuBar</span></span> 

<span data-ttu-id="843cd-143">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="843cd-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="843cd-144">общедоступные значения HRESULT [get_MenuBar](#get_menubar)(bool \* MenuBar)</span><span class="sxs-lookup"><span data-stu-id="843cd-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="843cd-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="843cd-145">get_ScrollBars</span></span> 

<span data-ttu-id="843cd-146">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="843cd-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="843cd-147">общедоступные значения HRESULT [get_ScrollBars](#get_scrollbars)(логические \* полосы прокрутки)</span><span class="sxs-lookup"><span data-stu-id="843cd-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="843cd-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="843cd-148">get_Status</span></span> 

<span data-ttu-id="843cd-149">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="843cd-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="843cd-150">общедоступные значения HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="843cd-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="843cd-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="843cd-151">get_Toolbar</span></span> 

<span data-ttu-id="843cd-152">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="843cd-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="843cd-153">общедоступные значения HRESULT [get_Toolbar](#get_toolbar)(bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="843cd-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="843cd-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="843cd-154">get_Top</span></span> 

<span data-ttu-id="843cd-155">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="843cd-155">The top position of the window.</span></span> <span data-ttu-id="843cd-156">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="843cd-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="843cd-157">общедоступные значения HRESULT [get_Top](#get_top)(UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="843cd-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="843cd-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="843cd-158">get_Width</span></span> 

<span data-ttu-id="843cd-159">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="843cd-159">The width of the window.</span></span>

> <span data-ttu-id="843cd-160">общедоступные значения HRESULT [get_Width](#get_width)(UINT32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="843cd-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="843cd-161">Минимальное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="843cd-161">Minimum value is 100.</span></span> <span data-ttu-id="843cd-162">Если HasSize имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="843cd-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="843cd-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="843cd-163">HasPosition</span></span> 

<span data-ttu-id="843cd-164">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="843cd-164">Has specified left and top values.</span></span>

> <span data-ttu-id="843cd-165">общедоступные значения HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="843cd-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="843cd-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="843cd-166">HasSize</span></span> 

<span data-ttu-id="843cd-167">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="843cd-167">Has specified height and width values.</span></span>

> <span data-ttu-id="843cd-168">общедоступные значения HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="843cd-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

