---
description: Получение основного хранилища памяти, используемого DataView.
title: Функция JsGetDataViewStorage | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 54f8a91b6dea1e0997ad31d6585ea741fde8ba99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571395"
---
# Функция JsGetDataViewStorage
Получение основного хранилища памяти, используемого в `DataView` .  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### Параметры  
 `dataView`  
 Экземпляр объекта DataView.  
  
 `buffer`  
 Буфер объекта DataView. Время существования возвращаемого буфера совпадает со сроком существования `DataView` . Указатель буфера не считается ссылкой на объект в `DataView` целях сборки мусора.  
  
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