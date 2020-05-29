---
description: Создает объект типизированного массива JavaScript.
title: Функция JsCreateTypedArray | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 937a2a91-6f5f-4aaa-a018-d3089702bf36
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 57c5d15d76bf8b3ff29d10f7500fe41b3e959f68
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571415"
---
# <span data-ttu-id="16d9e-103">Функция JsCreateTypedArray</span><span class="sxs-lookup"><span data-stu-id="16d9e-103">JsCreateTypedArray Function</span></span>
<span data-ttu-id="16d9e-104">Создает объект типизированного массива JavaScript.</span><span class="sxs-lookup"><span data-stu-id="16d9e-104">Creates a JavaScript typed array object.</span></span>  
  
## <span data-ttu-id="16d9e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16d9e-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateTypedArray(  
   _In_ JsTypedArrayType arrayType,  
   _In_ JsValueRef baseArray,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int elementLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="16d9e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="16d9e-106">Parameters</span></span>  
 `arrayType`  
 <span data-ttu-id="16d9e-107">Тип создаваемого массива.</span><span class="sxs-lookup"><span data-stu-id="16d9e-107">The type of the array to create.</span></span>  
  
 `baseArray`  
 <span data-ttu-id="16d9e-108">Базовый массив нового массива.</span><span class="sxs-lookup"><span data-stu-id="16d9e-108">The base array of the new array.</span></span> <span data-ttu-id="16d9e-109">Используйте `JS_INVALID_REFERENCE` , если базовый массив отсутствует.</span><span class="sxs-lookup"><span data-stu-id="16d9e-109">Use `JS_INVALID_REFERENCE` if no base array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="16d9e-110">Смещение в байтах от начала `baseArray` ( `ArrayBuffer` ) для массива с типом результата, на который должна указывать ссылка.</span><span class="sxs-lookup"><span data-stu-id="16d9e-110">The offset in bytes from the start of `baseArray` (`ArrayBuffer`) for result typed array to reference.</span></span> <span data-ttu-id="16d9e-111">Применимо только `baseArray` в том случае, если `ArrayBuffer` объект является объектом.</span><span class="sxs-lookup"><span data-stu-id="16d9e-111">Only applicable when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="16d9e-112">В противном случае оно должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="16d9e-112">Must be 0 otherwise.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="16d9e-113">Количество элементов в массиве.</span><span class="sxs-lookup"><span data-stu-id="16d9e-113">The number of elements in the array.</span></span> <span data-ttu-id="16d9e-114">Применимо только в том случае, если вы создаете новый типизированный массив без `baseArray` ( `baseArray` — `JS_INVALID_REFERENCE` ) или когда `baseArray` — `ArrayBuffer` объект.</span><span class="sxs-lookup"><span data-stu-id="16d9e-114">Only applicable when creating a new typed array without `baseArray` (`baseArray` is `JS_INVALID_REFERENCE`) or when `baseArray` is an `ArrayBuffer` object.</span></span> <span data-ttu-id="16d9e-115">В противном случае оно должно быть равно 0.</span><span class="sxs-lookup"><span data-stu-id="16d9e-115">Must be 0 otherwise.</span></span>  
  
 `result`  
 <span data-ttu-id="16d9e-116">Новый объект типизированного массива.</span><span class="sxs-lookup"><span data-stu-id="16d9e-116">The new typed array object.</span></span>  
  
## <span data-ttu-id="16d9e-117">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="16d9e-117">Return Value</span></span>  
 <span data-ttu-id="16d9e-118">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="16d9e-118">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="16d9e-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16d9e-119">Remarks</span></span>  
 <span data-ttu-id="16d9e-120">Это `baseArray` может быть `ArrayBuffer` , другой типизированный массив или JavaScript `Array` .</span><span class="sxs-lookup"><span data-stu-id="16d9e-120">The `baseArray` can be an `ArrayBuffer`, another typed array, or a JavaScript `Array`.</span></span> <span data-ttu-id="16d9e-121">Возвращаемый типизированный массив будет использовать массив в том `baseArray` случае, если он является `ArrayBuffer` , или, в противном случае, создать и использовать копию нижележащего исходного массива.</span><span class="sxs-lookup"><span data-stu-id="16d9e-121">The returned typed array will use the `baseArray` if it is an `ArrayBuffer`, or otherwise create and use a copy of the underlying source array.</span></span>  
  
 <span data-ttu-id="16d9e-122">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="16d9e-122">Requires an active script context.</span></span>  
  
 <span data-ttu-id="16d9e-123">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="16d9e-123">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="16d9e-124">Требования</span><span class="sxs-lookup"><span data-stu-id="16d9e-124">Requirements</span></span>  
 <span data-ttu-id="16d9e-125">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="16d9e-125">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="16d9e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="16d9e-126">See Also</span></span>  
 [<span data-ttu-id="16d9e-127">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="16d9e-127">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)