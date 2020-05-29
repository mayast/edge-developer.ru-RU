---
description: Извлекает указатель строки в строковом значении.
title: Функция JsStringToPointer | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1f5997894c4ea479378a323b230492dde28ab177
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572338"
---
# Функция JsStringToPointer
Извлекает указатель строки в строковом значении.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### Параметры  
 `value`  
 Строковое значение, которое нужно преобразовать в указатель строки.  
  
 `stringValue`  
 Указатель строки.  
  
 `stringLength`  
 Длина строки.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Эта функция извлекает указатель строки в строковом значении. `JsErrorInvalidArgument`Если тип значения не является строковым, произойдет сбой. Время существования возвращаемой строки будет совпадать со временем существования значения, из которого она была получена, но указатель строки не считается ссылкой на значение (и поэтому не будет храниться).  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)