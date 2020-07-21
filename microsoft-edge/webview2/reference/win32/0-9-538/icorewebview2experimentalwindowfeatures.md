---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalWindowFeatures
ms.openlocfilehash: 2672f2aac842fd475f6148c439dbecdacd7793ee
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885405"
---
# интерфейс ICoreWebView2ExperimentalWindowFeatures 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

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

