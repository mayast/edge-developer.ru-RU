---
description: Вызывается средой выполнения, когда она завершает работу со всеми ресурсами, относящимися к выполнению сценария. Вызывающий объект должен освобождать источник, если в настоящее время загружено, байтовый код и контекст.
title: JsSerializedScriptUnloadCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3da27af18ebc7a1913980a865d926bac6a29d11
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751942"
---
# JsSerializedScriptUnloadCallback typedef
Вызывается средой выполнения, когда она завершает работу со всеми ресурсами, относящимися к выполнению сценария. Вызывающий объект должен освобождать источник, если в настоящее время загружено, байтовый код и контекст.  
  
## Синтаксис  
  
```cpp  
 typedef void (CALLBACK * JsSerializedScriptUnloadCallback)(  
  _In_ JsSourceContext sourceContext  
);  
```  
  
#### Параметры  
 `sourceContext`  
 Контекст, переданный `JsParseSerializedScriptWithCallback` или `JsRunSerializedScriptWithCallback` .  
  
## Комментарии  
  
> [!WARNING]
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)