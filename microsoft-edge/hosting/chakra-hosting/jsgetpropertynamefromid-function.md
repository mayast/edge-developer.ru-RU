---
description: Получает имя, связанное с ИДЕНТИФИКАТОРом свойства.
title: Функция JsGetPropertyNameFromId | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e76c69c1d746302bb95cd7229872845c4fbcc88
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571384"
---
# Функция JsGetPropertyNameFromId
Получает имя, связанное с ИДЕНТИФИКАТОРом свойства.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### Параметры  
 `propertyId`  
 Идентификатор свойства, для которого нужно получить имя.  
  
 `name`  
 Имя, связанное с ИДЕНТИФИКАТОРом свойства.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Возвращенный буфер действителен, пока среда выполнения активна и не может использоваться после удаления среды выполнения.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)