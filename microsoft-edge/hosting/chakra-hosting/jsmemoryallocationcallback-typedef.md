---
description: Пользователь реализовал подпрограмму обратного вызова для событий выделения памяти.
title: JsMemoryAllocationCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 511babc7-3caa-4ee5-82a2-943bbd34db8d
caps.latest.revision: 7
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b11b3d076c01dbfcae190fd665528323d6f8b987
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571356"
---
# JsMemoryAllocationCallback typedef
Пользователь реализовал подпрограмму обратного вызова для событий выделения памяти.  
  
## Синтаксис  
  
```cpp  
typedef bool (CALLBACK * JsMemoryAllocationCallback)(  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryEventType allocationEvent,  
   _In_ size_t allocationSize  
);  
```  
  
#### Параметры  
 callbackState  
 Состояние, передаваемое в JsSetRuntimeMemoryAllocationCallback.  
  
 allocationEvent  
 Тип события выделения типа.  
  
 allocationSize  
 Размер выделения.  
  
## Значение свойства/возвращаемое значение  
 Для события JsMemoryAllocate возвращаемое значение true позволяет среде выполнения продолжить выделение. Если возвращено значение false, запрос на выделение отклоняется. Возвращаемое значение игнорируется для других событий выделения.  
  
## Комментарии  
 Для регистрации этого обратного вызова используйте JsSetRuntimeMemoryAllocationCallback.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)