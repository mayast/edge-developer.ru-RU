---
description: Создает объект JavaScript `DataView` .
title: Функция JsCreateDataView | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 161e59eb-d429-46f7-9a38-bbf2149ccf44
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1bf237458e8561b7070e4f3f0d4a14050f028375
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571440"
---
# <span data-ttu-id="0abb1-103">Функция JsCreateDataView</span><span class="sxs-lookup"><span data-stu-id="0abb1-103">JsCreateDataView Function</span></span>
<span data-ttu-id="0abb1-104">Создает объект JavaScript `DataView` .</span><span class="sxs-lookup"><span data-stu-id="0abb1-104">Creates a Javascript `DataView` object.</span></span>  
  
## <span data-ttu-id="0abb1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0abb1-105">Syntax</span></span>  
  
```cpp  
JsErrorCode  JsCreateDataView(  
   _In_ JsValueRef arrayBuffer,  
   _In_ unsigned int byteOffset,  
   _In_ unsigned int byteLength,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="0abb1-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0abb1-106">Parameters</span></span>  
 `arrayBuffer`  
 <span data-ttu-id="0abb1-107">Существующий `ArrayBuffer` объект, который будет использоваться в качестве хранилища для `DataView` объекта результата.</span><span class="sxs-lookup"><span data-stu-id="0abb1-107">An existing `ArrayBuffer` object to use as the storage for the result `DataView` object.</span></span>  
  
 `byteOffset`  
 <span data-ttu-id="0abb1-108">Смещение в байтах от начала `arrayBuffer` результата `DataView` до ссылки.</span><span class="sxs-lookup"><span data-stu-id="0abb1-108">The offset in bytes from the start of `arrayBuffer` for result `DataView` to reference.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="0abb1-109">Количество байтов в ArrayBuffer для представления результатов для ссылки.</span><span class="sxs-lookup"><span data-stu-id="0abb1-109">The number of bytes in the ArrayBuffer for result DataView to reference.</span></span>  
  
 `result`  
 <span data-ttu-id="0abb1-110">Новый объект DataView.</span><span class="sxs-lookup"><span data-stu-id="0abb1-110">The new DataView object.</span></span>  
  
## <span data-ttu-id="0abb1-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="0abb1-111">Return Value</span></span>  
 <span data-ttu-id="0abb1-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0abb1-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="0abb1-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0abb1-113">Remarks</span></span>  
 <span data-ttu-id="0abb1-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="0abb1-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="0abb1-115">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="0abb1-115">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="0abb1-116">Требования</span><span class="sxs-lookup"><span data-stu-id="0abb1-116">Requirements</span></span>  
 <span data-ttu-id="0abb1-117">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="0abb1-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="0abb1-118">См. также</span><span class="sxs-lookup"><span data-stu-id="0abb1-118">See Also</span></span>  
 [<span data-ttu-id="0abb1-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="0abb1-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)