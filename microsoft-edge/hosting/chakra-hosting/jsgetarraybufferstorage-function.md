---
description: Получение основного хранилища памяти, используемого в ArrayBuffer.
title: Функция JsGetArrayBufferStorage | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e8d265f3e81015ba9f5d0547b6b1c7246c23ce5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572531"
---
# Функция JsGetArrayBufferStorage
Получение основного хранилища памяти, используемого в `ArrayBuffer` .  
  
## Синтаксис  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Параметры  
 `arrayBuffer`  
 Экземпляр ArrayBuffer.  
  
 `buffer`  
 Буфер ArrayBuffer. Время существования возвращаемого буфера совпадает со сроком существования `ArrayBuffer` . Указатель буфера не считается ссылкой на объект в `ArrayBuffer` целях сборки мусора.  
  
 `bufferLength`  
 Количество байтов в буфере.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)