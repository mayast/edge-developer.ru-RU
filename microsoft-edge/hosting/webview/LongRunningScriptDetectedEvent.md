---
description: ''
title: Объект LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 6cf7af656531eea5046f7af44d4d43ff224d0f08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571310"
---
# Объект LongRunningScriptDetectedEvent

Представлена информация для [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).

## Свойства

### executionTime

Возвращает количество миллисекунд, в течение которых элемент [WebView](../webview.md) выполнял долго выполняемый сценарий.

```js
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```

#### Значение свойства
Тип: **длинный**

### stopPageScriptExecution
Останавливает выполнение долго выполняющегося сценария в элементе [WebView](../webview.md) .

```js
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```

#### Значение свойства
Тип: **логический**