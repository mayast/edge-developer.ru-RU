---
description: Выполняет полную сборку мусора.
title: Функция JsCollectGarbage | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCollectGarbage
helpviewer_keywords:
- JsCollectGarbage function
ms.assetid: 995c79a5-6e18-45be-81ff-2a5d3348edb8
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1702ad960a0a2f366e97b8a994abd0700cec50e7
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571460"
---
# <span data-ttu-id="e6b51-103">Функция JsCollectGarbage</span><span class="sxs-lookup"><span data-stu-id="e6b51-103">JsCollectGarbage Function</span></span>
<span data-ttu-id="e6b51-104">Выполняет полную сборку мусора.</span><span class="sxs-lookup"><span data-stu-id="e6b51-104">Performs a full garbage collection.</span></span>  
  
## <span data-ttu-id="e6b51-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6b51-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCollectGarbage(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="e6b51-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6b51-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="e6b51-107">Среда выполнения, в которой будет выполняться сборка мусора.</span><span class="sxs-lookup"><span data-stu-id="e6b51-107">The runtime in which the garbage collection will be performed.</span></span>  
  
## <span data-ttu-id="e6b51-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e6b51-108">Return Value</span></span>  
 <span data-ttu-id="e6b51-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e6b51-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e6b51-110">Требования</span><span class="sxs-lookup"><span data-stu-id="e6b51-110">Requirements</span></span>  
 <span data-ttu-id="e6b51-111">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e6b51-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e6b51-112">См. также</span><span class="sxs-lookup"><span data-stu-id="e6b51-112">See Also</span></span>  
 [<span data-ttu-id="e6b51-113">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e6b51-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)