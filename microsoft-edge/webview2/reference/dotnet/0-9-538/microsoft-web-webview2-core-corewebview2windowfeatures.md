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
ms.openlocfilehash: 9ee85620ece653a2312076f7b6f4fe9f6ca3da92
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699273"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures 

> [!NOTE]
> Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Функции окна для всплывающего окна WebView.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Полноразмерных](#height) | Высота окна.
[Влево](#left) | Левое расположение окна.
[MenuBar](#menubar) | Указывает, следует ли отображать строку меню.
[Полосы прокрутки](#scrollbars) | Указывает, следует ли отображать полосы прокрутки.
[Состояние](#status) | Следует ли добавить строку состояния.
[панель инструментов;](#toolbar) | Указывает, следует ли отображать панель инструментов браузера.
[Top](#top) | Верхнее расположение окна.
[Ширина](#width) | Ширина окна.
[HasPosition](#hasposition) | Заданные значения Left и Top.
[HasSize](#hassize) | Заданные значения Height и Width.

## Участников

#### Полноразмерных 

Высота окна.

> открытая [Высота](#height) с uint

#### Влево 

Левое расположение окна.

> Открытый uint [слева](#left)

Если HasPosition имеет значение false, произойдет сбой.

#### MenuBar 

Указывает, следует ли отображать строку меню.

> public int [Remenubar](#menubar)

#### Полосы прокрутки 

Указывает, следует ли отображать полосы прокрутки.

> открытые [прокрутки](#scrollbars) int

#### Состояние 

Следует ли добавить строку состояния.

> общедоступный целочисленный [статус](#status)

#### панель инструментов; 

Указывает, следует ли отображать панель инструментов браузера.

> общедоступная [панель инструментов](#toolbar) int

#### Top 

Верхнее расположение окна.

> Открытый uint, [сверху](#top)

Если HasPosition имеет значение false, произойдет сбой.

#### Ширина 

Ширина окна.

> открытая [Ширина](#width) с uint

#### HasPosition 

Заданные значения Left и Top.

> public int [HasPosition](#hasposition)()

#### HasSize 

Заданные значения Height и Width.

> public int [HasSize](#hassize)()

