---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 887dcd438a89dcff4da239872df4bdb51e90f1f0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880614"
---
# <span data-ttu-id="352fa-104">0.9.515-Interface ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="352fa-104">0.9.515 - interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="352fa-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="352fa-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="352fa-106">Это преимущественно представляет объединенный объект Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="352fa-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="352fa-107">Summary</span></span>

 <span data-ttu-id="352fa-108">Участников</span><span class="sxs-lookup"><span data-stu-id="352fa-108">Members</span></span>                        | <span data-ttu-id="352fa-109">Описания</span><span class="sxs-lookup"><span data-stu-id="352fa-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="352fa-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="352fa-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="352fa-111">Получение ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="352fa-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="352fa-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="352fa-113">Получите DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="352fa-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="352fa-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="352fa-115">Получение FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="352fa-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="352fa-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="352fa-117">Получение HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="352fa-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="352fa-119">Получение HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="352fa-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="352fa-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="352fa-121">Получение HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="352fa-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="352fa-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="352fa-123">Получение InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="352fa-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="352fa-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="352fa-125">Получение KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="352fa-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="352fa-127">Получение PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="352fa-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="352fa-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="352fa-129">Получение PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="352fa-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="352fa-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="352fa-131">Получение PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="352fa-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="352fa-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="352fa-133">Получение PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="352fa-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="352fa-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="352fa-135">Получение PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="352fa-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="352fa-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="352fa-137">Получение PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="352fa-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="352fa-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="352fa-139">Получение PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="352fa-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="352fa-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="352fa-141">Получение PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="352fa-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="352fa-143">Получение PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="352fa-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="352fa-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="352fa-145">Получите PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="352fa-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="352fa-147">Получение PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="352fa-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="352fa-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="352fa-149">Получение PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="352fa-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="352fa-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="352fa-151">Получение PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="352fa-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="352fa-152">get_Time</span></span>](#get_time) | <span data-ttu-id="352fa-153">Получить время события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="352fa-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="352fa-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="352fa-155">Получение TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="352fa-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="352fa-157">Получение TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="352fa-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="352fa-159">Получение TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="352fa-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="352fa-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="352fa-161">Получение TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="352fa-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="352fa-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="352fa-163">Получение TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="352fa-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="352fa-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="352fa-165">Получение TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="352fa-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="352fa-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="352fa-167">Задайте ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="352fa-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="352fa-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="352fa-169">Задайте DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="352fa-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="352fa-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="352fa-171">Задайте FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="352fa-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="352fa-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="352fa-173">Задайте HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="352fa-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="352fa-175">Задайте HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="352fa-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="352fa-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="352fa-177">Задайте HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="352fa-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="352fa-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="352fa-179">Задайте InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="352fa-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="352fa-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="352fa-181">Задайте KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="352fa-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="352fa-183">Задайте PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="352fa-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="352fa-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="352fa-185">Задайте PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="352fa-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="352fa-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="352fa-187">Задайте PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="352fa-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="352fa-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="352fa-189">Задайте PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="352fa-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="352fa-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="352fa-191">Задайте PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="352fa-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="352fa-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="352fa-193">Задайте PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="352fa-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="352fa-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="352fa-195">Задайте PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="352fa-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="352fa-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="352fa-197">Задайте PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="352fa-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="352fa-199">Задайте PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="352fa-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="352fa-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="352fa-201">Задайте PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="352fa-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="352fa-203">Задайте PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="352fa-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="352fa-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="352fa-205">Задайте PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="352fa-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="352fa-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="352fa-207">Задайте PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="352fa-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="352fa-208">put_Time</span></span>](#put_time) | <span data-ttu-id="352fa-209">Задайте время события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="352fa-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="352fa-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="352fa-211">Задайте TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="352fa-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="352fa-213">Задайте TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="352fa-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="352fa-215">Задайте TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="352fa-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="352fa-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="352fa-217">Задайте TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="352fa-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="352fa-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="352fa-219">Задайте TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="352fa-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="352fa-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="352fa-221">Задайте TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="352fa-222">Он берет на себя поля из всех трех типов данных, таких как HWND и ДЕСКРИПТОРы.</span><span class="sxs-lookup"><span data-stu-id="352fa-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="352fa-223">Обратите внимание, что sourceDevice используется, но мы ожидаем, что PointerDeviceRect и DisplayRect будут охватывать существующие варианты использования sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="352fa-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="352fa-224">Еще одна большая разница заключается в том, что любое из расположений Point или Rect ожидается в WebView физических координат.</span><span class="sxs-lookup"><span data-stu-id="352fa-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="352fa-225">Это значит, что координаты относительно WebView и не применяются к масштабированию DPI.</span><span class="sxs-lookup"><span data-stu-id="352fa-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="352fa-226">Участников</span><span class="sxs-lookup"><span data-stu-id="352fa-226">Members</span></span>

#### <span data-ttu-id="352fa-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="352fa-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="352fa-228">Получение ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="352fa-229">общедоступные значения HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(Int32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="352fa-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="352fa-230">Это соответствует свойству ButtonChangeKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="352fa-231">Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="352fa-232">get_DisplayRect</span></span> 

<span data-ttu-id="352fa-233">Получите DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="352fa-234">общедоступные значения HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="352fa-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="352fa-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="352fa-235">get_FrameId</span></span> 

<span data-ttu-id="352fa-236">Получение FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="352fa-237">общедоступные значения HRESULT [get_FrameId](#get_frameid)(UINT32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="352fa-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="352fa-238">Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="352fa-239">get_HimetricLocation</span></span> 

<span data-ttu-id="352fa-240">Получение HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="352fa-241">общедоступные значения HRESULT [get_HimetricLocation](#get_himetriclocation)(Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="352fa-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="352fa-242">Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="352fa-244">Получение HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="352fa-245">общедоступные значения HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="352fa-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="352fa-246">Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="352fa-247">get_HistoryCount</span></span> 

<span data-ttu-id="352fa-248">Получение HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="352fa-249">общедоступные значения HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="352fa-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="352fa-250">Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="352fa-251">get_InputData</span></span> 

<span data-ttu-id="352fa-252">Получение InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="352fa-253">общедоступные значения HRESULT [get_InputData](#get_inputdata)(Int32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="352fa-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="352fa-254">Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="352fa-255">get_KeyStates</span></span> 

<span data-ttu-id="352fa-256">Получение KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="352fa-257">общедоступные значения HRESULT [get_KeyStates](#get_keystates)(DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="352fa-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="352fa-258">Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-259">get_PenFlags</span></span> 

<span data-ttu-id="352fa-260">Получение PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="352fa-261">общедоступные значения HRESULT [get_PenFlags](#get_penflags)(UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="352fa-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="352fa-262">Это соответствует свойству penFlags структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="352fa-263">Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="352fa-264">get_PenMask</span></span> 

<span data-ttu-id="352fa-265">Получение PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="352fa-266">общедоступные значения HRESULT [get_PenMask](#get_penmask)(UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="352fa-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="352fa-267">Это соответствует свойству penMask структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="352fa-268">Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="352fa-269">get_PenPressure</span></span> 

<span data-ttu-id="352fa-270">Получение PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="352fa-271">общедоступные значения HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="352fa-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="352fa-272">Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="352fa-273">get_PenRotation</span></span> 

<span data-ttu-id="352fa-274">Получение PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="352fa-275">общедоступные значения HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="352fa-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="352fa-276">Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="352fa-277">get_PenTiltX</span></span> 

<span data-ttu-id="352fa-278">Получение PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="352fa-279">общедоступные значения HRESULT [get_PenTiltX](#get_pentiltx)(Int32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="352fa-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="352fa-280">Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="352fa-281">get_PenTiltY</span></span> 

<span data-ttu-id="352fa-282">Получение PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="352fa-283">общедоступные значения HRESULT [get_PenTiltY](#get_pentilty)(Int32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="352fa-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="352fa-284">Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="352fa-285">get_PerformanceCount</span></span> 

<span data-ttu-id="352fa-286">Получение PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="352fa-287">общедоступные значения HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="352fa-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="352fa-288">Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="352fa-289">get_PixelLocation</span></span> 

<span data-ttu-id="352fa-290">Получение PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="352fa-291">общедоступные значения HRESULT [get_PixelLocation](#get_pixellocation)(Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="352fa-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="352fa-292">Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="352fa-294">Получение PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="352fa-295">общедоступные значения HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="352fa-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="352fa-296">Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="352fa-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="352fa-298">Получите PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="352fa-299">общедоступные значения HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="352fa-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="352fa-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-300">get_PointerFlags</span></span> 

<span data-ttu-id="352fa-301">Получение PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="352fa-302">общедоступные значения HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="352fa-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="352fa-303">Это соответствует свойству pointerFlags структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="352fa-304">Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="352fa-305">get_PointerId</span></span> 

<span data-ttu-id="352fa-306">Получение PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="352fa-307">общедоступные значения HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span><span class="sxs-lookup"><span data-stu-id="352fa-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="352fa-308">Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="352fa-309">get_PointerKind</span></span> 

<span data-ttu-id="352fa-310">Получение PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="352fa-311">общедоступные значения HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="352fa-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="352fa-312">Это соответствует свойству pointerKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="352fa-313">Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="352fa-314">Поддерживает PT_PEN и PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="352fa-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="352fa-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="352fa-315">get_Time</span></span> 

<span data-ttu-id="352fa-316">Получить время события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="352fa-317">общедоступные значения HRESULT [get_Time](#get_time)(DWORD \* Time)</span><span class="sxs-lookup"><span data-stu-id="352fa-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="352fa-318">Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="352fa-319">get_TouchContact</span></span> 

<span data-ttu-id="352fa-320">Получение TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="352fa-321">общедоступные значения HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="352fa-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="352fa-322">Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="352fa-324">Получение TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="352fa-325">общедоступные значения HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="352fa-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="352fa-326">Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-327">get_TouchFlags</span></span> 

<span data-ttu-id="352fa-328">Получение TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="352fa-329">общедоступные значения HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="352fa-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="352fa-330">Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="352fa-331">Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="352fa-332">get_TouchMask</span></span> 

<span data-ttu-id="352fa-333">Получение TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="352fa-334">общедоступные значения HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="352fa-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="352fa-335">Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="352fa-336">Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="352fa-337">get_TouchOrientation</span></span> 

<span data-ttu-id="352fa-338">Получение TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="352fa-339">общедоступные значения HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="352fa-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="352fa-340">Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="352fa-341">get_TouchPressure</span></span> 

<span data-ttu-id="352fa-342">Получение TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="352fa-343">общедоступные значения HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="352fa-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="352fa-344">Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="352fa-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="352fa-346">Задайте ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="352fa-347">общедоступные значения HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(Int32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="352fa-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="352fa-348">Это соответствует свойству ButtonChangeKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="352fa-349">Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="352fa-350">put_DisplayRect</span></span> 

<span data-ttu-id="352fa-351">Задайте DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="352fa-352">общедоступные значения HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="352fa-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="352fa-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="352fa-353">put_FrameId</span></span> 

<span data-ttu-id="352fa-354">Задайте FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="352fa-355">общедоступные значения HRESULT [put_FrameId](#put_frameid)(UINT32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="352fa-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="352fa-356">Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="352fa-357">put_HimetricLocation</span></span> 

<span data-ttu-id="352fa-358">Задайте HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="352fa-359">общедоступные значения HRESULT [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="352fa-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="352fa-360">Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="352fa-362">Задайте HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="352fa-363">общедоступные значения HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="352fa-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="352fa-364">Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="352fa-365">put_HistoryCount</span></span> 

<span data-ttu-id="352fa-366">Задайте HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="352fa-367">общедоступные значения HRESULT [put_HistoryCount](#put_historycount)(UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="352fa-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="352fa-368">Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="352fa-369">put_InputData</span></span> 

<span data-ttu-id="352fa-370">Задайте InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="352fa-371">общедоступные значения HRESULT [put_InputData](#put_inputdata)(Int32 InputData)</span><span class="sxs-lookup"><span data-stu-id="352fa-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="352fa-372">Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="352fa-373">put_KeyStates</span></span> 

<span data-ttu-id="352fa-374">Задайте KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="352fa-375">общедоступные значения HRESULT [put_KeyStates](#put_keystates)(DWORD KeyStates)</span><span class="sxs-lookup"><span data-stu-id="352fa-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="352fa-376">Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-377">put_PenFlags</span></span> 

<span data-ttu-id="352fa-378">Задайте PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="352fa-379">общедоступные значения HRESULT [put_PenFlags](#put_penflags)(UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="352fa-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="352fa-380">Это соответствует свойству penFlags структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="352fa-381">Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="352fa-382">put_PenMask</span></span> 

<span data-ttu-id="352fa-383">Задайте PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="352fa-384">общедоступные значения HRESULT [put_PenMask](#put_penmask)(UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="352fa-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="352fa-385">Это соответствует свойству penMask структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="352fa-386">Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="352fa-387">put_PenPressure</span></span> 

<span data-ttu-id="352fa-388">Задайте PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="352fa-389">общедоступные значения HRESULT [put_PenPressure](#put_penpressure)(UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="352fa-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="352fa-390">Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="352fa-391">put_PenRotation</span></span> 

<span data-ttu-id="352fa-392">Задайте PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="352fa-393">общедоступные значения HRESULT [put_PenRotation](#put_penrotation)(UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="352fa-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="352fa-394">Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="352fa-395">put_PenTiltX</span></span> 

<span data-ttu-id="352fa-396">Задайте PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="352fa-397">общедоступные значения HRESULT [put_PenTiltX](#put_pentiltx)(Int32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="352fa-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="352fa-398">Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="352fa-399">put_PenTiltY</span></span> 

<span data-ttu-id="352fa-400">Задайте PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="352fa-401">общедоступные значения HRESULT [put_PenTiltY](#put_pentilty)(Int32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="352fa-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="352fa-402">Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="352fa-403">put_PerformanceCount</span></span> 

<span data-ttu-id="352fa-404">Задайте PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="352fa-405">общедоступные значения HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="352fa-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="352fa-406">Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="352fa-407">put_PixelLocation</span></span> 

<span data-ttu-id="352fa-408">Задайте PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="352fa-409">общедоступные значения HRESULT [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="352fa-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="352fa-410">Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="352fa-412">Задайте PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="352fa-413">общедоступные значения HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="352fa-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="352fa-414">Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="352fa-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="352fa-416">Задайте PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="352fa-417">общедоступные значения HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="352fa-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="352fa-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-418">put_PointerFlags</span></span> 

<span data-ttu-id="352fa-419">Задайте PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="352fa-420">общедоступные значения HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="352fa-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="352fa-421">Это соответствует свойству pointerFlags структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="352fa-422">Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="352fa-423">put_PointerId</span></span> 

<span data-ttu-id="352fa-424">Задайте PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="352fa-425">общедоступные значения HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span><span class="sxs-lookup"><span data-stu-id="352fa-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="352fa-426">Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="352fa-427">put_PointerKind</span></span> 

<span data-ttu-id="352fa-428">Задайте PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="352fa-429">общедоступные значения HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="352fa-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="352fa-430">Это соответствует свойству pointerKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="352fa-431">Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="352fa-432">Поддерживает PT_PEN и PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="352fa-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="352fa-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="352fa-433">put_Time</span></span> 

<span data-ttu-id="352fa-434">Задайте время события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="352fa-435">общедоступные значения HRESULT [put_Time](#put_time)(время в DWORD)</span><span class="sxs-lookup"><span data-stu-id="352fa-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="352fa-436">Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="352fa-437">put_TouchContact</span></span> 

<span data-ttu-id="352fa-438">Задайте TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="352fa-439">общедоступные значения HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="352fa-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="352fa-440">Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="352fa-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="352fa-442">Задайте TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="352fa-443">общедоступные значения HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="352fa-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="352fa-444">Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="352fa-445">put_TouchFlags</span></span> 

<span data-ttu-id="352fa-446">Задайте TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="352fa-447">общедоступные значения HRESULT [put_TouchFlags](#put_touchflags)(UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="352fa-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="352fa-448">Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="352fa-449">Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="352fa-450">put_TouchMask</span></span> 

<span data-ttu-id="352fa-451">Задайте TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="352fa-452">общедоступные значения HRESULT [put_TouchMask](#put_touchmask)(UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="352fa-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="352fa-453">Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="352fa-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="352fa-454">Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="352fa-455">put_TouchOrientation</span></span> 

<span data-ttu-id="352fa-456">Задайте TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="352fa-457">общедоступные значения HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="352fa-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="352fa-458">Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="352fa-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="352fa-459">put_TouchPressure</span></span> 

<span data-ttu-id="352fa-460">Задайте TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="352fa-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="352fa-461">общедоступные значения HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="352fa-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="352fa-462">Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="352fa-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

