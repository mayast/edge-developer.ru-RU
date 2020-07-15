---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Matrix4x4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: bac470b29b08357d27ba77e986f19739acaaa05d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878878"
---
# <span data-ttu-id="7513e-104">Структура Microsoft. Web. WebView2. Core. CoreWebView2Matrix4x4</span><span class="sxs-lookup"><span data-stu-id="7513e-104">Microsoft.Web.WebView2.Core.CoreWebView2Matrix4x4 struct</span></span> 

> [!NOTE]
> <span data-ttu-id="7513e-105">Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="7513e-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="7513e-106">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7513e-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7513e-107">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="7513e-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7513e-108">Это преобразование используется для вычисления правильных координат при вызове CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="7513e-108">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span>

## <span data-ttu-id="7513e-109">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7513e-109">Summary</span></span>

 <span data-ttu-id="7513e-110">Участников</span><span class="sxs-lookup"><span data-stu-id="7513e-110">Members</span></span>                        | <span data-ttu-id="7513e-111">Описания</span><span class="sxs-lookup"><span data-stu-id="7513e-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7513e-112">_11</span><span class="sxs-lookup"><span data-stu-id="7513e-112">_11</span></span>](#_11) | <span data-ttu-id="7513e-113">Значение в первой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-113">The value in the first row and first column of the matrix.</span></span>
[<span data-ttu-id="7513e-114">_12</span><span class="sxs-lookup"><span data-stu-id="7513e-114">_12</span></span>](#_12) | <span data-ttu-id="7513e-115">Значение в первой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-115">The value in the first row and second column of the matrix.</span></span>
[<span data-ttu-id="7513e-116">_13</span><span class="sxs-lookup"><span data-stu-id="7513e-116">_13</span></span>](#_13) | <span data-ttu-id="7513e-117">Значение в первой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-117">The value in the first row and third column of the matrix.</span></span>
[<span data-ttu-id="7513e-118">_14</span><span class="sxs-lookup"><span data-stu-id="7513e-118">_14</span></span>](#_14) | <span data-ttu-id="7513e-119">Значение в первой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-119">The value in the first row and fourth column of the matrix.</span></span>
[<span data-ttu-id="7513e-120">_21</span><span class="sxs-lookup"><span data-stu-id="7513e-120">_21</span></span>](#_21) | <span data-ttu-id="7513e-121">Значение во второй строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-121">The value in the second row and first column of the matrix.</span></span>
[<span data-ttu-id="7513e-122">_22</span><span class="sxs-lookup"><span data-stu-id="7513e-122">_22</span></span>](#_22) | <span data-ttu-id="7513e-123">Значение во второй строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-123">The value in the second row and second column of the matrix.</span></span>
[<span data-ttu-id="7513e-124">_23</span><span class="sxs-lookup"><span data-stu-id="7513e-124">_23</span></span>](#_23) | <span data-ttu-id="7513e-125">Значение в второй строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-125">The value in the second row and third column of the matrix.</span></span>
[<span data-ttu-id="7513e-126">_24</span><span class="sxs-lookup"><span data-stu-id="7513e-126">_24</span></span>](#_24) | <span data-ttu-id="7513e-127">Значение во второй строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-127">The value in the second row and fourth column of the matrix.</span></span>
[<span data-ttu-id="7513e-128">_31</span><span class="sxs-lookup"><span data-stu-id="7513e-128">_31</span></span>](#_31) | <span data-ttu-id="7513e-129">Значение в третьей строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-129">The value in the third row and first column of the matrix.</span></span>
[<span data-ttu-id="7513e-130">_32</span><span class="sxs-lookup"><span data-stu-id="7513e-130">_32</span></span>](#_32) | <span data-ttu-id="7513e-131">Значение в третьей строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-131">The value in the third row and second column of the matrix.</span></span>
[<span data-ttu-id="7513e-132">_33</span><span class="sxs-lookup"><span data-stu-id="7513e-132">_33</span></span>](#_33) | <span data-ttu-id="7513e-133">Значение в третьей строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-133">The value in the third row and third column of the matrix.</span></span>
[<span data-ttu-id="7513e-134">_34</span><span class="sxs-lookup"><span data-stu-id="7513e-134">_34</span></span>](#_34) | <span data-ttu-id="7513e-135">Значение в третьей строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-135">The value in the third row and fourth column of the matrix.</span></span>
[<span data-ttu-id="7513e-136">_41</span><span class="sxs-lookup"><span data-stu-id="7513e-136">_41</span></span>](#_41) | <span data-ttu-id="7513e-137">Значение в четвертой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-137">The value in the fourth row and first column of the matrix.</span></span>
[<span data-ttu-id="7513e-138">_42</span><span class="sxs-lookup"><span data-stu-id="7513e-138">_42</span></span>](#_42) | <span data-ttu-id="7513e-139">Значение в четвертой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-139">The value in the fourth row and second column of the matrix.</span></span>
[<span data-ttu-id="7513e-140">_43</span><span class="sxs-lookup"><span data-stu-id="7513e-140">_43</span></span>](#_43) | <span data-ttu-id="7513e-141">Значение в четвертой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-141">The value in the fourth row and third column of the matrix.</span></span>
[<span data-ttu-id="7513e-142">_44</span><span class="sxs-lookup"><span data-stu-id="7513e-142">_44</span></span>](#_44) | <span data-ttu-id="7513e-143">Значение в четвертой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-143">The value in the fourth row and fourth column of the matrix.</span></span>

<span data-ttu-id="7513e-144">Это эквивалентно D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="7513e-144">This is equivalent to a D2D1_MATRIX_4X4_F.</span></span>

## <span data-ttu-id="7513e-145">Участников</span><span class="sxs-lookup"><span data-stu-id="7513e-145">Members</span></span>

#### <span data-ttu-id="7513e-146">_11</span><span class="sxs-lookup"><span data-stu-id="7513e-146">_11</span></span> 

<span data-ttu-id="7513e-147">Значение в первой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-147">The value in the first row and first column of the matrix.</span></span>

> <span data-ttu-id="7513e-148">общедоступная единая [_11](#_11)</span><span class="sxs-lookup"><span data-stu-id="7513e-148">public Single [_11](#_11)</span></span>

#### <span data-ttu-id="7513e-149">_12</span><span class="sxs-lookup"><span data-stu-id="7513e-149">_12</span></span> 

<span data-ttu-id="7513e-150">Значение в первой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-150">The value in the first row and second column of the matrix.</span></span>

> <span data-ttu-id="7513e-151">общедоступная единая [_12](#_12)</span><span class="sxs-lookup"><span data-stu-id="7513e-151">public Single [_12](#_12)</span></span>

#### <span data-ttu-id="7513e-152">_13</span><span class="sxs-lookup"><span data-stu-id="7513e-152">_13</span></span> 

<span data-ttu-id="7513e-153">Значение в первой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-153">The value in the first row and third column of the matrix.</span></span>

> <span data-ttu-id="7513e-154">общедоступная единая [_13](#_13)</span><span class="sxs-lookup"><span data-stu-id="7513e-154">public Single [_13](#_13)</span></span>

#### <span data-ttu-id="7513e-155">_14</span><span class="sxs-lookup"><span data-stu-id="7513e-155">_14</span></span> 

<span data-ttu-id="7513e-156">Значение в первой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-156">The value in the first row and fourth column of the matrix.</span></span>

> <span data-ttu-id="7513e-157">общедоступная единая [_14](#_14)</span><span class="sxs-lookup"><span data-stu-id="7513e-157">public Single [_14](#_14)</span></span>

#### <span data-ttu-id="7513e-158">_21</span><span class="sxs-lookup"><span data-stu-id="7513e-158">_21</span></span> 

<span data-ttu-id="7513e-159">Значение во второй строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-159">The value in the second row and first column of the matrix.</span></span>

> <span data-ttu-id="7513e-160">общедоступная единая [_21](#_21)</span><span class="sxs-lookup"><span data-stu-id="7513e-160">public Single [_21](#_21)</span></span>

#### <span data-ttu-id="7513e-161">_22</span><span class="sxs-lookup"><span data-stu-id="7513e-161">_22</span></span> 

<span data-ttu-id="7513e-162">Значение во второй строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-162">The value in the second row and second column of the matrix.</span></span>

> <span data-ttu-id="7513e-163">общедоступная единая [_22](#_22)</span><span class="sxs-lookup"><span data-stu-id="7513e-163">public Single [_22](#_22)</span></span>

#### <span data-ttu-id="7513e-164">_23</span><span class="sxs-lookup"><span data-stu-id="7513e-164">_23</span></span> 

<span data-ttu-id="7513e-165">Значение в второй строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-165">The value in the second row and third column of the matrix.</span></span>

> <span data-ttu-id="7513e-166">общедоступная единая [_23](#_23)</span><span class="sxs-lookup"><span data-stu-id="7513e-166">public Single [_23](#_23)</span></span>

#### <span data-ttu-id="7513e-167">_24</span><span class="sxs-lookup"><span data-stu-id="7513e-167">_24</span></span> 

<span data-ttu-id="7513e-168">Значение во второй строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-168">The value in the second row and fourth column of the matrix.</span></span>

> <span data-ttu-id="7513e-169">общедоступная единая [_24](#_24)</span><span class="sxs-lookup"><span data-stu-id="7513e-169">public Single [_24](#_24)</span></span>

#### <span data-ttu-id="7513e-170">_31</span><span class="sxs-lookup"><span data-stu-id="7513e-170">_31</span></span> 

<span data-ttu-id="7513e-171">Значение в третьей строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-171">The value in the third row and first column of the matrix.</span></span>

> <span data-ttu-id="7513e-172">общедоступная единая [_31](#_31)</span><span class="sxs-lookup"><span data-stu-id="7513e-172">public Single [_31](#_31)</span></span>

#### <span data-ttu-id="7513e-173">_32</span><span class="sxs-lookup"><span data-stu-id="7513e-173">_32</span></span> 

<span data-ttu-id="7513e-174">Значение в третьей строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-174">The value in the third row and second column of the matrix.</span></span>

> <span data-ttu-id="7513e-175">общедоступная единая [_32](#_32)</span><span class="sxs-lookup"><span data-stu-id="7513e-175">public Single [_32](#_32)</span></span>

#### <span data-ttu-id="7513e-176">_33</span><span class="sxs-lookup"><span data-stu-id="7513e-176">_33</span></span> 

<span data-ttu-id="7513e-177">Значение в третьей строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-177">The value in the third row and third column of the matrix.</span></span>

> <span data-ttu-id="7513e-178">общедоступная единая [_33](#_33)</span><span class="sxs-lookup"><span data-stu-id="7513e-178">public Single [_33](#_33)</span></span>

#### <span data-ttu-id="7513e-179">_34</span><span class="sxs-lookup"><span data-stu-id="7513e-179">_34</span></span> 

<span data-ttu-id="7513e-180">Значение в третьей строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-180">The value in the third row and fourth column of the matrix.</span></span>

> <span data-ttu-id="7513e-181">общедоступная единая [_34](#_34)</span><span class="sxs-lookup"><span data-stu-id="7513e-181">public Single [_34](#_34)</span></span>

#### <span data-ttu-id="7513e-182">_41</span><span class="sxs-lookup"><span data-stu-id="7513e-182">_41</span></span> 

<span data-ttu-id="7513e-183">Значение в четвертой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-183">The value in the fourth row and first column of the matrix.</span></span>

> <span data-ttu-id="7513e-184">общедоступная единая [_41](#_41)</span><span class="sxs-lookup"><span data-stu-id="7513e-184">public Single [_41](#_41)</span></span>

#### <span data-ttu-id="7513e-185">_42</span><span class="sxs-lookup"><span data-stu-id="7513e-185">_42</span></span> 

<span data-ttu-id="7513e-186">Значение в четвертой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-186">The value in the fourth row and second column of the matrix.</span></span>

> <span data-ttu-id="7513e-187">общедоступная единая [_42](#_42)</span><span class="sxs-lookup"><span data-stu-id="7513e-187">public Single [_42](#_42)</span></span>

#### <span data-ttu-id="7513e-188">_43</span><span class="sxs-lookup"><span data-stu-id="7513e-188">_43</span></span> 

<span data-ttu-id="7513e-189">Значение в четвертой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-189">The value in the fourth row and third column of the matrix.</span></span>

> <span data-ttu-id="7513e-190">общедоступная единая [_43](#_43)</span><span class="sxs-lookup"><span data-stu-id="7513e-190">public Single [_43](#_43)</span></span>

#### <span data-ttu-id="7513e-191">_44</span><span class="sxs-lookup"><span data-stu-id="7513e-191">_44</span></span> 

<span data-ttu-id="7513e-192">Значение в четвертой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="7513e-192">The value in the fourth row and fourth column of the matrix.</span></span>

> <span data-ttu-id="7513e-193">общедоступная единая [_44](#_44)</span><span class="sxs-lookup"><span data-stu-id="7513e-193">public Single [_44](#_44)</span></span>

