---
description: Возвращает `double` значение числового значения.
title: Функция JsNumberToDouble | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsNumberToDouble
helpviewer_keywords:
- JsNumberToDouble function
ms.assetid: 5f52e8b6-2b70-49a3-879a-bd83ebf2ac33
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: fc99e02aa0376bb100b4e1302c29532a57bd539f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571350"
---
# Функция JsNumberToDouble
Возвращает `double` значение числового значения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToDouble(  
   _In_ JsValueRef value,  
   _Out_ double *doubleValue  
);  
```  
  
#### Параметры  
 `value`  
 Числовое значение, которое нужно преобразовать в `double` значение.  
  
 `doubleValue`  
 `double`Значение.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Эта функция возвращает значение числового значения. `JsErrorInvalidArgument`Если тип значения не является числом, произойдет сбой.  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)