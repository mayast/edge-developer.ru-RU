---
description: Задает внутренние данные JsrtContext.
title: Функция JsSetContextData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: be90aa6a-b001-4a6f-90c5-c2135e913be0
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: e874f500ca82328dddeaaa03a0b78a188b8fd241
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751935"
---
# <span data-ttu-id="e85e7-103">Функция JsSetContextData</span><span class="sxs-lookup"><span data-stu-id="e85e7-103">JsSetContextData Function</span></span>
<span data-ttu-id="e85e7-104">Задает внутренние данные JsrtContext.</span><span class="sxs-lookup"><span data-stu-id="e85e7-104">Sets the internal data of JsrtContext.</span></span>  
  
## <span data-ttu-id="e85e7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e85e7-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetContextData(  
  _In_ JsContextRef context,  
  _In_ void *data  
);  
  
```  
  
#### <span data-ttu-id="e85e7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e85e7-106">Parameters</span></span>  
 `context`  
 <span data-ttu-id="e85e7-107">Контекст, для которого необходимо установить данные.</span><span class="sxs-lookup"><span data-stu-id="e85e7-107">The context to set the data to.</span></span>  
  
 `data`  
 <span data-ttu-id="e85e7-108">Указатель на данные, которые нужно настроить.</span><span class="sxs-lookup"><span data-stu-id="e85e7-108">The pointer to the data to be set.</span></span>  
  
## <span data-ttu-id="e85e7-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e85e7-109">Return Value</span></span>  
 <span data-ttu-id="e85e7-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e85e7-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e85e7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e85e7-111">Remarks</span></span>  
 <span data-ttu-id="e85e7-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="e85e7-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e85e7-113">Требования</span><span class="sxs-lookup"><span data-stu-id="e85e7-113">Requirements</span></span>  
 <span data-ttu-id="e85e7-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e85e7-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e85e7-115">См. также</span><span class="sxs-lookup"><span data-stu-id="e85e7-115">See Also</span></span>  
 [<span data-ttu-id="e85e7-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e85e7-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)