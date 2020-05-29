---
description: Возвращает значение, указывающее, является ли объект расширяемым.
title: Функция JsGetExtensionAllowed | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExtensionAllowed
helpviewer_keywords:
- JsGetExtensionAllowed function
ms.assetid: 839054a1-d643-47d9-89db-6a015bba0d91
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e3baa6449294f7b055251d861a32095deb1bdfe9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571392"
---
# Функция JsGetExtensionAllowed
Возвращает значение, указывающее, является ли объект расширяемым.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExtensionAllowed(  
   _In_ JsValueRef object,  
   _Out_ bool *value  
);  
```  
  
#### Параметры  
 `object`  
 Проверяемый объект.  
  
 `value`  
 Является ли объект расширяемым.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)