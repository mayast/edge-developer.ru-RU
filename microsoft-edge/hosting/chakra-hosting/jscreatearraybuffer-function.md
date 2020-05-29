---
description: Создает объект JavaScript `ArrayBuffer` .
title: Функция JsCreateArrayBuffer | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c9e74184-7dd9-41a7-a1fe-9575e1701392
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7e81c50317de5243fbcdf761c09c084f97a8e1e0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571447"
---
# <span data-ttu-id="23241-103">Функция JsCreateArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="23241-103">JsCreateArrayBuffer Function</span></span>
<span data-ttu-id="23241-104">Создает объект JavaScript `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="23241-104">Creates a JavaScript `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="23241-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="23241-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateArrayBuffer(  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="23241-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="23241-106">Parameters</span></span>  
 `byteLength`  
 <span data-ttu-id="23241-107">Число байтов в ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="23241-107">The number of bytes in the ArrayBuffer.</span></span>  
  
 `result`  
 <span data-ttu-id="23241-108">Новый объект ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="23241-108">The new ArrayBuffer object.</span></span>  
  
## <span data-ttu-id="23241-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="23241-109">Return Value</span></span>  
 <span data-ttu-id="23241-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="23241-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="23241-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="23241-111">Remarks</span></span>  
 <span data-ttu-id="23241-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="23241-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="23241-113">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23241-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="23241-114">Требования</span><span class="sxs-lookup"><span data-stu-id="23241-114">Requirements</span></span>  
 <span data-ttu-id="23241-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="23241-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="23241-116">См. также</span><span class="sxs-lookup"><span data-stu-id="23241-116">See Also</span></span>  
 [<span data-ttu-id="23241-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="23241-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)