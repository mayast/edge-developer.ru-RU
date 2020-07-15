---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 5c4807a6f1772354f4448b25d49ea7ea86278f57
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880607"
---
# 0.9.515-Interface ICoreWebView2HistoryChangedEventHandler 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

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

