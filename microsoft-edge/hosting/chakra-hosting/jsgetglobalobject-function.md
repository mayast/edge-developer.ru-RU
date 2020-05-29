---
description: Получает глобальный объект в текущем контексте сценария.
title: Функция JsGetGlobalObject | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetGlobalObject
helpviewer_keywords:
- JsGetGlobalObject function
ms.assetid: d3e91e64-1ca3-4d2b-aada-725ded0fd0b1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 9f8b540485e75ef80d42ba66f031b3e827b475fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571388"
---
# <span data-ttu-id="a0216-103">Функция JsGetGlobalObject</span><span class="sxs-lookup"><span data-stu-id="a0216-103">JsGetGlobalObject Function</span></span>
<span data-ttu-id="a0216-104">Получает глобальный объект в текущем контексте сценария.</span><span class="sxs-lookup"><span data-stu-id="a0216-104">Gets the global object in the current script context.</span></span>  
  
## <span data-ttu-id="a0216-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0216-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetGlobalObject(  
   _Out_ JsValueRef *globalObject  
);  
```  
  
#### <span data-ttu-id="a0216-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0216-106">Parameters</span></span>  
 `globalObject`  
 <span data-ttu-id="a0216-107">Глобальный объект.</span><span class="sxs-lookup"><span data-stu-id="a0216-107">The global object.</span></span>  
  
## <span data-ttu-id="a0216-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a0216-108">Return Value</span></span>  
 <span data-ttu-id="a0216-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a0216-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a0216-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a0216-110">Remarks</span></span>  
 <span data-ttu-id="a0216-111">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="a0216-111">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a0216-112">Требования</span><span class="sxs-lookup"><span data-stu-id="a0216-112">Requirements</span></span>  
 <span data-ttu-id="a0216-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a0216-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a0216-114">См. также</span><span class="sxs-lookup"><span data-stu-id="a0216-114">See Also</span></span>  
 [<span data-ttu-id="a0216-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a0216-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)