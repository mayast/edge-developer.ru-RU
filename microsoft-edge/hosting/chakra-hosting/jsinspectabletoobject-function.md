---
description: Создает значение JavaScript, которое является проекцией переданного `IInspectable` указателя.
title: Функция JsInspectableToObject | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 26ce17eb3abcefcf9a1f0cc773e9fe4c3aaf05cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571367"
---
# Функция JsInspectableToObject
Создает значение JavaScript, которое является проекцией переданного `IInspectable` указателя.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### Параметры  
 `inspectable`  
 `IInspectable`Для прогноза.  
  
 `value`  
 Значение JavaScript, которое является проекцией `IInspectable` .  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Проецируемое значение может использоваться сценарием для вызова объекта WinRT. Узлы ответственны за принудительное использование правил COM Threading.  
  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)