---
description: Получение часто используемых свойств типизированного массива.
title: Функция JsGetTypedArrayInfo | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b33b0c515733864c1849a08aa2f8dc6e884c22ad
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571368"
---
# <span data-ttu-id="bfa0c-103">Функция JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="bfa0c-103">JsGetTypedArrayInfo Function</span></span>
<span data-ttu-id="bfa0c-104">Получение часто используемых свойств типизированного массива.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="bfa0c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bfa0c-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="bfa0c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bfa0c-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="bfa0c-107">Экземпляр типизированного массива.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="bfa0c-108">Тип массива.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="bfa0c-109">`ArrayBuffer`Восстановление массива.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="bfa0c-110">Смещение в байтах от начала arrayBuffer, на которое ссылается массив.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="bfa0c-111">Число байтов в массиве.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="bfa0c-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="bfa0c-112">Return Value</span></span>  
 <span data-ttu-id="bfa0c-113">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bfa0c-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfa0c-114">Remarks</span></span>  
 <span data-ttu-id="bfa0c-115">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="bfa0c-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bfa0c-116">Требования</span><span class="sxs-lookup"><span data-stu-id="bfa0c-116">Requirements</span></span>  
 <span data-ttu-id="bfa0c-117">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bfa0c-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bfa0c-118">См. также</span><span class="sxs-lookup"><span data-stu-id="bfa0c-118">See Also</span></span>  
 [<span data-ttu-id="bfa0c-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bfa0c-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)