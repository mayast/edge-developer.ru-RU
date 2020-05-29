---
description: Контекст, переданный в обратный вызов приложения, JsProjectionEnqueueCallback из JsRT и затем передаваемый обратно в JsRT в указанном обратном вызове, в `JsProjectionCallback` приложении в правильном потоке.
title: JsProjectionCallbackContext typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571346"
---
# JsProjectionCallbackContext typedef
Контекст, переданный в обратный вызов приложения, JsProjectionEnqueueCallback из JsRT и затем передаваемый обратно в JsRT в указанном обратном вызове, в `JsProjectionCallback` приложении в правильном потоке.  
  
## Синтаксис  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## Комментарии  
 Требуется вызов `JsSetProjectionEnqueueCallback` для приема обратных вызовов.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)