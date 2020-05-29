---
description: Возвращает текущее ограничение памяти для среды выполнения.
title: Функция JsGetRuntimeMemoryLimit | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetRuntimeMemoryLimit
helpviewer_keywords:
- JsGetRuntimeMemoryLimit function
ms.assetid: ed81ca60-99fd-46b0-89ae-f6ac07926904
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e6b44bb1dc8ad5fb8c07248a225c10682f96c86a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571377"
---
# <span data-ttu-id="0180e-103">Функция JsGetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="0180e-103">JsGetRuntimeMemoryLimit Function</span></span>
<span data-ttu-id="0180e-104">Возвращает текущее ограничение памяти для среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="0180e-104">Gets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="0180e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0180e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ size_t *memoryLimit  
);  
```  
  
#### <span data-ttu-id="0180e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0180e-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="0180e-107">Среда выполнения, предел памяти которой требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="0180e-107">The runtime whose memory limit is to be retrieved.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="0180e-108">Текущий лимит памяти среды выполнения (в байтах) или-1, если не установлен предел.</span><span class="sxs-lookup"><span data-stu-id="0180e-108">The runtime's current memory limit, in bytes, or -1 if no limit has been set.</span></span>  
  
## <span data-ttu-id="0180e-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="0180e-109">Return Value</span></span>  
 <span data-ttu-id="0180e-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0180e-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0180e-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0180e-111">Remarks</span></span>  
 <span data-ttu-id="0180e-112">Предельное значение объема памяти может быть получено всегда, независимо от того, активна ли среда выполнения в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="0180e-112">The memory limit of a runtime can be always be retrieved, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="0180e-113">Требования</span><span class="sxs-lookup"><span data-stu-id="0180e-113">Requirements</span></span>  
 <span data-ttu-id="0180e-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0180e-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0180e-115">См. также</span><span class="sxs-lookup"><span data-stu-id="0180e-115">See Also</span></span>  
 [<span data-ttu-id="0180e-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0180e-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)