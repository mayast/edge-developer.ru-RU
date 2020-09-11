---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Matrix4x4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 1ea98d55323e2f38dbac5e4e68ab2cfc437d16f1
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010980"
---
# <span data-ttu-id="6bb39-104">Структура 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Matrix4x4</span><span class="sxs-lookup"><span data-stu-id="6bb39-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2Matrix4x4 struct</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="6bb39-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6bb39-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6bb39-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6bb39-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6bb39-107">Это преобразование используется для вычисления правильных координат при вызове CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="6bb39-107">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span>

## <span data-ttu-id="6bb39-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6bb39-108">Summary</span></span>

 <span data-ttu-id="6bb39-109">Участников</span><span class="sxs-lookup"><span data-stu-id="6bb39-109">Members</span></span>                        | <span data-ttu-id="6bb39-110">Описания</span><span class="sxs-lookup"><span data-stu-id="6bb39-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6bb39-111">_11</span><span class="sxs-lookup"><span data-stu-id="6bb39-111">_11</span></span>](#_11) | <span data-ttu-id="6bb39-112">Значение в первой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-112">The value in the first row and first column of the matrix.</span></span>
[<span data-ttu-id="6bb39-113">_12</span><span class="sxs-lookup"><span data-stu-id="6bb39-113">_12</span></span>](#_12) | <span data-ttu-id="6bb39-114">Значение в первой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-114">The value in the first row and second column of the matrix.</span></span>
[<span data-ttu-id="6bb39-115">_13</span><span class="sxs-lookup"><span data-stu-id="6bb39-115">_13</span></span>](#_13) | <span data-ttu-id="6bb39-116">Значение в первой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-116">The value in the first row and third column of the matrix.</span></span>
[<span data-ttu-id="6bb39-117">_14</span><span class="sxs-lookup"><span data-stu-id="6bb39-117">_14</span></span>](#_14) | <span data-ttu-id="6bb39-118">Значение в первой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-118">The value in the first row and fourth column of the matrix.</span></span>
[<span data-ttu-id="6bb39-119">_21</span><span class="sxs-lookup"><span data-stu-id="6bb39-119">_21</span></span>](#_21) | <span data-ttu-id="6bb39-120">Значение во второй строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-120">The value in the second row and first column of the matrix.</span></span>
[<span data-ttu-id="6bb39-121">_22</span><span class="sxs-lookup"><span data-stu-id="6bb39-121">_22</span></span>](#_22) | <span data-ttu-id="6bb39-122">Значение во второй строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-122">The value in the second row and second column of the matrix.</span></span>
[<span data-ttu-id="6bb39-123">_23</span><span class="sxs-lookup"><span data-stu-id="6bb39-123">_23</span></span>](#_23) | <span data-ttu-id="6bb39-124">Значение в второй строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-124">The value in the second row and third column of the matrix.</span></span>
[<span data-ttu-id="6bb39-125">_24</span><span class="sxs-lookup"><span data-stu-id="6bb39-125">_24</span></span>](#_24) | <span data-ttu-id="6bb39-126">Значение во второй строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-126">The value in the second row and fourth column of the matrix.</span></span>
[<span data-ttu-id="6bb39-127">_31</span><span class="sxs-lookup"><span data-stu-id="6bb39-127">_31</span></span>](#_31) | <span data-ttu-id="6bb39-128">Значение в третьей строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-128">The value in the third row and first column of the matrix.</span></span>
[<span data-ttu-id="6bb39-129">_32</span><span class="sxs-lookup"><span data-stu-id="6bb39-129">_32</span></span>](#_32) | <span data-ttu-id="6bb39-130">Значение в третьей строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-130">The value in the third row and second column of the matrix.</span></span>
[<span data-ttu-id="6bb39-131">_33</span><span class="sxs-lookup"><span data-stu-id="6bb39-131">_33</span></span>](#_33) | <span data-ttu-id="6bb39-132">Значение в третьей строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-132">The value in the third row and third column of the matrix.</span></span>
[<span data-ttu-id="6bb39-133">_34</span><span class="sxs-lookup"><span data-stu-id="6bb39-133">_34</span></span>](#_34) | <span data-ttu-id="6bb39-134">Значение в третьей строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-134">The value in the third row and fourth column of the matrix.</span></span>
[<span data-ttu-id="6bb39-135">_41</span><span class="sxs-lookup"><span data-stu-id="6bb39-135">_41</span></span>](#_41) | <span data-ttu-id="6bb39-136">Значение в четвертой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-136">The value in the fourth row and first column of the matrix.</span></span>
[<span data-ttu-id="6bb39-137">_42</span><span class="sxs-lookup"><span data-stu-id="6bb39-137">_42</span></span>](#_42) | <span data-ttu-id="6bb39-138">Значение в четвертой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-138">The value in the fourth row and second column of the matrix.</span></span>
[<span data-ttu-id="6bb39-139">_43</span><span class="sxs-lookup"><span data-stu-id="6bb39-139">_43</span></span>](#_43) | <span data-ttu-id="6bb39-140">Значение в четвертой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-140">The value in the fourth row and third column of the matrix.</span></span>
[<span data-ttu-id="6bb39-141">_44</span><span class="sxs-lookup"><span data-stu-id="6bb39-141">_44</span></span>](#_44) | <span data-ttu-id="6bb39-142">Значение в четвертой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-142">The value in the fourth row and fourth column of the matrix.</span></span>

<span data-ttu-id="6bb39-143">Это эквивалентно D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="6bb39-143">This is equivalent to a D2D1_MATRIX_4X4_F.</span></span>

## <span data-ttu-id="6bb39-144">Участников</span><span class="sxs-lookup"><span data-stu-id="6bb39-144">Members</span></span>

#### <span data-ttu-id="6bb39-145">_11</span><span class="sxs-lookup"><span data-stu-id="6bb39-145">_11</span></span> 

<span data-ttu-id="6bb39-146">Значение в первой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-146">The value in the first row and first column of the matrix.</span></span>

> <span data-ttu-id="6bb39-147">общедоступная единая [_11](#_11)</span><span class="sxs-lookup"><span data-stu-id="6bb39-147">public Single [_11](#_11)</span></span>

#### <span data-ttu-id="6bb39-148">_12</span><span class="sxs-lookup"><span data-stu-id="6bb39-148">_12</span></span> 

<span data-ttu-id="6bb39-149">Значение в первой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-149">The value in the first row and second column of the matrix.</span></span>

> <span data-ttu-id="6bb39-150">общедоступная единая [_12](#_12)</span><span class="sxs-lookup"><span data-stu-id="6bb39-150">public Single [_12](#_12)</span></span>

#### <span data-ttu-id="6bb39-151">_13</span><span class="sxs-lookup"><span data-stu-id="6bb39-151">_13</span></span> 

<span data-ttu-id="6bb39-152">Значение в первой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-152">The value in the first row and third column of the matrix.</span></span>

> <span data-ttu-id="6bb39-153">общедоступная единая [_13](#_13)</span><span class="sxs-lookup"><span data-stu-id="6bb39-153">public Single [_13](#_13)</span></span>

#### <span data-ttu-id="6bb39-154">_14</span><span class="sxs-lookup"><span data-stu-id="6bb39-154">_14</span></span> 

<span data-ttu-id="6bb39-155">Значение в первой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-155">The value in the first row and fourth column of the matrix.</span></span>

> <span data-ttu-id="6bb39-156">общедоступная единая [_14](#_14)</span><span class="sxs-lookup"><span data-stu-id="6bb39-156">public Single [_14](#_14)</span></span>

#### <span data-ttu-id="6bb39-157">_21</span><span class="sxs-lookup"><span data-stu-id="6bb39-157">_21</span></span> 

<span data-ttu-id="6bb39-158">Значение во второй строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-158">The value in the second row and first column of the matrix.</span></span>

> <span data-ttu-id="6bb39-159">общедоступная единая [_21](#_21)</span><span class="sxs-lookup"><span data-stu-id="6bb39-159">public Single [_21](#_21)</span></span>

#### <span data-ttu-id="6bb39-160">_22</span><span class="sxs-lookup"><span data-stu-id="6bb39-160">_22</span></span> 

<span data-ttu-id="6bb39-161">Значение во второй строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-161">The value in the second row and second column of the matrix.</span></span>

> <span data-ttu-id="6bb39-162">общедоступная единая [_22](#_22)</span><span class="sxs-lookup"><span data-stu-id="6bb39-162">public Single [_22](#_22)</span></span>

#### <span data-ttu-id="6bb39-163">_23</span><span class="sxs-lookup"><span data-stu-id="6bb39-163">_23</span></span> 

<span data-ttu-id="6bb39-164">Значение в второй строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-164">The value in the second row and third column of the matrix.</span></span>

> <span data-ttu-id="6bb39-165">общедоступная единая [_23](#_23)</span><span class="sxs-lookup"><span data-stu-id="6bb39-165">public Single [_23](#_23)</span></span>

#### <span data-ttu-id="6bb39-166">_24</span><span class="sxs-lookup"><span data-stu-id="6bb39-166">_24</span></span> 

<span data-ttu-id="6bb39-167">Значение во второй строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-167">The value in the second row and fourth column of the matrix.</span></span>

> <span data-ttu-id="6bb39-168">общедоступная единая [_24](#_24)</span><span class="sxs-lookup"><span data-stu-id="6bb39-168">public Single [_24](#_24)</span></span>

#### <span data-ttu-id="6bb39-169">_31</span><span class="sxs-lookup"><span data-stu-id="6bb39-169">_31</span></span> 

<span data-ttu-id="6bb39-170">Значение в третьей строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-170">The value in the third row and first column of the matrix.</span></span>

> <span data-ttu-id="6bb39-171">общедоступная единая [_31](#_31)</span><span class="sxs-lookup"><span data-stu-id="6bb39-171">public Single [_31](#_31)</span></span>

#### <span data-ttu-id="6bb39-172">_32</span><span class="sxs-lookup"><span data-stu-id="6bb39-172">_32</span></span> 

<span data-ttu-id="6bb39-173">Значение в третьей строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-173">The value in the third row and second column of the matrix.</span></span>

> <span data-ttu-id="6bb39-174">общедоступная единая [_32](#_32)</span><span class="sxs-lookup"><span data-stu-id="6bb39-174">public Single [_32](#_32)</span></span>

#### <span data-ttu-id="6bb39-175">_33</span><span class="sxs-lookup"><span data-stu-id="6bb39-175">_33</span></span> 

<span data-ttu-id="6bb39-176">Значение в третьей строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-176">The value in the third row and third column of the matrix.</span></span>

> <span data-ttu-id="6bb39-177">общедоступная единая [_33](#_33)</span><span class="sxs-lookup"><span data-stu-id="6bb39-177">public Single [_33](#_33)</span></span>

#### <span data-ttu-id="6bb39-178">_34</span><span class="sxs-lookup"><span data-stu-id="6bb39-178">_34</span></span> 

<span data-ttu-id="6bb39-179">Значение в третьей строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-179">The value in the third row and fourth column of the matrix.</span></span>

> <span data-ttu-id="6bb39-180">общедоступная единая [_34](#_34)</span><span class="sxs-lookup"><span data-stu-id="6bb39-180">public Single [_34](#_34)</span></span>

#### <span data-ttu-id="6bb39-181">_41</span><span class="sxs-lookup"><span data-stu-id="6bb39-181">_41</span></span> 

<span data-ttu-id="6bb39-182">Значение в четвертой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-182">The value in the fourth row and first column of the matrix.</span></span>

> <span data-ttu-id="6bb39-183">общедоступная единая [_41](#_41)</span><span class="sxs-lookup"><span data-stu-id="6bb39-183">public Single [_41](#_41)</span></span>

#### <span data-ttu-id="6bb39-184">_42</span><span class="sxs-lookup"><span data-stu-id="6bb39-184">_42</span></span> 

<span data-ttu-id="6bb39-185">Значение в четвертой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-185">The value in the fourth row and second column of the matrix.</span></span>

> <span data-ttu-id="6bb39-186">общедоступная единая [_42](#_42)</span><span class="sxs-lookup"><span data-stu-id="6bb39-186">public Single [_42](#_42)</span></span>

#### <span data-ttu-id="6bb39-187">_43</span><span class="sxs-lookup"><span data-stu-id="6bb39-187">_43</span></span> 

<span data-ttu-id="6bb39-188">Значение в четвертой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-188">The value in the fourth row and third column of the matrix.</span></span>

> <span data-ttu-id="6bb39-189">общедоступная единая [_43](#_43)</span><span class="sxs-lookup"><span data-stu-id="6bb39-189">public Single [_43](#_43)</span></span>

#### <span data-ttu-id="6bb39-190">_44</span><span class="sxs-lookup"><span data-stu-id="6bb39-190">_44</span></span> 

<span data-ttu-id="6bb39-191">Значение в четвертой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="6bb39-191">The value in the fourth row and fourth column of the matrix.</span></span>

> <span data-ttu-id="6bb39-192">общедоступная единая [_44](#_44)</span><span class="sxs-lookup"><span data-stu-id="6bb39-192">public Single [_44](#_44)</span></span>

