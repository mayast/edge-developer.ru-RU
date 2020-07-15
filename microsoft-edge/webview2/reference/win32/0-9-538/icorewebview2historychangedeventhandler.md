---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: cf9d04c14f39a9ba1686d5cc9b002041313b645d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879914"
---
# интерфейс ICoreWebView2HistoryChangedEventHandler 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Аргументы события отсутствуют, а параметр args — null.

## Участников

#### Invoke 

Аргументы события отсутствуют, а параметр args — null.

> Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) * WebView, IUnknown * args)

