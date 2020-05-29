---
description: Приостанавливает выполнение сценария и прерывает выполнение сценариев в среде выполнения.
title: Функция JsDisableRuntimeExecution | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisableRuntimeExecution
helpviewer_keywords:
- JsDisableRuntimeExecution function
ms.assetid: 4bd4670a-a9da-4f8c-b3fd-1fd366d915c3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 575947d3038eaa136e9d6ae62507501bc768eabe
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571406"
---
# <span data-ttu-id="98b18-103">Функция JsDisableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="98b18-103">JsDisableRuntimeExecution Function</span></span>
<span data-ttu-id="98b18-104">Приостанавливает выполнение сценария и прерывает выполнение сценариев в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="98b18-104">Suspends script execution and terminates any running scripts in a runtime.</span></span>  
  
## <span data-ttu-id="98b18-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="98b18-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="98b18-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="98b18-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="98b18-107">Приостановленная среда выполнения.</span><span class="sxs-lookup"><span data-stu-id="98b18-107">The runtime to be suspended.</span></span>  
  
## <span data-ttu-id="98b18-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="98b18-108">Return Value</span></span>  
 <span data-ttu-id="98b18-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="98b18-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="98b18-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="98b18-110">Remarks</span></span>  
 <span data-ttu-id="98b18-111">Вызов приостановленной среды выполнения завершается сбоем, пока `JsEnableRuntimeExecution` не будет вызван.</span><span class="sxs-lookup"><span data-stu-id="98b18-111">Calls to a suspended runtime will fail until `JsEnableRuntimeExecution` is called.</span></span>  
  
 <span data-ttu-id="98b18-112">Этот API-интерфейс не должен вызываться в потоке, для которого активна среда выполнения.</span><span class="sxs-lookup"><span data-stu-id="98b18-112">This API does not have to be called on the thread the runtime is active on.</span></span> <span data-ttu-id="98b18-113">Несмотря на то что среда выполнения будет переведена в состояние SUSPENDED, выполняемый сценарий может быть приостановлен немедленно. выполняемый сценарий будет завершен с неперехваченным исключением как можно скорее.</span><span class="sxs-lookup"><span data-stu-id="98b18-113">Although the runtime will be set into a suspended state, an executing script may not be suspended immediately; a running script will be terminated with an uncatchable exception as soon as possible.</span></span>  
  
 <span data-ttu-id="98b18-114">Приостановка выполнения в среде выполнения, которая уже приостановлена, — это отсутствие операций.</span><span class="sxs-lookup"><span data-stu-id="98b18-114">Suspending execution in a runtime that is already suspended is a no-op.</span></span>  
  
## <span data-ttu-id="98b18-115">Требования</span><span class="sxs-lookup"><span data-stu-id="98b18-115">Requirements</span></span>  
 <span data-ttu-id="98b18-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="98b18-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="98b18-117">См. также</span><span class="sxs-lookup"><span data-stu-id="98b18-117">See Also</span></span>  
 [<span data-ttu-id="98b18-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="98b18-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)