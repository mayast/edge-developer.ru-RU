---
description: Обратный вызов для продолжения обещания.
title: JsPromiseContinuationCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 51a3fd02-9668-4cf7-bb0b-e1fd03b2528f
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 023d88af5ff82056d8f57453e0a53b91b34565a6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571338"
---
# JsPromiseContinuationCallback typedef
Обратный вызов для продолжения обещания.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsPromiseContinuationCallback)(  
  _In_ JsValueRef task,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Параметры  
 `task`  
  `callbackState`  
  
## Комментарии  
 Основное приложение может указать обратный вызов для продолжения Promise `JsSetPromiseContinuationCallback` . Если сценарий создает задачу, которая должна выполняться позже, для нее будет вызван обратный вызов для продолжения по обещанию, а задача должна быть помещена в очередь FIFO, чтобы выполняться при завершении выполнения текущего сценария.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)