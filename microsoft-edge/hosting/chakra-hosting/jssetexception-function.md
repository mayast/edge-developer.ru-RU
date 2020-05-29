---
description: Задает в качестве среды выполнения текущего контекста состояние исключения.
title: Функция JsSetException | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetException
helpviewer_keywords:
- JsSetException function
ms.assetid: c528793a-2e1b-4ee1-bd2e-e63fd547dc40
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 75d2895a725c622a0b46887d10154c3a0c56c7e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572449"
---
# Функция JsSetException
Задает в качестве среды выполнения текущего контекста состояние исключения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetException(  
   _In_ JsValueRef exception  
);  
```  
  
#### Параметры  
 `exception`  
 Исключение JavaScript, которое необходимо установить для среды выполнения текущего контекста.  
  
## Возвращенное значение  
 `JsNoError` Если обработчик установил состояние исключения, в противном случае — код ошибки.  
  
## Комментарии  
 Если среда выполнения текущего контекста уже находится в состоянии исключения, этот API будет возвращен `JsErrorInExceptionState` .  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)