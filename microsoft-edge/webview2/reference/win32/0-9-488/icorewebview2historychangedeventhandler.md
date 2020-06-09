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
ms.openlocfilehash: 0305517d17bfa812dbaee9b238403f2d9f1fb22d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697807"
---
# интерфейс ICoreWebView2HistoryChangedEventHandler 

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

