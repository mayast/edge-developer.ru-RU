---
description: Возвращает значение, указывающее, отключено ли выполнение сценария в среде выполнения.
title: Функция JsIsRuntimeExecutionDisabled | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6968a31c9acab70589fe58c86cc566e631778c3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571357"
---
# Функция JsIsRuntimeExecutionDisabled
Возвращает значение, указывающее, отключено ли выполнение сценария в среде выполнения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### Параметры  
 `runtime`  
 Задает среду выполнения для проверки того, отключено ли выполнение.  
  
 `isDisabled`  
 `true` , если выполнение отключено, `false` в противном случае.  
  
## Возвращенное значение  
 `JsNoError` Если операция выполнена успешно, код ошибки в противном случае.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)