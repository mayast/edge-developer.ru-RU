---
description: Задает обратный вызов выделения памяти для указанной среды выполнения.
title: Функция JsSetRuntimeMemoryAllocationCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5c648761473023f00e894fbf75c794cfcc9422c5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572342"
---
# Функция JsSetRuntimeMemoryAllocationCallback
Задает обратный вызов выделения памяти для указанной среды выполнения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### Параметры  
 `runtime`  
 Среда выполнения, для которой регистрируется обратный вызов выделения.  
  
 `callbackState`  
 Указанное пользователем состояние, которое будет передано обратно обратному вызову.  
  
 `allocationCallback`  
 Обратный вызов выделения памяти, который нужно вызвать для событий выделения памяти.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Регистрация обратного вызова для выделения памяти приведет к тому, что среда выполнения будет вызывать приложение, когда он получает память из памяти или освобождает ее. Процедура обратного вызова вызывается перед тем, как диспетчер памяти среды выполнения выделяет блок памяти. Выделение будет отклонено, если обратный вызов возвращает значение false. Диспетчер памяти среды выполнения также вызывает процедуру обратного вызова после освобождения блока памяти, а также после сбоя выделения ресурсов.  
  
 Обратный вызов вызывается в текущем потоке выполнения среды выполнения, поэтому выполнение блокируется до тех пор, пока не завершится обратный вызов.  
  
 Возвращаемое значение обратного вызова не сохраняется; ранее отклоненные выделения не мешают среде выполнения повторно вызвать обратный вызов для новых операций выделения памяти.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)