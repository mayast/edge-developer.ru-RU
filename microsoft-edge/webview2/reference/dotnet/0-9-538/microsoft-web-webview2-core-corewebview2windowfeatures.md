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
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699273"
---
# <span data-ttu-id="03a4c-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="03a4c-104">Microsoft.Web.WebView2.Core.CoreWebView2WindowFeatures class</span></span> 

> [!NOTE]
> <span data-ttu-id="03a4c-105">Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="03a4c-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="03a4c-106">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="03a4c-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="03a4c-107">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="03a4c-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="03a4c-108">Функции окна для всплывающего окна WebView.</span><span class="sxs-lookup"><span data-stu-id="03a4c-108">Window features for a WebView popup window.</span></span>

## <span data-ttu-id="03a4c-109">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="03a4c-109">Summary</span></span>

 <span data-ttu-id="03a4c-110">Участников</span><span class="sxs-lookup"><span data-stu-id="03a4c-110">Members</span></span>                        | <span data-ttu-id="03a4c-111">Описания</span><span class="sxs-lookup"><span data-stu-id="03a4c-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="03a4c-112">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="03a4c-112">Height</span></span>](#height) | <span data-ttu-id="03a4c-113">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="03a4c-113">The height of the window.</span></span>
[<span data-ttu-id="03a4c-114">Влево</span><span class="sxs-lookup"><span data-stu-id="03a4c-114">Left</span></span>](#left) | <span data-ttu-id="03a4c-115">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="03a4c-115">The left position of the window.</span></span>
[<span data-ttu-id="03a4c-116">MenuBar</span><span class="sxs-lookup"><span data-stu-id="03a4c-116">MenuBar</span></span>](#menubar) | <span data-ttu-id="03a4c-117">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="03a4c-117">Whether or not to display the menu bar.</span></span>
[<span data-ttu-id="03a4c-118">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="03a4c-118">ScrollBars</span></span>](#scrollbars) | <span data-ttu-id="03a4c-119">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="03a4c-119">Whether or not to display scroll bars.</span></span>
[<span data-ttu-id="03a4c-120">Состояние</span><span class="sxs-lookup"><span data-stu-id="03a4c-120">Status</span></span>](#status) | <span data-ttu-id="03a4c-121">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="03a4c-121">Whether or not to add a status bar.</span></span>
[<span data-ttu-id="03a4c-122">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="03a4c-122">Toolbar</span></span>](#toolbar) | <span data-ttu-id="03a4c-123">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="03a4c-123">Whether or not to display the browser toolbar.</span></span>
[<span data-ttu-id="03a4c-124">Top</span><span class="sxs-lookup"><span data-stu-id="03a4c-124">Top</span></span>](#top) | <span data-ttu-id="03a4c-125">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="03a4c-125">The top position of the window.</span></span>
[<span data-ttu-id="03a4c-126">Ширина</span><span class="sxs-lookup"><span data-stu-id="03a4c-126">Width</span></span>](#width) | <span data-ttu-id="03a4c-127">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="03a4c-127">The width of the window.</span></span>
[<span data-ttu-id="03a4c-128">HasPosition</span><span class="sxs-lookup"><span data-stu-id="03a4c-128">HasPosition</span></span>](#hasposition) | <span data-ttu-id="03a4c-129">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="03a4c-129">Has specified left and top values.</span></span>
[<span data-ttu-id="03a4c-130">HasSize</span><span class="sxs-lookup"><span data-stu-id="03a4c-130">HasSize</span></span>](#hassize) | <span data-ttu-id="03a4c-131">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="03a4c-131">Has specified height and width values.</span></span>

## <span data-ttu-id="03a4c-132">Участников</span><span class="sxs-lookup"><span data-stu-id="03a4c-132">Members</span></span>

#### <span data-ttu-id="03a4c-133">Полноразмерных</span><span class="sxs-lookup"><span data-stu-id="03a4c-133">Height</span></span> 

<span data-ttu-id="03a4c-134">Высота окна.</span><span class="sxs-lookup"><span data-stu-id="03a4c-134">The height of the window.</span></span>

> <span data-ttu-id="03a4c-135">открытая [Высота](#height) с uint</span><span class="sxs-lookup"><span data-stu-id="03a4c-135">public uint [Height](#height)</span></span>

#### <span data-ttu-id="03a4c-136">Влево</span><span class="sxs-lookup"><span data-stu-id="03a4c-136">Left</span></span> 

<span data-ttu-id="03a4c-137">Левое расположение окна.</span><span class="sxs-lookup"><span data-stu-id="03a4c-137">The left position of the window.</span></span>

> <span data-ttu-id="03a4c-138">Открытый uint [слева](#left)</span><span class="sxs-lookup"><span data-stu-id="03a4c-138">public uint [Left](#left)</span></span>

<span data-ttu-id="03a4c-139">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="03a4c-139">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="03a4c-140">MenuBar</span><span class="sxs-lookup"><span data-stu-id="03a4c-140">MenuBar</span></span> 

<span data-ttu-id="03a4c-141">Указывает, следует ли отображать строку меню.</span><span class="sxs-lookup"><span data-stu-id="03a4c-141">Whether or not to display the menu bar.</span></span>

> <span data-ttu-id="03a4c-142">public int [Remenubar](#menubar)</span><span class="sxs-lookup"><span data-stu-id="03a4c-142">public int [MenuBar](#menubar)</span></span>

#### <span data-ttu-id="03a4c-143">Полосы прокрутки</span><span class="sxs-lookup"><span data-stu-id="03a4c-143">ScrollBars</span></span> 

<span data-ttu-id="03a4c-144">Указывает, следует ли отображать полосы прокрутки.</span><span class="sxs-lookup"><span data-stu-id="03a4c-144">Whether or not to display scroll bars.</span></span>

> <span data-ttu-id="03a4c-145">открытые [прокрутки](#scrollbars) int</span><span class="sxs-lookup"><span data-stu-id="03a4c-145">public int [ScrollBars](#scrollbars)</span></span>

#### <span data-ttu-id="03a4c-146">Состояние</span><span class="sxs-lookup"><span data-stu-id="03a4c-146">Status</span></span> 

<span data-ttu-id="03a4c-147">Следует ли добавить строку состояния.</span><span class="sxs-lookup"><span data-stu-id="03a4c-147">Whether or not to add a status bar.</span></span>

> <span data-ttu-id="03a4c-148">общедоступный целочисленный [статус](#status)</span><span class="sxs-lookup"><span data-stu-id="03a4c-148">public int [Status](#status)</span></span>

#### <span data-ttu-id="03a4c-149">панель инструментов;</span><span class="sxs-lookup"><span data-stu-id="03a4c-149">Toolbar</span></span> 

<span data-ttu-id="03a4c-150">Указывает, следует ли отображать панель инструментов браузера.</span><span class="sxs-lookup"><span data-stu-id="03a4c-150">Whether or not to display the browser toolbar.</span></span>

> <span data-ttu-id="03a4c-151">общедоступная [панель инструментов](#toolbar) int</span><span class="sxs-lookup"><span data-stu-id="03a4c-151">public int [Toolbar](#toolbar)</span></span>

#### <span data-ttu-id="03a4c-152">Top</span><span class="sxs-lookup"><span data-stu-id="03a4c-152">Top</span></span> 

<span data-ttu-id="03a4c-153">Верхнее расположение окна.</span><span class="sxs-lookup"><span data-stu-id="03a4c-153">The top position of the window.</span></span>

> <span data-ttu-id="03a4c-154">Открытый uint, [сверху](#top)</span><span class="sxs-lookup"><span data-stu-id="03a4c-154">public uint [Top](#top)</span></span>

<span data-ttu-id="03a4c-155">Если HasPosition имеет значение false, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="03a4c-155">Will fail if HasPosition is false.</span></span>

#### <span data-ttu-id="03a4c-156">Ширина</span><span class="sxs-lookup"><span data-stu-id="03a4c-156">Width</span></span> 

<span data-ttu-id="03a4c-157">Ширина окна.</span><span class="sxs-lookup"><span data-stu-id="03a4c-157">The width of the window.</span></span>

> <span data-ttu-id="03a4c-158">открытая [Ширина](#width) с uint</span><span class="sxs-lookup"><span data-stu-id="03a4c-158">public uint [Width](#width)</span></span>

#### <span data-ttu-id="03a4c-159">HasPosition</span><span class="sxs-lookup"><span data-stu-id="03a4c-159">HasPosition</span></span> 

<span data-ttu-id="03a4c-160">Заданные значения Left и Top.</span><span class="sxs-lookup"><span data-stu-id="03a4c-160">Has specified left and top values.</span></span>

> <span data-ttu-id="03a4c-161">public int [HasPosition](#hasposition)()</span><span class="sxs-lookup"><span data-stu-id="03a4c-161">public int [HasPosition](#hasposition)()</span></span>

#### <span data-ttu-id="03a4c-162">HasSize</span><span class="sxs-lookup"><span data-stu-id="03a4c-162">HasSize</span></span> 

<span data-ttu-id="03a4c-163">Заданные значения Height и Width.</span><span class="sxs-lookup"><span data-stu-id="03a4c-163">Has specified height and width values.</span></span>

> <span data-ttu-id="03a4c-164">public int [HasSize](#hassize)()</span><span class="sxs-lookup"><span data-stu-id="03a4c-164">public int [HasSize](#hassize)()</span></span>

