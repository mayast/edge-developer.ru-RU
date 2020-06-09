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
# интерфейс ICoreWebView2ExperimentalPointerInfo 

> [!NOTE]
> Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.

```
interface ICoreWebView2ExperimentalPointerInfo
  : public IUnknown
```

Это преимущественно представляет объединенный объект Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_ButtonChangeKind](#get_buttonchangekind) | Получение ButtonChangeKind события указателя.
[get_DisplayRect](#get_displayrect) | Получите DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).
[get_FrameId](#get_frameid) | Получение FrameID события указателя.
[get_HimetricLocation](#get_himetriclocation) | Получение HimetricLocation события указателя.
[get_HimetricLocationRaw](#get_himetriclocationraw) | Получение HimetricLocationRaw события указателя.
[get_HistoryCount](#get_historycount) | Получение HistoryCount события указателя.
[get_InputData](#get_inputdata) | Получение InputData события указателя.
[get_KeyStates](#get_keystates) | Получение KeyStates события указателя.
[get_PenFlags](#get_penflags) | Получение PenFlags события указателя.
[get_PenMask](#get_penmask) | Получение PenMask события указателя.
[get_PenPressure](#get_penpressure) | Получение PenPressure события указателя.
[get_PenRotation](#get_penrotation) | Получение PenRotation события указателя.
[get_PenTiltX](#get_pentiltx) | Получение PenTiltX события указателя.
[get_PenTiltY](#get_pentilty) | Получение PenTiltY события указателя.
[get_PerformanceCount](#get_performancecount) | Получение PerformanceCount события указателя.
[get_PixelLocation](#get_pixellocation) | Получение PixelLocation события указателя.
[get_PixelLocationRaw](#get_pixellocationraw) | Получение PixelLocationRaw события указателя.
[get_PointerDeviceRect](#get_pointerdevicerect) | Получите PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).
[get_PointerFlags](#get_pointerflags) | Получение PointerFlags события указателя.
[get_PointerId](#get_pointerid) | Получение PointerId события указателя.
[get_PointerKind](#get_pointerkind) | Получение PointerKind события указателя.
[get_Time](#get_time) | Получить время события указателя.
[get_TouchContact](#get_touchcontact) | Получение TouchContact события указателя.
[get_TouchContactRaw](#get_touchcontactraw) | Получение TouchContactRaw события указателя.
[get_TouchFlags](#get_touchflags) | Получение TouchFlags события указателя.
[get_TouchMask](#get_touchmask) | Получение TouchMask события указателя.
[get_TouchOrientation](#get_touchorientation) | Получение TouchOrientation события указателя.
[get_TouchPressure](#get_touchpressure) | Получение TouchPressure события указателя.
[put_ButtonChangeKind](#put_buttonchangekind) | Задайте ButtonChangeKind события указателя.
[put_DisplayRect](#put_displayrect) | Задайте DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).
[put_FrameId](#put_frameid) | Задайте FrameID события указателя.
[put_HimetricLocation](#put_himetriclocation) | Задайте HimetricLocation события указателя.
[put_HimetricLocationRaw](#put_himetriclocationraw) | Задайте HimetricLocationRaw события указателя.
[put_HistoryCount](#put_historycount) | Задайте HistoryCount события указателя.
[put_InputData](#put_inputdata) | Задайте InputData события указателя.
[put_KeyStates](#put_keystates) | Задайте KeyStates события указателя.
[put_PenFlags](#put_penflags) | Задайте PenFlags события указателя.
[put_PenMask](#put_penmask) | Задайте PenMask события указателя.
[put_PenPressure](#put_penpressure) | Задайте PenPressure события указателя.
[put_PenRotation](#put_penrotation) | Задайте PenRotation события указателя.
[put_PenTiltX](#put_pentiltx) | Задайте PenTiltX события указателя.
[put_PenTiltY](#put_pentilty) | Задайте PenTiltY события указателя.
[put_PerformanceCount](#put_performancecount) | Задайте PerformanceCount события указателя.
[put_PixelLocation](#put_pixellocation) | Задайте PixelLocation события указателя.
[put_PixelLocationRaw](#put_pixellocationraw) | Задайте PixelLocationRaw события указателя.
[put_PointerDeviceRect](#put_pointerdevicerect) | Задайте PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).
[put_PointerFlags](#put_pointerflags) | Задайте PointerFlags события указателя.
[put_PointerId](#put_pointerid) | Задайте PointerId события указателя.
[put_PointerKind](#put_pointerkind) | Задайте PointerKind события указателя.
[put_Time](#put_time) | Задайте время события указателя.
[put_TouchContact](#put_touchcontact) | Задайте TouchContact события указателя.
[put_TouchContactRaw](#put_touchcontactraw) | Задайте TouchContactRaw события указателя.
[put_TouchFlags](#put_touchflags) | Задайте TouchFlags события указателя.
[put_TouchMask](#put_touchmask) | Задайте TouchMask события указателя.
[put_TouchOrientation](#put_touchorientation) | Задайте TouchOrientation события указателя.
[put_TouchPressure](#put_touchpressure) | Задайте TouchPressure события указателя.

Он берет на себя поля из всех трех типов данных, таких как HWND и ДЕСКРИПТОРы. Обратите внимание, что sourceDevice используется, но мы ожидаем, что PointerDeviceRect и DisplayRect будут охватывать существующие варианты использования sourceDevice. Еще одна большая разница заключается в том, что любое из расположений Point или Rect ожидается в WebView физических координат. Это значит, что координаты относительно WebView и не применяются к масштабированию DPI.

## Участников

#### get_ButtonChangeKind 

Получение ButtonChangeKind события указателя.

> общедоступные значения HRESULT [get_ButtonChangeKind](#get_buttonchangekind)(Int32 * ButtonChangeKind)

Это соответствует свойству ButtonChangeKind структуры POINTER_INFO. Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).

#### get_DisplayRect 

Получите DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).

> общедоступные значения HRESULT [get_DisplayRect](#get_displayrect)(Rect * DisplayRect)

#### get_FrameId 

Получение FrameID события указателя.

> общедоступные значения HRESULT [get_FrameId](#get_frameid)(UINT32 * FrameId)

Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_HimetricLocation 

Получение HimetricLocation события указателя.

> общедоступные значения HRESULT [get_HimetricLocation](#get_himetriclocation)(Point * HimetricLocation)

Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_HimetricLocationRaw 

Получение HimetricLocationRaw события указателя.

> общедоступные значения HRESULT [get_HimetricLocationRaw](#get_himetriclocationraw)(Point * HimetricLocationRaw)

Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_HistoryCount 

Получение HistoryCount события указателя.

> общедоступные значения HRESULT [get_HistoryCount](#get_historycount)(UINT32 * HistoryCount)

Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_InputData 

Получение InputData события указателя.

> общедоступные значения HRESULT [get_InputData](#get_inputdata)(Int32 * InputData)

Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_KeyStates 

Получение KeyStates события указателя.

> общедоступные значения HRESULT [get_KeyStates](#get_keystates)(DWORD * KeyStates)

Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_PenFlags 

Получение PenFlags события указателя.

> общедоступные значения HRESULT [get_PenFlags](#get_penflags)(UINT32 * PenFlags)

Это соответствует свойству penFlags структуры POINTER_PEN_INFO. Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).

#### get_PenMask 

Получение PenMask события указателя.

> общедоступные значения HRESULT [get_PenMask](#get_penmask)(UINT32 * PenMask)

Это соответствует свойству penMask структуры POINTER_PEN_INFO. Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).

#### get_PenPressure 

Получение PenPressure события указателя.

> общедоступные значения HRESULT [get_PenPressure](#get_penpressure)(UINT32 * PenPressure)

Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).

#### get_PenRotation 

Получение PenRotation события указателя.

> общедоступные значения HRESULT [get_PenRotation](#get_penrotation)(UINT32 * PenRotation)

Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).

#### get_PenTiltX 

Получение PenTiltX события указателя.

> общедоступные значения HRESULT [get_PenTiltX](#get_pentiltx)(Int32 * PenTiltX)

Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).

#### get_PenTiltY 

Получение PenTiltY события указателя.

> общедоступные значения HRESULT [get_PenTiltY](#get_pentilty)(Int32 * PenTiltY)

Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).

#### get_PerformanceCount 

Получение PerformanceCount события указателя.

> общедоступные значения HRESULT [get_PerformanceCount](#get_performancecount)(UINT64 * PerformanceCount)

Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_PixelLocation 

Получение PixelLocation события указателя.

> общедоступные значения HRESULT [get_PixelLocation](#get_pixellocation)(Point * PixelLocation)

Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_PixelLocationRaw 

Получение PixelLocationRaw события указателя.

> общедоступные значения HRESULT [get_PixelLocationRaw](#get_pixellocationraw)(Point * PixelLocationRaw)

Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_PointerDeviceRect 

Получите PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).

> общедоступные значения HRESULT [get_PointerDeviceRect](#get_pointerdevicerect)(Rect * PointerDeviceRect)

#### get_PointerFlags 

Получение PointerFlags события указателя.

> общедоступные значения HRESULT [get_PointerFlags](#get_pointerflags)(UINT32 * PointerFlags)

Это соответствует свойству pointerFlags структуры POINTER_INFO. Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).

#### get_PointerId 

Получение PointerId события указателя.

> общедоступные значения HRESULT [get_PointerId](#get_pointerid)(UINT32 * pointerId)

Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_PointerKind 

Получение PointerKind события указателя.

> общедоступные значения HRESULT [get_PointerKind](#get_pointerkind)(DWORD * PointerKind)

Это соответствует свойству pointerKind структуры POINTER_INFO. Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h). Поддерживает PT_PEN и PT_TOUCH.

#### get_Time 

Получить время события указателя.

> общедоступные значения HRESULT [get_Time](#get_time)(DWORD * Time)

Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### get_TouchContact 

Получение TouchContact события указателя.

> общедоступные значения HRESULT [get_TouchContact](#get_touchcontact)(Rect * TouchContact)

Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).

#### get_TouchContactRaw 

Получение TouchContactRaw события указателя.

> общедоступные значения HRESULT [get_TouchContactRaw](#get_touchcontactraw)(Rect * TouchContactRaw)

Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).

#### get_TouchFlags 

Получение TouchFlags события указателя.

> общедоступные значения HRESULT [get_TouchFlags](#get_touchflags)(UINT32 * TouchFlags)

Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO. Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).

#### get_TouchMask 

Получение TouchMask события указателя.

> общедоступные значения HRESULT [get_TouchMask](#get_touchmask)(UINT32 * TouchMask)

Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO. Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).

#### get_TouchOrientation 

Получение TouchOrientation события указателя.

> общедоступные значения HRESULT [get_TouchOrientation](#get_touchorientation)(UINT32 * TouchOrientation)

Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).

#### get_TouchPressure 

Получение TouchPressure события указателя.

> общедоступные значения HRESULT [get_TouchPressure](#get_touchpressure)(UINT32 * TouchPressure)

Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).

#### put_ButtonChangeKind 

Задайте ButtonChangeKind события указателя.

> общедоступные значения HRESULT [put_ButtonChangeKind](#put_buttonchangekind)(Int32 ButtonChangeKind)

Это соответствует свойству ButtonChangeKind структуры POINTER_INFO. Значения определяются POINTER_BUTTON_CHANGE_KIND Enum в Windows SDK (Winuser. h).

#### put_DisplayRect 

Задайте DisplayRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).

> общедоступные значения HRESULT [put_DisplayRect](#put_displayrect)(Rect DisplayRect)

#### put_FrameId 

Задайте FrameID события указателя.

> общедоступные значения HRESULT [put_FrameId](#put_frameid)(UINT32 FrameId)

Это соответствует свойству frameId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_HimetricLocation 

Задайте HimetricLocation события указателя.

> общедоступные значения HRESULT [put_HimetricLocation](#put_himetriclocation)(Point HimetricLocation)

Это соответствует свойству ptHimetricLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_HimetricLocationRaw 

Задайте HimetricLocationRaw события указателя.

> общедоступные значения HRESULT [put_HimetricLocationRaw](#put_himetriclocationraw)(Point HimetricLocationRaw)

Это соответствует свойству ptHimetricLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_HistoryCount 

Задайте HistoryCount события указателя.

> общедоступные значения HRESULT [put_HistoryCount](#put_historycount)(UINT32 HistoryCount)

Это соответствует свойству historyCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_InputData 

Задайте InputData события указателя.

> общедоступные значения HRESULT [put_InputData](#put_inputdata)(Int32 InputData)

Это соответствует свойству InputData структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_KeyStates 

Задайте KeyStates события указателя.

> общедоступные значения HRESULT [put_KeyStates](#put_keystates)(DWORD KeyStates)

Это соответствует свойству dwKeyStates структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_PenFlags 

Задайте PenFlags события указателя.

> общедоступные значения HRESULT [put_PenFlags](#put_penflags)(UINT32 PenFlags)

Это соответствует свойству penFlags структуры POINTER_PEN_INFO. Значения определяются константами PEN_FLAGS в Windows SDK (Winuser. h).

#### put_PenMask 

Задайте PenMask события указателя.

> общедоступные значения HRESULT [put_PenMask](#put_penmask)(UINT32 PenMask)

Это соответствует свойству penMask структуры POINTER_PEN_INFO. Значения определяются константами PEN_MASK в Windows SDK (Winuser. h).

#### put_PenPressure 

Задайте PenPressure события указателя.

> общедоступные значения HRESULT [put_PenPressure](#put_penpressure)(UINT32 PenPressure)

Это соответствует свойству "нажим" структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).

#### put_PenRotation 

Задайте PenRotation события указателя.

> общедоступные значения HRESULT [put_PenRotation](#put_penrotation)(UINT32 PenRotation)

Это соответствует свойству "поворот" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).

#### put_PenTiltX 

Задайте PenTiltX события указателя.

> общедоступные значения HRESULT [put_PenTiltX](#put_pentiltx)(Int32 PenTiltX)

Это соответствует свойству tiltX структуры POINTER_PEN_INFO, определенному в Windows SDK (Winuser. h).

#### put_PenTiltY 

Задайте PenTiltY события указателя.

> общедоступные значения HRESULT [put_PenTiltY](#put_pentilty)(Int32 PenTiltY)

Это соответствует свойству "наклон" структуры POINTER_PEN_INFO, как определено в Windows SDK (Winuser. h).

#### put_PerformanceCount 

Задайте PerformanceCount события указателя.

> общедоступные значения HRESULT [put_PerformanceCount](#put_performancecount)(UINT64 PerformanceCount)

Это соответствует свойству PerformanceCount структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_PixelLocation 

Задайте PixelLocation события указателя.

> общедоступные значения HRESULT [put_PixelLocation](#put_pixellocation)(Point PixelLocation)

Это соответствует свойству ptPixelLocation структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_PixelLocationRaw 

Задайте PixelLocationRaw события указателя.

> общедоступные значения HRESULT [put_PixelLocationRaw](#put_pixellocationraw)(Point PixelLocationRaw)

Это соответствует свойству ptPixelLocationRaw структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_PointerDeviceRect 

Задайте PointerDeviceRect свойства sourceDevice структуры POINTER_INFO, как определено в Windows SDK (Winuser. h).

> общедоступные значения HRESULT [put_PointerDeviceRect](#put_pointerdevicerect)(Rect PointerDeviceRect)

#### put_PointerFlags 

Задайте PointerFlags события указателя.

> общедоступные значения HRESULT [put_PointerFlags](#put_pointerflags)(UINT32 PointerFlags)

Это соответствует свойству pointerFlags структуры POINTER_INFO. Значения определяются константами POINTER_FLAGS в Windows SDK (Winuser. h).

#### put_PointerId 

Задайте PointerId события указателя.

> общедоступные значения HRESULT [put_PointerId](#put_pointerid)(UINT32 pointerId)

Это соответствует свойству pointerId структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_PointerKind 

Задайте PointerKind события указателя.

> общедоступные значения HRESULT [put_PointerKind](#put_pointerkind)(DWORD PointerKind)

Это соответствует свойству pointerKind структуры POINTER_INFO. Значения определяются POINTER_INPUT_KIND Enum в Windows SDK (Winuser. h). Поддерживает PT_PEN и PT_TOUCH.

#### put_Time 

Задайте время события указателя.

> общедоступные значения HRESULT [put_Time](#put_time)(время в DWORD)

Это соответствует свойству dwTime структуры POINTER_INFO, определенному в Windows SDK (Winuser. h).

#### put_TouchContact 

Задайте TouchContact события указателя.

> общедоступные значения HRESULT [put_TouchContact](#put_touchcontact)(Rect TouchContact)

Это соответствует свойству rcContact структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).

#### put_TouchContactRaw 

Задайте TouchContactRaw события указателя.

> общедоступные значения HRESULT [put_TouchContactRaw](#put_touchcontactraw)(Rect TouchContactRaw)

Это соответствует свойству rcContactRaw структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).

#### put_TouchFlags 

Задайте TouchFlags события указателя.

> общедоступные значения HRESULT [put_TouchFlags](#put_touchflags)(UINT32 TouchFlags)

Это соответствует свойству touchFlags структуры POINTER_TOUCH_INFO. Значения определяются константами TOUCH_FLAGS в Windows SDK (Winuser. h).

#### put_TouchMask 

Задайте TouchMask события указателя.

> общедоступные значения HRESULT [put_TouchMask](#put_touchmask)(UINT32 TouchMask)

Это соответствует свойству touchMask структуры POINTER_TOUCH_INFO. Значения определяются константами TOUCH_MASK в Windows SDK (Winuser. h).

#### put_TouchOrientation 

Задайте TouchOrientation события указателя.

> общедоступные значения HRESULT [put_TouchOrientation](#put_touchorientation)(UINT32 TouchOrientation)

Это соответствует свойству Orientation структуры POINTER_TOUCH_INFO, как определено в Windows SDK (Winuser. h).

#### put_TouchPressure 

Задайте TouchPressure события указателя.

> общедоступные значения HRESULT [put_TouchPressure](#put_touchpressure)(UINT32 TouchPressure)

Это соответствует свойству "нажим" структуры POINTER_TOUCH_INFO, определенному в Windows SDK (Winuser. h).

