---
description: Создает новую функцию JavaScript с именем.
title: Функция JsCreateNamedFunction | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 72f40d06-ab82-4fed-a632-68af6b4126c2
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d963fe196b8e56394e22501ed3898a0d887a3d3b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571430"
---
# Функция JsCreateNamedFunction
Создает новую функцию JavaScript с именем.
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateNamedFunction(  
   _In_ JsValueRef name,  
   _In_ JsNativeFunction nativeFunction,  
   _In_opt_ void *callbackState,  
   _Out_ JsValueRef *function  
);  
```  
  
#### Параметры  
 `name`  
 Имя функции, которая будет использоваться в целях диагностики и stringification.  
  
 `nativeFunction`  
 Метод, который нужно вызвать при вызове функции.  
  
 `callbackState`  
 Указанное пользователем состояние, которое будет передано обратно обратному вызову.  
  
 `function`  
 Новый объект Function.  
  
## Возвращенное значение  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)