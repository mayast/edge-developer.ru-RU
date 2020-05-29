---
description: Ссылка на контекст сценария.
title: JsContextRef typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571457"
---
# JsContextRef typedef
Ссылка на контекст сценария.  
  
## Синтаксис  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## Комментарии  
 Каждый контекст сценария имеет собственный глобальный объект, отличный от глобального объекта в других контекстах сценария.  
  
 Для многих API размещения Chakra требуется контекст сценария "активный", который можно настроить с помощью `JsSetCurrentContext` . API размещения Chakra, для которых требуется задать текущий контекст, запомните о том, что они будут явно указаны в документации.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)