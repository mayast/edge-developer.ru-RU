---
description: Обратный вызов функции.
title: JsNativeFunction typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c0b73a11d3a0b2ed0867ef001f3c29c5643132a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571354"
---
# JsNativeFunction typedef
Обратный вызов функции.  
  
## Синтаксис  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### Параметры  
 Вызываемый абонент  
 `Function`Объект, представляющий вызываемую функцию.  
  
 isConstructCall  
 Показывает, является ли этот вызов регулярным или новым.  
  
 arguments  
 Аргументы для вызова.  
  
 argumentCount  
 Число аргументов.  
  
## Значение свойства/возвращаемое значение  
 Результат звонка (если таковой имеется).  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)