---
description: Возвращает `int` значение числового значения.
title: Функция JsNumberToInt | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8b9256d6-76ac-4c74-a97c-fbb16c13f5f5
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cf4c8cb42c737cfb9efee5422fe6bb3c1389cbfd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572490"
---
# Функция JsNumberToInt
Возвращает `int` значение числового значения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsNumberToInt(  
      _In_ JsValueRef value,  
      _Out_ int *intValue  
);  
```  
  
#### Параметры  
 `value`  
 Числовое значение, которое нужно преобразовать в `int` значение.  
  
 `intValue`  
 `int`Значение.  
  
## Возвращенное значение  
  
## Комментарии  
 Эта функция извлекает значение числового значения и преобразует его в `int` значение. `JsErrorInvalidArgument`Если тип значения не является числом, произойдет сбой.  
  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)