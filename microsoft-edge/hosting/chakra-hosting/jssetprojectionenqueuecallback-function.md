---
description: Задает метод обратного вызова, который должен использоваться для того, чтобы вызвать завершение проекции для потока вызывающих абонентов.
title: Функция JsSetProjectionEnqueueCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c751ccef-20d2-4d41-9568-1c54adf47cdf
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 02da0238360b0dc6fff9bb86c9f5ab04d1ba7112
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572436"
---
# Функция JsSetProjectionEnqueueCallback
Задает метод обратного вызова, который должен использоваться для того, чтобы вызвать завершение проекции для потока вызывающих абонентов.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetProjectionEnqueueCallback(  
   _In_ JsProjectionEnqueueCallback projectionEnqueueCallback,  
   _In_opt_ void *projectionEnqueueContext);  
  
```  
  
#### Параметры  
 `projectionEnqueueContext`  
 Обратный вызов, который будет вызываться каждый раз, когда завершение проекции выполняется в фоновом потоке.  
  
 `callbackState`  
 Контекст приложения, представленный в `projectionEnqueueContext` .  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Вызов должен выполняться из другого апартамента COM или из другого потока в том же MTA.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
> [!CAUTION]
>  Для этого API в настоящее время не поддерживается PInvoke.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)