---
description: Создает объект JavaScript `DataView` .
title: Функция JsCreateDataView | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1bf237458e8561b7070e4f3f0d4a14050f028375
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571440"
---
# Функция JsCreateDataView
Создает объект JavaScript `DataView` .  
  
## Синтаксис  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### Параметры  
 `arrayBuffer`  
 Существующий `ArrayBuffer` объект, который будет использоваться в качестве хранилища для `DataView` объекта результата.  
  
 `byteOffset`  
 Смещение в байтах от начала `arrayBuffer` результата `DataView` до ссылки.  
  
 `byteLength`  
 Количество байтов в ArrayBuffer для представления результатов для ссылки.  
  
 `result`  
 Новый объект DataView.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Требуется активный контекст сценария.  
  
 Этот API поддерживается только в режиме Microsoft Edge.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)