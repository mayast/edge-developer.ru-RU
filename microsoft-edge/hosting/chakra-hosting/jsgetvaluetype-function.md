---
description: Возвращает тип JavaScript JsValueRef.
title: Функция JsGetValueType | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetValueType
helpviewer_keywords:
- JsGetValueType function
ms.assetid: f403cf7c-c8c0-4a17-bfa9-0302d00e760e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 85dc6644e26017c6085ab64d914a86196cca8080
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572499"
---
# <span data-ttu-id="72041-103">Функция JsGetValueType</span><span class="sxs-lookup"><span data-stu-id="72041-103">JsGetValueType Function</span></span>
<span data-ttu-id="72041-104">Возвращает тип JavaScript JsValueRef.</span><span class="sxs-lookup"><span data-stu-id="72041-104">Gets the JavaScript type of a JsValueRef.</span></span>  
  
## <span data-ttu-id="72041-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="72041-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetValueType(  
   _In_ JsValueRef value,  
   _Out_ JsValueType *type  
);  
```  
  
#### <span data-ttu-id="72041-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72041-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="72041-107">Значение, тип которого нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="72041-107">The value whose type is to be returned.</span></span>  
  
 `type`  
 <span data-ttu-id="72041-108">Тип значения.</span><span class="sxs-lookup"><span data-stu-id="72041-108">The type of the value.</span></span>  
  
## <span data-ttu-id="72041-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="72041-109">Return Value</span></span>  
 <span data-ttu-id="72041-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="72041-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="72041-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72041-111">Remarks</span></span>  
 <span data-ttu-id="72041-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="72041-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="72041-113">Требования</span><span class="sxs-lookup"><span data-stu-id="72041-113">Requirements</span></span>  
 <span data-ttu-id="72041-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="72041-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="72041-115">См. также</span><span class="sxs-lookup"><span data-stu-id="72041-115">See Also</span></span>  
 [<span data-ttu-id="72041-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="72041-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)