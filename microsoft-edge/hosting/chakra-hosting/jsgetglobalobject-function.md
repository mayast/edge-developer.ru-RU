---
description: Получает глобальный объект в текущем контексте сценария.
title: Функция JsGetGlobalObject | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9f8b540485e75ef80d42ba66f031b3e827b475fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571388"
---
# Функция JsGetGlobalObject
Получает глобальный объект в текущем контексте сценария.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### Параметры  
 `globalObject`  
 Глобальный объект.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)