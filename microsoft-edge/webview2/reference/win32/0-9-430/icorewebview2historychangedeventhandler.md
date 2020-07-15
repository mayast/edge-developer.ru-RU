---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6afd1983b90b4412fd3011dc35f192809a9583b7
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881020"
---
# 0.9.430-Interface ICoreWebView2HistoryChangedEventHandler 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

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

> Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) * WebView, IUnknown * args)

