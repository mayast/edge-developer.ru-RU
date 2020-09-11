---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WindowFeatures
ms.openlocfilehash: 90b5a09a752250dc342e7eefad031c9b5b83d345
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012507"
---
# <span data-ttu-id="71ff4-104">интерфейс ICoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="71ff4-104">interface ICoreWebView2WindowFeatures</span></span> 

```
interface ICoreWebView2WindowFeatures
  : public IUnknown
```

<span data-ttu-id="71ff4-105">Функции окна для всплывающего окна WebView.</span><span class="sxs-lookup"><span data-stu-id="71ff4-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="71ff4-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="71ff4-106">Summary</span></span>

 <span data-ttu-id="71ff4-107">Участников</span><span class="sxs-lookup"><span data-stu-id="71ff4-107">Members</span></span>                        | <span data-ttu-id="71ff4-108">Описания</span><span class="sxs-lookup"><span data-stu-id="71ff4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="71ff4-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="71ff4-109">get_Height</span></span>](#get_height) | <span data-ttu-id="71ff4-110">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="71ff4-110">The height of the window.</span></span>
[<span data-ttu-id="71ff4-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="71ff4-111">get_Left</span></span>](#get_left) | <span data-ttu-id="71ff4-112">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="71ff4-112">The left position of the window.</span></span> <span data-ttu-id="71ff4-113">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="71ff4-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="71ff4-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="71ff4-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="71ff4-115">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="71ff4-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="71ff4-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="71ff4-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="71ff4-117">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="71ff4-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="71ff4-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="71ff4-118">get_Status</span></span>](#get_status) | <span data-ttu-id="71ff4-119">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="71ff4-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="71ff4-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="71ff4-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="71ff4-121">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="71ff4-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="71ff4-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="71ff4-122">get_Top</span></span>](#get_top) | <span data-ttu-id="71ff4-123">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="71ff4-123">The top position of the window.</span></span> <span data-ttu-id="71ff4-124">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="71ff4-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="71ff4-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="71ff4-125">get_Width</span></span>](#get_width) | <span data-ttu-id="71ff4-126">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="71ff4-126">The width of the window.</span></span>
[<span data-ttu-id="71ff4-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="71ff4-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="71ff4-128">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="71ff4-128">Has specified left and top values.</span></span>
[<span data-ttu-id="71ff4-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="71ff4-129">HasSize</span></span>](#hassize) | <span data-ttu-id="71ff4-130">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="71ff4-130">Has specified height and width values.</span></span>

<span data-ttu-id="71ff4-131">Эти поля соответствуют параметру "windowFeatures", передаваемому в Window. Open, как указано в [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="71ff4-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="71ff4-132">Участников</span><span class="sxs-lookup"><span data-stu-id="71ff4-132">Members</span></span>

#### <span data-ttu-id="71ff4-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="71ff4-133">get_Height</span></span> 

<span data-ttu-id="71ff4-134">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="71ff4-134">The height of the window.</span></span>

> <span data-ttu-id="71ff4-135">общедоступные значения HRESULT [get_Height](#get_height)(UINT32 \* высота)</span><span class="sxs-lookup"><span data-stu-id="71ff4-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="71ff4-136">Минимальное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="71ff4-136">Minimum value is 100.</span></span> <span data-ttu-id="71ff4-137">Если HasSize имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="71ff4-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="71ff4-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="71ff4-138">get_Left</span></span> 

<span data-ttu-id="71ff4-139">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="71ff4-139">The left position of the window.</span></span> <span data-ttu-id="71ff4-140">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="71ff4-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="71ff4-141">общедоступные значения HRESULT [get_Left](#get_left)(UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="71ff4-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="71ff4-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="71ff4-142">get_MenuBar</span></span> 

<span data-ttu-id="71ff4-143">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="71ff4-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="71ff4-144">общедоступные значения HRESULT [get_MenuBar](#get_menubar)(bool \* MenuBar)</span><span class="sxs-lookup"><span data-stu-id="71ff4-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="71ff4-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="71ff4-145">get_ScrollBars</span></span> 

<span data-ttu-id="71ff4-146">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="71ff4-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="71ff4-147">общедоступные значения HRESULT [get_ScrollBars](#get_scrollbars)(логические \* полосы прокрутки)</span><span class="sxs-lookup"><span data-stu-id="71ff4-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="71ff4-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="71ff4-148">get_Status</span></span> 

<span data-ttu-id="71ff4-149">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="71ff4-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="71ff4-150">общедоступные значения HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="71ff4-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="71ff4-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="71ff4-151">get_Toolbar</span></span> 

<span data-ttu-id="71ff4-152">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="71ff4-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="71ff4-153">общедоступные значения HRESULT [get_Toolbar](#get_toolbar)(bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="71ff4-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="71ff4-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="71ff4-154">get_Top</span></span> 

<span data-ttu-id="71ff4-155">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="71ff4-155">The top position of the window.</span></span> <span data-ttu-id="71ff4-156">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="71ff4-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="71ff4-157">общедоступные значения HRESULT [get_Top](#get_top)(UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="71ff4-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="71ff4-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="71ff4-158">get_Width</span></span> 

<span data-ttu-id="71ff4-159">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="71ff4-159">The width of the window.</span></span>

> <span data-ttu-id="71ff4-160">общедоступные значения HRESULT [get_Width](#get_width)(UINT32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="71ff4-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="71ff4-161">Минимальное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="71ff4-161">Minimum value is 100.</span></span> <span data-ttu-id="71ff4-162">Если HasSize имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="71ff4-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="71ff4-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="71ff4-163">HasPosition</span></span> 

<span data-ttu-id="71ff4-164">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="71ff4-164">Has specified left and top values.</span></span>

> <span data-ttu-id="71ff4-165">общедоступные значения HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="71ff4-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="71ff4-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="71ff4-166">HasSize</span></span> 

<span data-ttu-id="71ff4-167">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="71ff4-167">Has specified height and width values.</span></span>

> <span data-ttu-id="71ff4-168">общедоступные значения HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="71ff4-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

