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
ms.openlocfilehash: ef0546c03e2d2ccc87677125772b1663f2ec6362
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699237"
---
# <span data-ttu-id="f0ed0-104">интерфейс ICoreWebView2ExperimentalPointerInfo</span><span class="sxs-lookup"><span data-stu-id="f0ed0-104">interface ICoreWebView2ExperimentalPointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="f0ed0-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

<span data-ttu-id="f0ed0-106">Это преимущественно представляет объединенный объект Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-106">This mostly represents a combined win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO object.</span></span>

## <span data-ttu-id="f0ed0-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f0ed0-107">Summary</span></span>

 <span data-ttu-id="f0ed0-108">Участников</span><span class="sxs-lookup"><span data-stu-id="f0ed0-108">Members</span></span>                        | <span data-ttu-id="f0ed0-109">Описания</span><span class="sxs-lookup"><span data-stu-id="f0ed0-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f0ed0-110">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="f0ed0-110">get_ButtonChangeKind</span></span>](#get_buttonchangekind) | <span data-ttu-id="f0ed0-111">Получение ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-111">Get the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-112">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="f0ed0-112">get_DisplayRect</span></span>](#get_displayrect) | <span data-ttu-id="f0ed0-113">Получите DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-113">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="f0ed0-114">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="f0ed0-114">get_FrameId</span></span>](#get_frameid) | <span data-ttu-id="f0ed0-115">Получение FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-115">Get the FrameID of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-116">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-116">get_HimetricLocation</span></span>](#get_himetriclocation) | <span data-ttu-id="f0ed0-117">Получение HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-117">Get the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-118">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-118">get_HimetricLocationRaw</span></span>](#get_himetriclocationraw) | <span data-ttu-id="f0ed0-119">Получение HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-119">Get the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-120">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="f0ed0-120">get_HistoryCount</span></span>](#get_historycount) | <span data-ttu-id="f0ed0-121">Получение HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-121">Get the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-122">get_InputData</span><span class="sxs-lookup"><span data-stu-id="f0ed0-122">get_InputData</span></span>](#get_inputdata) | <span data-ttu-id="f0ed0-123">Получение InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-123">Get the InputData of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-124">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="f0ed0-124">get_KeyStates</span></span>](#get_keystates) | <span data-ttu-id="f0ed0-125">Получение KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-125">Get the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-126">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-126">get_PenFlags</span></span>](#get_penflags) | <span data-ttu-id="f0ed0-127">Получение PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-127">Get the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-128">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="f0ed0-128">get_PenMask</span></span>](#get_penmask) | <span data-ttu-id="f0ed0-129">Получение PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-129">Get the PenMask of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-130">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="f0ed0-130">get_PenPressure</span></span>](#get_penpressure) | <span data-ttu-id="f0ed0-131">Получение PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-131">Get the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-132">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-132">get_PenRotation</span></span>](#get_penrotation) | <span data-ttu-id="f0ed0-133">Получение PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-133">Get the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-134">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="f0ed0-134">get_PenTiltX</span></span>](#get_pentiltx) | <span data-ttu-id="f0ed0-135">Получение PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-135">Get the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-136">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="f0ed0-136">get_PenTiltY</span></span>](#get_pentilty) | <span data-ttu-id="f0ed0-137">Получение PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-137">Get the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-138">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="f0ed0-138">get_PerformanceCount</span></span>](#get_performancecount) | <span data-ttu-id="f0ed0-139">Получение PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-139">Get the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-140">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-140">get_PixelLocation</span></span>](#get_pixellocation) | <span data-ttu-id="f0ed0-141">Получение PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-141">Get the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-142">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-142">get_PixelLocationRaw</span></span>](#get_pixellocationraw) | <span data-ttu-id="f0ed0-143">Получение PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-143">Get the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-144">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="f0ed0-144">get_PointerDeviceRect</span></span>](#get_pointerdevicerect) | <span data-ttu-id="f0ed0-145">Получите PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-145">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="f0ed0-146">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-146">get_PointerFlags</span></span>](#get_pointerflags) | <span data-ttu-id="f0ed0-147">Получение PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-147">Get the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-148">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="f0ed0-148">get_PointerId</span></span>](#get_pointerid) | <span data-ttu-id="f0ed0-149">Получение PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-149">Get the PointerId of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-150">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="f0ed0-150">get_PointerKind</span></span>](#get_pointerkind) | <span data-ttu-id="f0ed0-151">Получение PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-151">Get the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-152">get_Time</span><span class="sxs-lookup"><span data-stu-id="f0ed0-152">get_Time</span></span>](#get_time) | <span data-ttu-id="f0ed0-153">Получить время события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-153">Get the Time of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-154">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="f0ed0-154">get_TouchContact</span></span>](#get_touchcontact) | <span data-ttu-id="f0ed0-155">Получение TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-155">Get the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-156">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-156">get_TouchContactRaw</span></span>](#get_touchcontactraw) | <span data-ttu-id="f0ed0-157">Получение TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-157">Get the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-158">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-158">get_TouchFlags</span></span>](#get_touchflags) | <span data-ttu-id="f0ed0-159">Получение TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-159">Get the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-160">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="f0ed0-160">get_TouchMask</span></span>](#get_touchmask) | <span data-ttu-id="f0ed0-161">Получение TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-161">Get the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-162">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-162">get_TouchOrientation</span></span>](#get_touchorientation) | <span data-ttu-id="f0ed0-163">Получение TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-163">Get the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-164">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="f0ed0-164">get_TouchPressure</span></span>](#get_touchpressure) | <span data-ttu-id="f0ed0-165">Получение TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-165">Get the TouchPressure of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-166">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="f0ed0-166">put_ButtonChangeKind</span></span>](#put_buttonchangekind) | <span data-ttu-id="f0ed0-167">Задайте ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-167">Set the ButtonChangeKind of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-168">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="f0ed0-168">put_DisplayRect</span></span>](#put_displayrect) | <span data-ttu-id="f0ed0-169">Задайте DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-169">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="f0ed0-170">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="f0ed0-170">put_FrameId</span></span>](#put_frameid) | <span data-ttu-id="f0ed0-171">Задайте FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-171">Set the FrameID of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-172">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-172">put_HimetricLocation</span></span>](#put_himetriclocation) | <span data-ttu-id="f0ed0-173">Задайте HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-173">Set the HimetricLocation of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-174">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-174">put_HimetricLocationRaw</span></span>](#put_himetriclocationraw) | <span data-ttu-id="f0ed0-175">Задайте HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-175">Set the HimetricLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-176">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="f0ed0-176">put_HistoryCount</span></span>](#put_historycount) | <span data-ttu-id="f0ed0-177">Задайте HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-177">Set the HistoryCount of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-178">put_InputData</span><span class="sxs-lookup"><span data-stu-id="f0ed0-178">put_InputData</span></span>](#put_inputdata) | <span data-ttu-id="f0ed0-179">Задайте InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-179">Set the InputData of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-180">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="f0ed0-180">put_KeyStates</span></span>](#put_keystates) | <span data-ttu-id="f0ed0-181">Задайте KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-181">Set the KeyStates of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-182">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-182">put_PenFlags</span></span>](#put_penflags) | <span data-ttu-id="f0ed0-183">Задайте PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-183">Set the PenFlags of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-184">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="f0ed0-184">put_PenMask</span></span>](#put_penmask) | <span data-ttu-id="f0ed0-185">Задайте PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-185">Set the PenMask of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-186">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="f0ed0-186">put_PenPressure</span></span>](#put_penpressure) | <span data-ttu-id="f0ed0-187">Задайте PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-187">Set the PenPressure of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-188">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-188">put_PenRotation</span></span>](#put_penrotation) | <span data-ttu-id="f0ed0-189">Задайте PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-189">Set the PenRotation of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-190">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="f0ed0-190">put_PenTiltX</span></span>](#put_pentiltx) | <span data-ttu-id="f0ed0-191">Задайте PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-191">Set the PenTiltX of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-192">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="f0ed0-192">put_PenTiltY</span></span>](#put_pentilty) | <span data-ttu-id="f0ed0-193">Задайте PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-193">Set the PenTiltY of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-194">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="f0ed0-194">put_PerformanceCount</span></span>](#put_performancecount) | <span data-ttu-id="f0ed0-195">Задайте PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-195">Set the PerformanceCount of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-196">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-196">put_PixelLocation</span></span>](#put_pixellocation) | <span data-ttu-id="f0ed0-197">Задайте PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-197">Set the PixelLocation of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-198">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-198">put_PixelLocationRaw</span></span>](#put_pixellocationraw) | <span data-ttu-id="f0ed0-199">Задайте PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-199">Set the PixelLocationRaw of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-200">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="f0ed0-200">put_PointerDeviceRect</span></span>](#put_pointerdevicerect) | <span data-ttu-id="f0ed0-201">Задайте PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-201">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>
[<span data-ttu-id="f0ed0-202">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-202">put_PointerFlags</span></span>](#put_pointerflags) | <span data-ttu-id="f0ed0-203">Задайте PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-203">Set the PointerFlags of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-204">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="f0ed0-204">put_PointerId</span></span>](#put_pointerid) | <span data-ttu-id="f0ed0-205">Задайте PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-205">Set the PointerId of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-206">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="f0ed0-206">put_PointerKind</span></span>](#put_pointerkind) | <span data-ttu-id="f0ed0-207">Задайте PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-207">Set the PointerKind of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-208">put_Time</span><span class="sxs-lookup"><span data-stu-id="f0ed0-208">put_Time</span></span>](#put_time) | <span data-ttu-id="f0ed0-209">Задайте время события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-209">Set the Time of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-210">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="f0ed0-210">put_TouchContact</span></span>](#put_touchcontact) | <span data-ttu-id="f0ed0-211">Задайте TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-211">Set the TouchContact of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-212">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-212">put_TouchContactRaw</span></span>](#put_touchcontactraw) | <span data-ttu-id="f0ed0-213">Задайте TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-213">Set the TouchContactRaw of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-214">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-214">put_TouchFlags</span></span>](#put_touchflags) | <span data-ttu-id="f0ed0-215">Задайте TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-215">Set the TouchFlags of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-216">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="f0ed0-216">put_TouchMask</span></span>](#put_touchmask) | <span data-ttu-id="f0ed0-217">Задайте TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-217">Set the TouchMask of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-218">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-218">put_TouchOrientation</span></span>](#put_touchorientation) | <span data-ttu-id="f0ed0-219">Задайте TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-219">Set the TouchOrientation of the pointer event.</span></span>
[<span data-ttu-id="f0ed0-220">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="f0ed0-220">put_TouchPressure</span></span>](#put_touchpressure) | <span data-ttu-id="f0ed0-221">Задайте TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-221">Set the TouchPressure of the pointer event.</span></span>

<span data-ttu-id="f0ed0-222">Он берет на себя поля из всех трех типов данных, таких как HWND и ДЕСКРИПТОРы.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-222">It takes fields from all three and excludes some win32 specific data types like HWND and HANDLE.</span></span> <span data-ttu-id="f0ed0-223">Обратите внимание, что sourceDevice используется, но мы ожидаем, что PointerDeviceRect и DisplayRect будут охватывать существующие варианты использования sourceDevice.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-223">Note, sourceDevice is taken out but we expect the PointerDeviceRect and DisplayRect to cover the existing use cases of sourceDevice.</span></span> <span data-ttu-id="f0ed0-224">Еще одна большая разница заключается в том, что любое из расположений Point или Rect ожидается в WebView физических координат.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-224">Another big difference is that any of the point or rect locations are expected to be in webview physical coordinates.</span></span> <span data-ttu-id="f0ed0-225">Это значит, что координаты относительно WebView и не применяются к масштабированию DPI.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-225">That is, coordinates relative to the webview and no DPI scaling applied.</span></span>

## <span data-ttu-id="f0ed0-226">Участников</span><span class="sxs-lookup"><span data-stu-id="f0ed0-226">Members</span></span>

#### <span data-ttu-id="f0ed0-227">get_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="f0ed0-227">get_ButtonChangeKind</span></span> 

<span data-ttu-id="f0ed0-228">Получение ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-228">Get the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-229">общедоступные значения HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(Int32 \* ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-229">public HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(INT32 \* buttonChangeKind)</span></span>

<span data-ttu-id="f0ed0-230">Это соответствует свойству ButtonChangeKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-230">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="f0ed0-231">Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-231">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-232">get_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="f0ed0-232">get_DisplayRect</span></span> 

<span data-ttu-id="f0ed0-233">Получите DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-233">Get the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="f0ed0-234">общедоступные значения HRESULT [get_DisplayRect](#get_displayrect)(Rect \* DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-234">public HRESULT [get_DisplayRect](#get_displayrect)(RECT \* displayRect)</span></span>

#### <span data-ttu-id="f0ed0-235">get_FrameId</span><span class="sxs-lookup"><span data-stu-id="f0ed0-235">get_FrameId</span></span> 

<span data-ttu-id="f0ed0-236">Получение FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-236">Get the FrameID of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-237">общедоступные значения HRESULT [get_FrameId](#get_frameid)(UINT32 \* FrameId)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-237">public HRESULT [get_FrameId](#get_frameid)(UINT32 \* frameId)</span></span>

<span data-ttu-id="f0ed0-238">Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-238">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-239">get_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-239">get_HimetricLocation</span></span> 

<span data-ttu-id="f0ed0-240">Получение HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-240">Get the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-241">общедоступные значения HRESULT [get_HimetricLocation](#get_himetriclocation)(Point \* HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-241">public HRESULT [get_HimetricLocation](#get_himetriclocation)(POINT \* himetricLocation)</span></span>

<span data-ttu-id="f0ed0-242">Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-242">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-243">get_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-243">get_HimetricLocationRaw</span></span> 

<span data-ttu-id="f0ed0-244">Получение HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-244">Get the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-245">общедоступные значения HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(Point \* HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-245">public HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(POINT \* himetricLocationRaw)</span></span>

<span data-ttu-id="f0ed0-246">Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-246">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-247">get_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="f0ed0-247">get_HistoryCount</span></span> 

<span data-ttu-id="f0ed0-248">Получение HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-248">Get the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-249">общедоступные значения HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-249">public HRESULT [get_HistoryCount](#get_historycount)(UINT32 \* historyCount)</span></span>

<span data-ttu-id="f0ed0-250">Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-250">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-251">get_InputData</span><span class="sxs-lookup"><span data-stu-id="f0ed0-251">get_InputData</span></span> 

<span data-ttu-id="f0ed0-252">Получение InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-252">Get the InputData of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-253">общедоступные значения HRESULT [get_InputData](#get_inputdata)(Int32 \* InputData)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-253">public HRESULT [get_InputData](#get_inputdata)(INT32 \* inputData)</span></span>

<span data-ttu-id="f0ed0-254">Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-254">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-255">get_KeyStates</span><span class="sxs-lookup"><span data-stu-id="f0ed0-255">get_KeyStates</span></span> 

<span data-ttu-id="f0ed0-256">Получение KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-256">Get the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-257">общедоступные значения HRESULT [get_KeyStates](#get_keystates)(DWORD \* KeyStates)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-257">public HRESULT [get_KeyStates](#get_keystates)(DWORD \* keyStates)</span></span>

<span data-ttu-id="f0ed0-258">Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-258">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-259">get_PenFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-259">get_PenFlags</span></span> 

<span data-ttu-id="f0ed0-260">Получение PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-260">Get the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-261">общедоступные значения HRESULT [get_PenFlags](#get_penflags)(UINT32 \* PenFlags)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-261">public HRESULT [get_PenFlags](#get_penflags)(UINT32 \* penFLags)</span></span>

<span data-ttu-id="f0ed0-262">Это соответствует свойству penFlags структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-262">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="f0ed0-263">Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-263">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-264">get_PenMask</span><span class="sxs-lookup"><span data-stu-id="f0ed0-264">get_PenMask</span></span> 

<span data-ttu-id="f0ed0-265">Получение PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-265">Get the PenMask of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-266">общедоступные значения HRESULT [get_PenMask](#get_penmask)(UINT32 \* PenMask)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-266">public HRESULT [get_PenMask](#get_penmask)(UINT32 \* penMask)</span></span>

<span data-ttu-id="f0ed0-267">Это соответствует свойству penMask структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-267">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="f0ed0-268">Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-268">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-269">get_PenPressure</span><span class="sxs-lookup"><span data-stu-id="f0ed0-269">get_PenPressure</span></span> 

<span data-ttu-id="f0ed0-270">Получение PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-270">Get the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-271">общедоступные значения HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* PenPressure)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-271">public HRESULT [get_PenPressure](#get_penpressure)(UINT32 \* penPressure)</span></span>

<span data-ttu-id="f0ed0-272">Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-272">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-273">get_PenRotation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-273">get_PenRotation</span></span> 

<span data-ttu-id="f0ed0-274">Получение PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-274">Get the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-275">общедоступные значения HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* PenRotation)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-275">public HRESULT [get_PenRotation](#get_penrotation)(UINT32 \* penRotation)</span></span>

<span data-ttu-id="f0ed0-276">Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-276">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-277">get_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="f0ed0-277">get_PenTiltX</span></span> 

<span data-ttu-id="f0ed0-278">Получение PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-278">Get the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-279">общедоступные значения HRESULT [get_PenTiltX](#get_pentiltx)(Int32 \* PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-279">public HRESULT [get_PenTiltX](#get_pentiltx)(INT32 \* penTiltX)</span></span>

<span data-ttu-id="f0ed0-280">Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-280">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-281">get_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="f0ed0-281">get_PenTiltY</span></span> 

<span data-ttu-id="f0ed0-282">Получение PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-282">Get the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-283">общедоступные значения HRESULT [get_PenTiltY](#get_pentilty)(Int32 \* PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-283">public HRESULT [get_PenTiltY](#get_pentilty)(INT32 \* penTiltY)</span></span>

<span data-ttu-id="f0ed0-284">Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-284">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-285">get_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="f0ed0-285">get_PerformanceCount</span></span> 

<span data-ttu-id="f0ed0-286">Получение PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-286">Get the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-287">общедоступные значения HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-287">public HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 \* performanceCount)</span></span>

<span data-ttu-id="f0ed0-288">Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-288">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-289">get_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-289">get_PixelLocation</span></span> 

<span data-ttu-id="f0ed0-290">Получение PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-290">Get the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-291">общедоступные значения HRESULT [get_PixelLocation](#get_pixellocation)(Point \* PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-291">public HRESULT [get_PixelLocation](#get_pixellocation)(POINT \* pixelLocation)</span></span>

<span data-ttu-id="f0ed0-292">Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-292">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-293">get_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-293">get_PixelLocationRaw</span></span> 

<span data-ttu-id="f0ed0-294">Получение PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-294">Get the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-295">общедоступные значения HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(Point \* PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-295">public HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(POINT \* pixelLocationRaw)</span></span>

<span data-ttu-id="f0ed0-296">Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-296">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-297">get_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="f0ed0-297">get_PointerDeviceRect</span></span> 

<span data-ttu-id="f0ed0-298">Получите PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-298">Get the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="f0ed0-299">общедоступные значения HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect \* PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-299">public HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(RECT \* pointerDeviceRect)</span></span>

#### <span data-ttu-id="f0ed0-300">get_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-300">get_PointerFlags</span></span> 

<span data-ttu-id="f0ed0-301">Получение PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-301">Get the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-302">общедоступные значения HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-302">public HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 \* pointerFlags)</span></span>

<span data-ttu-id="f0ed0-303">Это соответствует свойству pointerFlags структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-303">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="f0ed0-304">Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-304">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-305">get_PointerId</span><span class="sxs-lookup"><span data-stu-id="f0ed0-305">get_PointerId</span></span> 

<span data-ttu-id="f0ed0-306">Получение PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-306">Get the PointerId of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-307">общедоступные значения HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-307">public HRESULT [get_PointerId](#get_pointerid)(UINT32 \* pointerId)</span></span>

<span data-ttu-id="f0ed0-308">Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-308">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-309">get_PointerKind</span><span class="sxs-lookup"><span data-stu-id="f0ed0-309">get_PointerKind</span></span> 

<span data-ttu-id="f0ed0-310">Получение PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-310">Get the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-311">общедоступные значения HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* PointerKind)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-311">public HRESULT [get_PointerKind](#get_pointerkind)(DWORD \* pointerKind)</span></span>

<span data-ttu-id="f0ed0-312">Это соответствует свойству pointerKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-312">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="f0ed0-313">Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-313">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="f0ed0-314">Поддерживает PT_PEN и PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-314">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="f0ed0-315">get_Time</span><span class="sxs-lookup"><span data-stu-id="f0ed0-315">get_Time</span></span> 

<span data-ttu-id="f0ed0-316">Получить время события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-316">Get the Time of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-317">общедоступные значения HRESULT [get_Time](#get_time)(DWORD \* Time)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-317">public HRESULT [get_Time](#get_time)(DWORD \* time)</span></span>

<span data-ttu-id="f0ed0-318">Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-318">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-319">get_TouchContact</span><span class="sxs-lookup"><span data-stu-id="f0ed0-319">get_TouchContact</span></span> 

<span data-ttu-id="f0ed0-320">Получение TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-320">Get the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-321">общедоступные значения HRESULT [get_TouchContact](#get_touchcontact)(Rect \* TouchContact)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-321">public HRESULT [get_TouchContact](#get_touchcontact)(RECT \* touchContact)</span></span>

<span data-ttu-id="f0ed0-322">Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-322">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-323">get_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-323">get_TouchContactRaw</span></span> 

<span data-ttu-id="f0ed0-324">Получение TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-324">Get the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-325">общедоступные значения HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect \* TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-325">public HRESULT [get_TouchContactRaw](#get_touchcontactraw)(RECT \* touchContactRaw)</span></span>

<span data-ttu-id="f0ed0-326">Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-326">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-327">get_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-327">get_TouchFlags</span></span> 

<span data-ttu-id="f0ed0-328">Получение TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-328">Get the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-329">общедоступные значения HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-329">public HRESULT [get_TouchFlags](#get_touchflags)(UINT32 \* touchFlags)</span></span>

<span data-ttu-id="f0ed0-330">Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-330">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="f0ed0-331">Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-331">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-332">get_TouchMask</span><span class="sxs-lookup"><span data-stu-id="f0ed0-332">get_TouchMask</span></span> 

<span data-ttu-id="f0ed0-333">Получение TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-333">Get the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-334">общедоступные значения HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* TouchMask)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-334">public HRESULT [get_TouchMask](#get_touchmask)(UINT32 \* touchMask)</span></span>

<span data-ttu-id="f0ed0-335">Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-335">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="f0ed0-336">Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-336">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-337">get_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-337">get_TouchOrientation</span></span> 

<span data-ttu-id="f0ed0-338">Получение TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-338">Get the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-339">общедоступные значения HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-339">public HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 \* touchOrientation)</span></span>

<span data-ttu-id="f0ed0-340">Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-340">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-341">get_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="f0ed0-341">get_TouchPressure</span></span> 

<span data-ttu-id="f0ed0-342">Получение TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-342">Get the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-343">общедоступные значения HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-343">public HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 \* touchPressure)</span></span>

<span data-ttu-id="f0ed0-344">Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-344">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-345">put_ButtonChangeKind</span><span class="sxs-lookup"><span data-stu-id="f0ed0-345">put_ButtonChangeKind</span></span> 

<span data-ttu-id="f0ed0-346">Задайте ButtonChangeKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-346">Set the ButtonChangeKind of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-347">общедоступные значения HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(Int32 ButtonChangeKind)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-347">public HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(INT32 buttonChangeKind)</span></span>

<span data-ttu-id="f0ed0-348">Это соответствует свойству ButtonChangeKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-348">This corresponds to the ButtonChangeKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="f0ed0-349">Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-349">The values are defined by the POINTER_BUTTON_CHANGE_KIND enum in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-350">put_DisplayRect</span><span class="sxs-lookup"><span data-stu-id="f0ed0-350">put_DisplayRect</span></span> 

<span data-ttu-id="f0ed0-351">Задайте DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-351">Set the DisplayRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="f0ed0-352">общедоступные значения HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-352">public HRESULT [put_DisplayRect](#put_displayrect)(RECT displayRect)</span></span>

#### <span data-ttu-id="f0ed0-353">put_FrameId</span><span class="sxs-lookup"><span data-stu-id="f0ed0-353">put_FrameId</span></span> 

<span data-ttu-id="f0ed0-354">Задайте FrameID события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-354">Set the FrameID of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-355">общедоступные значения HRESULT [put_FrameId](#put_frameid)(UINT32 FrameId)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-355">public HRESULT [put_FrameId](#put_frameid)(UINT32 frameId)</span></span>

<span data-ttu-id="f0ed0-356">Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-356">This corresponds to the frameId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-357">put_HimetricLocation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-357">put_HimetricLocation</span></span> 

<span data-ttu-id="f0ed0-358">Задайте HimetricLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-358">Set the HimetricLocation of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-359">общедоступные значения HRESULT [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-359">public HRESULT [put_HimetricLocation](#put_himetriclocation)(POINT himetricLocation)</span></span>

<span data-ttu-id="f0ed0-360">Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-360">This corresponds to the ptHimetricLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-361">put_HimetricLocationRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-361">put_HimetricLocationRaw</span></span> 

<span data-ttu-id="f0ed0-362">Задайте HimetricLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-362">Set the HimetricLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-363">общедоступные значения HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-363">public HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(POINT himetricLocationRaw)</span></span>

<span data-ttu-id="f0ed0-364">Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-364">This corresponds to the ptHimetricLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-365">put_HistoryCount</span><span class="sxs-lookup"><span data-stu-id="f0ed0-365">put_HistoryCount</span></span> 

<span data-ttu-id="f0ed0-366">Задайте HistoryCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-366">Set the HistoryCount of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-367">общедоступные значения HRESULT [put_HistoryCount](#put_historycount)(UINT32 HistoryCount)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-367">public HRESULT [put_HistoryCount](#put_historycount)(UINT32 historyCount)</span></span>

<span data-ttu-id="f0ed0-368">Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-368">This corresponds to the historyCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-369">put_InputData</span><span class="sxs-lookup"><span data-stu-id="f0ed0-369">put_InputData</span></span> 

<span data-ttu-id="f0ed0-370">Задайте InputData события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-370">Set the InputData of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-371">общедоступные значения HRESULT [put_InputData](#put_inputdata)(Int32 InputData)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-371">public HRESULT [put_InputData](#put_inputdata)(INT32 inputData)</span></span>

<span data-ttu-id="f0ed0-372">Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-372">This corresponds to the InputData property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-373">put_KeyStates</span><span class="sxs-lookup"><span data-stu-id="f0ed0-373">put_KeyStates</span></span> 

<span data-ttu-id="f0ed0-374">Задайте KeyStates события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-374">Set the KeyStates of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-375">общедоступные значения HRESULT [put_KeyStates](#put_keystates)(DWORD KeyStates)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-375">public HRESULT [put_KeyStates](#put_keystates)(DWORD keyStates)</span></span>

<span data-ttu-id="f0ed0-376">Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-376">This corresponds to the dwKeyStates property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-377">put_PenFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-377">put_PenFlags</span></span> 

<span data-ttu-id="f0ed0-378">Задайте PenFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-378">Set the PenFlags of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-379">общедоступные значения HRESULT [put_PenFlags](#put_penflags)(UINT32 PenFlags)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-379">public HRESULT [put_PenFlags](#put_penflags)(UINT32 penFLags)</span></span>

<span data-ttu-id="f0ed0-380">Это соответствует свойству penFlags структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-380">This corresponds to the penFlags property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="f0ed0-381">Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-381">The values are defined by the PEN_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-382">put_PenMask</span><span class="sxs-lookup"><span data-stu-id="f0ed0-382">put_PenMask</span></span> 

<span data-ttu-id="f0ed0-383">Задайте PenMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-383">Set the PenMask of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-384">общедоступные значения HRESULT [put_PenMask](#put_penmask)(UINT32 PenMask)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-384">public HRESULT [put_PenMask](#put_penmask)(UINT32 penMask)</span></span>

<span data-ttu-id="f0ed0-385">Это соответствует свойству penMask структуры POINTER_PEN_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-385">This corresponds to the penMask property of the POINTER_PEN_INFO struct.</span></span> <span data-ttu-id="f0ed0-386">Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-386">The values are defined by the PEN_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-387">put_PenPressure</span><span class="sxs-lookup"><span data-stu-id="f0ed0-387">put_PenPressure</span></span> 

<span data-ttu-id="f0ed0-388">Задайте PenPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-388">Set the PenPressure of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-389">общедоступные значения HRESULT [put_PenPressure](#put_penpressure)(UINT32 PenPressure)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-389">public HRESULT [put_PenPressure](#put_penpressure)(UINT32 penPressure)</span></span>

<span data-ttu-id="f0ed0-390">Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-390">This corresponds to the pressure property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-391">put_PenRotation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-391">put_PenRotation</span></span> 

<span data-ttu-id="f0ed0-392">Задайте PenRotation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-392">Set the PenRotation of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-393">общедоступные значения HRESULT [put_PenRotation](#put_penrotation)(UINT32 PenRotation)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-393">public HRESULT [put_PenRotation](#put_penrotation)(UINT32 penRotation)</span></span>

<span data-ttu-id="f0ed0-394">Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-394">This corresponds to the rotation property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-395">put_PenTiltX</span><span class="sxs-lookup"><span data-stu-id="f0ed0-395">put_PenTiltX</span></span> 

<span data-ttu-id="f0ed0-396">Задайте PenTiltX события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-396">Set the PenTiltX of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-397">общедоступные значения HRESULT [put_PenTiltX](#put_pentiltx)(Int32 PenTiltX)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-397">public HRESULT [put_PenTiltX](#put_pentiltx)(INT32 penTiltX)</span></span>

<span data-ttu-id="f0ed0-398">Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-398">This corresponds to the tiltX property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-399">put_PenTiltY</span><span class="sxs-lookup"><span data-stu-id="f0ed0-399">put_PenTiltY</span></span> 

<span data-ttu-id="f0ed0-400">Задайте PenTiltY события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-400">Set the PenTiltY of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-401">общедоступные значения HRESULT [put_PenTiltY](#put_pentilty)(Int32 PenTiltY)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-401">public HRESULT [put_PenTiltY](#put_pentilty)(INT32 penTiltY)</span></span>

<span data-ttu-id="f0ed0-402">Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-402">This corresponds to the tiltY property of the POINTER_PEN_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-403">put_PerformanceCount</span><span class="sxs-lookup"><span data-stu-id="f0ed0-403">put_PerformanceCount</span></span> 

<span data-ttu-id="f0ed0-404">Задайте PerformanceCount события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-404">Set the PerformanceCount of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-405">общедоступные значения HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-405">public HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 performanceCount)</span></span>

<span data-ttu-id="f0ed0-406">Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-406">This corresponds to the PerformanceCount property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-407">put_PixelLocation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-407">put_PixelLocation</span></span> 

<span data-ttu-id="f0ed0-408">Задайте PixelLocation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-408">Set the PixelLocation of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-409">общедоступные значения HRESULT [put_PixelLocation](#put_pixellocation)(Point PixelLocation)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-409">public HRESULT [put_PixelLocation](#put_pixellocation)(POINT pixelLocation)</span></span>

<span data-ttu-id="f0ed0-410">Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-410">This corresponds to the ptPixelLocation property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-411">put_PixelLocationRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-411">put_PixelLocationRaw</span></span> 

<span data-ttu-id="f0ed0-412">Задайте PixelLocationRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-412">Set the PixelLocationRaw of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-413">общедоступные значения HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-413">public HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(POINT pixelLocationRaw)</span></span>

<span data-ttu-id="f0ed0-414">Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-414">This corresponds to the ptPixelLocationRaw property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-415">put_PointerDeviceRect</span><span class="sxs-lookup"><span data-stu-id="f0ed0-415">put_PointerDeviceRect</span></span> 

<span data-ttu-id="f0ed0-416">Задайте PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-416">Set the PointerDeviceRect of the sourceDevice property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

> <span data-ttu-id="f0ed0-417">общедоступные значения HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-417">public HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(RECT pointerDeviceRect)</span></span>

#### <span data-ttu-id="f0ed0-418">put_PointerFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-418">put_PointerFlags</span></span> 

<span data-ttu-id="f0ed0-419">Задайте PointerFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-419">Set the PointerFlags of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-420">общедоступные значения HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 PointerFlags)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-420">public HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 pointerFlags)</span></span>

<span data-ttu-id="f0ed0-421">Это соответствует свойству pointerFlags структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-421">This corresponds to the pointerFlags property of the POINTER_INFO struct.</span></span> <span data-ttu-id="f0ed0-422">Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-422">The values are defined by the POINTER_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-423">put_PointerId</span><span class="sxs-lookup"><span data-stu-id="f0ed0-423">put_PointerId</span></span> 

<span data-ttu-id="f0ed0-424">Задайте PointerId события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-424">Set the PointerId of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-425">общедоступные значения HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-425">public HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)</span></span>

<span data-ttu-id="f0ed0-426">Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-426">This corresponds to the pointerId property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-427">put_PointerKind</span><span class="sxs-lookup"><span data-stu-id="f0ed0-427">put_PointerKind</span></span> 

<span data-ttu-id="f0ed0-428">Задайте PointerKind события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-428">Set the PointerKind of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-429">общедоступные значения HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-429">public HRESULT [put_PointerKind](#put_pointerkind)(DWORD pointerKind)</span></span>

<span data-ttu-id="f0ed0-430">Это соответствует свойству pointerKind структуры POINTER_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-430">This corresponds to the pointerKind property of the POINTER_INFO struct.</span></span> <span data-ttu-id="f0ed0-431">Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-431">The values are defined by the POINTER_INPUT_KIND enum in the Windows SDK (winuser.h).</span></span> <span data-ttu-id="f0ed0-432">Поддерживает PT_PEN и PT_TOUCH.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-432">Supports PT_PEN and PT_TOUCH.</span></span>

#### <span data-ttu-id="f0ed0-433">put_Time</span><span class="sxs-lookup"><span data-stu-id="f0ed0-433">put_Time</span></span> 

<span data-ttu-id="f0ed0-434">Задайте время события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-434">Set the Time of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-435">общедоступные значения HRESULT [put_Time](#put_time)(время в DWORD)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-435">public HRESULT [put_Time](#put_time)(DWORD time)</span></span>

<span data-ttu-id="f0ed0-436">Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-436">This corresponds to the dwTime property of the POINTER_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-437">put_TouchContact</span><span class="sxs-lookup"><span data-stu-id="f0ed0-437">put_TouchContact</span></span> 

<span data-ttu-id="f0ed0-438">Задайте TouchContact события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-438">Set the TouchContact of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-439">общедоступные значения HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-439">public HRESULT [put_TouchContact](#put_touchcontact)(RECT touchContact)</span></span>

<span data-ttu-id="f0ed0-440">Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-440">This corresponds to the rcContact property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-441">put_TouchContactRaw</span><span class="sxs-lookup"><span data-stu-id="f0ed0-441">put_TouchContactRaw</span></span> 

<span data-ttu-id="f0ed0-442">Задайте TouchContactRaw события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-442">Set the TouchContactRaw of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-443">общедоступные значения HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-443">public HRESULT [put_TouchContactRaw](#put_touchcontactraw)(RECT touchContactRaw)</span></span>

<span data-ttu-id="f0ed0-444">Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-444">This corresponds to the rcContactRaw property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-445">put_TouchFlags</span><span class="sxs-lookup"><span data-stu-id="f0ed0-445">put_TouchFlags</span></span> 

<span data-ttu-id="f0ed0-446">Задайте TouchFlags события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-446">Set the TouchFlags of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-447">общедоступные значения HRESULT [put_TouchFlags](#put_touchflags)(UINT32 TouchFlags)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-447">public HRESULT [put_TouchFlags](#put_touchflags)(UINT32 touchFlags)</span></span>

<span data-ttu-id="f0ed0-448">Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-448">This corresponds to the touchFlags property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="f0ed0-449">Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-449">The values are defined by the TOUCH_FLAGS constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-450">put_TouchMask</span><span class="sxs-lookup"><span data-stu-id="f0ed0-450">put_TouchMask</span></span> 

<span data-ttu-id="f0ed0-451">Задайте TouchMask события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-451">Set the TouchMask of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-452">общедоступные значения HRESULT [put_TouchMask](#put_touchmask)(UINT32 TouchMask)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-452">public HRESULT [put_TouchMask](#put_touchmask)(UINT32 touchMask)</span></span>

<span data-ttu-id="f0ed0-453">Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-453">This corresponds to the touchMask property of the POINTER_TOUCH_INFO struct.</span></span> <span data-ttu-id="f0ed0-454">Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-454">The values are defined by the TOUCH_MASK constants in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-455">put_TouchOrientation</span><span class="sxs-lookup"><span data-stu-id="f0ed0-455">put_TouchOrientation</span></span> 

<span data-ttu-id="f0ed0-456">Задайте TouchOrientation события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-456">Set the TouchOrientation of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-457">общедоступные значения HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 TouchOrientation)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-457">public HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 touchOrientation)</span></span>

<span data-ttu-id="f0ed0-458">Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-458">This corresponds to the orientation property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

#### <span data-ttu-id="f0ed0-459">put_TouchPressure</span><span class="sxs-lookup"><span data-stu-id="f0ed0-459">put_TouchPressure</span></span> 

<span data-ttu-id="f0ed0-460">Задайте TouchPressure события указателя.</span><span class="sxs-lookup"><span data-stu-id="f0ed0-460">Set the TouchPressure of the pointer event.</span></span>

> <span data-ttu-id="f0ed0-461">общедоступные значения HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 TouchPressure)</span><span class="sxs-lookup"><span data-stu-id="f0ed0-461">public HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 touchPressure)</span></span>

<span data-ttu-id="f0ed0-462">Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).</span><span class="sxs-lookup"><span data-stu-id="f0ed0-462">This corresponds to the pressure property of the POINTER_TOUCH_INFO struct as defined in the Windows SDK (winuser.h).</span></span>

