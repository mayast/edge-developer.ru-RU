---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b5fcd04d702483778ef31549c2e7d989ebfe3689
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699186"
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

