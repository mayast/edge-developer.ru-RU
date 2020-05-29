---
description: Выполняет сериализацию проанализированного сценария в буфер, чем может быть повторно использован.
title: Функция JsSerializeScript | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1b45067fddb7ea4dff02e527e460db1270011c61
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572453"
---
# Функция JsSerializeScript
Выполняет сериализацию проанализированного сценария в буфер, чем может быть повторно использован.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### Параметры  
 `script`  
 Сценарий, который нужно сериализовать.  
  
 `buffer`  
 Буфер, в который будет помещен сериализованный сценарий. Может иметь значение null.  
  
 `bufferSize`  
 На входе — размер буфера в байтах; при выходе — размер буфера (в байтах), который должен хранить сериализованный сценарий.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 `JsSerializeScript` анализирует сценарий и сохраняет проанализированную форму сценария в формате, не зависящем от среды выполнения. Сериализованный сценарий затем можно десериализовать в любой среде выполнения, не требуя повторного синтаксического анализа сценария.  
  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)