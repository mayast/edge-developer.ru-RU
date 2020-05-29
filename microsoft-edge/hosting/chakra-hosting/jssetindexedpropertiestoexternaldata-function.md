---
description: Задает для индексированных свойств объекта внешние данные. Внешние данные будут использоваться в качестве резервного хранилища для индексированных свойств объекта и доступны как типизированный массив.
title: Функция JsSetIndexedPropertiesToExternalData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c1aed6e194b1dc1c35f403626a7b6c02a7752ffb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572443"
---
# Функция JsSetIndexedPropertiesToExternalData
Задает для индексированных свойств объекта внешние данные. Внешние данные будут использоваться в качестве резервного хранилища для индексированных свойств объекта и доступны как типизированный массив.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### Параметры  
 `object`  
 Объект для работы.  
  
 `data`  
 Внешние данные, которые будут использоваться в качестве резервного хранилища для индексированных свойств объекта.  
  
 `arrayType`  
 Тип элемента массива во внешних данных.  
  
 `elementLength`  
 Количество элементов массива во внешних данных.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме EdgeHTML.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)