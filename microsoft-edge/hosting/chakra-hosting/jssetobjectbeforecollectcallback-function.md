---
description: Задает функцию обратного вызова, вызываемую средой выполнения перед сборкой мусора объекта.
title: Функция JsSetObjectBeforeCollectCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: ea2cbd94-d8b0-4fa9-a4a1-c75a4e338eaf
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 77a59c6ace96809c0b232c96aa9639555e7badcd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572440"
---
# Функция JsSetObjectBeforeCollectCallback
Задает функцию обратного вызова, вызываемую средой выполнения перед сборкой мусора объекта.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetObjectBeforeCollectCallback(  
   _In_ JsRef ref,  
   _In_opt_ void *callbackState,  
   _In_ JsObjectBeforeCollectCallback objectBeforeCollectCallback  
);  
```  
  
#### Параметры  
 `ref`  
 Объект, для которого регистрируется обратный вызов.  
  
 `callbackState`  
 Определяемое пользователем состояние, которое будет передано обратно обратному вызову.  
  
 `objectBeforeCollectCallback`  
 Задается функция обратного вызова. Используйте значение null, чтобы удалить ранее зарегистрированный обратный вызов.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Обратный вызов вызывается в текущем потоке выполнения среды выполнения, поэтому выполнение блокируется до тех пор, пока не завершится обратный вызов.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)