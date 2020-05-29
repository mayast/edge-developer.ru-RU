---
description: Вызывается средой выполнения, когда она завершает работу со всеми ресурсами, относящимися к выполнению сценария. Вызывающий объект должен освобождать источник, если в настоящее время загружено, байтовый код и контекст.
title: JsSerializedScriptUnloadCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 8d18c392-cca0-411e-9f2b-0d788b16161a
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9555b3fd8c14c9629d17c13592e3c78a78be150e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572455"
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