---
description: Перечисление кучи текущего контекста.
title: Функция JsEnumerateHeap | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnumerateHeap
helpviewer_keywords:
- JsEnumerateHeap function
ms.assetid: 3e518e0b-b959-4686-899c-83e6b1946c9d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f1c2590388fcc09b641e3908d45eef7271bcb1ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572540"
---
# <span data-ttu-id="0de13-103">Функция JsEnumerateHeap</span><span class="sxs-lookup"><span data-stu-id="0de13-103">JsEnumerateHeap Function</span></span>
<span data-ttu-id="0de13-104">Перечисление кучи текущего контекста.</span><span class="sxs-lookup"><span data-stu-id="0de13-104">Enumerates the heap of the current context.</span></span>  
  
## <span data-ttu-id="0de13-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0de13-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnumerateHeap(  
   _Out_ IActiveScriptProfilerHeapEnum **enumerator  
);  
```  
  
#### <span data-ttu-id="0de13-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0de13-106">Parameters</span></span>  
 `enumerator`  
 <span data-ttu-id="0de13-107">Перечислитель кучи.</span><span class="sxs-lookup"><span data-stu-id="0de13-107">The heap enumerator.</span></span>  
  
## <span data-ttu-id="0de13-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="0de13-108">Return Value</span></span>  
 <span data-ttu-id="0de13-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0de13-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0de13-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0de13-110">Remarks</span></span>  
 <span data-ttu-id="0de13-111">При перечислении кучи текущий контекст не может быть удален, и все вызовы для изменения состояния контекста будут завершаться сбоем, пока не будет освобожден перечислитель кучи.</span><span class="sxs-lookup"><span data-stu-id="0de13-111">While the heap is being enumerated, the current context cannot be removed, and all calls to modify the state of the context will fail until the heap enumerator is released.</span></span>  
  
 <span data-ttu-id="0de13-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="0de13-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="0de13-113">Этот API поддерживается в классических приложениях, но не поддерживается в приложениях Магазина.</span><span class="sxs-lookup"><span data-stu-id="0de13-113">This API is supported in desktop apps, but is not supported in Store apps.</span></span>  
  
## <span data-ttu-id="0de13-114">Требования</span><span class="sxs-lookup"><span data-stu-id="0de13-114">Requirements</span></span>  
 <span data-ttu-id="0de13-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0de13-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0de13-116">См. также</span><span class="sxs-lookup"><span data-stu-id="0de13-116">See Also</span></span>  
 [<span data-ttu-id="0de13-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0de13-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)