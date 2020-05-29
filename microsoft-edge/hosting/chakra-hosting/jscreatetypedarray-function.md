---
description: Создает объект типизированного массива JavaScript.
title: Функция JsCreateTypedArray | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57c5d15d76bf8b3ff29d10f7500fe41b3e959f68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571415"
---
# Функция JsCreateTypedArray
Создает объект типизированного массива JavaScript.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Параметры  
 `arrayType`  
 Тип создаваемого массива.  
  
 `baseArray`  
 Базовый массив нового массива. Используйте `JS_INVALID_REFERENCE` , если базовый массив отсутствует.  
  
 `byteOffset`  
 Смещение в байтах от начала `baseArray` ( `ArrayBuffer` ) для массива с типом результата, на который должна указывать ссылка. Применимо только `baseArray` в том случае, если `ArrayBuffer` объект является объектом. В противном случае оно должно быть равно 0.  
  
 `elementLength`  
 Количество элементов в массиве. Применимо только в том случае, если вы создаете новый типизированный массив без `baseArray` ( `baseArray` — `JS_INVALID_REFERENCE` ) или когда `baseArray` — `ArrayBuffer` объект. В противном случае оно должно быть равно 0.  
  
 `result`  
 Новый объект типизированного массива.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Это `baseArray` может быть `ArrayBuffer` , другой типизированный массив или JavaScript `Array` . Возвращаемый типизированный массив будет использовать массив в том `baseArray` случае, если он является `ArrayBuffer` , или, в противном случае, создать и использовать копию нижележащего исходного массива.  
  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)