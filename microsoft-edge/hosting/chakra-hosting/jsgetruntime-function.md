---
description: Возвращает среду выполнения, в которую входит контекст.
title: Функция JsGetRuntime | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntime
helpviewer_keywords:
- JsGetRuntime function
ms.assetid: 5b62e940-a885-405a-9fdd-0495fb391b95
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6eeb132dd35fcb5104828bef8e8f27334a5f34e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571380"
---
# <span data-ttu-id="6b34e-103">Функция JsGetRuntime</span><span class="sxs-lookup"><span data-stu-id="6b34e-103">JsGetRuntime Function</span></span>
<span data-ttu-id="6b34e-104">Возвращает среду выполнения, в которую входит контекст.</span><span class="sxs-lookup"><span data-stu-id="6b34e-104">Gets the runtime that the context belongs to.</span></span>  
  
## <span data-ttu-id="6b34e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b34e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntime(  
   _In_ JsContextRef context,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="6b34e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b34e-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="6b34e-107">Контекст, из которого требуется получить среду выполнения.</span><span class="sxs-lookup"><span data-stu-id="6b34e-107">The context to get the runtime from.</span></span>  
  
 `runtime`  
 <span data-ttu-id="6b34e-108">Среда выполнения, к которой относится контекст.</span><span class="sxs-lookup"><span data-stu-id="6b34e-108">The runtime the context belongs to.</span></span>  
  
## <span data-ttu-id="6b34e-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="6b34e-109">Return Value</span></span>  
 <span data-ttu-id="6b34e-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6b34e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6b34e-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6b34e-111">Requirements</span></span>  
 <span data-ttu-id="6b34e-112">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6b34e-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6b34e-113">См. также</span><span class="sxs-lookup"><span data-stu-id="6b34e-113">See Also</span></span>  
 [<span data-ttu-id="6b34e-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6b34e-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)