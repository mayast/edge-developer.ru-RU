---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 41ae506965067b478c3cb588eed0c8029704c4a3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012425"
---
# <span data-ttu-id="49852-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="49852-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

<span data-ttu-id="49852-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="49852-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="49852-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="49852-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="49852-107">Функции окна для всплывающего окна WebView.</span><span class="sxs-lookup"><span data-stu-id="49852-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="49852-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="49852-108">Summary</span></span>

 <span data-ttu-id="49852-109">Участников</span><span class="sxs-lookup"><span data-stu-id="49852-109">Members</span></span>                        | <span data-ttu-id="49852-110">Описания</span><span class="sxs-lookup"><span data-stu-id="49852-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49852-111">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="49852-111">Height</span></span>](#height) | <span data-ttu-id="49852-112">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="49852-112">The height of the window.</span></span>
[<span data-ttu-id="49852-113">Влево</span><span class="sxs-lookup"><span data-stu-id="49852-113">Left</span></span>](#left) | <span data-ttu-id="49852-114">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="49852-114">The left position of the window.</span></span>
[<span data-ttu-id="49852-115">MenuBar</span><span class="sxs-lookup"><span data-stu-id="49852-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="49852-116">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="49852-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="49852-117">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="49852-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="49852-118">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="49852-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="49852-119">Состояние</span><span class="sxs-lookup"><span data-stu-id="49852-119">Status</span></span>](#status) | <span data-ttu-id="49852-120">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="49852-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="49852-121">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="49852-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="49852-122">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="49852-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="49852-123">Top</span><span class="sxs-lookup"><span data-stu-id="49852-123">Top</span></span>](#top) | <span data-ttu-id="49852-124">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="49852-124">The top position of the window.</span></span>
[<span data-ttu-id="49852-125">Ширина</span><span class="sxs-lookup"><span data-stu-id="49852-125">Width</span></span>](#width) | <span data-ttu-id="49852-126">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="49852-126">The width of the window.</span></span>
[<span data-ttu-id="49852-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="49852-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="49852-128">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="49852-128">Has specified left and top values.</span></span>
[<span data-ttu-id="49852-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="49852-129">HasSize</span></span>](#hassize) | <span data-ttu-id="49852-130">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="49852-130">Has specified height and width values.</span></span>

## <span data-ttu-id="49852-131">Участников</span><span class="sxs-lookup"><span data-stu-id="49852-131">Members</span></span>

#### <span data-ttu-id="49852-132">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="49852-132">Height</span></span> 

<span data-ttu-id="49852-133">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="49852-133">The height of the window.</span></span>

> <span data-ttu-id="49852-134">открытая [Высота](#height) с uint</span><span class="sxs-lookup"><span data-stu-id="49852-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="49852-135">Влево</span><span class="sxs-lookup"><span data-stu-id="49852-135">Left</span></span> 

<span data-ttu-id="49852-136">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="49852-136">The left position of the window.</span></span>

> <span data-ttu-id="49852-137">Открытый uint [слева](#left)</span><span class="sxs-lookup"><span data-stu-id="49852-137">public uint [Left](#left)</span></span>

<span data-ttu-id="49852-138">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="49852-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="49852-139">MenuBar</span><span class="sxs-lookup"><span data-stu-id="49852-139">MenuBar</span></span> 

<span data-ttu-id="49852-140">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="49852-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="49852-141">public int [Remenubar](#menubar)</span><span class="sxs-lookup"><span data-stu-id="49852-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="49852-142">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="49852-142">ScrollBars</span></span> 

<span data-ttu-id="49852-143">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="49852-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="49852-144">открытые [прокрутки](#scrollbars) int</span><span class="sxs-lookup"><span data-stu-id="49852-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="49852-145">Состояние</span><span class="sxs-lookup"><span data-stu-id="49852-145">Status</span></span> 

<span data-ttu-id="49852-146">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="49852-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="49852-147">общедоступный целочисленный [статус](#status)</span><span class="sxs-lookup"><span data-stu-id="49852-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="49852-148">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="49852-148">Toolbar</span></span> 

<span data-ttu-id="49852-149">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="49852-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="49852-150">общедоступная [панель инструментов](#toolbar) int</span><span class="sxs-lookup"><span data-stu-id="49852-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="49852-151">Top</span><span class="sxs-lookup"><span data-stu-id="49852-151">Top</span></span> 

<span data-ttu-id="49852-152">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="49852-152">The top position of the window.</span></span>

> <span data-ttu-id="49852-153">Открытый uint, [сверху](#top)</span><span class="sxs-lookup"><span data-stu-id="49852-153">public uint [Top](#top)</span></span>

<span data-ttu-id="49852-154">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="49852-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="49852-155">Ширина</span><span class="sxs-lookup"><span data-stu-id="49852-155">Width</span></span> 

<span data-ttu-id="49852-156">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="49852-156">The width of the window.</span></span>

> <span data-ttu-id="49852-157">открытая [Ширина](#width) с uint</span><span class="sxs-lookup"><span data-stu-id="49852-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="49852-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="49852-158">HasPosition</span></span> 

<span data-ttu-id="49852-159">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="49852-159">Has specified left and top values.</span></span>

> <span data-ttu-id="49852-160">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="49852-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="49852-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="49852-161">HasSize</span></span> 

<span data-ttu-id="49852-162">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="49852-162">Has specified height and width values.</span></span>

> <span data-ttu-id="49852-163">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="49852-163">public int [HasSize](#hassize)()</span></span>

