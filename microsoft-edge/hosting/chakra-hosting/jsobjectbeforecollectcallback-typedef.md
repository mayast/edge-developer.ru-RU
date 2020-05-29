---
description: Обратный вызов, вызываемый перед сбором объекта.
title: JsObjectBeforeCollectCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: f21a064a-579f-44cb-9d21-76b62e8c18f5
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 27bbd1aed72cc751397ac4e6734f107612653b66
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571348"
---
# JsObjectBeforeCollectCallback typedef
Обратный вызов, вызываемый перед сбором объекта.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsObjectBeforeCollectCallback)(  
  _In_ JsRef ref,  
  _In_opt_ void *callbackState  
);  
```  
  
#### Параметры  
 `ref`  
 Объект, который нужно собрать.  
  
 `callbackState`  
 Состояние, в которое передается `JsSetObjectBeforeCollectCallback` .  
  
## Комментарии  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)