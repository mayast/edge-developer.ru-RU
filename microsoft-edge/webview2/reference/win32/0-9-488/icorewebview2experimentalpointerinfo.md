---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ExperimentalPointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8c0ed40c61344fe0a3177fd36d5629953f8801d7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885487"
---
# <span data-ttu-id="ac856-104">0.9.515-Interface ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="ac856-104">0.9.515 - interface ICoreWebView2ExperimentalPointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="ac856-105">Это преимущественно представляет объединенный объект Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-105">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="ac856-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ac856-106">Summary</span></span>

 <span data-ttu-id="ac856-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ac856-107">Members</span></span>                        | <span data-ttu-id="ac856-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ac856-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac856-109">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ac856-109">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="ac856-110">Получение ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-110">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="ac856-111">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ac856-111">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="ac856-112">Получите DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-112">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ac856-113">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="ac856-113">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="ac856-114">Получение FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-114">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="ac856-115">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ac856-115">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="ac856-116">Получение HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-116">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="ac856-117">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-117">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="ac856-118">Получение HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-118">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ac856-119">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ac856-119">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="ac856-120">Получение HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-120">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="ac856-121">get_InputData</span><span class="sxs-lookup"><span data-stu-id="ac856-121">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="ac856-122">Получение InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-122">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="ac856-123">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ac856-123">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="ac856-124">Получение KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-124">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="ac856-125">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-125">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="ac856-126">Получение PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-126">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="ac856-127">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="ac856-127">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="ac856-128">Получение PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-128">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="ac856-129">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ac856-129">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="ac856-130">Получение PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-130">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="ac856-131">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ac856-131">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="ac856-132">Получение PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-132">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="ac856-133">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ac856-133">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="ac856-134">Получение PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-134">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="ac856-135">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ac856-135">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="ac856-136">Получение PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-136">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="ac856-137">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ac856-137">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="ac856-138">Получение PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-138">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="ac856-139">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ac856-139">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="ac856-140">Получение PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-140">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="ac856-141">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-141">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="ac856-142">Получение PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-142">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ac856-143">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ac856-143">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="ac856-144">Получите PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-144">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ac856-145">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-145">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="ac856-146">Получение PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-146">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="ac856-147">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="ac856-147">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="ac856-148">Получение PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-148">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="ac856-149">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ac856-149">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="ac856-150">Получение PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-150">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="ac856-151">get_Time</span><span class="sxs-lookup"><span data-stu-id="ac856-151">get_Time</span></span>](#get_time) | <span data-ttu-id="ac856-152">Получить время события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-152">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="ac856-153">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ac856-153">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="ac856-154">Получение TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-154">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="ac856-155">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-155">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="ac856-156">Получение TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-156">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="ac856-157">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-157">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="ac856-158">Получение TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-158">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="ac856-159">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ac856-159">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="ac856-160">Получение TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-160">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="ac856-161">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ac856-161">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="ac856-162">Получение TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-162">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="ac856-163">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ac856-163">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="ac856-164">Получение TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-164">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="ac856-165">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ac856-165">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="ac856-166">Задайте ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-166">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="ac856-167">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ac856-167">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="ac856-168">Задайте DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-168">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ac856-169">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="ac856-169">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="ac856-170">Задайте FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-170">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="ac856-171">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ac856-171">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="ac856-172">Задайте HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-172">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="ac856-173">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-173">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="ac856-174">Задайте HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-174">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ac856-175">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ac856-175">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="ac856-176">Задайте HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-176">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="ac856-177">put_InputData</span><span class="sxs-lookup"><span data-stu-id="ac856-177">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="ac856-178">Задайте InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-178">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="ac856-179">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ac856-179">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="ac856-180">Задайте KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-180">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="ac856-181">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-181">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="ac856-182">Задайте PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-182">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="ac856-183">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="ac856-183">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="ac856-184">Задайте PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-184">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="ac856-185">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ac856-185">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="ac856-186">Задайте PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-186">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="ac856-187">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ac856-187">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="ac856-188">Задайте PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-188">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="ac856-189">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ac856-189">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="ac856-190">Задайте PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-190">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="ac856-191">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ac856-191">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="ac856-192">Задайте PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-192">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="ac856-193">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ac856-193">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="ac856-194">Задайте PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-194">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="ac856-195">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ac856-195">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="ac856-196">Задайте PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-196">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="ac856-197">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-197">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="ac856-198">Задайте PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-198">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="ac856-199">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ac856-199">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="ac856-200">Задайте PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-200">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="ac856-201">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-201">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="ac856-202">Задайте PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-202">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="ac856-203">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="ac856-203">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="ac856-204">Задайте PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-204">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="ac856-205">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ac856-205">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="ac856-206">Задайте PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-206">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="ac856-207">put_Time</span><span class="sxs-lookup"><span data-stu-id="ac856-207">put_Time</span></span>](#put_time) | <span data-ttu-id="ac856-208">Задайте время события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-208">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="ac856-209">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ac856-209">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="ac856-210">Задайте TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-210">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="ac856-211">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-211">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="ac856-212">Задайте TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-212">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="ac856-213">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-213">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="ac856-214">Задайте TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-214">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="ac856-215">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ac856-215">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="ac856-216">Задайте TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-216">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="ac856-217">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ac856-217">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="ac856-218">Задайте TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-218">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="ac856-219">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ac856-219">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="ac856-220">Задайте TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-220">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="ac856-221">Он берет на себя поля из всех трех типов данных, таких как HWND и ДЕСКРИПТОРы.</span><span class="sxs-lookup"><span data-stu-id="ac856-221">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="ac856-222">Обратите внимание, что sourceDevice используется, но мы ожидаем, что PointerDeviceRect и DisplayRect будут охватывать существующие варианты использования sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="ac856-222">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="ac856-223">Еще одна большая разница заключается в том, что любое из расположений Point или Rect ожидается в WebView физических координат.</span><span class="sxs-lookup"><span data-stu-id="ac856-223">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="ac856-224">Это значит, что координаты относительно WebView и не применяются к масштабированию DPI.</span><span class="sxs-lookup"><span data-stu-id="ac856-224">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="ac856-225">Участников</span><span class="sxs-lookup"><span data-stu-id="ac856-225">Members</span></span>

#### <span data-ttu-id="ac856-226">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ac856-226">get_ButtonChangeKind</span></span> 

<span data-ttu-id="ac856-227">Получение ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-227">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="ac856-228">общедоступные значения HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(Int32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="ac856-228">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="ac856-229">Это соответствует свойству ButtonChangeKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-229">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac856-230">Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-230">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-231">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ac856-231">get_DisplayRect</span></span> 

<span data-ttu-id="ac856-232">Получите DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-232">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ac856-233">общедоступные значения HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="ac856-233">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="ac856-234">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="ac856-234">get_FrameId</span></span> 

<span data-ttu-id="ac856-235">Получение FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-235">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="ac856-236">общедоступные значения HRESULT [get_FrameId](#get_frameid)(UINT32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="ac856-236">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="ac856-237">Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-237">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-238">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ac856-238">get_HimetricLocation</span></span> 

<span data-ttu-id="ac856-239">Получение HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-239">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="ac856-240">общедоступные значения HRESULT [get_HimetricLocation](#get_himetriclocation)(Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="ac856-240">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="ac856-241">Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-241">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-242">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-242">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="ac856-243">Получение HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-243">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ac856-244">общедоступные значения HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ac856-244">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="ac856-245">Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-245">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-246">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ac856-246">get_HistoryCount</span></span> 

<span data-ttu-id="ac856-247">Получение HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-247">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="ac856-248">общедоступные значения HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="ac856-248">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="ac856-249">Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-249">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-250">get_InputData</span><span class="sxs-lookup"><span data-stu-id="ac856-250">get_InputData</span></span> 

<span data-ttu-id="ac856-251">Получение InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-251">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="ac856-252">общедоступные значения HRESULT [get_InputData](#get_inputdata)(Int32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="ac856-252">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="ac856-253">Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-253">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-254">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ac856-254">get_KeyStates</span></span> 

<span data-ttu-id="ac856-255">Получение KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-255">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="ac856-256">общедоступные значения HRESULT [get_KeyStates](#get_keystates)(DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="ac856-256">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="ac856-257">Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-257">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-258">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-258">get_PenFlags</span></span> 

<span data-ttu-id="ac856-259">Получение PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-259">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="ac856-260">общедоступные значения HRESULT [get_PenFlags](#get_penflags)(UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="ac856-260">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="ac856-261">Это соответствует свойству penFlags структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-261">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ac856-262">Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-262">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-263">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="ac856-263">get_PenMask</span></span> 

<span data-ttu-id="ac856-264">Получение PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-264">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="ac856-265">общедоступные значения HRESULT [get_PenMask](#get_penmask)(UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="ac856-265">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="ac856-266">Это соответствует свойству penMask структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-266">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ac856-267">Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-267">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-268">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ac856-268">get_PenPressure</span></span> 

<span data-ttu-id="ac856-269">Получение PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-269">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="ac856-270">общедоступные значения HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="ac856-270">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="ac856-271">Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-271">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-272">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ac856-272">get_PenRotation</span></span> 

<span data-ttu-id="ac856-273">Получение PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-273">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="ac856-274">общедоступные значения HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="ac856-274">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="ac856-275">Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-275">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-276">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ac856-276">get_PenTiltX</span></span> 

<span data-ttu-id="ac856-277">Получение PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-277">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="ac856-278">общедоступные значения HRESULT [get_PenTiltX](#get_pentiltx)(Int32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="ac856-278">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="ac856-279">Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-279">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-280">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ac856-280">get_PenTiltY</span></span> 

<span data-ttu-id="ac856-281">Получение PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-281">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="ac856-282">общедоступные значения HRESULT [get_PenTiltY](#get_pentilty)(Int32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="ac856-282">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="ac856-283">Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-283">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-284">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ac856-284">get_PerformanceCount</span></span> 

<span data-ttu-id="ac856-285">Получение PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-285">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="ac856-286">общедоступные значения HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="ac856-286">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="ac856-287">Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-287">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-288">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ac856-288">get_PixelLocation</span></span> 

<span data-ttu-id="ac856-289">Получение PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-289">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="ac856-290">общедоступные значения HRESULT [get_PixelLocation](#get_pixellocation)(Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="ac856-290">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="ac856-291">Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-291">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-292">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-292">get_PixelLocationRaw</span></span> 

<span data-ttu-id="ac856-293">Получение PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-293">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ac856-294">общедоступные значения HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ac856-294">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="ac856-295">Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-295">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-296">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ac856-296">get_PointerDeviceRect</span></span> 

<span data-ttu-id="ac856-297">Получите PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-297">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ac856-298">общедоступные значения HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="ac856-298">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="ac856-299">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-299">get_PointerFlags</span></span> 

<span data-ttu-id="ac856-300">Получение PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-300">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="ac856-301">общедоступные значения HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="ac856-301">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="ac856-302">Это соответствует свойству pointerFlags структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-302">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac856-303">Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-303">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-304">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="ac856-304">get_PointerId</span></span> 

<span data-ttu-id="ac856-305">Получение PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-305">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="ac856-306">общедоступные значения HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span><span class="sxs-lookup"><span data-stu-id="ac856-306">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="ac856-307">Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-307">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-308">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ac856-308">get_PointerKind</span></span> 

<span data-ttu-id="ac856-309">Получение PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-309">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="ac856-310">общедоступные значения HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="ac856-310">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="ac856-311">Это соответствует свойству pointerKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-311">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac856-312">Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-312">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="ac856-313">Поддерживает PT_PEN и PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="ac856-313">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="ac856-314">get_Time</span><span class="sxs-lookup"><span data-stu-id="ac856-314">get_Time</span></span> 

<span data-ttu-id="ac856-315">Получить время события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-315">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="ac856-316">общедоступные значения HRESULT [get_Time](#get_time)(DWORD \* Time)</span><span class="sxs-lookup"><span data-stu-id="ac856-316">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="ac856-317">Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-317">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-318">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ac856-318">get_TouchContact</span></span> 

<span data-ttu-id="ac856-319">Получение TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-319">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="ac856-320">общедоступные значения HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="ac856-320">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="ac856-321">Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-321">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-322">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-322">get_TouchContactRaw</span></span> 

<span data-ttu-id="ac856-323">Получение TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-323">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="ac856-324">общедоступные значения HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="ac856-324">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="ac856-325">Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-325">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-326">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-326">get_TouchFlags</span></span> 

<span data-ttu-id="ac856-327">Получение TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-327">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="ac856-328">общедоступные значения HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="ac856-328">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="ac856-329">Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-329">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ac856-330">Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-330">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-331">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ac856-331">get_TouchMask</span></span> 

<span data-ttu-id="ac856-332">Получение TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-332">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="ac856-333">общедоступные значения HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="ac856-333">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="ac856-334">Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-334">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ac856-335">Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-335">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-336">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ac856-336">get_TouchOrientation</span></span> 

<span data-ttu-id="ac856-337">Получение TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-337">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="ac856-338">общедоступные значения HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="ac856-338">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="ac856-339">Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-339">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-340">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ac856-340">get_TouchPressure</span></span> 

<span data-ttu-id="ac856-341">Получение TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-341">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="ac856-342">общедоступные значения HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="ac856-342">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="ac856-343">Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-343">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-344">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="ac856-344">put_ButtonChangeKind</span></span> 

<span data-ttu-id="ac856-345">Задайте ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-345">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="ac856-346">общедоступные значения HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(Int32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="ac856-346">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="ac856-347">Это соответствует свойству ButtonChangeKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-347">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac856-348">Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-348">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-349">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="ac856-349">put_DisplayRect</span></span> 

<span data-ttu-id="ac856-350">Задайте DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-350">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ac856-351">общедоступные значения HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="ac856-351">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="ac856-352">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="ac856-352">put_FrameId</span></span> 

<span data-ttu-id="ac856-353">Задайте FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-353">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="ac856-354">общедоступные значения HRESULT [put_FrameId](#put_frameid)(UINT32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="ac856-354">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="ac856-355">Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-355">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-356">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="ac856-356">put_HimetricLocation</span></span> 

<span data-ttu-id="ac856-357">Задайте HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-357">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="ac856-358">общедоступные значения HRESULT [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="ac856-358">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="ac856-359">Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-359">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-360">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-360">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="ac856-361">Задайте HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-361">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ac856-362">общедоступные значения HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ac856-362">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="ac856-363">Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-363">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-364">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="ac856-364">put_HistoryCount</span></span> 

<span data-ttu-id="ac856-365">Задайте HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-365">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="ac856-366">общедоступные значения HRESULT [put_HistoryCount](#put_historycount)(UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="ac856-366">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="ac856-367">Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-367">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-368">put_InputData</span><span class="sxs-lookup"><span data-stu-id="ac856-368">put_InputData</span></span> 

<span data-ttu-id="ac856-369">Задайте InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-369">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="ac856-370">общедоступные значения HRESULT [put_InputData](#put_inputdata)(Int32 InputData)</span><span class="sxs-lookup"><span data-stu-id="ac856-370">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="ac856-371">Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-371">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-372">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="ac856-372">put_KeyStates</span></span> 

<span data-ttu-id="ac856-373">Задайте KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-373">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="ac856-374">общедоступные значения HRESULT [put_KeyStates](#put_keystates)(DWORD KeyStates)</span><span class="sxs-lookup"><span data-stu-id="ac856-374">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="ac856-375">Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-375">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-376">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-376">put_PenFlags</span></span> 

<span data-ttu-id="ac856-377">Задайте PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-377">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="ac856-378">общедоступные значения HRESULT [put_PenFlags](#put_penflags)(UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="ac856-378">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="ac856-379">Это соответствует свойству penFlags структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-379">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ac856-380">Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-380">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-381">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="ac856-381">put_PenMask</span></span> 

<span data-ttu-id="ac856-382">Задайте PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-382">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="ac856-383">общедоступные значения HRESULT [put_PenMask](#put_penmask)(UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="ac856-383">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="ac856-384">Это соответствует свойству penMask структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-384">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="ac856-385">Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-385">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-386">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="ac856-386">put_PenPressure</span></span> 

<span data-ttu-id="ac856-387">Задайте PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-387">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="ac856-388">общедоступные значения HRESULT [put_PenPressure](#put_penpressure)(UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="ac856-388">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="ac856-389">Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-389">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-390">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="ac856-390">put_PenRotation</span></span> 

<span data-ttu-id="ac856-391">Задайте PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-391">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="ac856-392">общедоступные значения HRESULT [put_PenRotation](#put_penrotation)(UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="ac856-392">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="ac856-393">Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-393">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-394">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="ac856-394">put_PenTiltX</span></span> 

<span data-ttu-id="ac856-395">Задайте PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-395">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="ac856-396">общедоступные значения HRESULT [put_PenTiltX](#put_pentiltx)(Int32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="ac856-396">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="ac856-397">Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-397">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-398">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="ac856-398">put_PenTiltY</span></span> 

<span data-ttu-id="ac856-399">Задайте PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-399">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="ac856-400">общедоступные значения HRESULT [put_PenTiltY](#put_pentilty)(Int32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="ac856-400">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="ac856-401">Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-401">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-402">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="ac856-402">put_PerformanceCount</span></span> 

<span data-ttu-id="ac856-403">Задайте PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-403">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="ac856-404">общедоступные значения HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="ac856-404">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="ac856-405">Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-405">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-406">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="ac856-406">put_PixelLocation</span></span> 

<span data-ttu-id="ac856-407">Задайте PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-407">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="ac856-408">общедоступные значения HRESULT [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="ac856-408">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="ac856-409">Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-409">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-410">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-410">put_PixelLocationRaw</span></span> 

<span data-ttu-id="ac856-411">Задайте PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-411">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="ac856-412">общедоступные значения HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="ac856-412">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="ac856-413">Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-413">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-414">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="ac856-414">put_PointerDeviceRect</span></span> 

<span data-ttu-id="ac856-415">Задайте PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-415">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="ac856-416">общедоступные значения HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="ac856-416">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="ac856-417">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-417">put_PointerFlags</span></span> 

<span data-ttu-id="ac856-418">Задайте PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-418">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="ac856-419">общедоступные значения HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="ac856-419">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="ac856-420">Это соответствует свойству pointerFlags структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-420">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac856-421">Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-421">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-422">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="ac856-422">put_PointerId</span></span> 

<span data-ttu-id="ac856-423">Задайте PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-423">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="ac856-424">общедоступные значения HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span><span class="sxs-lookup"><span data-stu-id="ac856-424">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="ac856-425">Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-425">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-426">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="ac856-426">put_PointerKind</span></span> 

<span data-ttu-id="ac856-427">Задайте PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-427">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="ac856-428">общедоступные значения HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="ac856-428">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="ac856-429">Это соответствует свойству pointerKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-429">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="ac856-430">Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-430">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="ac856-431">Поддерживает PT_PEN и PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="ac856-431">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="ac856-432">put_Time</span><span class="sxs-lookup"><span data-stu-id="ac856-432">put_Time</span></span> 

<span data-ttu-id="ac856-433">Задайте время события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-433">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="ac856-434">общедоступные значения HRESULT [put_Time](#put_time)(время в DWORD)</span><span class="sxs-lookup"><span data-stu-id="ac856-434">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="ac856-435">Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-435">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-436">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="ac856-436">put_TouchContact</span></span> 

<span data-ttu-id="ac856-437">Задайте TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-437">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="ac856-438">общедоступные значения HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="ac856-438">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="ac856-439">Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-439">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-440">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="ac856-440">put_TouchContactRaw</span></span> 

<span data-ttu-id="ac856-441">Задайте TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-441">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="ac856-442">общедоступные значения HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="ac856-442">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="ac856-443">Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-443">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-444">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="ac856-444">put_TouchFlags</span></span> 

<span data-ttu-id="ac856-445">Задайте TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-445">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="ac856-446">общедоступные значения HRESULT [put_TouchFlags](#put_touchflags)(UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="ac856-446">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="ac856-447">Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-447">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ac856-448">Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-448">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-449">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="ac856-449">put_TouchMask</span></span> 

<span data-ttu-id="ac856-450">Задайте TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-450">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="ac856-451">общедоступные значения HRESULT [put_TouchMask](#put_touchmask)(UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="ac856-451">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="ac856-452">Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="ac856-452">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="ac856-453">Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-453">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-454">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="ac856-454">put_TouchOrientation</span></span> 

<span data-ttu-id="ac856-455">Задайте TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-455">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="ac856-456">общедоступные значения HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="ac856-456">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="ac856-457">Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-457">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="ac856-458">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="ac856-458">put_TouchPressure</span></span> 

<span data-ttu-id="ac856-459">Задайте TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="ac856-459">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="ac856-460">общедоступные значения HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="ac856-460">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="ac856-461">Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="ac856-461">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

