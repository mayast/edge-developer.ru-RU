---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 59e051c0537357fed89d6300db69ea479b656c7e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010518"
---
# <span data-ttu-id="397bc-104">класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="397bc-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="397bc-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="397bc-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="397bc-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="397bc-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="397bc-107">Функции окна для всплывающего окна WebView.</span><span class="sxs-lookup"><span data-stu-id="397bc-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="397bc-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="397bc-108">Summary</span></span>

 <span data-ttu-id="397bc-109">Участников</span><span class="sxs-lookup"><span data-stu-id="397bc-109">Members</span></span>                        | <span data-ttu-id="397bc-110">Описания</span><span class="sxs-lookup"><span data-stu-id="397bc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="397bc-111">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="397bc-111">Height</span></span>](#height) | <span data-ttu-id="397bc-112">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="397bc-112">The height of the window.</span></span>
[<span data-ttu-id="397bc-113">Влево</span><span class="sxs-lookup"><span data-stu-id="397bc-113">Left</span></span>](#left) | <span data-ttu-id="397bc-114">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="397bc-114">The left position of the window.</span></span>
[<span data-ttu-id="397bc-115">MenuBar</span><span class="sxs-lookup"><span data-stu-id="397bc-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="397bc-116">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="397bc-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="397bc-117">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="397bc-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="397bc-118">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="397bc-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="397bc-119">Состояние</span><span class="sxs-lookup"><span data-stu-id="397bc-119">Status</span></span>](#status) | <span data-ttu-id="397bc-120">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="397bc-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="397bc-121">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="397bc-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="397bc-122">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="397bc-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="397bc-123">Top</span><span class="sxs-lookup"><span data-stu-id="397bc-123">Top</span></span>](#top) | <span data-ttu-id="397bc-124">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="397bc-124">The top position of the window.</span></span>
[<span data-ttu-id="397bc-125">Ширина</span><span class="sxs-lookup"><span data-stu-id="397bc-125">Width</span></span>](#width) | <span data-ttu-id="397bc-126">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="397bc-126">The width of the window.</span></span>
[<span data-ttu-id="397bc-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="397bc-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="397bc-128">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="397bc-128">Has specified left and top values.</span></span>
[<span data-ttu-id="397bc-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="397bc-129">HasSize</span></span>](#hassize) | <span data-ttu-id="397bc-130">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="397bc-130">Has specified height and width values.</span></span>

## <span data-ttu-id="397bc-131">Участников</span><span class="sxs-lookup"><span data-stu-id="397bc-131">Members</span></span>

#### <span data-ttu-id="397bc-132">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="397bc-132">Height</span></span> 

<span data-ttu-id="397bc-133">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="397bc-133">The height of the window.</span></span>

> <span data-ttu-id="397bc-134">открытая [Высота](#height) с uint</span><span class="sxs-lookup"><span data-stu-id="397bc-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="397bc-135">Влево</span><span class="sxs-lookup"><span data-stu-id="397bc-135">Left</span></span> 

<span data-ttu-id="397bc-136">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="397bc-136">The left position of the window.</span></span>

> <span data-ttu-id="397bc-137">Открытый uint [слева](#left)</span><span class="sxs-lookup"><span data-stu-id="397bc-137">public uint [Left](#left)</span></span>

<span data-ttu-id="397bc-138">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="397bc-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="397bc-139">MenuBar</span><span class="sxs-lookup"><span data-stu-id="397bc-139">MenuBar</span></span> 

<span data-ttu-id="397bc-140">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="397bc-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="397bc-141">public int [Remenubar](#menubar)</span><span class="sxs-lookup"><span data-stu-id="397bc-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="397bc-142">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="397bc-142">ScrollBars</span></span> 

<span data-ttu-id="397bc-143">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="397bc-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="397bc-144">открытые [прокрутки](#scrollbars) int</span><span class="sxs-lookup"><span data-stu-id="397bc-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="397bc-145">Состояние</span><span class="sxs-lookup"><span data-stu-id="397bc-145">Status</span></span> 

<span data-ttu-id="397bc-146">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="397bc-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="397bc-147">общедоступный целочисленный [статус](#status)</span><span class="sxs-lookup"><span data-stu-id="397bc-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="397bc-148">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="397bc-148">Toolbar</span></span> 

<span data-ttu-id="397bc-149">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="397bc-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="397bc-150">общедоступная [панель инструментов](#toolbar) int</span><span class="sxs-lookup"><span data-stu-id="397bc-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="397bc-151">Top</span><span class="sxs-lookup"><span data-stu-id="397bc-151">Top</span></span> 

<span data-ttu-id="397bc-152">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="397bc-152">The top position of the window.</span></span>

> <span data-ttu-id="397bc-153">Открытый uint, [сверху](#top)</span><span class="sxs-lookup"><span data-stu-id="397bc-153">public uint [Top](#top)</span></span>

<span data-ttu-id="397bc-154">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="397bc-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="397bc-155">Ширина</span><span class="sxs-lookup"><span data-stu-id="397bc-155">Width</span></span> 

<span data-ttu-id="397bc-156">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="397bc-156">The width of the window.</span></span>

> <span data-ttu-id="397bc-157">открытая [Ширина](#width) с uint</span><span class="sxs-lookup"><span data-stu-id="397bc-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="397bc-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="397bc-158">HasPosition</span></span> 

<span data-ttu-id="397bc-159">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="397bc-159">Has specified left and top values.</span></span>

> <span data-ttu-id="397bc-160">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="397bc-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="397bc-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="397bc-161">HasSize</span></span> 

<span data-ttu-id="397bc-162">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="397bc-162">Has specified height and width values.</span></span>

> <span data-ttu-id="397bc-163">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="397bc-163">public int [HasSize](#hassize)()</span></span>

