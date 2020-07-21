---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: d6d6f52456823488c07288c8ed07b9655a29883a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884439"
---
# <span data-ttu-id="34b1f-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="34b1f-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="34b1f-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="34b1f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="34b1f-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="34b1f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="34b1f-107">Функции окна для всплывающего окна WebView.</span><span class="sxs-lookup"><span data-stu-id="34b1f-107">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="34b1f-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="34b1f-108">Summary</span></span>

 <span data-ttu-id="34b1f-109">Участников</span><span class="sxs-lookup"><span data-stu-id="34b1f-109">Members</span></span>                        | <span data-ttu-id="34b1f-110">Описания</span><span class="sxs-lookup"><span data-stu-id="34b1f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="34b1f-111">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="34b1f-111">Height</span></span>](#height) | <span data-ttu-id="34b1f-112">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="34b1f-112">The height of the window.</span></span>
[<span data-ttu-id="34b1f-113">Влево</span><span class="sxs-lookup"><span data-stu-id="34b1f-113">Left</span></span>](#left) | <span data-ttu-id="34b1f-114">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="34b1f-114">The left position of the window.</span></span>
[<span data-ttu-id="34b1f-115">MenuBar</span><span class="sxs-lookup"><span data-stu-id="34b1f-115">MenuBar</span></span>](#menubar) | <span data-ttu-id="34b1f-116">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="34b1f-116">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="34b1f-117">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="34b1f-117">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="34b1f-118">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="34b1f-118">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="34b1f-119">Состояние</span><span class="sxs-lookup"><span data-stu-id="34b1f-119">Status</span></span>](#status) | <span data-ttu-id="34b1f-120">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="34b1f-120">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="34b1f-121">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="34b1f-121">Toolbar</span></span>](#toolbar) | <span data-ttu-id="34b1f-122">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="34b1f-122">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="34b1f-123">Top</span><span class="sxs-lookup"><span data-stu-id="34b1f-123">Top</span></span>](#top) | <span data-ttu-id="34b1f-124">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="34b1f-124">The top position of the window.</span></span>
[<span data-ttu-id="34b1f-125">Ширина</span><span class="sxs-lookup"><span data-stu-id="34b1f-125">Width</span></span>](#width) | <span data-ttu-id="34b1f-126">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="34b1f-126">The width of the window.</span></span>
[<span data-ttu-id="34b1f-127">HasPosition</span><span class="sxs-lookup"><span data-stu-id="34b1f-127">HasPosition</span></span>](#hasposition) | <span data-ttu-id="34b1f-128">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="34b1f-128">Has specified left and top values.</span></span>
[<span data-ttu-id="34b1f-129">HasSize</span><span class="sxs-lookup"><span data-stu-id="34b1f-129">HasSize</span></span>](#hassize) | <span data-ttu-id="34b1f-130">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="34b1f-130">Has specified height and width values.</span></span>

## <span data-ttu-id="34b1f-131">Участников</span><span class="sxs-lookup"><span data-stu-id="34b1f-131">Members</span></span>

#### <span data-ttu-id="34b1f-132">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="34b1f-132">Height</span></span> 

<span data-ttu-id="34b1f-133">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="34b1f-133">The height of the window.</span></span>

> <span data-ttu-id="34b1f-134">открытая [Высота](#height) с uint</span><span class="sxs-lookup"><span data-stu-id="34b1f-134">public uint [Height](#height)</span></span>

#### <span data-ttu-id="34b1f-135">Влево</span><span class="sxs-lookup"><span data-stu-id="34b1f-135">Left</span></span> 

<span data-ttu-id="34b1f-136">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="34b1f-136">The left position of the window.</span></span>

> <span data-ttu-id="34b1f-137">Открытый uint [слева](#left)</span><span class="sxs-lookup"><span data-stu-id="34b1f-137">public uint [Left](#left)</span></span>

<span data-ttu-id="34b1f-138">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="34b1f-138">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="34b1f-139">MenuBar</span><span class="sxs-lookup"><span data-stu-id="34b1f-139">MenuBar</span></span> 

<span data-ttu-id="34b1f-140">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="34b1f-140">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="34b1f-141">public int [Remenubar](#menubar)</span><span class="sxs-lookup"><span data-stu-id="34b1f-141">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="34b1f-142">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="34b1f-142">ScrollBars</span></span> 

<span data-ttu-id="34b1f-143">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="34b1f-143">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="34b1f-144">открытые [прокрутки](#scrollbars) int</span><span class="sxs-lookup"><span data-stu-id="34b1f-144">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="34b1f-145">Состояние</span><span class="sxs-lookup"><span data-stu-id="34b1f-145">Status</span></span> 

<span data-ttu-id="34b1f-146">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="34b1f-146">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="34b1f-147">общедоступный целочисленный [статус](#status)</span><span class="sxs-lookup"><span data-stu-id="34b1f-147">public int [Status](#status)</span></span>

#### <span data-ttu-id="34b1f-148">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="34b1f-148">Toolbar</span></span> 

<span data-ttu-id="34b1f-149">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="34b1f-149">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="34b1f-150">общедоступная [панель инструментов](#toolbar) int</span><span class="sxs-lookup"><span data-stu-id="34b1f-150">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="34b1f-151">Top</span><span class="sxs-lookup"><span data-stu-id="34b1f-151">Top</span></span> 

<span data-ttu-id="34b1f-152">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="34b1f-152">The top position of the window.</span></span>

> <span data-ttu-id="34b1f-153">Открытый uint, [сверху](#top)</span><span class="sxs-lookup"><span data-stu-id="34b1f-153">public uint [Top](#top)</span></span>

<span data-ttu-id="34b1f-154">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="34b1f-154">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="34b1f-155">Ширина</span><span class="sxs-lookup"><span data-stu-id="34b1f-155">Width</span></span> 

<span data-ttu-id="34b1f-156">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="34b1f-156">The width of the window.</span></span>

> <span data-ttu-id="34b1f-157">открытая [Ширина](#width) с uint</span><span class="sxs-lookup"><span data-stu-id="34b1f-157">public uint [Width](#width)</span></span>

#### <span data-ttu-id="34b1f-158">HasPosition</span><span class="sxs-lookup"><span data-stu-id="34b1f-158">HasPosition</span></span> 

<span data-ttu-id="34b1f-159">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="34b1f-159">Has specified left and top values.</span></span>

> <span data-ttu-id="34b1f-160">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="34b1f-160">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="34b1f-161">HasSize</span><span class="sxs-lookup"><span data-stu-id="34b1f-161">HasSize</span></span> 

<span data-ttu-id="34b1f-162">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="34b1f-162">Has specified height and width values.</span></span>

> <span data-ttu-id="34b1f-163">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="34b1f-163">public int [HasSize](#hassize)()</span></span>

