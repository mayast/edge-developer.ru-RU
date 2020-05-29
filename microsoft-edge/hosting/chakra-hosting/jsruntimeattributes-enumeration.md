---
description: 'Атрибуты среды выполнения. '
title: Перечисление JsRuntimeAttributes | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRuntimeAttributes
helpviewer_keywords:
- JsRuntimeAttributes enumeration
ms.assetid: f76d82e9-a695-4d6a-96c1-b3a4d27fed68
caps.latest.revision: 14
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9b8f6788f1de4988e3936701cfc742a564c92cfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572459"
---
# Перечисление JsRuntimeAttributes
Атрибуты среды выполнения.  
  
## Синтаксис  
  
```cpp  
enum JsRuntimeAttributes;  
```  
  
## Участников  
  
### Данные  
  
|Имя|Описание|  
|----------|-----------------|  
|`JsRuntimeAttributeAllowScriptInterrupt`|Среда выполнения должна поддерживать надежное прерывание сценария. Это позволяет увеличить количество мест, в которых среда выполнения будет проверять запрос на прерывание сценария с учетом затрат на небольшое количество производительности во время выполнения.|  
|`JsRuntimeAttributeDisableBackgroundWork`|Среда выполнения не будет выполнять какие-либо действия (такие как сборка мусора) в фоновых потоках.|  
|`JsRuntimeAttributeDisableEval`|Использование `eval` или `function` конструктор вызывает исключение.|  
|`JsRuntimeAttributeDisableNativeCodeGeneration`|Среда выполнения не будет создавать машинный код.|  
|`JsRuntimeAttributeEnableExperimentalFeatures`|В среде выполнения будут включены все экспериментальные функции.|  
|`JsRuntimeAttributeEnableIdleProcessing`|Ведущее приложение будет вызываться `JsIdle` , поэтому Включите обработку бездействия. В противном случае среда выполнения будет несколько более агрессивно управлять памятью.|  
|`JsRuntimeAttributeDispatchSetExceptionsToDebugger`|Вызов `JsSetException` также выдает исключение в отладчик сценариев (если есть), давая отладчику шанс на прерывание на исключении.|  
|`JsRuntimeAttributeNone`|Никаких специальных атрибутов.|  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)