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
ms.openlocfilehash: 14b549fc299b4feb185fb391b9ad4ec1a9dde892
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699159"
---
# <span data-ttu-id="c0c50-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="c0c50-104">Microsoft.Web.WebView2.Core.CoreWebView2PointerInfo class</span></span> 

<span data-ttu-id="c0c50-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c0c50-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c0c50-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="c0c50-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c0c50-107">Это преимущественно представляет объединенный объект Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="c0c50-107">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="c0c50-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c0c50-108">Summary</span></span>

 <span data-ttu-id="c0c50-109">Участников</span><span class="sxs-lookup"><span data-stu-id="c0c50-109">Members</span></span>                        | <span data-ttu-id="c0c50-110">Описания</span><span class="sxs-lookup"><span data-stu-id="c0c50-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0c50-111">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="c0c50-111">ButtonChangeKind</span></span>](#buttonchangekind) | <span data-ttu-id="c0c50-112">ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-112">The ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="c0c50-113">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="c0c50-113">DisplayRect</span></span>](#displayrect) | <span data-ttu-id="c0c50-114">DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-114">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="c0c50-115">FrameId</span><span class="sxs-lookup"><span data-stu-id="c0c50-115">FrameId</span></span>](#frameid) | <span data-ttu-id="c0c50-116">FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-116">The FrameID of the pointer event.</span></span>
[<span data-ttu-id="c0c50-117">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="c0c50-117">HimetricLocation</span></span>](#himetriclocation) | <span data-ttu-id="c0c50-118">HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-118">The HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="c0c50-119">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="c0c50-119">HimetricLocationRaw</span></span>](#himetriclocationraw) | <span data-ttu-id="c0c50-120">HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-120">The HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="c0c50-121">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="c0c50-121">HistoryCount</span></span>](#historycount) | <span data-ttu-id="c0c50-122">HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-122">The HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="c0c50-123">InputData</span><span class="sxs-lookup"><span data-stu-id="c0c50-123">InputData</span></span>](#inputdata) | <span data-ttu-id="c0c50-124">InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-124">The InputData of the pointer event.</span></span>
[<span data-ttu-id="c0c50-125">KeyStates</span><span class="sxs-lookup"><span data-stu-id="c0c50-125">KeyStates</span></span>](#keystates) | <span data-ttu-id="c0c50-126">KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-126">The KeyStates of the pointer event.</span></span>
[<span data-ttu-id="c0c50-127">PenFlags</span><span class="sxs-lookup"><span data-stu-id="c0c50-127">PenFlags</span></span>](#penflags) | <span data-ttu-id="c0c50-128">PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-128">The PenFlags of the pointer event.</span></span>
[<span data-ttu-id="c0c50-129">PenMask</span><span class="sxs-lookup"><span data-stu-id="c0c50-129">PenMask</span></span>](#penmask) | <span data-ttu-id="c0c50-130">PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-130">The PenMask of the pointer event.</span></span>
[<span data-ttu-id="c0c50-131">PenPressure</span><span class="sxs-lookup"><span data-stu-id="c0c50-131">PenPressure</span></span>](#penpressure) | <span data-ttu-id="c0c50-132">PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-132">The PenPressure of the pointer event.</span></span>
[<span data-ttu-id="c0c50-133">PenRotation</span><span class="sxs-lookup"><span data-stu-id="c0c50-133">PenRotation</span></span>](#penrotation) | <span data-ttu-id="c0c50-134">PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-134">The PenRotation of the pointer event.</span></span>
[<span data-ttu-id="c0c50-135">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="c0c50-135">PenTiltX</span></span>](#pentiltx) | <span data-ttu-id="c0c50-136">PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-136">The PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="c0c50-137">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="c0c50-137">PenTiltY</span></span>](#pentilty) | <span data-ttu-id="c0c50-138">PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-138">The PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="c0c50-139">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="c0c50-139">PerformanceCount</span></span>](#performancecount) | <span data-ttu-id="c0c50-140">PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-140">The PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="c0c50-141">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="c0c50-141">PixelLocation</span></span>](#pixellocation) | <span data-ttu-id="c0c50-142">PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-142">The PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="c0c50-143">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="c0c50-143">PixelLocationRaw</span></span>](#pixellocationraw) | <span data-ttu-id="c0c50-144">PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-144">The PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="c0c50-145">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="c0c50-145">PointerDeviceRect</span></span>](#pointerdevicerect) | <span data-ttu-id="c0c50-146">PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-146">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="c0c50-147">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="c0c50-147">PointerFlags</span></span>](#pointerflags) | <span data-ttu-id="c0c50-148">PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-148">The PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="c0c50-149">PointerId</span><span class="sxs-lookup"><span data-stu-id="c0c50-149">PointerId</span></span>](#pointerid) | <span data-ttu-id="c0c50-150">PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-150">The PointerId of the pointer event.</span></span>
[<span data-ttu-id="c0c50-151">PointerKind</span><span class="sxs-lookup"><span data-stu-id="c0c50-151">PointerKind</span></span>](#pointerkind) | <span data-ttu-id="c0c50-152">PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-152">The PointerKind of the pointer event.</span></span>
[<span data-ttu-id="c0c50-153">Время</span><span class="sxs-lookup"><span data-stu-id="c0c50-153">Time</span></span>](#time) | <span data-ttu-id="c0c50-154">Время события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-154">The Time of the pointer event.</span></span>
[<span data-ttu-id="c0c50-155">TouchContact</span><span class="sxs-lookup"><span data-stu-id="c0c50-155">TouchContact</span></span>](#touchcontact) | <span data-ttu-id="c0c50-156">TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-156">The TouchContact of the pointer event.</span></span>
[<span data-ttu-id="c0c50-157">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="c0c50-157">TouchContactRaw</span></span>](#touchcontactraw) | <span data-ttu-id="c0c50-158">TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-158">The TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="c0c50-159">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="c0c50-159">TouchFlags</span></span>](#touchflags) | <span data-ttu-id="c0c50-160">TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-160">The TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="c0c50-161">TouchMask</span><span class="sxs-lookup"><span data-stu-id="c0c50-161">TouchMask</span></span>](#touchmask) | <span data-ttu-id="c0c50-162">TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-162">The TouchMask of the pointer event.</span></span>
[<span data-ttu-id="c0c50-163">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="c0c50-163">TouchOrientation</span></span>](#touchorientation) | <span data-ttu-id="c0c50-164">TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-164">The TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="c0c50-165">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="c0c50-165">TouchPressure</span></span>](#touchpressure) | <span data-ttu-id="c0c50-166">TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-166">The TouchPressure of the pointer event.</span></span>

## <span data-ttu-id="c0c50-167">Участников</span><span class="sxs-lookup"><span data-stu-id="c0c50-167">Members</span></span>

#### <span data-ttu-id="c0c50-168">ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="c0c50-168">ButtonChangeKind</span></span> 

<span data-ttu-id="c0c50-169">ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-169">The ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="c0c50-170">public int [ButtonChangeKind](#buttonchangekind)</span><span class="sxs-lookup"><span data-stu-id="c0c50-170">public int [ButtonChangeKind](#buttonchangekind)</span></span>

<span data-ttu-id="c0c50-171">Это соответствует свойству ButtonChangeKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="c0c50-171">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="c0c50-172">Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-172">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-173">DisplayRect</span><span class="sxs-lookup"><span data-stu-id="c0c50-173">DisplayRect</span></span> 

<span data-ttu-id="c0c50-174">DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-174">The DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="c0c50-175">общедоступный Rect [DisplayRect](#displayrect)</span><span class="sxs-lookup"><span data-stu-id="c0c50-175">public Rect [DisplayRect](#displayrect)</span></span>

#### <span data-ttu-id="c0c50-176">FrameId</span><span class="sxs-lookup"><span data-stu-id="c0c50-176">FrameId</span></span> 

<span data-ttu-id="c0c50-177">FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-177">The FrameID of the pointer event.</span></span>

> <span data-ttu-id="c0c50-178">Открытый uint [FrameId](#frameid)</span><span class="sxs-lookup"><span data-stu-id="c0c50-178">public uint [FrameId](#frameid)</span></span>

<span data-ttu-id="c0c50-179">Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-179">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-180">HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="c0c50-180">HimetricLocation</span></span> 

<span data-ttu-id="c0c50-181">HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-181">The HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="c0c50-182">общедоступная точка [HimetricLocation](#himetriclocation)</span><span class="sxs-lookup"><span data-stu-id="c0c50-182">public Point [HimetricLocation](#himetriclocation)</span></span>

<span data-ttu-id="c0c50-183">Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-183">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-184">HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="c0c50-184">HimetricLocationRaw</span></span> 

<span data-ttu-id="c0c50-185">HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-185">The HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="c0c50-186">общедоступная точка [HimetricLocationRaw](#himetriclocationraw)</span><span class="sxs-lookup"><span data-stu-id="c0c50-186">public Point [HimetricLocationRaw](#himetriclocationraw)</span></span>

<span data-ttu-id="c0c50-187">Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-187">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-188">HistoryCount</span><span class="sxs-lookup"><span data-stu-id="c0c50-188">HistoryCount</span></span> 

<span data-ttu-id="c0c50-189">HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-189">The HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="c0c50-190">Открытый uint [HistoryCount](#historycount)</span><span class="sxs-lookup"><span data-stu-id="c0c50-190">public uint [HistoryCount](#historycount)</span></span>

<span data-ttu-id="c0c50-191">Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-191">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-192">InputData</span><span class="sxs-lookup"><span data-stu-id="c0c50-192">InputData</span></span> 

<span data-ttu-id="c0c50-193">InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-193">The InputData of the pointer event.</span></span>

> <span data-ttu-id="c0c50-194">public int [InputData](#inputdata)</span><span class="sxs-lookup"><span data-stu-id="c0c50-194">public int [InputData](#inputdata)</span></span>

<span data-ttu-id="c0c50-195">Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-195">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-196">KeyStates</span><span class="sxs-lookup"><span data-stu-id="c0c50-196">KeyStates</span></span> 

<span data-ttu-id="c0c50-197">KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-197">The KeyStates of the pointer event.</span></span>

> <span data-ttu-id="c0c50-198">Открытый uint [KeyStates](#keystates)</span><span class="sxs-lookup"><span data-stu-id="c0c50-198">public uint [KeyStates](#keystates)</span></span>

<span data-ttu-id="c0c50-199">Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-199">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-200">PenFlags</span><span class="sxs-lookup"><span data-stu-id="c0c50-200">PenFlags</span></span> 

<span data-ttu-id="c0c50-201">PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-201">The PenFlags of the pointer event.</span></span>

> <span data-ttu-id="c0c50-202">Открытый uint [PenFlags](#penflags)</span><span class="sxs-lookup"><span data-stu-id="c0c50-202">public uint [PenFlags](#penflags)</span></span>

<span data-ttu-id="c0c50-203">Это соответствует свойству penFlags структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="c0c50-203">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="c0c50-204">Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-204">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-205">PenMask</span><span class="sxs-lookup"><span data-stu-id="c0c50-205">PenMask</span></span> 

<span data-ttu-id="c0c50-206">PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-206">The PenMask of the pointer event.</span></span>

> <span data-ttu-id="c0c50-207">Открытый uint [PenMask](#penmask)</span><span class="sxs-lookup"><span data-stu-id="c0c50-207">public uint [PenMask](#penmask)</span></span>

<span data-ttu-id="c0c50-208">Это соответствует свойству penMask структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="c0c50-208">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="c0c50-209">Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-209">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-210">PenPressure</span><span class="sxs-lookup"><span data-stu-id="c0c50-210">PenPressure</span></span> 

<span data-ttu-id="c0c50-211">PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-211">The PenPressure of the pointer event.</span></span>

> <span data-ttu-id="c0c50-212">Открытый uint [PenPressure](#penpressure)</span><span class="sxs-lookup"><span data-stu-id="c0c50-212">public uint [PenPressure](#penpressure)</span></span>

<span data-ttu-id="c0c50-213">Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-213">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-214">PenRotation</span><span class="sxs-lookup"><span data-stu-id="c0c50-214">PenRotation</span></span> 

<span data-ttu-id="c0c50-215">PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-215">The PenRotation of the pointer event.</span></span>

> <span data-ttu-id="c0c50-216">Открытый uint [PenRotation](#penrotation)</span><span class="sxs-lookup"><span data-stu-id="c0c50-216">public uint [PenRotation](#penrotation)</span></span>

<span data-ttu-id="c0c50-217">Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-217">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-218">PenTiltX</span><span class="sxs-lookup"><span data-stu-id="c0c50-218">PenTiltX</span></span> 

<span data-ttu-id="c0c50-219">PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-219">The PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="c0c50-220">public int [PenTiltX](#pentiltx)</span><span class="sxs-lookup"><span data-stu-id="c0c50-220">public int [PenTiltX](#pentiltx)</span></span>

<span data-ttu-id="c0c50-221">Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-221">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-222">PenTiltY</span><span class="sxs-lookup"><span data-stu-id="c0c50-222">PenTiltY</span></span> 

<span data-ttu-id="c0c50-223">PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-223">The PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="c0c50-224">public int [PenTiltY](#pentilty)</span><span class="sxs-lookup"><span data-stu-id="c0c50-224">public int [PenTiltY](#pentilty)</span></span>

<span data-ttu-id="c0c50-225">Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-225">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-226">PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="c0c50-226">PerformanceCount</span></span> 

<span data-ttu-id="c0c50-227">PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-227">The PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="c0c50-228">общедоступный ulong [PerformanceCount](#performancecount)</span><span class="sxs-lookup"><span data-stu-id="c0c50-228">public ulong [PerformanceCount](#performancecount)</span></span>

<span data-ttu-id="c0c50-229">Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-229">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-230">PixelLocation</span><span class="sxs-lookup"><span data-stu-id="c0c50-230">PixelLocation</span></span> 

<span data-ttu-id="c0c50-231">PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-231">The PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="c0c50-232">общедоступная точка [PixelLocation](#pixellocation)</span><span class="sxs-lookup"><span data-stu-id="c0c50-232">public Point [PixelLocation](#pixellocation)</span></span>

<span data-ttu-id="c0c50-233">Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-233">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-234">PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="c0c50-234">PixelLocationRaw</span></span> 

<span data-ttu-id="c0c50-235">PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-235">The PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="c0c50-236">общедоступная точка [PixelLocationRaw](#pixellocationraw)</span><span class="sxs-lookup"><span data-stu-id="c0c50-236">public Point [PixelLocationRaw](#pixellocationraw)</span></span>

<span data-ttu-id="c0c50-237">Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-237">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-238">PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="c0c50-238">PointerDeviceRect</span></span> 

<span data-ttu-id="c0c50-239">PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-239">The PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="c0c50-240">общедоступный Rect [PointerDeviceRect](#pointerdevicerect)</span><span class="sxs-lookup"><span data-stu-id="c0c50-240">public Rect [PointerDeviceRect](#pointerdevicerect)</span></span>

#### <span data-ttu-id="c0c50-241">PointerFlags</span><span class="sxs-lookup"><span data-stu-id="c0c50-241">PointerFlags</span></span> 

<span data-ttu-id="c0c50-242">PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-242">The PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="c0c50-243">Открытый uint [PointerFlags](#pointerflags)</span><span class="sxs-lookup"><span data-stu-id="c0c50-243">public uint [PointerFlags](#pointerflags)</span></span>

<span data-ttu-id="c0c50-244">Это соответствует свойству pointerFlags структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="c0c50-244">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="c0c50-245">Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-245">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-246">PointerId</span><span class="sxs-lookup"><span data-stu-id="c0c50-246">PointerId</span></span> 

<span data-ttu-id="c0c50-247">PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-247">The PointerId of the pointer event.</span></span>

> <span data-ttu-id="c0c50-248">Открытый uint [pointerId](#pointerid)</span><span class="sxs-lookup"><span data-stu-id="c0c50-248">public uint [PointerId](#pointerid)</span></span>

<span data-ttu-id="c0c50-249">Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-249">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-250">PointerKind</span><span class="sxs-lookup"><span data-stu-id="c0c50-250">PointerKind</span></span> 

<span data-ttu-id="c0c50-251">PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-251">The PointerKind of the pointer event.</span></span>

> <span data-ttu-id="c0c50-252">Открытый uint [PointerKind](#pointerkind)</span><span class="sxs-lookup"><span data-stu-id="c0c50-252">public uint [PointerKind](#pointerkind)</span></span>

<span data-ttu-id="c0c50-253">Это соответствует свойству pointerKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="c0c50-253">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="c0c50-254">Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-254">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="c0c50-255">Поддерживает PT_PEN и PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="c0c50-255">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="c0c50-256">Время</span><span class="sxs-lookup"><span data-stu-id="c0c50-256">Time</span></span> 

<span data-ttu-id="c0c50-257">Время события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-257">The Time of the pointer event.</span></span>

> <span data-ttu-id="c0c50-258">общедоступное [время](#time) (UINT)</span><span class="sxs-lookup"><span data-stu-id="c0c50-258">public uint [Time](#time)</span></span>

<span data-ttu-id="c0c50-259">Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-259">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-260">TouchContact</span><span class="sxs-lookup"><span data-stu-id="c0c50-260">TouchContact</span></span> 

<span data-ttu-id="c0c50-261">TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-261">The TouchContact of the pointer event.</span></span>

> <span data-ttu-id="c0c50-262">общедоступный Rect [TouchContact](#touchcontact)</span><span class="sxs-lookup"><span data-stu-id="c0c50-262">public Rect [TouchContact](#touchcontact)</span></span>

<span data-ttu-id="c0c50-263">Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-263">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-264">TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="c0c50-264">TouchContactRaw</span></span> 

<span data-ttu-id="c0c50-265">TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-265">The TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="c0c50-266">общедоступный Rect [TouchContactRaw](#touchcontactraw)</span><span class="sxs-lookup"><span data-stu-id="c0c50-266">public Rect [TouchContactRaw](#touchcontactraw)</span></span>

<span data-ttu-id="c0c50-267">Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-267">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-268">TouchFlags</span><span class="sxs-lookup"><span data-stu-id="c0c50-268">TouchFlags</span></span> 

<span data-ttu-id="c0c50-269">TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-269">The TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="c0c50-270">Открытый uint [TouchFlags](#touchflags)</span><span class="sxs-lookup"><span data-stu-id="c0c50-270">public uint [TouchFlags](#touchflags)</span></span>

<span data-ttu-id="c0c50-271">Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="c0c50-271">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="c0c50-272">Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-272">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-273">TouchMask</span><span class="sxs-lookup"><span data-stu-id="c0c50-273">TouchMask</span></span> 

<span data-ttu-id="c0c50-274">TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-274">The TouchMask of the pointer event.</span></span>

> <span data-ttu-id="c0c50-275">Открытый uint [TouchMask](#touchmask)</span><span class="sxs-lookup"><span data-stu-id="c0c50-275">public uint [TouchMask](#touchmask)</span></span>

<span data-ttu-id="c0c50-276">Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="c0c50-276">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="c0c50-277">Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-277">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-278">TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="c0c50-278">TouchOrientation</span></span> 

<span data-ttu-id="c0c50-279">TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-279">The TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="c0c50-280">Открытый uint [TouchOrientation](#touchorientation)</span><span class="sxs-lookup"><span data-stu-id="c0c50-280">public uint [TouchOrientation](#touchorientation)</span></span>

<span data-ttu-id="c0c50-281">Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-281">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="c0c50-282">TouchPressure</span><span class="sxs-lookup"><span data-stu-id="c0c50-282">TouchPressure</span></span> 

<span data-ttu-id="c0c50-283">TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="c0c50-283">The TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="c0c50-284">Открытый uint [TouchPressure](#touchpressure)</span><span class="sxs-lookup"><span data-stu-id="c0c50-284">public uint [TouchPressure](#touchpressure)</span></span>

<span data-ttu-id="c0c50-285">Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="c0c50-285">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

