---
description: Создает строковое значение из указателя строки.
title: Функция JsPointerToString | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsPointerToString
helpviewer_keywords:
- JsPointerToString function
ms.assetid: c71ce07e-4359-450c-afbf-a6ab7d48dddf
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b3c5b2d6439244bc9584e15c361412c8a1e87557
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572482"
---
# <span data-ttu-id="f94f7-103">Функция JsPointerToString</span><span class="sxs-lookup"><span data-stu-id="f94f7-103">JsPointerToString Function</span></span>
<span data-ttu-id="f94f7-104">Создает строковое значение из указателя строки.</span><span class="sxs-lookup"><span data-stu-id="f94f7-104">Creates a string value from a string pointer.</span></span>  
  
## <span data-ttu-id="f94f7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f94f7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsPointerToString(  
   _In_reads_(stringLength) const wchar_t *stringValue,  
   _In_ size_t stringLength,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="f94f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f94f7-106">Parameters</span></span>  
 `stringValue`  
 <span data-ttu-id="f94f7-107">Указатель строки для преобразования в строковое значение.</span><span class="sxs-lookup"><span data-stu-id="f94f7-107">The string pointer to convert to a string value.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="f94f7-108">Длина строки для преобразования.</span><span class="sxs-lookup"><span data-stu-id="f94f7-108">The length of the string to convert.</span></span>  
  
 `value`  
 <span data-ttu-id="f94f7-109">Новое строковое значение.</span><span class="sxs-lookup"><span data-stu-id="f94f7-109">The new string value.</span></span>  
  
## <span data-ttu-id="f94f7-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="f94f7-110">Return Value</span></span>  
 <span data-ttu-id="f94f7-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f94f7-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="f94f7-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f94f7-112">Remarks</span></span>  
 <span data-ttu-id="f94f7-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="f94f7-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="f94f7-114">Требования</span><span class="sxs-lookup"><span data-stu-id="f94f7-114">Requirements</span></span>  
 <span data-ttu-id="f94f7-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f94f7-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f94f7-116">См. также</span><span class="sxs-lookup"><span data-stu-id="f94f7-116">See Also</span></span>  
 [<span data-ttu-id="f94f7-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f94f7-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)