---
description: Получает имя, связанное с ИДЕНТИФИКАТОРом свойства.
title: Функция JsGetPropertyNameFromId | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetPropertyNameFromId
helpviewer_keywords:
- JsGetPropertyNameFromId function
ms.assetid: b4ca442c-573d-4bc3-adf7-1b8d48480b3a
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e76c69c1d746302bb95cd7229872845c4fbcc88
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571384"
---
# <span data-ttu-id="afed4-103">Функция JsGetPropertyNameFromId</span><span class="sxs-lookup"><span data-stu-id="afed4-103">JsGetPropertyNameFromId Function</span></span>
<span data-ttu-id="afed4-104">Получает имя, связанное с ИДЕНТИФИКАТОРом свойства.</span><span class="sxs-lookup"><span data-stu-id="afed4-104">Gets the name associated with the property ID.</span></span>  
  
## <span data-ttu-id="afed4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="afed4-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetPropertyNameFromId(  
   _In_ JsPropertyIdRef propertyId,  
   _Outptr_result_z_ const wchar_t **name  
);  
```  
  
#### <span data-ttu-id="afed4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="afed4-106">Parameters</span></span>  
 `propertyId`  
 <span data-ttu-id="afed4-107">Идентификатор свойства, для которого нужно получить имя.</span><span class="sxs-lookup"><span data-stu-id="afed4-107">The property ID to get the name of.</span></span>  
  
 `name`  
 <span data-ttu-id="afed4-108">Имя, связанное с ИДЕНТИФИКАТОРом свойства.</span><span class="sxs-lookup"><span data-stu-id="afed4-108">The name associated with the property ID.</span></span>  
  
## <span data-ttu-id="afed4-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="afed4-109">Return Value</span></span>  
 <span data-ttu-id="afed4-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="afed4-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="afed4-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="afed4-111">Remarks</span></span>  
 <span data-ttu-id="afed4-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="afed4-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="afed4-113">Возвращенный буфер действителен, пока среда выполнения активна и не может использоваться после удаления среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="afed4-113">The returned buffer is valid as long as the runtime is alive and cannot be used once the runtime has been disposed.</span></span>  
  
## <span data-ttu-id="afed4-114">Требования</span><span class="sxs-lookup"><span data-stu-id="afed4-114">Requirements</span></span>  
 <span data-ttu-id="afed4-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="afed4-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="afed4-116">См. также</span><span class="sxs-lookup"><span data-stu-id="afed4-116">See Also</span></span>  
 [<span data-ttu-id="afed4-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="afed4-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)