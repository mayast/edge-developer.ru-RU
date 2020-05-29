---
description: Анализирует сериализованный сценарий и возвращает функцию, которая представляет сценарий.
title: Функция JsParseSerializedScript | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a778a007e69f15063d23cc55f999144ab55a306c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572484"
---
# Функция JsParseSerializedScript
Анализирует сериализованный сценарий и возвращает функцию, которая представляет сценарий.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Параметры  
 `script`  
 Сценарий для синтаксического анализа.  
  
 `buffer`  
 Сериализованный сценарий.  
  
 `sourceContext`  
 Объект cookie, определяющий сценарий, который можно использовать для контекстно-отлаженных сценариев.  
  
 `sourceUrl`  
 Расположение, из которого получен сценарий.  
  
 `result`  
 Функция, представляющая код сценария.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Буфер не сохраняется в памяти обработчиком сценариев, поэтому ваш код должен поддерживать его, пока он может использоваться для выполнения сценариев.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)