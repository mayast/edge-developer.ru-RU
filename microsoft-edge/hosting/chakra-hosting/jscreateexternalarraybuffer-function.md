---
description: Создает объект JavaScript `ArrayBuffer` для доступа к внешней памяти.
title: Функция JsCreateExternalArrayBuffer | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571434"
---
# Функция JsCreateExternalArrayBuffer
Создает объект JavaScript `ArrayBuffer` для доступа к внешней памяти.
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### Параметры  
 `data`  
 Указатель на внешнюю память.  
  
 `byteLength`  
 Количество байтов во внешней памяти.  
  
 `finalizeCallback`  
 Обратный вызов для завершения работы объекта. Может иметь значение null.  
  
 `callbackState`  
 Указанное пользователем состояние, которое будет возвращено в finalizeCallback.  
  
 `result`  
 Новый `ArrayBuffer` объект.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)