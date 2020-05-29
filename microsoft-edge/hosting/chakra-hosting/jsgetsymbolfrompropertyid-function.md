---
description: Возвращает символ, связанный с ИДЕНТИФИКАТОРом свойства.
title: Функция JsGetSymbolFromPropertyId | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 0e822cb4-ba9e-44df-bf3a-fae97c354daa
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6902384772f29f80751660ce2d4a295d2ea620ab
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571372"
---
# Функция JsGetSymbolFromPropertyId
Возвращает символ, связанный с ИДЕНТИФИКАТОРом свойства.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetSymbolFromPropertyId(  
   _In_ JsPropertyIdRef propertyId,  
   _Out_ JsValueRef *symbol  
);  
```  
  
#### Параметры  
 `propertyId`  
 Идентификатор свойства, для которого нужно получить символ.  
  
 `symbol`  
 Символ, связанный с ИДЕНТИФИКАТОРом свойства.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)