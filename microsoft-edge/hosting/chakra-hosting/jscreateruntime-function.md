---
description: Создает новую среду выполнения.
title: Функция JsCreateRuntime | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d25c1b46354be1fda0ce906dc68c3643989fe2c6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571423"
---
# Функция JsCreateRuntime
Создает новую среду выполнения.
  
## Синтаксис  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_ JsRuntimeVersion version,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### Параметры  
 `attributes`  
 Атрибуты создаваемой среды выполнения.  
  
 `version`  
 Версия среды выполнения, которую нужно создать.  
  
 `threadService`  
 Служба потока для среды выполнения. Может иметь значение null.  
  
 `runtime`  
 Среда выполнения создана.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 `version`В режиме Microsoft Edge этот параметр не поддерживается. Дополнительные сведения об использовании этого API в режиме Microsoft EDGE можно найти в разделе [назначение Microsoft EDGE и устаревших ядер](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)