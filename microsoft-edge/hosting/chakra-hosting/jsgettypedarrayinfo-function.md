---
description: Получение часто используемых свойств типизированного массива.
title: Функция JsGetTypedArrayInfo | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b33b0c515733864c1849a08aa2f8dc6e884c22ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571368"
---
# Функция JsGetTypedArrayInfo
Получение часто используемых свойств типизированного массива.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### Параметры  
 `typedArray`  
 Экземпляр типизированного массива.  
  
 `arrayType`  
 Тип массива.  
  
 `arrayBuffer`  
 `ArrayBuffer`Восстановление массива.  
  
 `byteOffset`  
 Смещение в байтах от начала arrayBuffer, на которое ссылается массив.  
  
 `byteLength`  
 Число байтов в массиве.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)