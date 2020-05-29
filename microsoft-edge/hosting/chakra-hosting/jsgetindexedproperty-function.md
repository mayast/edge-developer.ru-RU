---
description: Получение значения по указанному индексу объекта.
title: Функция JsGetIndexedProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetIndexedProperty
helpviewer_keywords:
- JsGetIndexedProperty function
ms.assetid: f61ea388-0ae6-4a19-b3b5-75ed49a3f32d
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7bb048b841462e27604ab169c69e4c051209a67d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572520"
---
# <span data-ttu-id="68635-103">Функция JsGetIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="68635-103">JsGetIndexedProperty Function</span></span>
<span data-ttu-id="68635-104">Получение значения по указанному индексу объекта.</span><span class="sxs-lookup"><span data-stu-id="68635-104">Retrieve the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="68635-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="68635-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="68635-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="68635-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="68635-107">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="68635-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="68635-108">Индекс, который требуется извлечь.</span><span class="sxs-lookup"><span data-stu-id="68635-108">The index to retrieve.</span></span>  
  
 `result`  
 <span data-ttu-id="68635-109">Извлеченное значение.</span><span class="sxs-lookup"><span data-stu-id="68635-109">The retrieved value.</span></span>  
  
## <span data-ttu-id="68635-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="68635-110">Return Value</span></span>  
 <span data-ttu-id="68635-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="68635-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="68635-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="68635-112">Remarks</span></span>  
 <span data-ttu-id="68635-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="68635-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="68635-114">Требования</span><span class="sxs-lookup"><span data-stu-id="68635-114">Requirements</span></span>  
 <span data-ttu-id="68635-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="68635-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="68635-116">См. также</span><span class="sxs-lookup"><span data-stu-id="68635-116">See Also</span></span>  
 [<span data-ttu-id="68635-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="68635-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)