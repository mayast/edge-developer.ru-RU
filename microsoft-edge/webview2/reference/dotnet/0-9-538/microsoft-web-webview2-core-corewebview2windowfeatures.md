---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 4866626111908eae9800da0baabec0356d5d4bf8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879655"
---
# <span data-ttu-id="40769-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="40769-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

> [!NOTE]
> <span data-ttu-id="40769-105">Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="40769-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="40769-106">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="40769-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="40769-107">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="40769-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="40769-108">Функции окна для всплывающего окна WebView.</span><span class="sxs-lookup"><span data-stu-id="40769-108">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="40769-109">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="40769-109">Summary</span></span>

 <span data-ttu-id="40769-110">Участников</span><span class="sxs-lookup"><span data-stu-id="40769-110">Members</span></span>                        | <span data-ttu-id="40769-111">Описания</span><span class="sxs-lookup"><span data-stu-id="40769-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="40769-112">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="40769-112">Height</span></span>](#height) | <span data-ttu-id="40769-113">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="40769-113">The height of the window.</span></span>
[<span data-ttu-id="40769-114">Влево</span><span class="sxs-lookup"><span data-stu-id="40769-114">Left</span></span>](#left) | <span data-ttu-id="40769-115">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="40769-115">The left position of the window.</span></span>
[<span data-ttu-id="40769-116">MenuBar</span><span class="sxs-lookup"><span data-stu-id="40769-116">MenuBar</span></span>](#menubar) | <span data-ttu-id="40769-117">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="40769-117">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="40769-118">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="40769-118">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="40769-119">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="40769-119">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="40769-120">Состояние</span><span class="sxs-lookup"><span data-stu-id="40769-120">Status</span></span>](#status) | <span data-ttu-id="40769-121">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="40769-121">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="40769-122">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="40769-122">Toolbar</span></span>](#toolbar) | <span data-ttu-id="40769-123">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="40769-123">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="40769-124">Top</span><span class="sxs-lookup"><span data-stu-id="40769-124">Top</span></span>](#top) | <span data-ttu-id="40769-125">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="40769-125">The top position of the window.</span></span>
[<span data-ttu-id="40769-126">Ширина</span><span class="sxs-lookup"><span data-stu-id="40769-126">Width</span></span>](#width) | <span data-ttu-id="40769-127">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="40769-127">The width of the window.</span></span>
[<span data-ttu-id="40769-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="40769-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="40769-129">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="40769-129">Has specified left and top values.</span></span>
[<span data-ttu-id="40769-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="40769-130">HasSize</span></span>](#hassize) | <span data-ttu-id="40769-131">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="40769-131">Has specified height and width values.</span></span>

## <span data-ttu-id="40769-132">Участников</span><span class="sxs-lookup"><span data-stu-id="40769-132">Members</span></span>

#### <span data-ttu-id="40769-133">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="40769-133">Height</span></span> 

<span data-ttu-id="40769-134">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="40769-134">The height of the window.</span></span>

> <span data-ttu-id="40769-135">открытая [Высота](#height) с uint</span><span class="sxs-lookup"><span data-stu-id="40769-135">public uint [Height](#height)</span></span>

#### <span data-ttu-id="40769-136">Влево</span><span class="sxs-lookup"><span data-stu-id="40769-136">Left</span></span> 

<span data-ttu-id="40769-137">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="40769-137">The left position of the window.</span></span>

> <span data-ttu-id="40769-138">Открытый uint [слева](#left)</span><span class="sxs-lookup"><span data-stu-id="40769-138">public uint [Left](#left)</span></span>

<span data-ttu-id="40769-139">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="40769-139">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="40769-140">MenuBar</span><span class="sxs-lookup"><span data-stu-id="40769-140">MenuBar</span></span> 

<span data-ttu-id="40769-141">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="40769-141">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="40769-142">public int [Remenubar](#menubar)</span><span class="sxs-lookup"><span data-stu-id="40769-142">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="40769-143">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="40769-143">ScrollBars</span></span> 

<span data-ttu-id="40769-144">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="40769-144">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="40769-145">открытые [прокрутки](#scrollbars) int</span><span class="sxs-lookup"><span data-stu-id="40769-145">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="40769-146">Состояние</span><span class="sxs-lookup"><span data-stu-id="40769-146">Status</span></span> 

<span data-ttu-id="40769-147">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="40769-147">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="40769-148">общедоступный целочисленный [статус](#status)</span><span class="sxs-lookup"><span data-stu-id="40769-148">public int [Status](#status)</span></span>

#### <span data-ttu-id="40769-149">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="40769-149">Toolbar</span></span> 

<span data-ttu-id="40769-150">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="40769-150">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="40769-151">общедоступная [панель инструментов](#toolbar) int</span><span class="sxs-lookup"><span data-stu-id="40769-151">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="40769-152">Top</span><span class="sxs-lookup"><span data-stu-id="40769-152">Top</span></span> 

<span data-ttu-id="40769-153">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="40769-153">The top position of the window.</span></span>

> <span data-ttu-id="40769-154">Открытый uint, [сверху](#top)</span><span class="sxs-lookup"><span data-stu-id="40769-154">public uint [Top](#top)</span></span>

<span data-ttu-id="40769-155">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="40769-155">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="40769-156">Ширина</span><span class="sxs-lookup"><span data-stu-id="40769-156">Width</span></span> 

<span data-ttu-id="40769-157">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="40769-157">The width of the window.</span></span>

> <span data-ttu-id="40769-158">открытая [Ширина](#width) с uint</span><span class="sxs-lookup"><span data-stu-id="40769-158">public uint [Width](#width)</span></span>

#### <span data-ttu-id="40769-159">HasPosition</span><span class="sxs-lookup"><span data-stu-id="40769-159">HasPosition</span></span> 

<span data-ttu-id="40769-160">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="40769-160">Has specified left and top values.</span></span>

> <span data-ttu-id="40769-161">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="40769-161">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="40769-162">HasSize</span><span class="sxs-lookup"><span data-stu-id="40769-162">HasSize</span></span> 

<span data-ttu-id="40769-163">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="40769-163">Has specified height and width values.</span></span>

> <span data-ttu-id="40769-164">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="40769-164">public int [HasSize](#hassize)()</span></span>

