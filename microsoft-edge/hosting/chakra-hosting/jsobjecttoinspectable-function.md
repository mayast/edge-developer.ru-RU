---
description: Распаковывает объект JavaScript в `IInspectable` указатель.
title: Функция JsObjectToInspectable | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 1d15b0b8-516f-4fc6-95aa-2ddd65f8ab75
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7127e1cf1372020e0df00b81ed172739379426f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572489"
---
# Функция JsObjectToInspectable
Распаковывает объект JavaScript в `IInspectable` указатель.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsObjectToInspectable(  
   _In_ JsValueRef value,  
   _Out_ IInspectable  **inspectable  
);  
```  
  
#### Параметры  
 `value`  
 Значение JavaScript, на которое должно быть запланировано проецирование `IInspectable` .  
  
 `inspectable`  
 `IInspectable`Значение объекта.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Узлы ответственны за принудительное использование правил COM Threading.  
  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)