---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8fd3533d8f479866989f719be6e48c437fae4ddb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654967"
---
# интерфейс ICoreWebView2HistoryChangedEventHandler 

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

