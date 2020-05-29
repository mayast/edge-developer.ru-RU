---
description: Возвращает среду выполнения, в которую входит контекст.
title: Функция JsGetRuntime | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6eeb132dd35fcb5104828bef8e8f27334a5f34e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571380"
---
# Функция JsGetRuntime
Возвращает среду выполнения, в которую входит контекст.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### Параметры  
 `context`  
 Контекст, из которого требуется получить среду выполнения.  
  
 `runtime`  
 Среда выполнения, к которой относится контекст.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)