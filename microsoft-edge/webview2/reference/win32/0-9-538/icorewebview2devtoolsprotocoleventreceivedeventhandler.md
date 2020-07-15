---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2DevToolsProtocolEventReceivedEventHandler
ms.openlocfilehash: 2cb38d40e4e4a5e527cc8e8643b31ae7ceebecbe
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879599"
---
# интерфейс ICoreWebView2DevToolsProtocolEventReceivedEventHandler 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс, чтобы получать события DevToolsProtocolEventReceived из WebView.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления средству реализации аргументов события для соответствующего события.

## Участников

#### Invoke 

Вызывается для предоставления средству реализации аргументов события для соответствующего события.

> Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) * sender, [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](icorewebview2devtoolsprotocoleventreceivedeventargs.md) * args)

