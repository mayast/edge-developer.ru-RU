---
description: Извлекает сведения о внешних данных индексированных свойств объекта.
title: Функция JsGetIndexedPropertiesExternalData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 96fdcd4b6fe29ffc20a796983cc1de692c80a3f1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571387"
---
# Функция JsGetIndexedPropertiesExternalData
Извлекает сведения о внешних данных индексированных свойств объекта.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### Параметры  
 `object`  
 Объект.  
  
 `data`  
 Резервное хранилище внешних данных для индексированных свойств объекта.  
  
 `arrayType`  
 Тип элемента массива во внешних данных.  
  
 `elementLength`  
 Количество элементов массива во внешних данных.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)