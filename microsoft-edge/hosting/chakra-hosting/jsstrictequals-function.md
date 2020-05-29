---
description: Сравните два значения JavaScript для строгого равенства.
title: Функция JsStrictEquals | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStrictEquals
helpviewer_keywords:
- JsStrictEquals function
ms.assetid: b35bc655-7ff8-496a-b678-8950bb976047
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b7f2b7a66c32428100f0c0d0f9db6150559ed7a2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572434"
---
# Функция JsStrictEquals
Сравните два значения JavaScript для строгого равенства.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsStrictEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### Параметры  
 `object1`  
 Первый сравниваемый объект.  
  
 `object2`  
 Второй сравниваемый объект.  
  
 `result`  
 Являются ли значения строго эквивалентными.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Эта функция эквивалентна `===` оператору в JavaScript.  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)