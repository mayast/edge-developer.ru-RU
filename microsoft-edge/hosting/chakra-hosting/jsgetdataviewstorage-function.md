---
description: Получение основного хранилища памяти, используемого DataView.
title: Функция JsGetDataViewStorage | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 7c2180e0-51d5-4cc8-ad21-8bf29ff7c583
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 54f8a91b6dea1e0997ad31d6585ea741fde8ba99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571395"
---
# <span data-ttu-id="6b04f-103">Функция JsGetDataViewStorage</span><span class="sxs-lookup"><span data-stu-id="6b04f-103">JsGetDataViewStorage Function</span></span>
<span data-ttu-id="6b04f-104">Получение основного хранилища памяти, используемого в `DataView` .</span><span class="sxs-lookup"><span data-stu-id="6b04f-104">Obtains the underlying memory storage used by a `DataView`.</span></span>  
  
## <span data-ttu-id="6b04f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6b04f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetDataViewStorage(  
   _In_ JsValueRef dataView,  
   _Outptr_result_bytebuffer_(*bufferLength) BYTE **buffer,  
   _Out_ unsigned int *bufferLength  
);  
```  
  
#### <span data-ttu-id="6b04f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b04f-106">Parameters</span></span>  
 `dataView`  
 <span data-ttu-id="6b04f-107">Экземпляр объекта DataView.</span><span class="sxs-lookup"><span data-stu-id="6b04f-107">The DataView instance.</span></span>  
  
 `buffer`  
 <span data-ttu-id="6b04f-108">Буфер объекта DataView.</span><span class="sxs-lookup"><span data-stu-id="6b04f-108">The DataView's buffer.</span></span> <span data-ttu-id="6b04f-109">Время существования возвращаемого буфера совпадает со сроком существования `DataView` .</span><span class="sxs-lookup"><span data-stu-id="6b04f-109">The lifetime of the buffer returned is the same as the lifetime of the `DataView`.</span></span> <span data-ttu-id="6b04f-110">Указатель буфера не считается ссылкой на объект в `DataView` целях сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="6b04f-110">The buffer pointer does not count as a reference to the `DataView` for the purpose of garbage collection.</span></span>  
  
 `bufferLength`  
 <span data-ttu-id="6b04f-111">Количество байтов в буфере.</span><span class="sxs-lookup"><span data-stu-id="6b04f-111">The number of bytes in the buffer.</span></span>  
  
## <span data-ttu-id="6b04f-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="6b04f-112">Return Value</span></span>  
 <span data-ttu-id="6b04f-113">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6b04f-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="6b04f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6b04f-114">Remarks</span></span>  
 <span data-ttu-id="6b04f-115">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="6b04f-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="6b04f-116">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6b04f-116">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="6b04f-117">Требования</span><span class="sxs-lookup"><span data-stu-id="6b04f-117">Requirements</span></span>  
 <span data-ttu-id="6b04f-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="6b04f-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="6b04f-119">См. также</span><span class="sxs-lookup"><span data-stu-id="6b04f-119">See Also</span></span>  
 [<span data-ttu-id="6b04f-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="6b04f-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)