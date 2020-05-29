---
description: Задает обратный вызов выделения памяти для указанной среды выполнения.
title: Функция JsSetRuntimeMemoryAllocationCallback | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetRuntimeMemoryAllocationCallback
helpviewer_keywords:
- JsSetRuntimeMemoryAllocationCallback function
ms.assetid: 6aa7d58d-6456-4df1-815f-1ba36fb4ae14
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5c648761473023f00e894fbf75c794cfcc9422c5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572342"
---
# <span data-ttu-id="e3e0f-103">Функция JsSetRuntimeMemoryAllocationCallback</span><span class="sxs-lookup"><span data-stu-id="e3e0f-103">JsSetRuntimeMemoryAllocationCallback Function</span></span>
<span data-ttu-id="e3e0f-104">Задает обратный вызов выделения памяти для указанной среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-104">Sets a memory allocation callback for specified runtime.</span></span>  
  
## <span data-ttu-id="e3e0f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e3e0f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetRuntimeMemoryAllocationCallback(  
   _In_ JsRuntimeHandle runtime,  
   _In_opt_ void *callbackState,  
   _In_ JsMemoryAllocationCallback allocationCallback  
);  
```  
  
#### <span data-ttu-id="e3e0f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e3e0f-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="e3e0f-107">Среда выполнения, для которой регистрируется обратный вызов выделения.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-107">The runtime for which to register the allocation callback.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="e3e0f-108">Указанное пользователем состояние, которое будет передано обратно обратному вызову.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-108">User provided state that will be passed back to the callback.</span></span>  
  
 `allocationCallback`  
 <span data-ttu-id="e3e0f-109">Обратный вызов выделения памяти, который нужно вызвать для событий выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-109">Memory allocation callback to be called for memory allocation events.</span></span>  
  
## <span data-ttu-id="e3e0f-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e3e0f-110">Return Value</span></span>  
 <span data-ttu-id="e3e0f-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e3e0f-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e3e0f-112">Remarks</span></span>  
 <span data-ttu-id="e3e0f-113">Регистрация обратного вызова для выделения памяти приведет к тому, что среда выполнения будет вызывать приложение, когда он получает память из памяти или освобождает ее.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-113">Registering a memory allocation callback will cause the runtime to call back to the host whenever it acquires memory from, or releases memory to, the OS.</span></span> <span data-ttu-id="e3e0f-114">Процедура обратного вызова вызывается перед тем, как диспетчер памяти среды выполнения выделяет блок памяти.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-114">The callback routine is called before the runtime memory manager allocates a block of memory.</span></span> <span data-ttu-id="e3e0f-115">Выделение будет отклонено, если обратный вызов возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-115">The allocation will be rejected if the callback returns false.</span></span> <span data-ttu-id="e3e0f-116">Диспетчер памяти среды выполнения также вызывает процедуру обратного вызова после освобождения блока памяти, а также после сбоя выделения ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-116">The runtime memory manager will also invoke the callback routine after freeing a block of memory, as well as after allocation failures.</span></span>  
  
 <span data-ttu-id="e3e0f-117">Обратный вызов вызывается в текущем потоке выполнения среды выполнения, поэтому выполнение блокируется до тех пор, пока не завершится обратный вызов.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-117">The callback is invoked on the current runtime execution thread, therefore execution is blocked until the callback completes.</span></span>  
  
 <span data-ttu-id="e3e0f-118">Возвращаемое значение обратного вызова не сохраняется; ранее отклоненные выделения не мешают среде выполнения повторно вызвать обратный вызов для новых операций выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="e3e0f-118">The return value of the callback is not stored; previously rejected allocations will not prevent the runtime from invoking the callback again later for new memory allocations.</span></span>  
  
## <span data-ttu-id="e3e0f-119">Требования</span><span class="sxs-lookup"><span data-stu-id="e3e0f-119">Requirements</span></span>  
 <span data-ttu-id="e3e0f-120">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e3e0f-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e3e0f-121">См. также</span><span class="sxs-lookup"><span data-stu-id="e3e0f-121">See Also</span></span>  
 [<span data-ttu-id="e3e0f-122">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e3e0f-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)