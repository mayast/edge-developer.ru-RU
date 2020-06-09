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
ms.openlocfilehash: e8563bdd77972945a1e4b81662071d07d1efeb02
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699160"
---
# <span data-ttu-id="204c7-104">Структура Microsoft. Web. WebView2. Core. CoreWebView2Matrix4x4</span><span class="sxs-lookup"><span data-stu-id="204c7-104">Microsoft.Web.WebView2.Core.CoreWebView2Matrix4x4 struct</span></span> 

> [!NOTE]
> <span data-ttu-id="204c7-105">Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="204c7-105">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="204c7-106">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="204c7-106">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="204c7-107">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="204c7-107">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="204c7-108">Это преобразование используется для вычисления правильных координат при вызове CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="204c7-108">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span>

## <span data-ttu-id="204c7-109">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="204c7-109">Summary</span></span>

 <span data-ttu-id="204c7-110">Участников</span><span class="sxs-lookup"><span data-stu-id="204c7-110">Members</span></span>                        | <span data-ttu-id="204c7-111">Описания</span><span class="sxs-lookup"><span data-stu-id="204c7-111">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="204c7-112">_11</span><span class="sxs-lookup"><span data-stu-id="204c7-112">_11</span></span>](#_11) | <span data-ttu-id="204c7-113">Значение в первой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-113">The value in the first row and first column of the matrix.</span></span>
[<span data-ttu-id="204c7-114">_12</span><span class="sxs-lookup"><span data-stu-id="204c7-114">_12</span></span>](#_12) | <span data-ttu-id="204c7-115">Значение в первой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-115">The value in the first row and second column of the matrix.</span></span>
[<span data-ttu-id="204c7-116">_13</span><span class="sxs-lookup"><span data-stu-id="204c7-116">_13</span></span>](#_13) | <span data-ttu-id="204c7-117">Значение в первой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-117">The value in the first row and third column of the matrix.</span></span>
[<span data-ttu-id="204c7-118">_14</span><span class="sxs-lookup"><span data-stu-id="204c7-118">_14</span></span>](#_14) | <span data-ttu-id="204c7-119">Значение в первой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-119">The value in the first row and fourth column of the matrix.</span></span>
[<span data-ttu-id="204c7-120">_21</span><span class="sxs-lookup"><span data-stu-id="204c7-120">_21</span></span>](#_21) | <span data-ttu-id="204c7-121">Значение во второй строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-121">The value in the second row and first column of the matrix.</span></span>
[<span data-ttu-id="204c7-122">_22</span><span class="sxs-lookup"><span data-stu-id="204c7-122">_22</span></span>](#_22) | <span data-ttu-id="204c7-123">Значение во второй строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-123">The value in the second row and second column of the matrix.</span></span>
[<span data-ttu-id="204c7-124">_23</span><span class="sxs-lookup"><span data-stu-id="204c7-124">_23</span></span>](#_23) | <span data-ttu-id="204c7-125">Значение в второй строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-125">The value in the second row and third column of the matrix.</span></span>
[<span data-ttu-id="204c7-126">_24</span><span class="sxs-lookup"><span data-stu-id="204c7-126">_24</span></span>](#_24) | <span data-ttu-id="204c7-127">Значение во второй строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-127">The value in the second row and fourth column of the matrix.</span></span>
[<span data-ttu-id="204c7-128">_31</span><span class="sxs-lookup"><span data-stu-id="204c7-128">_31</span></span>](#_31) | <span data-ttu-id="204c7-129">Значение в третьей строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-129">The value in the third row and first column of the matrix.</span></span>
[<span data-ttu-id="204c7-130">_32</span><span class="sxs-lookup"><span data-stu-id="204c7-130">_32</span></span>](#_32) | <span data-ttu-id="204c7-131">Значение в третьей строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-131">The value in the third row and second column of the matrix.</span></span>
[<span data-ttu-id="204c7-132">_33</span><span class="sxs-lookup"><span data-stu-id="204c7-132">_33</span></span>](#_33) | <span data-ttu-id="204c7-133">Значение в третьей строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-133">The value in the third row and third column of the matrix.</span></span>
[<span data-ttu-id="204c7-134">_34</span><span class="sxs-lookup"><span data-stu-id="204c7-134">_34</span></span>](#_34) | <span data-ttu-id="204c7-135">Значение в третьей строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-135">The value in the third row and fourth column of the matrix.</span></span>
[<span data-ttu-id="204c7-136">_41</span><span class="sxs-lookup"><span data-stu-id="204c7-136">_41</span></span>](#_41) | <span data-ttu-id="204c7-137">Значение в четвертой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-137">The value in the fourth row and first column of the matrix.</span></span>
[<span data-ttu-id="204c7-138">_42</span><span class="sxs-lookup"><span data-stu-id="204c7-138">_42</span></span>](#_42) | <span data-ttu-id="204c7-139">Значение в четвертой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-139">The value in the fourth row and second column of the matrix.</span></span>
[<span data-ttu-id="204c7-140">_43</span><span class="sxs-lookup"><span data-stu-id="204c7-140">_43</span></span>](#_43) | <span data-ttu-id="204c7-141">Значение в четвертой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-141">The value in the fourth row and third column of the matrix.</span></span>
[<span data-ttu-id="204c7-142">_44</span><span class="sxs-lookup"><span data-stu-id="204c7-142">_44</span></span>](#_44) | <span data-ttu-id="204c7-143">Значение в четвертой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-143">The value in the fourth row and fourth column of the matrix.</span></span>

<span data-ttu-id="204c7-144">Это эквивалентно D2D1_MATRIX_4X4_F.</span><span class="sxs-lookup"><span data-stu-id="204c7-144">This is equivalent to a D2D1_MATRIX_4X4_F.</span></span>

## <span data-ttu-id="204c7-145">Участников</span><span class="sxs-lookup"><span data-stu-id="204c7-145">Members</span></span>

#### <span data-ttu-id="204c7-146">_11</span><span class="sxs-lookup"><span data-stu-id="204c7-146">_11</span></span> 

<span data-ttu-id="204c7-147">Значение в первой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-147">The value in the first row and first column of the matrix.</span></span>

> <span data-ttu-id="204c7-148">общедоступная единая [_11](#_11)</span><span class="sxs-lookup"><span data-stu-id="204c7-148">public Single [_11](#_11)</span></span>

#### <span data-ttu-id="204c7-149">_12</span><span class="sxs-lookup"><span data-stu-id="204c7-149">_12</span></span> 

<span data-ttu-id="204c7-150">Значение в первой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-150">The value in the first row and second column of the matrix.</span></span>

> <span data-ttu-id="204c7-151">общедоступная единая [_12](#_12)</span><span class="sxs-lookup"><span data-stu-id="204c7-151">public Single [_12](#_12)</span></span>

#### <span data-ttu-id="204c7-152">_13</span><span class="sxs-lookup"><span data-stu-id="204c7-152">_13</span></span> 

<span data-ttu-id="204c7-153">Значение в первой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-153">The value in the first row and third column of the matrix.</span></span>

> <span data-ttu-id="204c7-154">общедоступная единая [_13](#_13)</span><span class="sxs-lookup"><span data-stu-id="204c7-154">public Single [_13](#_13)</span></span>

#### <span data-ttu-id="204c7-155">_14</span><span class="sxs-lookup"><span data-stu-id="204c7-155">_14</span></span> 

<span data-ttu-id="204c7-156">Значение в первой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-156">The value in the first row and fourth column of the matrix.</span></span>

> <span data-ttu-id="204c7-157">общедоступная единая [_14](#_14)</span><span class="sxs-lookup"><span data-stu-id="204c7-157">public Single [_14](#_14)</span></span>

#### <span data-ttu-id="204c7-158">_21</span><span class="sxs-lookup"><span data-stu-id="204c7-158">_21</span></span> 

<span data-ttu-id="204c7-159">Значение во второй строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-159">The value in the second row and first column of the matrix.</span></span>

> <span data-ttu-id="204c7-160">общедоступная единая [_21](#_21)</span><span class="sxs-lookup"><span data-stu-id="204c7-160">public Single [_21](#_21)</span></span>

#### <span data-ttu-id="204c7-161">_22</span><span class="sxs-lookup"><span data-stu-id="204c7-161">_22</span></span> 

<span data-ttu-id="204c7-162">Значение во второй строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-162">The value in the second row and second column of the matrix.</span></span>

> <span data-ttu-id="204c7-163">общедоступная единая [_22](#_22)</span><span class="sxs-lookup"><span data-stu-id="204c7-163">public Single [_22](#_22)</span></span>

#### <span data-ttu-id="204c7-164">_23</span><span class="sxs-lookup"><span data-stu-id="204c7-164">_23</span></span> 

<span data-ttu-id="204c7-165">Значение в второй строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-165">The value in the second row and third column of the matrix.</span></span>

> <span data-ttu-id="204c7-166">общедоступная единая [_23](#_23)</span><span class="sxs-lookup"><span data-stu-id="204c7-166">public Single [_23](#_23)</span></span>

#### <span data-ttu-id="204c7-167">_24</span><span class="sxs-lookup"><span data-stu-id="204c7-167">_24</span></span> 

<span data-ttu-id="204c7-168">Значение во второй строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-168">The value in the second row and fourth column of the matrix.</span></span>

> <span data-ttu-id="204c7-169">общедоступная единая [_24](#_24)</span><span class="sxs-lookup"><span data-stu-id="204c7-169">public Single [_24](#_24)</span></span>

#### <span data-ttu-id="204c7-170">_31</span><span class="sxs-lookup"><span data-stu-id="204c7-170">_31</span></span> 

<span data-ttu-id="204c7-171">Значение в третьей строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-171">The value in the third row and first column of the matrix.</span></span>

> <span data-ttu-id="204c7-172">общедоступная единая [_31](#_31)</span><span class="sxs-lookup"><span data-stu-id="204c7-172">public Single [_31](#_31)</span></span>

#### <span data-ttu-id="204c7-173">_32</span><span class="sxs-lookup"><span data-stu-id="204c7-173">_32</span></span> 

<span data-ttu-id="204c7-174">Значение в третьей строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-174">The value in the third row and second column of the matrix.</span></span>

> <span data-ttu-id="204c7-175">общедоступная единая [_32](#_32)</span><span class="sxs-lookup"><span data-stu-id="204c7-175">public Single [_32](#_32)</span></span>

#### <span data-ttu-id="204c7-176">_33</span><span class="sxs-lookup"><span data-stu-id="204c7-176">_33</span></span> 

<span data-ttu-id="204c7-177">Значение в третьей строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-177">The value in the third row and third column of the matrix.</span></span>

> <span data-ttu-id="204c7-178">общедоступная единая [_33](#_33)</span><span class="sxs-lookup"><span data-stu-id="204c7-178">public Single [_33](#_33)</span></span>

#### <span data-ttu-id="204c7-179">_34</span><span class="sxs-lookup"><span data-stu-id="204c7-179">_34</span></span> 

<span data-ttu-id="204c7-180">Значение в третьей строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-180">The value in the third row and fourth column of the matrix.</span></span>

> <span data-ttu-id="204c7-181">общедоступная единая [_34](#_34)</span><span class="sxs-lookup"><span data-stu-id="204c7-181">public Single [_34](#_34)</span></span>

#### <span data-ttu-id="204c7-182">_41</span><span class="sxs-lookup"><span data-stu-id="204c7-182">_41</span></span> 

<span data-ttu-id="204c7-183">Значение в четвертой строке и первом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-183">The value in the fourth row and first column of the matrix.</span></span>

> <span data-ttu-id="204c7-184">общедоступная единая [_41](#_41)</span><span class="sxs-lookup"><span data-stu-id="204c7-184">public Single [_41](#_41)</span></span>

#### <span data-ttu-id="204c7-185">_42</span><span class="sxs-lookup"><span data-stu-id="204c7-185">_42</span></span> 

<span data-ttu-id="204c7-186">Значение в четвертой строке и втором столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-186">The value in the fourth row and second column of the matrix.</span></span>

> <span data-ttu-id="204c7-187">общедоступная единая [_42](#_42)</span><span class="sxs-lookup"><span data-stu-id="204c7-187">public Single [_42](#_42)</span></span>

#### <span data-ttu-id="204c7-188">_43</span><span class="sxs-lookup"><span data-stu-id="204c7-188">_43</span></span> 

<span data-ttu-id="204c7-189">Значение в четвертой строке и третьем столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-189">The value in the fourth row and third column of the matrix.</span></span>

> <span data-ttu-id="204c7-190">общедоступная единая [_43](#_43)</span><span class="sxs-lookup"><span data-stu-id="204c7-190">public Single [_43](#_43)</span></span>

#### <span data-ttu-id="204c7-191">_44</span><span class="sxs-lookup"><span data-stu-id="204c7-191">_44</span></span> 

<span data-ttu-id="204c7-192">Значение в четвертой строке и четвертом столбце матрицы.</span><span class="sxs-lookup"><span data-stu-id="204c7-192">The value in the fourth row and fourth column of the matrix.</span></span>

> <span data-ttu-id="204c7-193">общедоступная единая [_44](#_44)</span><span class="sxs-lookup"><span data-stu-id="204c7-193">public Single [_44](#_44)</span></span>

