---
description: Вызывается средой выполнения для загрузки исходного кода сериализованного сценария. Вызывающий объект должен поддерживать буфер сценария, пока не будет `JsSerializedScriptUnloadCallback` .
title: JsSerializedScriptLoadSourceCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 9406c488-76ac-49e5-b305-39751f3412ea
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1264bdc77da10cadb44a570ae37e7f3cd9ce6b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572456"
---
# JsSerializedScriptLoadSourceCallback typedef
Вызывается средой выполнения для загрузки исходного кода сериализованного сценария. Вызывающий объект должен поддерживать буфер сценария, пока не будет `JsSerializedScriptUnloadCallback` .  
  
## Синтаксис  
  
```cpp  
typedef bool (CALLBACK * JsSerializedScriptLoadSourceCallback)(  
  _In_ JsSourceContextsourceContext,  
  _Outptr_result_z_ const wchar_t** scriptBuffer  
);  
```  
  
#### Параметры  
 `sourceContext`  
 Контекст, переданный `JsParseSerializedScriptWithCallback` или `JsRunSerializedScriptWithCallback` .  
  
 `scriptBuffer`  
 Возвращаемый сценарий.  
  
## Комментарии  
  
> [!WARNING]
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)