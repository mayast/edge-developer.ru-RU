---
description: Указывает среде выполнения, что она должна выполнить все необходимые действия.
title: Функция JsIdle | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4da7148bf7daa3db983ab8f5bba622bfe0b19466
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572492"
---
# Функция JsIdle
Указывает среде выполнения, что она должна выполнить все необходимые действия.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### Параметры  
 `nextIdleTick`  
 Следующий системный Квант, если у вас есть больше времени на работу. Может иметь значение null. Возвращает максимальное количество тактов в случае отсутствия предстоящих усилий.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Если для текущей среды выполнения включена обработка простаивающих ресурсов, при звонке `JsIdle` сообщается о текущей среде выполнения, когда узел бездействует и что среда выполнения может выполнять задачи по очистке памяти.  
  
 `JsIdle` также может возвращать число системных тактов, пока не будет более простой работы, чтобы среда выполнения работала. Вызов `JsIdle` до того, как это число тактов пройдет, не будет работать.  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)