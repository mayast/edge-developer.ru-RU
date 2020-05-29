---
description: 'Задает функцию обратного вызова, вызываемую средой выполнения перед сборкой мусора. '
title: Функция JsSetRuntimeBeforeCollectCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeBeforeCollectCallback
helpviewer_keywords:
- JsSetRuntimeBeforeCollectCallback function
ms.assetid: 7b2fb911-6007-4ed9-a307-66cefe590ea4
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 31aefd28698c14a6fe17421a990a7c8b120876bf
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572343"
---
# Функция JsSetRuntimeBeforeCollectCallback
Задает функцию обратного вызова, вызываемую средой выполнения перед сборкой мусора.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeBeforeCollectCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsBeforeCollectCallback beforeCollectCallback  
);  
```  
  
#### Параметры  
 `runtime`  
 Среда выполнения, для которой регистрируется обратный вызов выделения.  
  
 `callbackState`  
 Указанное пользователем состояние, которое будет передано обратно обратному вызову.  
  
 `beforeCollectCallback`  
 Задается функция обратного вызова.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Обратный вызов вызывается в текущем потоке выполнения среды выполнения, поэтому выполнение блокируется до тех пор, пока не завершится обратный вызов.  
  
 Обратный вызов может использоваться узлами для подготовки к сбору мусора. Например, освобождая ненужные ссылки на объекты Chakra.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)