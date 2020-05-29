---
description: Инициализирует переданный метод `VARIANT` как проекцию значения JavaScript.
title: Функция JsValueToVariant | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueToVariant
helpviewer_keywords:
- JsValueToVariant function
ms.assetid: 070244be-a69d-4b78-971b-69c0579c03cf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d8748fddcc149cf09fbd46ad3ad489cd66200b71
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571329"
---
# Функция JsValueToVariant
Инициализирует переданный метод `VARIANT` как проекцию значения JavaScript.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsValueToVariant(  
   _In_ JsValueRef object,  
   _Out_ VARIANT *variant  
);  
```  
  
#### Параметры  
 `object`  
 Значение JavaScript для проекта как `VARIANT` .  
  
 `variant`  
 Указатель на `VARIANT` структуру, которая будет инициализирована как проекция.  
  
## Возвращенное значение  
  
## Комментарии  
 Проекция `VARIANT` может использоваться клиентами автоматизации com для вызова проецируемого объекта JavaScript.  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)