---
description: Извлекает `bool` значение логического значения.
title: Функция JsBooleanToBool | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBooleanToBool
helpviewer_keywords:
- JsBooleanToBool function
ms.assetid: ab16ac71-fe47-475d-a7ee-46e4643dee60
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 55b0ef1278cbc73652fc8427e004cab002d76e5b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571468"
---
# Функция JsBooleanToBool
Извлекает `bool` значение логического значения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsBooleanToBool(  
   _In_ JsValueRef value,  
   _Out_ bool *boolValue  
);  
```  
  
#### Параметры  
 `value`  
 Преобразуемое значение.  
  
 `boolValue`  
 Преобразованное значение.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)