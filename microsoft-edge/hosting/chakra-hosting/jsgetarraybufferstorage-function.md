---
description: Получение основного хранилища памяти, используемого в ArrayBuffer.
title: Функция JsGetArrayBufferStorage | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 712ae298-36a9-47ef-b089-e51835c056bc
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e8d265f3e81015ba9f5d0547b6b1c7246c23ce5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572531"
---
# <span data-ttu-id="fe2b2-103">Функция JsGetArrayBufferStorage</span><span class="sxs-lookup"><span data-stu-id="fe2b2-103">JsGetArrayBufferStorage Function</span></span>
<span data-ttu-id="fe2b2-104">Получение основного хранилища памяти, используемого в `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="fe2b2-104">Obtains the underlying memory storage used by an `ArrayBuffer`.</span></span>  
  
## <span data-ttu-id="fe2b2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fe2b2-105">Syntax</span></span>  
  
```cpp  
JsErrorCode STDAPI_ JsGetArrayBufferStorage(  
   _In_ JsValueRef arrayBuffer,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="fe2b2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fe2b2-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="fe2b2-107">Экземпляр ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="fe2b2-107">The ArrayBuffer instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="fe2b2-108">Буфер ArrayBuffer.</span><span class="sxs-lookup"><span data-stu-id="fe2b2-108">The ArrayBuffer's buffer.</span></span> <span data-ttu-id="fe2b2-109">Время существования возвращаемого буфера совпадает со сроком существования `ArrayBuffer` .</span><span class="sxs-lookup"><span data-stu-id="fe2b2-109">The lifetime of the buffer returned is the same as the lifetime of the `ArrayBuffer`.</span></span> <span data-ttu-id="fe2b2-110">Указатель буфера не считается ссылкой на объект в `ArrayBuffer` целях сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="fe2b2-110">The buffer pointer does not count as a reference to the `ArrayBuffer` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="fe2b2-111">Количество байтов в буфере.</span><span class="sxs-lookup"><span data-stu-id="fe2b2-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="fe2b2-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="fe2b2-112">Return Value</span></span>  
 <span data-ttu-id="fe2b2-113">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fe2b2-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="fe2b2-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fe2b2-114">Remarks</span></span>  
 <span data-ttu-id="fe2b2-115">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="fe2b2-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="fe2b2-116">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fe2b2-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="fe2b2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="fe2b2-117">Requirements</span></span>  
 <span data-ttu-id="fe2b2-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="fe2b2-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="fe2b2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="fe2b2-119">See Also</span></span>  
 [<span data-ttu-id="fe2b2-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="fe2b2-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)