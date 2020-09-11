---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ProcessFailedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ProcessFailedEventArgs
ms.openlocfilehash: 0f4ce5d4922b7a721ce2652fadfa5169a52cb458
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012527"
---
# интерфейс ICoreWebView2ProcessFailedEventArgs 

```
interface ICoreWebView2ProcessFailedEventArgs
  : public IUnknown
```

Аргументы события для события ProcessFailed.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_ProcessFailedKind](#get_processfailedkind) | Произошел сбой процесса.

## Участников

#### get_ProcessFailedKind 

Произошел сбой процесса.

> общедоступные значения HRESULT [get_ProcessFailedKind](#get_processfailedkind)(COREWEBVIEW2_PROCESS_FAILED_KIND * ProcessFailedKind)

