---
description: Устанавливает текущее ограничение объема памяти для среды выполнения.
title: Функция JsSetRuntimeMemoryLimit | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryLimit
helpviewer_keywords:
- JsSetRuntimeMemoryLimit function
ms.assetid: 74feb31f-19f6-43e3-b117-0694c59ac593
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: ec8d098c528ac813926797280541aa2c9c4fee79
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572341"
---
# <span data-ttu-id="7744c-103">Функция JsSetRuntimeMemoryLimit</span><span class="sxs-lookup"><span data-stu-id="7744c-103">JsSetRuntimeMemoryLimit Function</span></span>
<span data-ttu-id="7744c-104">Устанавливает текущее ограничение объема памяти для среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="7744c-104">Sets the current memory limit for a runtime.</span></span>  
  
## <span data-ttu-id="7744c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7744c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryLimit(  
   _In_ JsRuntimeHandle runtime,  
   _In_ size_t memoryLimit  
);  
```  
  
#### <span data-ttu-id="7744c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7744c-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="7744c-107">Среда выполнения, для которой необходимо установить ограничение объема памяти.</span><span class="sxs-lookup"><span data-stu-id="7744c-107">The runtime whose memory limit is to be set.</span></span>  
  
 `memoryLimit`  
 <span data-ttu-id="7744c-108">Предельный размер памяти среды выполнения, в байтах или-1, чтобы ограничить объем памяти.</span><span class="sxs-lookup"><span data-stu-id="7744c-108">The new runtime memory limit, in bytes, or -1 for no memory limit.</span></span>  
  
## <span data-ttu-id="7744c-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="7744c-109">Return Value</span></span>  
 <span data-ttu-id="7744c-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7744c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="7744c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7744c-111">Remarks</span></span>  
 <span data-ttu-id="7744c-112">Предельный объем памяти может привести к тому, что любая операция, превышающая ограничение, завершится ошибкой из-за ошибки "недостаточно памяти".</span><span class="sxs-lookup"><span data-stu-id="7744c-112">A memory limit will cause any operation which exceeds the limit to fail with an "out of memory" error.</span></span> <span data-ttu-id="7744c-113">Установка ограничения памяти среды выполнения равным-1 означает, что в среде выполнения не будет ограничения объема памяти.</span><span class="sxs-lookup"><span data-stu-id="7744c-113">Setting a runtime's memory limit to -1 means that the runtime has no memory limit.</span></span> <span data-ttu-id="7744c-114">Новые среды выполнения по умолчанию не ограничивают объем памяти.</span><span class="sxs-lookup"><span data-stu-id="7744c-114">New runtimes default to having no memory limit.</span></span> <span data-ttu-id="7744c-115">Если новый лимит памяти превышает текущее использование, вызов завершится успешно, а все будущие выделения в этой среде выполнения будут завершаться сбоем, пока использование памяти среды выполнения не станет меньше предела.</span><span class="sxs-lookup"><span data-stu-id="7744c-115">If the new memory limit exceeds current usage, the call will succeed and any future allocations in this runtime will fail until the runtime's memory usage drops below the limit.</span></span>  
  
 <span data-ttu-id="7744c-116">Ограничение памяти среды выполнения может быть всегда задано, независимо от того, активна ли среда выполнения в другом потоке.</span><span class="sxs-lookup"><span data-stu-id="7744c-116">A runtime's memory limit can be always be set, regardless of whether or not the runtime is active on another thread.</span></span>  
  
## <span data-ttu-id="7744c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="7744c-117">Requirements</span></span>  
 <span data-ttu-id="7744c-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="7744c-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="7744c-119">См. также</span><span class="sxs-lookup"><span data-stu-id="7744c-119">See Also</span></span>  
 [<span data-ttu-id="7744c-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="7744c-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)