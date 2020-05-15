---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e2469dd9a587735efcf88a48e0ce950cb4f85239
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654910"
---
# интерфейс ICoreWebView2ZoomFactorChangedEventHandler 

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления средству реализации аргументов события для соответствующего события.

Используйте свойство ICoreWebView2Controller. ZoomFactor, чтобы получить измененный коэффициент масштабирования.

## Участников

#### Invoke 

Вызывается для предоставления средству реализации аргументов события для соответствующего события.

> Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) * sender, IUnknown * args)

Аргументы события отсутствуют, а параметр args — null.

