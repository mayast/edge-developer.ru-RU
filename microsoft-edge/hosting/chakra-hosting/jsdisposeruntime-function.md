---
description: Уничтожает среду выполнения.
title: Функция JsDisposeRuntime | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 89166249616c265ce75ebc43a01c838d607bdd08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572542"
---
# Функция JsDisposeRuntime
Уничтожает среду выполнения.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### Параметры  
 `runtime`  
 Среда выполнения для удаления.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 После удаления среды выполнения все ресурсы, которыми владеет она, недопустимы и не могут использоваться. Если среда выполнения активна (то есть она должна быть актуальной в конкретном потоке), она не может быть удалена.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)