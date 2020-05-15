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
ms.openlocfilehash: 9c8cd627275a98382f079bc4f64dd7f565d46630
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655001"
---
# интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler 

> [!NOTE]
> Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.488.

```
interface ICoreWebView2ExperimentalCursorChangedEventHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс, чтобы получать события CursorChanged.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления средству реализации аргументов события для соответствующего события.

Используйте свойство Cursor для получения нового курсора.

## Участников

#### Invoke 

Вызывается для предоставления средству реализации аргументов события для соответствующего события.

> Открытый [вызов](#invoke)HRESULT ([ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) * sender, IUnknown * args)

Аргументы события отсутствуют, а параметр args — null.

