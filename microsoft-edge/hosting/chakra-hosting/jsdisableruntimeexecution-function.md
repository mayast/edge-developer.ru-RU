---
description: Приостанавливает выполнение сценария и прерывает выполнение сценариев в среде выполнения.
title: Функция JsDisableRuntimeExecution | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 575947d3038eaa136e9d6ae62507501bc768eabe
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571406"
---
# Функция JsDisableRuntimeExecution
Приостанавливает выполнение сценария и прерывает выполнение сценариев в среде выполнения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Параметры  
 `runtime`  
 Приостановленная среда выполнения.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Вызов приостановленной среды выполнения завершается сбоем, пока `JsEnableRuntimeExecution` не будет вызван.  
  
 Этот API-интерфейс не должен вызываться в потоке, для которого активна среда выполнения. Несмотря на то что среда выполнения будет переведена в состояние SUSPENDED, выполняемый сценарий может быть приостановлен немедленно. выполняемый сценарий будет завершен с неперехваченным исключением как можно скорее.  
  
 Приостановка выполнения в среде выполнения, которая уже приостановлена, — это отсутствие операций.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)