---
description: Обратный вызов приложения, вызываемый функцией JsRT, когда интерфейс API проекции завершается в потоке, отличном от исходного.
title: JsProjectionEnqueueCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 19c1cefb-a7be-4196-b780-9fe6adf35ba5
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 064a7d1077ae5222e44ab08ebe0592bb97b1f2af
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571344"
---
# JsProjectionEnqueueCallback typedef
Обратный вызов приложения, вызываемый функцией JsRT, когда интерфейс API проекции завершается в потоке, отличном от исходного.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsProjectionEnqueueCallback)(  
  _In_ JsProjectionCallback jsCallback,  
  _In_ JsProjectionCallbackContext jsContext,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Параметры  
 `jsCallback`  
 Обратный вызов, вызываемый в исходном потоке.  
  
 `jsContext`  
 Контекст приложения.  
  
 `callbackState`  
 Контекст JsRT, который необходимо передать `jsCallback` .  
  
## Комментарии  
 Требуется вызов JsSetProjectionEnqueueCallback для получения обратных вызовов.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)