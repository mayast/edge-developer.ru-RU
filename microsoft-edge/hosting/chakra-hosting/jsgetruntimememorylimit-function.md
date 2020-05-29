---
description: Возвращает текущее ограничение памяти для среды выполнения.
title: Функция JsGetRuntimeMemoryLimit | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e6b44bb1dc8ad5fb8c07248a225c10682f96c86a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571377"
---
# Функция JsGetRuntimeMemoryLimit
Возвращает текущее ограничение памяти для среды выполнения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### Параметры  
 `runtime`  
 Среда выполнения, предел памяти которой требуется извлечь.  
  
 `memoryLimit`  
 Текущий лимит памяти среды выполнения (в байтах) или-1, если не установлен предел.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Предельное значение объема памяти может быть получено всегда, независимо от того, активна ли среда выполнения в другом потоке.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)