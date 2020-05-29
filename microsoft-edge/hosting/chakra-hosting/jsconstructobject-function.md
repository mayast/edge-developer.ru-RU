---
description: Вызывает функцию в качестве конструктора.
title: Функция JsConstructObject | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConstructObject
helpviewer_keywords:
- JsConstructObject function
ms.assetid: b07d2440-db55-4a6a-8376-56b40a8039a1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6fb9654b5c7321d6c6b0b255ec897fb30a114041
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571458"
---
# <span data-ttu-id="4e411-103">Функция JsConstructObject</span><span class="sxs-lookup"><span data-stu-id="4e411-103">JsConstructObject Function</span></span>
<span data-ttu-id="4e411-104">Вызывает функцию в качестве конструктора.</span><span class="sxs-lookup"><span data-stu-id="4e411-104">Invokes a function as a constructor.</span></span>  
  
## <span data-ttu-id="4e411-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e411-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConstructObject(  
   _In_ JsValueRef function,  
   _In_reads_(argumentCount) JsValueRef *arguments,  
   _In_ unsigned short argumentCount,  
   _Out_opt_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="4e411-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e411-106">Parameters</span></span>  
 `function`  
 <span data-ttu-id="4e411-107">Функция, которую нужно вызвать как конструктор.</span><span class="sxs-lookup"><span data-stu-id="4e411-107">The function to invoke as a constructor.</span></span>  
  
 `arguments`  
 <span data-ttu-id="4e411-108">Аргументы для вызова.</span><span class="sxs-lookup"><span data-stu-id="4e411-108">The arguments to the call.</span></span>  
  
 `argumentCount`  
 <span data-ttu-id="4e411-109">Число аргументов, передаваемых функции.</span><span class="sxs-lookup"><span data-stu-id="4e411-109">The number of arguments being passed in to the function.</span></span>  
  
 `result`  
 <span data-ttu-id="4e411-110">Значение, возвращаемое при вызове функции.</span><span class="sxs-lookup"><span data-stu-id="4e411-110">The value returned from the function invocation.</span></span>  
  
## <span data-ttu-id="4e411-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="4e411-111">Return Value</span></span>  
 <span data-ttu-id="4e411-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4e411-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="4e411-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4e411-113">Remarks</span></span>  
 <span data-ttu-id="4e411-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="4e411-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="4e411-115">Требования</span><span class="sxs-lookup"><span data-stu-id="4e411-115">Requirements</span></span>  
 <span data-ttu-id="4e411-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="4e411-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="4e411-117">См. также</span><span class="sxs-lookup"><span data-stu-id="4e411-117">See Also</span></span>  
 [<span data-ttu-id="4e411-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="4e411-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)