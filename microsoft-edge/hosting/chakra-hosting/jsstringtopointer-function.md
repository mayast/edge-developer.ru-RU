---
description: Извлекает указатель строки в строковом значении.
title: Функция JsStringToPointer | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStringToPointer
helpviewer_keywords:
- JsStringToPointer function
ms.assetid: c7aa7a09-489d-4435-8f8a-aeb62f8875ae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1f5997894c4ea479378a323b230492dde28ab177
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572338"
---
# <span data-ttu-id="bf1ac-103">Функция JsStringToPointer</span><span class="sxs-lookup"><span data-stu-id="bf1ac-103">JsStringToPointer Function</span></span>
<span data-ttu-id="bf1ac-104">Извлекает указатель строки в строковом значении.</span><span class="sxs-lookup"><span data-stu-id="bf1ac-104">Retrieves the string pointer of a string value.</span></span>  
  
## <span data-ttu-id="bf1ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf1ac-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsStringToPointer(  
   _In_ JsValueRef value,  
   _Outptr_result_buffer_(*stringLength) const wchar_t **stringValue,  
   _Out_ size_t *stringLength  
);  
```  
  
#### <span data-ttu-id="bf1ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf1ac-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="bf1ac-107">Строковое значение, которое нужно преобразовать в указатель строки.</span><span class="sxs-lookup"><span data-stu-id="bf1ac-107">The string value to convert to a string pointer.</span></span>  
  
 `stringValue`  
 <span data-ttu-id="bf1ac-108">Указатель строки.</span><span class="sxs-lookup"><span data-stu-id="bf1ac-108">The string pointer.</span></span>  
  
 `stringLength`  
 <span data-ttu-id="bf1ac-109">Длина строки.</span><span class="sxs-lookup"><span data-stu-id="bf1ac-109">The length of the string.</span></span>  
  
## <span data-ttu-id="bf1ac-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="bf1ac-110">Return Value</span></span>  
 <span data-ttu-id="bf1ac-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="bf1ac-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bf1ac-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf1ac-112">Remarks</span></span>  
 <span data-ttu-id="bf1ac-113">Эта функция извлекает указатель строки в строковом значении.</span><span class="sxs-lookup"><span data-stu-id="bf1ac-113">This function retrieves the string pointer of a string value.</span></span> <span data-ttu-id="bf1ac-114">`JsErrorInvalidArgument`Если тип значения не является строковым, произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="bf1ac-114">It will fail with `JsErrorInvalidArgument` if the type of the value is not string.</span></span> <span data-ttu-id="bf1ac-115">Время существования возвращаемой строки будет совпадать со временем существования значения, из которого она была получена, но указатель строки не считается ссылкой на значение (и поэтому не будет храниться).</span><span class="sxs-lookup"><span data-stu-id="bf1ac-115">The lifetime of the string returned will be the same as the lifetime of the value it came from, however the string pointer is not considered a reference to the value (and so will not keep it from being collected).</span></span>  
  
 <span data-ttu-id="bf1ac-116">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="bf1ac-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bf1ac-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bf1ac-117">Requirements</span></span>  
 <span data-ttu-id="bf1ac-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bf1ac-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bf1ac-119">См. также</span><span class="sxs-lookup"><span data-stu-id="bf1ac-119">See Also</span></span>  
 [<span data-ttu-id="bf1ac-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bf1ac-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)