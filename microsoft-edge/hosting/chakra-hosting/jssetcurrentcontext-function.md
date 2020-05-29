---
description: Задает текущий контекст скрипта в потоке.
title: Функция JsSetCurrentContext | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetCurrentContext
helpviewer_keywords:
- JsSetCurrentContext function
ms.assetid: 603cc94c-6585-411b-89f9-c6f144e2aa30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57620ad0e986034791ec07765d7cc115b958d661
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572451"
---
# <span data-ttu-id="ba2a1-103">Функция JsSetCurrentContext</span><span class="sxs-lookup"><span data-stu-id="ba2a1-103">JsSetCurrentContext Function</span></span>
<span data-ttu-id="ba2a1-104">Задает текущий контекст скрипта в потоке.</span><span class="sxs-lookup"><span data-stu-id="ba2a1-104">Sets the current script context on the thread.</span></span>  
  
## <span data-ttu-id="ba2a1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba2a1-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetCurrentContext(  
   _In_ JsContextRef context  
);  
```  
  
#### <span data-ttu-id="ba2a1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba2a1-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="ba2a1-107">Контекст сценария, который нужно сделать текущим.</span><span class="sxs-lookup"><span data-stu-id="ba2a1-107">The script context to make current.</span></span>  
  
## <span data-ttu-id="ba2a1-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ba2a1-108">Return Value</span></span>  
 <span data-ttu-id="ba2a1-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ba2a1-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  

## <span data-ttu-id="ba2a1-110">Пример.</span><span class="sxs-lookup"><span data-stu-id="ba2a1-110">Example</span></span>

```cpp
JsRuntimeHandle runtime;
JsContextRef context;

// Create a runtime.
JsCreateRuntime(JsRuntimeAttributeNone, nullptr, &runtime);

// Create an execution context.
JsCreateContext(runtime, &context);

// Now set the current execution context.
JsSetCurrentContext(context);
```

## <span data-ttu-id="ba2a1-111">Требования</span><span class="sxs-lookup"><span data-stu-id="ba2a1-111">Requirements</span></span>  
 <span data-ttu-id="ba2a1-112">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ba2a1-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ba2a1-113">См. также</span><span class="sxs-lookup"><span data-stu-id="ba2a1-113">See Also</span></span>  
 [<span data-ttu-id="ba2a1-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ba2a1-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)