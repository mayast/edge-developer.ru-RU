---
description: ''
title: Объект LongRunningScriptDetectedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 5fe90495b83ab8f95ee594d3400c8c1a26f0547e
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752154"
---
# Объект LongRunningScriptDetectedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Представлена информация для [MSWebViewLongRunningScriptDetected](../webview.md#mswebviewlongrunningscriptdetected).  

## Свойства  

### executionTime  

Возвращает количество миллисекунд, в течение которых элемент [WebView](../webview.md) выполнял долго выполняемый сценарий.  

```javascript
var executionTime = LongRunningScriptDetectedEvent.executionTime;
```  

#### Значение свойства  

Тип: **длинный**  

### stopPageScriptExecution  

Останавливает выполнение долго выполняющегося сценария в элементе [WebView](../webview.md) .  

```javascript
var stopPageScriptExecution = LongRunningScriptDetectedEvent.stopPageScriptExecution;
```  

#### Значение свойства  

Тип: **логический**  
