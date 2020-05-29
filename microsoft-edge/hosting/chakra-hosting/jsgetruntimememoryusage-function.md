---
description: Получает текущее использование памяти для среды выполнения.
title: Функция JsGetRuntimeMemoryUsage | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryUsage
helpviewer_keywords:
- JsGetRuntimeMemoryUsage function
ms.assetid: b9bd4146-bfbc-4cb1-a0e9-a0ded7fb09bd
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9ec8472132b4c50b279ee95f36995bf46c0e29e5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571373"
---
# <span data-ttu-id="3b80e-103">Функция JsGetRuntimeMemoryUsage</span><span class="sxs-lookup"><span data-stu-id="3b80e-103">JsGetRuntimeMemoryUsage Function</span></span>
<span data-ttu-id="3b80e-104">Получает текущее использование памяти для среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="3b80e-104">Gets the current memory usage for a runtime.</span></span>  
  
## <span data-ttu-id="3b80e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b80e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryUsage(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryUsage  
);  
```  
  
#### <span data-ttu-id="3b80e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3b80e-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="3b80e-107">Среда выполнения, для которой требуется извлечь память.</span><span class="sxs-lookup"><span data-stu-id="3b80e-107">The runtime whose memory usage is to be retrieved.</span></span>  
  
 `memoryUsage`  
 <span data-ttu-id="3b80e-108">Текущее использование памяти среды выполнения (в байтах).</span><span class="sxs-lookup"><span data-stu-id="3b80e-108">The runtime's current memory usage, in bytes.</span></span>  
  
## <span data-ttu-id="3b80e-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="3b80e-109">Return Value</span></span>  
 <span data-ttu-id="3b80e-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3b80e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="3b80e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b80e-111">Remarks</span></span>  
 <span data-ttu-id="3b80e-112">Использование памяти может быть всегда извлекаться независимо от того, активна ли среда выполнения в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="3b80e-112">Memory usage can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="3b80e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3b80e-113">Requirements</span></span>  
 <span data-ttu-id="3b80e-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3b80e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="3b80e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="3b80e-115">See Also</span></span>  
 [<span data-ttu-id="3b80e-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3b80e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)