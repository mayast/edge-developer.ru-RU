---
description: Добавляет ссылку на объект, собранный сборщиком мусора.
title: Функция JsAddRef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd02dded6dc2877228f22b4d2800e41a78163467
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571471"
---
# Функция JsAddRef
Добавляет ссылку на объект, собранный сборщиком мусора.  
  
## Синтаксис  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### Параметры  
 `ref`  
 Объект, к которому нужно добавить ссылку.  
  
 `count`  
 Новая функция счетчика ссылок объекта (может передавать значение null).  
  
## Возвращенное значение  
 Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.  
  
## Комментарии  
 Это необходимо вызвать только для `JsRef` дескрипторов, которые не будут храниться в стеке. Вызов `JsAddRef` гарантирует, что объект, на который `JsRef` указывает ссылка, не будет освобожден до `JsRelease` вызова.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)