---
description: Получение основного хранилища памяти, используемого типизированным массивом.
title: Функция JsGetTypedArrayStorage | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 52e4ac5f-cc71-456d-95de-a48f7327503d
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f03414d64fa819ac464217c8362d02e866d45296
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572511"
---
# <span data-ttu-id="01608-103">Функция JsGetTypedArrayStorage</span><span class="sxs-lookup"><span data-stu-id="01608-103">JsGetTypedArrayStorage Function</span></span>
<span data-ttu-id="01608-104">Получение основного хранилища памяти, используемого типизированным массивом.</span><span class="sxs-lookup"><span data-stu-id="01608-104">Obtains the underlying memory storage used by a typed array.</span></span>  
  
## <span data-ttu-id="01608-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="01608-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayStorage(  
   _In_ JsValueRef typedArray,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength,  
   _Out_opt_ JsTypedArrayType *arrayType,  
   _Out_opt_ int *elementSize  
);  
```  
  
#### <span data-ttu-id="01608-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="01608-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="01608-107">Экземпляр типизированного массива.</span><span class="sxs-lookup"><span data-stu-id="01608-107">The typed array instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="01608-108">Буфер массива.</span><span class="sxs-lookup"><span data-stu-id="01608-108">The array's buffer.</span></span> <span data-ttu-id="01608-109">Время существования возвращаемого буфера совпадает со временем существования массива.</span><span class="sxs-lookup"><span data-stu-id="01608-109">The lifetime of the buffer returned is the same as the lifetime of the array.</span></span> <span data-ttu-id="01608-110">Указатель буфера не будет считаться ссылкой на массив в целях сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="01608-110">The buffer pointer does not count as a reference to the array for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="01608-111">Количество байтов в буфере.</span><span class="sxs-lookup"><span data-stu-id="01608-111">The number of bytes in the buffer.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="01608-112">Тип массива.</span><span class="sxs-lookup"><span data-stu-id="01608-112">The type of the array.</span></span>  
  
 `elementSize`  
 <span data-ttu-id="01608-113">Размер элемента массива.</span><span class="sxs-lookup"><span data-stu-id="01608-113">The size of an element of the array.</span></span>  
  
## <span data-ttu-id="01608-114">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="01608-114">Return Value</span></span>  
 <span data-ttu-id="01608-115">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="01608-115">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="01608-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="01608-116">Remarks</span></span>  
 <span data-ttu-id="01608-117">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="01608-117">Requires an active script context.</span></span>  
  
 <span data-ttu-id="01608-118">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="01608-118">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="01608-119">Требования</span><span class="sxs-lookup"><span data-stu-id="01608-119">Requirements</span></span>  
 <span data-ttu-id="01608-120">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="01608-120">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="01608-121">См. также</span><span class="sxs-lookup"><span data-stu-id="01608-121">See Also</span></span>  
 [<span data-ttu-id="01608-122">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="01608-122">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)