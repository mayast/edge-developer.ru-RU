---
description: Определяет, находится ли среда выполнения текущего контекста в состоянии исключения.
title: Функция JsHasException | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsHasException
helpviewer_keywords:
- JsHasException function
ms.assetid: ac7da3ce-c746-4154-bbb8-bcb0859a8d5b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 25ddb8f9cc407dd414a6cd2210c315eb4dd7b141
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572498"
---
# Функция JsHasException
Определяет, находится ли среда выполнения текущего контекста в состоянии исключения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsHasException(  
   _Out_ bool *hasException  
);  
```  
  
#### Параметры  
 `hasException`  
 Указывает, находится ли среда выполнения текущего контекста в состоянии исключения.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Если вызов в среду выполнения приводит к возникновению исключения (как в результате выполнения сценария, так и из-за ошибки преобразования), среда выполнения помещается в состояние Exception. Все звонки в любой контекст, созданный средой выполнения (за исключением API исключений), будут завершаться сбоем `JsErrorInExceptionState` до тех пор, пока не будет очищено исключение.  
  
 Если среда выполнения текущего контекста находится в состоянии исключения, когда обратный вызов возвращает обработчик, обработчик автоматически создаст исключение.  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)