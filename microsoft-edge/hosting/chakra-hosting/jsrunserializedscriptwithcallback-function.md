---
description: Выполняет сериализованный сценарий. Обеспечивает возможность отложенной загрузки источника сценария только в том случае, если он необходим.
title: Функция JsRunSerializedScriptWithCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 0608d778-f65b-4dc5-a745-364aac57ef59
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 31669615d5e00cb2dbe3730ed20e24d904161f8b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572465"
---
# Функция JsRunSerializedScriptWithCallback
Выполняет сериализованный сценарий. Обеспечивает возможность отложенной загрузки источника сценария только в том случае, если он необходим.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsRunSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_opt_ JsValueRef *result  
);  
  
```  
  
#### Параметры  
 `scriptLoadCallback`  
 Функция обратного вызова, вызываемая при необходимости загрузки исходного кода сценария.  
  
 `scriptUnloadCallback`  
 Функция обратного вызова вызывается, когда сериализованный сценарий и исходный код больше не нужны.  
  
 `buffer`  
 Сериализованный сценарий.  
  
 `sourceContext`  
 Объект cookie, определяющий сценарий, который можно использовать для контекстно-отлаженных сценариев.     Этот контекст будет передан в scriptLoadCallback и scriptUnloadCallback.  
  
 `sourceUrl`  
 Расположение, из которого получен сценарий.  
  
 `result`  
 Результат выполнения сценария, если таковой имеется. Этот параметр может быть равен null.  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
  
> [!NOTE]
>  Этот API пока не доступен для приложений Магазина.  
  
 Требуется активный контекст сценария.  
  
 Среда выполнения будет храниться в буфере до тех пор, пока все экземпляры функций, созданных из буфера, не будут собраны сборщиком мусора.  Затем он вызывает scriptUnloadCallback для информирования вызывающего абонента о том, что он безопасно в целях освобождения.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)