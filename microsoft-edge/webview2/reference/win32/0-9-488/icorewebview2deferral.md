---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ebaab6dfe0781f544e89e86afc9f16ab50cb9222
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654892"
---
# интерфейс ICoreWebView2Deferral 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Выполнено](#complete) | Завершает связанное отложенное событие.

## Участников

#### Выполнено 

Завершает связанное отложенное событие.

> общедоступное значение HRESULT [Complete](#complete)()

"Завершить" следует вызывать только один раз для каждого периода отсрочки.

