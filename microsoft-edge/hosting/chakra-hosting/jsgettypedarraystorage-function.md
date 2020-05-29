---
description: Получение основного хранилища памяти, используемого типизированным массивом.
title: Функция JsGetTypedArrayStorage | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f03414d64fa819ac464217c8362d02e866d45296
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572511"
---
# Функция JsGetTypedArrayStorage
Получение основного хранилища памяти, используемого типизированным массивом.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### Параметры  
 `typedArray`  
 Экземпляр типизированного массива.  
  
 `buffer`  
 Буфер массива. Время существования возвращаемого буфера совпадает со временем существования массива. Указатель буфера не будет считаться ссылкой на массив в целях сборки мусора.  
  
 `bufferLength`  
 Количество байтов в буфере.  
  
 `arrayType`  
 Тип массива.  
  
 `elementSize`  
 Размер элемента массива.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)