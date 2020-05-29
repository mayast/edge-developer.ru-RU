---
description: Делает объект нерасширяемым.
title: Функция JsPreventExtension | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPreventExtension
helpviewer_keywords:
- JsPreventExtension function
ms.assetid: 8da07e20-d076-4ae4-9fb0-3f3c141518c2
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: baa001b2fd26133ef3a20c88213ac6aaf34a2e0d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572476"
---
# Функция JsPreventExtension
Делает объект нерасширяемым.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsPreventExtension(  
   _In_ JsValueRef object  
);  
```  
  
#### Параметры  
 `object`  
 Объект, который нужно сделать нерасширяемым.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)