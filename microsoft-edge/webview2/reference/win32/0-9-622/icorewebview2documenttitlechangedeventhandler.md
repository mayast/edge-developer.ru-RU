---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2DocumentTitleChangedEventHandler
ms.openlocfilehash: 9332786935ba79adfd6ef215c9e11afa24c5ceb2
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012395"
---
# интерфейс ICoreWebView2DocumentTitleChangedEventHandler 

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс, чтобы получать события DocumentTitleChanged.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления средству реализации аргументов события для соответствующего события.

Используйте свойство DocumentTitle, чтобы получить измененный заголовок.

## Участников

#### Invoke 

Вызывается для предоставления средству реализации аргументов события для соответствующего события.

> Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) * sender, IUnknown * args)

Аргументы события отсутствуют, а параметр args — null.

