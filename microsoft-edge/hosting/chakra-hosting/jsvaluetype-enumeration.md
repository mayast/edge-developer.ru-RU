---
description: Тип JavaScript JsValueRef.
title: Перечисление JsValueType | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsValueType
helpviewer_keywords:
- JsValueType enumeration
ms.assetid: 6645e723-e554-41fc-b622-ab54ee044b3d
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c42231525b55b49f0931a2ace33b373e0d4ae441
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571328"
---
# Перечисление JsValueType
Тип JavaScript JsValueRef.  
  
## Синтаксис  
  
```cpp  
enum JsValueType {  
    JsUndefined      = 0,  
    JsNull           = 1,  
    JsNumber         = 2,  
    JsString         = 3,  
    JsBoolean        = 4,  
    JsObject         = 5,  
    JsFunction       = 6,  
    JsError          = 7,  
    JsArray          = 8,  
    JsSymbol         = 9,  
    JsArrayBuffer    = 10,  
    JsTypedArray     = 11,  
    JsDataView       = 12,  
};  
```  
  
## Участников  
  
### Данные  
  
|Имя|Описание|  
|----------|-----------------|  
|`JsUndefined`|Значением является `undefined` значение.|  
|`JsNull`|Значением является `null` значение.|  
|`JsNumber`|Значение является значением номера JavaScript.|  
|`JsString`|Значение — это строковое значение JavaScript.|  
|`JsBoolean`|Значение является логическим значением JavaScript.|  
|`JsObject`|Значение является значением объекта JavaScript.|  
|`JsFunction`|Значением является значение объекта функции JavaScript.|  
|`JsError`|Значением является значение объекта ошибки JavaScript.|  
|`JsArray`|Значение является значением объекта-массива JavaScript.|  
|`JsSymbol`|Значение является значением символа JavaScript.<br /><br /> Это значение перечисления поддерживается только в режиме Microsoft Edge.|  
|`JsArrayBuffer`|Значение является `ArrayBuffer` значением объекта JavaScript.<br /><br /> Это значение перечисления поддерживается только в режиме Microsoft Edge.|  
|`JsTypedArray`|Значение является значением объекта типизированного массива JavaScript.<br /><br /> Это значение перечисления поддерживается только в режиме Microsoft Edge.|  
|`JsDataView`|Значение является `DataView` значением объекта JavaScript.<br /><br /> Это значение перечисления поддерживается только в режиме Microsoft Edge.|  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)