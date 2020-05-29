---
description: Обратный вызов, вызванный перед коллекцией.
title: JsBeforeCollectCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 58bece47-4e6d-49e7-a93d-b6a8f9928b41
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 17f279c2d2ffcc8d02819994dddebfc22baa4cab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571467"
---
# JsBeforeCollectCallback typedef
Обратный вызов, вызванный перед коллекцией.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsBeforeCollectCallback)(  
_In_opt_ void *callbackState  
);  
```  
  
#### Параметры  
 callbackState  
 Состояние, передаваемое в JsSetBeforeCollectCallback.  
  
## Комментарии  
 Для регистрации этого обратного вызова используйте JsSetBeforeCollectCallback.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)