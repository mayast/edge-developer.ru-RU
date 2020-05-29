---
description: Тип события обратного вызова выделения.
title: Перечисление JsMemoryEventType | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e9833777ed8fe5a19fd2a1487715296279f7351
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571353"
---
# Перечисление JsMemoryEventType
Тип события обратного вызова выделения.  
  
## Синтаксис  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## Участников  
  
### Данные  
  
|Имя|Описание|  
|----------|-----------------|  
|`JsMemoryAllocate`|Указывает на запрос выделения памяти.|  
|`JsMemoryFailure`|Указывает на сбой выделения.|  
|`JsMemoryFree`|Указывает на событие освобождения памяти.|  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)