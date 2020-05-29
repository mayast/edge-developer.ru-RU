---
description: Возвращает исключение, которое привело к тому, что среда выполнения текущего контекста находится в состоянии исключения, и сбрасывает состояние исключения для этой среды выполнения.
title: Функция JsGetAndClearException | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetAndClearException
helpviewer_keywords:
- JsGetAndClearException function
ms.assetid: 6aec8a88-41ee-47f6-b5f4-32f3cae6bb7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: eb70b4b66b4bb270d9f26487708720efddc2effa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572532"
---
# Функция JsGetAndClearException
Возвращает исключение, которое привело к тому, что среда выполнения текущего контекста находится в состоянии исключения, и сбрасывает состояние исключения для этой среды выполнения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetAndClearException(  
   _Out_ JsValueRef *exception  
);  
```  
  
#### Параметры  
 `exception`  
 Исключение для среды выполнения текущего контекста.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Если среда выполнения текущего контекста не находится в состоянии исключения, этот API будет возвращен `JsErrorInvalidArgument` . Если среда выполнения отключена, будет возвращено исключение, указывающее на то, что сценарий был завершен, но не будет очищать это исключение (исключение будет очищено, если среда выполнения повторно включена с помощью `JsEnableRuntimeExecution` ).  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)