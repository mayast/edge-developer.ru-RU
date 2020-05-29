---
description: Событие, которое возникает при выполнении HTTP-запроса.
title: Объект WebResourceRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 79cff0d8fd68e3b5747008f343b5b46fb8093013
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570823"
---
# Объект WebResourceRequestedEvent

Событие, которое возникает при выполнении HTTP-запроса.

## Свойства

### аргументы

Сведения о запросе ресурсов. Это элемент [Windows. Web. UI. WebViewControlWebResourceRequestedEventArgs](/uwp/api/windows.web.ui.webviewcontrolwebresourcerequestedeventargs).

Это свойство доступно только для чтения.

```js
var args = webResourceRequestedEventArgs.args;
var request = args.request;
```

#### Значение свойства
Type (тип): **ANY**

