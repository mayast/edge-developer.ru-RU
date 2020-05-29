---
description: Выполняет сериализованный сценарий.
title: Функция JsRunSerializedScript | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRunSerializedScript
helpviewer_keywords:
- JsRunSerializedScript function
ms.assetid: 3fd3f6f1-eb3e-4751-92a5-c93b1035f3b2
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bc1e2fb7fdc5df52fde3b7cc59cf9173d658782a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572470"
---
# Функция JsRunSerializedScript
Выполняет сериализованный сценарий.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Параметры  
 `script`  
 Исходный код сериализованного сценария.  
  
 `buffer`  
 Сериализованный сценарий.  
  
 `sourceContext`  
 Объект cookie, определяющий сценарий, который можно использовать для контекстно-отлаженных сценариев.  
  
 `sourceUrl`  
 Расположение, из которого получен сценарий.  
  
 `result`  
 Результат выполнения сценария, если таковой имеется. Этот параметр может быть равен null.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Буфер не сохраняется в памяти обработчиком сценариев, поэтому ваш код должен поддерживать его, пока он может использоваться для выполнения сценариев.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)