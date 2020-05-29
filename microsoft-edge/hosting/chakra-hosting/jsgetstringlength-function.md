---
description: Возвращает длину строкового значения.
title: Функция JsGetStringLength | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetStringLength
helpviewer_keywords:
- JsGetStringLength function
ms.assetid: e9f9f28c-e644-439c-aee5-7ce362f71347
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6b562b2dc58341523910db41fb8b748453b2a836
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571376"
---
# Функция JsGetStringLength
Возвращает длину строкового значения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetStringLength(  
   _In_ JsValueRef stringValue,  
   _Out_ int *length  
);  
```  
  
#### Параметры  
 `stringValue`  
 Строковое значение, для которого требуется получить длину.  
  
 `length`  
 Длина строки.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)