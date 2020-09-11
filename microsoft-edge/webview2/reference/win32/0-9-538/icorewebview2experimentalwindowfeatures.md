---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: ee740f7d227ae98d451ba1c5e8f1017fe92514a8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011372"
---
# <span data-ttu-id="9e023-104">0.9.579-Interface ICoreWebView2ExperimentalWindowFeatures</span><span class="sxs-lookup"><span data-stu-id="9e023-104">0.9.579 - interface ICoreWebView2ExperimentalWindowFeatures</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

<span data-ttu-id="9e023-105">Функции окна для всплывающего окна WebView.</span><span class="sxs-lookup"><span data-stu-id="9e023-105">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="9e023-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9e023-106">Summary</span></span>

 <span data-ttu-id="9e023-107">Участников</span><span class="sxs-lookup"><span data-stu-id="9e023-107">Members</span></span>                        | <span data-ttu-id="9e023-108">Описания</span><span class="sxs-lookup"><span data-stu-id="9e023-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e023-109">get_Height</span><span class="sxs-lookup"><span data-stu-id="9e023-109">get_Height</span></span>](#get_height) | <span data-ttu-id="9e023-110">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="9e023-110">The height of the window.</span></span>
[<span data-ttu-id="9e023-111">get_Left</span><span class="sxs-lookup"><span data-stu-id="9e023-111">get_Left</span></span>](#get_left) | <span data-ttu-id="9e023-112">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="9e023-112">The left position of the window.</span></span> <span data-ttu-id="9e023-113">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="9e023-113">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="9e023-114">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="9e023-114">get_MenuBar</span></span>](#get_menubar) | <span data-ttu-id="9e023-115">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="9e023-115">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="9e023-116">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="9e023-116">get_ScrollBars</span></span>](#get_scrollbars) | <span data-ttu-id="9e023-117">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="9e023-117">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="9e023-118">get_Status</span><span class="sxs-lookup"><span data-stu-id="9e023-118">get_Status</span></span>](#get_status) | <span data-ttu-id="9e023-119">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="9e023-119">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="9e023-120">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="9e023-120">get_Toolbar</span></span>](#get_toolbar) | <span data-ttu-id="9e023-121">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="9e023-121">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="9e023-122">get_Top</span><span class="sxs-lookup"><span data-stu-id="9e023-122">get_Top</span></span>](#get_top) | <span data-ttu-id="9e023-123">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="9e023-123">The top position of the window.</span></span> <span data-ttu-id="9e023-124">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="9e023-124">Will fail if HasPosition is false.</span></span>
[<span data-ttu-id="9e023-125">get_Width</span><span class="sxs-lookup"><span data-stu-id="9e023-125">get_Width</span></span>](#get_width) | <span data-ttu-id="9e023-126">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="9e023-126">The width of the window.</span></span>
[<span data-ttu-id="9e023-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="9e023-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="9e023-128">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="9e023-128">Has specified left and top values.</span></span>
[<span data-ttu-id="9e023-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="9e023-129">HasSize</span></span>](#hassize) | <span data-ttu-id="9e023-130">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="9e023-130">Has specified height and width values.</span></span>

<span data-ttu-id="9e023-131">Эти поля соответствуют параметру "windowFeatures", передаваемому в Window. Open, как указано в [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span><span class="sxs-lookup"><span data-stu-id="9e023-131">These fields match the 'windowFeatures' passed to window.open as specified in [https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)</span></span>

## <span data-ttu-id="9e023-132">Участников</span><span class="sxs-lookup"><span data-stu-id="9e023-132">Members</span></span>

#### <span data-ttu-id="9e023-133">get_Height</span><span class="sxs-lookup"><span data-stu-id="9e023-133">get_Height</span></span> 

<span data-ttu-id="9e023-134">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="9e023-134">The height of the window.</span></span>

> <span data-ttu-id="9e023-135">общедоступные значения HRESULT [get_Height](#get_height)(UINT32 \* высота)</span><span class="sxs-lookup"><span data-stu-id="9e023-135">public HRESULT [get_Height](#get_height)(UINT32 \* height)</span></span>

<span data-ttu-id="9e023-136">Минимальное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="9e023-136">Minimum value is 100.</span></span> <span data-ttu-id="9e023-137">Если HasSize имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="9e023-137">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="9e023-138">get_Left</span><span class="sxs-lookup"><span data-stu-id="9e023-138">get_Left</span></span> 

<span data-ttu-id="9e023-139">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="9e023-139">The left position of the window.</span></span> <span data-ttu-id="9e023-140">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="9e023-140">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="9e023-141">общедоступные значения HRESULT [get_Left](#get_left)(UINT32 \* Left)</span><span class="sxs-lookup"><span data-stu-id="9e023-141">public HRESULT [get_Left](#get_left)(UINT32 \* left)</span></span>

#### <span data-ttu-id="9e023-142">get_MenuBar</span><span class="sxs-lookup"><span data-stu-id="9e023-142">get_MenuBar</span></span> 

<span data-ttu-id="9e023-143">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="9e023-143">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="9e023-144">общедоступные значения HRESULT [get_MenuBar](#get_menubar)(bool \* MenuBar)</span><span class="sxs-lookup"><span data-stu-id="9e023-144">public HRESULT [get_MenuBar](#get_menubar)(BOOL \* menuBar)</span></span>

#### <span data-ttu-id="9e023-145">get_ScrollBars</span><span class="sxs-lookup"><span data-stu-id="9e023-145">get_ScrollBars</span></span> 

<span data-ttu-id="9e023-146">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="9e023-146">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="9e023-147">общедоступные значения HRESULT [get_ScrollBars](#get_scrollbars)(логические \* полосы прокрутки)</span><span class="sxs-lookup"><span data-stu-id="9e023-147">public HRESULT [get_ScrollBars](#get_scrollbars)(BOOL \* scrollBars)</span></span>

#### <span data-ttu-id="9e023-148">get_Status</span><span class="sxs-lookup"><span data-stu-id="9e023-148">get_Status</span></span> 

<span data-ttu-id="9e023-149">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="9e023-149">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="9e023-150">общедоступные значения HRESULT [get_Status](#get_status)(bool \* Status)</span><span class="sxs-lookup"><span data-stu-id="9e023-150">public HRESULT [get_Status](#get_status)(BOOL \* status)</span></span>

#### <span data-ttu-id="9e023-151">get_Toolbar</span><span class="sxs-lookup"><span data-stu-id="9e023-151">get_Toolbar</span></span> 

<span data-ttu-id="9e023-152">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="9e023-152">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="9e023-153">общедоступные значения HRESULT [get_Toolbar](#get_toolbar)(bool \* Toolbar)</span><span class="sxs-lookup"><span data-stu-id="9e023-153">public HRESULT [get_Toolbar](#get_toolbar)(BOOL \* toolbar)</span></span>

#### <span data-ttu-id="9e023-154">get_Top</span><span class="sxs-lookup"><span data-stu-id="9e023-154">get_Top</span></span> 

<span data-ttu-id="9e023-155">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="9e023-155">The top position of the window.</span></span> <span data-ttu-id="9e023-156">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="9e023-156">Will fail if HasPosition is false.</span></span>

> <span data-ttu-id="9e023-157">общедоступные значения HRESULT [get_Top](#get_top)(UINT32 \* Top)</span><span class="sxs-lookup"><span data-stu-id="9e023-157">public HRESULT [get_Top](#get_top)(UINT32 \* top)</span></span>

#### <span data-ttu-id="9e023-158">get_Width</span><span class="sxs-lookup"><span data-stu-id="9e023-158">get_Width</span></span> 

<span data-ttu-id="9e023-159">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="9e023-159">The width of the window.</span></span>

> <span data-ttu-id="9e023-160">общедоступные значения HRESULT [get_Width](#get_width)(UINT32 \* Width)</span><span class="sxs-lookup"><span data-stu-id="9e023-160">public HRESULT [get_Width](#get_width)(UINT32 \* width)</span></span>

<span data-ttu-id="9e023-161">Минимальное значение — 100.</span><span class="sxs-lookup"><span data-stu-id="9e023-161">Minimum value is 100.</span></span> <span data-ttu-id="9e023-162">Если HasSize имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="9e023-162">Will fail if HasSize is false.</span></span>

#### <span data-ttu-id="9e023-163">HasPosition</span><span class="sxs-lookup"><span data-stu-id="9e023-163">HasPosition</span></span> 

<span data-ttu-id="9e023-164">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="9e023-164">Has specified left and top values.</span></span>

> <span data-ttu-id="9e023-165">общедоступные значения HRESULT [HasPosition](#hasposition)(bool \* HasPosition)</span><span class="sxs-lookup"><span data-stu-id="9e023-165">public HRESULT [HasPosition](#hasposition)(BOOL \* hasPosition)</span></span>

#### <span data-ttu-id="9e023-166">HasSize</span><span class="sxs-lookup"><span data-stu-id="9e023-166">HasSize</span></span> 

<span data-ttu-id="9e023-167">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="9e023-167">Has specified height and width values.</span></span>

> <span data-ttu-id="9e023-168">общедоступные значения HRESULT [HasSize](#hassize)(bool \* HasSize)</span><span class="sxs-lookup"><span data-stu-id="9e023-168">public HRESULT [HasSize](#hassize)(BOOL \* hasSize)</span></span>

