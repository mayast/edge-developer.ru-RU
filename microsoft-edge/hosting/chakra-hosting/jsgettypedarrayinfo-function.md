---
description: Получение часто используемых свойств типизированного массива.
title: Функция JsGetTypedArrayInfo | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 992bc4e9-3d06-4ad2-8b6b-88a437360f81
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 24046acc7118cd8f540ba8ceb9976368e93d51ff
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752271"
---
# <span data-ttu-id="03bf6-103">Функция JsGetTypedArrayInfo</span><span class="sxs-lookup"><span data-stu-id="03bf6-103">JsGetTypedArrayInfo Function</span></span>
<span data-ttu-id="03bf6-104">Получение часто используемых свойств типизированного массива.</span><span class="sxs-lookup"><span data-stu-id="03bf6-104">Obtains frequently used properties of a typed array.</span></span>  
  
## <span data-ttu-id="03bf6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="03bf6-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetTypedArrayInfo(  
  _In_ JsValueRef typedArray,  
  _Out_opt_ JsTypedArrayType *arrayType,  
  _Out_opt_ JsValueRef *arrayBuffer,  
  _Out_opt_ unsigned int *byteOffset,  
  _Out_opt_ unsigned int *byteLength  
);  
  
```  
  
#### <span data-ttu-id="03bf6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="03bf6-106">Parameters</span></span>  
 `typedArray`  
 <span data-ttu-id="03bf6-107">Экземпляр типизированного массива.</span><span class="sxs-lookup"><span data-stu-id="03bf6-107">The typed array instance.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="03bf6-108">Тип массива.</span><span class="sxs-lookup"><span data-stu-id="03bf6-108">The type of the array.</span></span>  
  
 `arrayBuffer`  
 <span data-ttu-id="03bf6-109">`ArrayBuffer`Восстановление массива.</span><span class="sxs-lookup"><span data-stu-id="03bf6-109">The `ArrayBuffer` backstore of the array.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="03bf6-110">Смещение в байтах от начала arrayBuffer, на которое ссылается массив.</span><span class="sxs-lookup"><span data-stu-id="03bf6-110">The offset in bytes from the start of arrayBuffer referenced by the array.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="03bf6-111">Число байтов в массиве.</span><span class="sxs-lookup"><span data-stu-id="03bf6-111">The number of bytes in the array.</span></span>  
  
## <span data-ttu-id="03bf6-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="03bf6-112">Return Value</span></span>  
 <span data-ttu-id="03bf6-113">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="03bf6-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="03bf6-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="03bf6-114">Remarks</span></span>  
 <span data-ttu-id="03bf6-115">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="03bf6-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="03bf6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="03bf6-116">Requirements</span></span>  
 <span data-ttu-id="03bf6-117">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="03bf6-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="03bf6-118">См. также</span><span class="sxs-lookup"><span data-stu-id="03bf6-118">See Also</span></span>  
 [<span data-ttu-id="03bf6-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="03bf6-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)