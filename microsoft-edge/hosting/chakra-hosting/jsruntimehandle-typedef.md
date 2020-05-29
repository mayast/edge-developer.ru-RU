---
description: Дескриптор среды выполнения Chakra.
title: JsRuntimeHandle typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 69e59bfd-9b0e-4710-9aa8-fbd6844171bc
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4ccdcf39ec6062db47e1b9de249d75c8804de405
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572457"
---
# JsRuntimeHandle typedef
Дескриптор среды выполнения Chakra.  
  
## Синтаксис  
  
```cpp  
typedef void *JsRuntimeHandle;  
```  
  
## Комментарии  
 У каждой среды выполнения Chakra есть собственный независимый обработчик выполнения, JIT-компилятор и куча, собранные сборщиком мусора. Таким образом, все среды выполнения полностью изолированы от других сред выполнения.  
  
 Среды выполнения можно использовать в любом потоке, но в любой момент можно вызвать среду выполнения только из одного потока.  
  
> [!WARNING]
>  JsRuntimeHandle, в отличие от других ссылок на объекты в API размещения Chakra, не собирается сборщиком мусора, так как он содержит саму кучу, в которой собрано мусора. Среда выполнения продолжает существовать до тех пор, пока JsDisposeRuntime не будет вызван.  
  
## Требования  
 **Верхний колонтитул:** jsrt. h  
  
## См. также  
 [Справочник (среда выполнения JavaScript)](../chakra-hosting/reference-javascript-runtime.md)