---
description: Преобразует значение в объект, используя стандартную семантику JavaScript.
title: Функция JsConvertValueToObject | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToObject
helpviewer_keywords:
- JsConvertValueToObject function
ms.assetid: 6528b28a-1d2b-417f-bf78-bf05547c52e1
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6a8b1a8933cdcaaf250a2e28ed8fc758ea66cc0e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571450"
---
# <span data-ttu-id="76eed-103">Функция JsConvertValueToObject</span><span class="sxs-lookup"><span data-stu-id="76eed-103">JsConvertValueToObject Function</span></span>
<span data-ttu-id="76eed-104">Преобразует значение в объект, используя стандартную семантику JavaScript.</span><span class="sxs-lookup"><span data-stu-id="76eed-104">Converts the value to object using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="76eed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76eed-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToObject(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *object  
);  
```  
  
#### <span data-ttu-id="76eed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76eed-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="76eed-107">Преобразуемое значение.</span><span class="sxs-lookup"><span data-stu-id="76eed-107">The value to be converted.</span></span>  
  
 `object`  
 <span data-ttu-id="76eed-108">Преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="76eed-108">The converted value.</span></span>  
  
## <span data-ttu-id="76eed-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="76eed-109">Return Value</span></span>  
 <span data-ttu-id="76eed-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="76eed-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="76eed-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76eed-111">Remarks</span></span>  
 <span data-ttu-id="76eed-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="76eed-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="76eed-113">Требования</span><span class="sxs-lookup"><span data-stu-id="76eed-113">Requirements</span></span>  
 <span data-ttu-id="76eed-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="76eed-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="76eed-115">См. также</span><span class="sxs-lookup"><span data-stu-id="76eed-115">See Also</span></span>  
 [<span data-ttu-id="76eed-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="76eed-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)