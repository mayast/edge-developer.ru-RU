---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 4866626111908eae9800da0baabec0356d5d4bf8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879655"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2WindowFeatures 

> [!NOTE]
> Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

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

