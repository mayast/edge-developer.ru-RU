---
description: Создание символа JavaScript.
title: Функция JsCreateSymbol | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2fccc5d9-f857-46cd-9aeb-f0a2e7cdee6b
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a4e634e6f0726ca32ad1056129186ce941edb77b
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571419"
---
# <span data-ttu-id="e7111-103">Функция JsCreateSymbol</span><span class="sxs-lookup"><span data-stu-id="e7111-103">JsCreateSymbol Function</span></span>
<span data-ttu-id="e7111-104">Создание символа JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e7111-104">Creates a JavaScript symbol.</span></span>
  
## <span data-ttu-id="e7111-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e7111-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateSymbol(  
   _In_ JsValueRef description,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="e7111-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e7111-106">Parameters</span></span>  
 `description`  
 <span data-ttu-id="e7111-107">Строковое описание символа.</span><span class="sxs-lookup"><span data-stu-id="e7111-107">The string description of the symbol.</span></span> <span data-ttu-id="e7111-108">Может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="e7111-108">Can be null.</span></span>  
  
 `result`  
 <span data-ttu-id="e7111-109">Новый символ.</span><span class="sxs-lookup"><span data-stu-id="e7111-109">The new symbol.</span></span>  
  
## <span data-ttu-id="e7111-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e7111-110">Return Value</span></span>  
 <span data-ttu-id="e7111-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e7111-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e7111-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e7111-112">Remarks</span></span>  
 <span data-ttu-id="e7111-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="e7111-113">Requires an active script context.</span></span>  
  
 <span data-ttu-id="e7111-114">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="e7111-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="e7111-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e7111-115">Requirements</span></span>  
 <span data-ttu-id="e7111-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e7111-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e7111-117">См. также</span><span class="sxs-lookup"><span data-stu-id="e7111-117">See Also</span></span>  
 [<span data-ttu-id="e7111-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e7111-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)