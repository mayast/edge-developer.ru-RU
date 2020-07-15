---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b9eb90c0735f290305327b4397cf90d24c76abb5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881153"
---
# 0.9.430-Interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2CallDevToolsProtocolMethodCompletedHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс, чтобы получать результаты выполнения CallDevToolsProtocolMethod.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.

## Участников

#### Invoke 

Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.

> общедоступный [вызов](#invoke)HRESULT (ErrorCode HRESULT, LPCWSTR returnObjectAsJson)

