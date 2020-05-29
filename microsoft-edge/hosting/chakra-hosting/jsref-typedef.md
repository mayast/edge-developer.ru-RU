---
description: Ссылка на объект, принадлежащий сборщику мусора Chakra.
title: JsRef typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f5ce1ada67a4530ba57345b90c0b7deba6954c7c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572474"
---
# JsRef typedef
Ссылка на объект, принадлежащий сборщику мусора Chakra.  
  
## Синтаксис  
  
```cpp  
typedef void *JsRef;  
```  
  
## Комментарии  
 Среда выполнения Chakra автоматически отслеживает ссылки JsRef, пока они хранятся в локальных переменных или в параметрах (например, в стеке). Для хранения JsRef, не включенных в стек, требуется вызвать JsAddRef и JsRelease для управления жизненным циклом объекта, в противном случае сборщик мусора может высвободить объект, пока он все еще используется.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)