---
description: Возвращает тип JavaScript JsValueRef.
title: Функция JsGetValueType | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85dc6644e26017c6085ab64d914a86196cca8080
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572499"
---
# Функция JsGetValueType
Возвращает тип JavaScript JsValueRef.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### Параметры  
 `value`  
 Значение, тип которого нужно вернуть.  
  
 `type`  
 Тип значения.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)