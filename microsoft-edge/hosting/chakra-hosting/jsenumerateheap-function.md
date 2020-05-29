---
description: Перечисление кучи текущего контекста.
title: Функция JsEnumerateHeap | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f1c2590388fcc09b641e3908d45eef7271bcb1ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572540"
---
# Функция JsEnumerateHeap
Перечисление кучи текущего контекста.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### Параметры  
 `enumerator`  
 Перечислитель кучи.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 При перечислении кучи текущий контекст не может быть удален, и все вызовы для изменения состояния контекста будут завершаться сбоем, пока не будет освобожден перечислитель кучи.  
  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)