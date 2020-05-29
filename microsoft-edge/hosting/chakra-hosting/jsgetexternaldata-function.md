---
description: Извлекает данные из внешнего объекта.
title: Функция JsGetExternalData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetExternalData
helpviewer_keywords:
- JsGetExternalData function
ms.assetid: 1919e1da-3ea7-4269-a5fb-a3be06bd029b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 469d28d47f89b06897e4b72d081baad34eb92a6c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571393"
---
# <span data-ttu-id="e1391-103">Функция JsGetExternalData</span><span class="sxs-lookup"><span data-stu-id="e1391-103">JsGetExternalData Function</span></span>
<span data-ttu-id="e1391-104">Извлекает данные из внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="e1391-104">Retrieves the data from an external object.</span></span>  
  
## <span data-ttu-id="e1391-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1391-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetExternalData(  
   _In_ JsValueRef object,  
   _Out_ void **externalData  
);  
```  
  
#### <span data-ttu-id="e1391-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e1391-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="e1391-107">Внешний объект.</span><span class="sxs-lookup"><span data-stu-id="e1391-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="e1391-108">Внешние данные, хранящиеся в объекте.</span><span class="sxs-lookup"><span data-stu-id="e1391-108">The external data stored in the object.</span></span> <span data-ttu-id="e1391-109">Может иметь значение null, если в объекте не хранятся внешние данные.</span><span class="sxs-lookup"><span data-stu-id="e1391-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="e1391-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e1391-110">Return Value</span></span>  
 <span data-ttu-id="e1391-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e1391-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e1391-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1391-112">Remarks</span></span>  
 <span data-ttu-id="e1391-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="e1391-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e1391-114">Требования</span><span class="sxs-lookup"><span data-stu-id="e1391-114">Requirements</span></span>  
 <span data-ttu-id="e1391-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e1391-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e1391-116">См. также</span><span class="sxs-lookup"><span data-stu-id="e1391-116">See Also</span></span>  
 [<span data-ttu-id="e1391-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e1391-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)