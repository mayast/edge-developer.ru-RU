---
description: Обратный вызов фонового рабочего элемента.
title: JsBackgroundWorkItemCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: e6db52e1-830c-46a2-b9f9-cc2d450a1da8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9bc1e5687d92d7286e1e6d4387bd6b69d95ceb68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571470"
---
# JsBackgroundWorkItemCallback typedef
Обратный вызов фонового рабочего элемента.  
  
## Синтаксис  
  
```cpp  
typedef void (CALLBACK *JsBackgroundWorkItemCallback)(  
   _In_opt_ void *callbackData  
);  
```  
  
#### Параметры  
 callbackData  
 Аргумент данных, передаваемый службе потока.  
  
## Комментарии  
 Это значение передается службе потока узла (если она предоставлена), чтобы разрешить ведущему приложению вызвать обратный вызов рабочего элемента в фоновом потоке выбора.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)