---
description: Устанавливает текущее ограничение объема памяти для среды выполнения.
title: Функция JsSetRuntimeMemoryLimit | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ec8d098c528ac813926797280541aa2c9c4fee79
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572341"
---
# Функция JsSetRuntimeMemoryLimit
Устанавливает текущее ограничение объема памяти для среды выполнения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### Параметры  
 `runtime`  
 Среда выполнения, для которой необходимо установить ограничение объема памяти.  
  
 `memoryLimit`  
 Предельный размер памяти среды выполнения, в байтах или-1, чтобы ограничить объем памяти.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Предельный объем памяти может привести к тому, что любая операция, превышающая ограничение, завершится ошибкой из-за ошибки "недостаточно памяти". Установка ограничения памяти среды выполнения равным-1 означает, что в среде выполнения не будет ограничения объема памяти. Новые среды выполнения по умолчанию не ограничивают объем памяти. Если новый лимит памяти превышает текущее использование, вызов завершится успешно, а все будущие выделения в этой среде выполнения будут завершаться сбоем, пока использование памяти среды выполнения не станет меньше предела.  
  
 Ограничение памяти среды выполнения может быть всегда задано, независимо от того, активна ли среда выполнения в другом потоке.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)