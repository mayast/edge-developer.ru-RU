---
description: Обратный вызов службы Threading.
title: JsThreadServiceCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dbe67be5-418a-4f66-8b68-b38078a6d140
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5eb9f2986c79db024f01f4d22050f79c9689400c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571336"
---
# JsThreadServiceCallback typedef
Обратный вызов службы Threading.  
  
## Синтаксис  
  
```cpp  
typedef bool (CALLBACK *JsThreadServiceCallback)(  
   _In_ JsBackgroundWorkItemCallback callback,  
   _In_opt_ void *callbackData  
);  
```  
  
#### Параметры  
 предусмотрен  
 Обратный вызов для элемента фоновой задачи.  
  
 callbackData  
 Аргумент данных, передаваемый обратному вызову.  
  
## Комментарии  
 Ведущее приложение может указать службу фонового потока при вызове JsCreateRuntime. Если задано, фоновые рабочие элементы будут переданы узлу с помощью этого обратного вызова. Предполагается, что основное приложение либо сразу же начинает выполнение фонового рабочего элемента, и возвращает значение true, и среда выполнения будет обрабатывать рабочий элемент in-Thread.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)