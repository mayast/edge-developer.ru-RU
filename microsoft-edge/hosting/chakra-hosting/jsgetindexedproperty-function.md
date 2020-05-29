---
description: Получение значения по указанному индексу объекта.
title: Функция JsGetIndexedProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7bb048b841462e27604ab169c69e4c051209a67d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572520"
---
# Функция JsGetIndexedProperty
Получение значения по указанному индексу объекта.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Параметры  
 `object`  
 Объект для работы.  
  
 `index`  
 Индекс, который требуется извлечь.  
  
 `result`  
 Извлеченное значение.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)