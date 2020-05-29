---
description: Преобразует значение в строку, используя стандартную семантику JavaScript.
title: Функция JsConvertValueToString | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsConvertValueToString
helpviewer_keywords:
- JsConvertValueToString function
ms.assetid: a97aca04-b2ce-446a-acf4-49cd6777a85c
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 21c77ca3050773c07572665c6d58e0ebc05d8ee9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571448"
---
# <span data-ttu-id="b496c-103">Функция JsConvertValueToString</span><span class="sxs-lookup"><span data-stu-id="b496c-103">JsConvertValueToString Function</span></span>
<span data-ttu-id="b496c-104">Преобразует значение в строку, используя стандартную семантику JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b496c-104">Converts the value to string using standard JavaScript semantics.</span></span>  
  
## <span data-ttu-id="b496c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b496c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsConvertValueToString(  
   _In_ JsValueRef value,  
   _Out_ JsValueRef *stringValue  
);  
```  
  
#### <span data-ttu-id="b496c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b496c-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="b496c-107">Преобразуемое значение.</span><span class="sxs-lookup"><span data-stu-id="b496c-107">The value to be converted.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="b496c-108">Преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="b496c-108">The converted value.</span></span>  
  
## <span data-ttu-id="b496c-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="b496c-109">Return Value</span></span>  
 <span data-ttu-id="b496c-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b496c-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b496c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b496c-111">Remarks</span></span>  
 <span data-ttu-id="b496c-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="b496c-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b496c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b496c-113">Requirements</span></span>  
 <span data-ttu-id="b496c-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b496c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b496c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="b496c-115">See Also</span></span>  
 [<span data-ttu-id="b496c-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b496c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)