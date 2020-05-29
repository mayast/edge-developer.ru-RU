---
description: Создает контекст сценария для выполнения сценариев.
title: Функция JsCreateContext | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 06bd4c4780a8c7610ebc95cfc0da058306ce5b78
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571443"
---
# Функция JsCreateContext
Создает контекст сценария для выполнения сценариев.  
  
## Синтаксис  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### Параметры  
 `runtime`  
 Среда выполнения, в которой создается контекст сценария.  
  
 `debugApplication`  
 Отладочное приложение, используемое для отладки. Этот параметр может иметь значение null, в этом случае отладка не включена для контекста.  
  
 `newContext`  
 Созданный контекст сценария.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Каждый контекст сценария имеет собственный глобальный объект, который изолирован от всех остальных контекстов сценария.  
  
 `debugApplication`В режиме Microsoft Edge этот параметр не поддерживается. Дополнительные сведения об использовании этого API в режиме Microsoft EDGE можно найти в разделе [назначение Microsoft EDGE и устаревших ядер](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)