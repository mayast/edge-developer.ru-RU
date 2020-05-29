---
description: Прекращение профилирования в текущем контексте.
title: Функция JsStopProfiling | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStopProfiling
helpviewer_keywords:
- JsStopProfiling function
ms.assetid: 3639c04f-a0f9-418b-be39-92f64b4e7ef8
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9d021c7c9849d20283a39d6ecffc89c5b2ea0db0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572336"
---
# Функция JsStopProfiling
Прекращение профилирования в текущем контексте.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsStopProfiling(  
   _In_ HRESULT reason  
);  
```  
  
#### Параметры  
 `reason`  
 Причина остановки профилирования для передачи обратного вызова профилировщика.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Не будет возвращать ошибку, если профилирование не началось.  
  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)