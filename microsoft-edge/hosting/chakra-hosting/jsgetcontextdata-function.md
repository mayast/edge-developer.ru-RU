---
description: Получает внутренний комплект данных для JsrtContext.
title: Функция JsGetContextData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: f5d7e446-267a-4a80-a427-6e1b95a3391b
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd85ccbc4008897643ec3840e8cdeca3611a50c8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571402"
---
# <span data-ttu-id="a32ea-103">Функция JsGetContextData</span><span class="sxs-lookup"><span data-stu-id="a32ea-103">JsGetContextData Function</span></span>
<span data-ttu-id="a32ea-104">Получает внутренний комплект данных для JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="a32ea-104">Gets the internal data set on JsrtContext.</span></span>  
  
## <span data-ttu-id="a32ea-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a32ea-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetContextData(  
  _In_ JsContextRef context,  
  _Out_ void **data  
);  
```  
  
#### <span data-ttu-id="a32ea-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a32ea-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="a32ea-107">Контекст, из которого нужно получить данные.</span><span class="sxs-lookup"><span data-stu-id="a32ea-107">The context to get the data from.</span></span>  
  
 `data`  
 <span data-ttu-id="a32ea-108">Указатель на данные, в которые будут возвращены данные.</span><span class="sxs-lookup"><span data-stu-id="a32ea-108">The pointer to the data where data will be returned.</span></span>  
  
## <span data-ttu-id="a32ea-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a32ea-109">Return Value</span></span>  
 <span data-ttu-id="a32ea-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a32ea-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a32ea-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a32ea-111">Remarks</span></span>  
 <span data-ttu-id="a32ea-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="a32ea-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="a32ea-113">Требования</span><span class="sxs-lookup"><span data-stu-id="a32ea-113">Requirements</span></span>  
 <span data-ttu-id="a32ea-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a32ea-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a32ea-115">См. также</span><span class="sxs-lookup"><span data-stu-id="a32ea-115">See Also</span></span>  
 [<span data-ttu-id="a32ea-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a32ea-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)