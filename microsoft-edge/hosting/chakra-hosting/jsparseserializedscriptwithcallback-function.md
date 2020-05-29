---
description: Анализирует сериализованный сценарий и возвращает функцию, которая представляет сценарий. Обеспечивает возможность отложенной загрузки источника сценария только в том случае, если он необходим.
title: Функция JsParseSerializedScriptWithCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 0a93ecfb-4b82-4a85-b24c-6816db2332ea
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ad6d635722f0b3fea8b19f8d16679b402d1fd56e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572481"
---
# Функция JsParseSerializedScriptWithCallback
Анализирует сериализованный сценарий и возвращает функцию, которая представляет сценарий. Обеспечивает возможность отложенной загрузки источника сценария только в том случае, если он необходим.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScriptWithCallback(  
  _In_ JsSerializedScriptLoadSourceCallback scriptLoadCallback,  
  _In_ JsSerializedScriptUnloadCallback scriptUnloadCallback,  
  _In_ BYTE *buffer,  
  _In_ JsSourceContext sourceContext,  
  _In_z_ const wchar_t *sourceUrl,  
  _Out_ JsValueRef * result  
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
 Функция, представляющая код сценария.  
  
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