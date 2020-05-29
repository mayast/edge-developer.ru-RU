---
description: Проверяет, имеет ли объект значение по указанному индексу.
title: Функция JsHasIndexedProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasIndexedProperty
helpviewer_keywords:
- JsHasIndexedProperty function
ms.assetid: 30436a3d-fda0-407e-aba2-142be2310372
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85d9fa12c44bd1d961ec2a7ba494484873635586
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572495"
---
# Функция JsHasIndexedProperty
Проверяет, имеет ли объект значение по указанному индексу.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ bool *result  
);  
```  
  
#### Параметры  
 `object`  
 Объект для работы.  
  
 `index`  
 Индекс для проверки.  
  
 `result`  
 Имеет ли объект значение по указанному индексу.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)