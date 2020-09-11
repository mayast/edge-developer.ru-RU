---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 34ffa5fe0eabfe8e822db2792d2b25ab5106442a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012445"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2PointerInfo 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Это преимущественно представляет объединенный объект Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[ButtonChangeKind](#buttonchangekind) | ButtonChangeKind события указателя.
[DisplayRect](#displayrect) | DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).
[FrameId](#frameid) | FrameID события указателя.
[HimetricLocation](#himetriclocation) | HimetricLocation события указателя.
[HimetricLocationRaw](#himetriclocationraw) | HimetricLocationRaw события указателя.
[HistoryCount](#historycount) | HistoryCount события указателя.
[InputData](#inputdata) | InputData события указателя.
[KeyStates](#keystates) | KeyStates события указателя.
[PenFlags](#penflags) | PenFlags события указателя.
[PenMask](#penmask) | PenMask события указателя.
[PenPressure](#penpressure) | PenPressure события указателя.
[PenRotation](#penrotation) | PenRotation события указателя.
[PenTiltX](#pentiltx) | PenTiltX события указателя.
[PenTiltY](#pentilty) | PenTiltY события указателя.
[PerformanceCount](#performancecount) | PerformanceCount события указателя.
[PixelLocation](#pixellocation) | PixelLocation события указателя.
[PixelLocationRaw](#pixellocationraw) | PixelLocationRaw события указателя.
[PointerDeviceRect](#pointerdevicerect) | PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).
[PointerFlags](#pointerflags) | PointerFlags события указателя.
[PointerId](#pointerid) | PointerId события указателя.
[PointerKind](#pointerkind) | PointerKind события указателя.
[Время](#time) | Время события указателя.
[TouchContact](#touchcontact) | TouchContact события указателя.
[TouchContactRaw](#touchcontactraw) | TouchContactRaw события указателя.
[TouchFlags](#touchflags) | TouchFlags события указателя.
[TouchMask](#touchmask) | TouchMask события указателя.
[TouchOrientation](#touchorientation) | TouchOrientation события указателя.
[TouchPressure](#touchpressure) | TouchPressure события указателя.

## Участников

#### ButtonChangeKind 

ButtonChangeKind события указателя.

> public int [ButtonChangeKind](#buttonchangekind)

Это соответствует свойству ButtonChangeKind структуры POINTER_INFO. Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).

#### DisplayRect 

DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).

> общедоступный прямоугольник [DisplayRect](#displayrect)

#### FrameId 

FrameID события указателя.

> Открытый uint [FrameId](#frameid)

Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### HimetricLocation 

HimetricLocation события указателя.

> общедоступная точка [HimetricLocation](#himetriclocation)

Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### HimetricLocationRaw 

HimetricLocationRaw события указателя.

> общедоступная точка [HimetricLocationRaw](#himetriclocationraw)

Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### HistoryCount 

HistoryCount события указателя.

> Открытый uint [HistoryCount](#historycount)

Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### InputData 

InputData события указателя.

> public int [InputData](#inputdata)

Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### KeyStates 

KeyStates события указателя.

> Открытый uint [KeyStates](#keystates)

Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### PenFlags 

PenFlags события указателя.

> Открытый uint [PenFlags](#penflags)

Это соответствует свойству penFlags структуры POINTER_PEN_INFO. Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).

#### PenMask 

PenMask события указателя.

> Открытый uint [PenMask](#penmask)

Это соответствует свойству penMask структуры POINTER_PEN_INFO. Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).

#### PenPressure 

PenPressure события указателя.

> Открытый uint [PenPressure](#penpressure)

Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).

#### PenRotation 

PenRotation события указателя.

> Открытый uint [PenRotation](#penrotation)

Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).

#### PenTiltX 

PenTiltX события указателя.

> public int [PenTiltX](#pentiltx)

Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).

#### PenTiltY 

PenTiltY события указателя.

> public int [PenTiltY](#pentilty)

Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).

#### PerformanceCount 

PerformanceCount события указателя.

> общедоступный ulong [PerformanceCount](#performancecount)

Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### PixelLocation 

PixelLocation события указателя.

> общедоступная точка [PixelLocation](#pixellocation)

Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### PixelLocationRaw 

PixelLocationRaw события указателя.

> общедоступная точка [PixelLocationRaw](#pixellocationraw)

Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### PointerDeviceRect 

PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).

> общедоступный прямоугольник [PointerDeviceRect](#pointerdevicerect)

#### PointerFlags 

PointerFlags события указателя.

> Открытый uint [PointerFlags](#pointerflags)

Это соответствует свойству pointerFlags структуры POINTER_INFO. Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).

#### PointerId 

PointerId события указателя.

> Открытый uint [pointerId](#pointerid)

Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### PointerKind 

PointerKind события указателя.

> Открытый uint [PointerKind](#pointerkind)

Это соответствует свойству pointerKind структуры POINTER_INFO. Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h). Поддерживает PT_PEN и PT_TOUCH.

#### Время 

Время события указателя.

> общедоступное [время](#time) (UINT)

Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### TouchContact 

TouchContact события указателя.

> общедоступный прямоугольник [TouchContact](#touchcontact)

Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).

#### TouchContactRaw 

TouchContactRaw события указателя.

> общедоступный прямоугольник [TouchContactRaw](#touchcontactraw)

Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).

#### TouchFlags 

TouchFlags события указателя.

> Открытый uint [TouchFlags](#touchflags)

Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO. Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).

#### TouchMask 

TouchMask события указателя.

> Открытый uint [TouchMask](#touchmask)

Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO. Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).

#### TouchOrientation 

TouchOrientation события указателя.

> Открытый uint [TouchOrientation](#touchorientation)

Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).

#### TouchPressure 

TouchPressure события указателя.

> Открытый uint [TouchPressure](#touchpressure)

Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).

