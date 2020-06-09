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
ms.openlocfilehash: 576f54f2a7ecc2e1e99758719e80cc589c5bc791
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699293"
---
# интерфейс ICoreWebView2ExperimentalWindowFeatures 

> [!NOTE]
> Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.

```
interface ICoreWebView2ExperimentalWindowFeatures
  : public IUnknown
```

Функции окна для всплывающего окна WebView.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Height](#get_height) | Высота окна.
[get_Left](#get_left) | Левое расположение окна. Если HasPosition имеет значение false, произойдет сбой.
[get_MenuBar](#get_menubar) | Указывает, следует ли отображать строку меню.
[get_ScrollBars](#get_scrollbars) | Указывает, следует ли отображать полосы прокрутки.
[get_Status](#get_status) | Следует ли добавить строку состояния.
[get_Toolbar](#get_toolbar) | Указывает, следует ли отображать панель инструментов браузера.
[get_Top](#get_top) | Верхнее расположение окна. Если HasPosition имеет значение false, произойдет сбой.
[get_Width](#get_width) | Ширина окна.
[HasPosition](#hasposition) | Заданные значения Left и Top.
[HasSize](#hassize) | Заданные значения Height и Width.

Эти поля соответствуют параметру "windowFeatures", передаваемому в Window. Open, как указано в[https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features](https://developer.mozilla.org/en-US/docs/Web/API/Window/open#Window_features)

## Участников

#### get_Height 

Высота окна.

> общедоступные значения HRESULT [get_Height](#get_height)(UINT32 * высота)

Минимальное значение — 100. Если HasSize имеет значение false, произойдет сбой.

#### get_Left 

Левое расположение окна. Если HasPosition имеет значение false, произойдет сбой.

> общедоступные значения HRESULT [get_Left](#get_left)(UINT32 * Left)

#### get_MenuBar 

Указывает, следует ли отображать строку меню.

> общедоступные значения HRESULT [get_MenuBar](#get_menubar)(bool * MenuBar)

#### get_ScrollBars 

Указывает, следует ли отображать полосы прокрутки.

> общедоступные значения HRESULT [get_ScrollBars](#get_scrollbars)(логические * полосы прокрутки)

#### get_Status 

Следует ли добавить строку состояния.

> общедоступные значения HRESULT [get_Status](#get_status)(bool * Status)

#### get_Toolbar 

Указывает, следует ли отображать панель инструментов браузера.

> общедоступные значения HRESULT [get_Toolbar](#get_toolbar)(bool * Toolbar)

#### get_Top 

Верхнее расположение окна. Если HasPosition имеет значение false, произойдет сбой.

> общедоступные значения HRESULT [get_Top](#get_top)(UINT32 * Top)

#### get_Width 

Ширина окна.

> общедоступные значения HRESULT [get_Width](#get_width)(UINT32 * Width)

Минимальное значение — 100. Если HasSize имеет значение false, произойдет сбой.

#### HasPosition 

Заданные значения Left и Top.

> общедоступные значения HRESULT [HasPosition](#hasposition)(bool * HasPosition)

#### HasSize 

Заданные значения Height и Width.

> общедоступные значения HRESULT [HasSize](#hassize)(bool * HasSize)

