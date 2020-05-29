---
description: Создает значение JavaScript, которое является проекцией переданного `VARIANT` .
title: Функция JsVariantToValue | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsVariantToValue
helpviewer_keywords:
- JsVariantToValue function
ms.assetid: e8f9eb8b-55b3-4b65-927e-cad5b482edee
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 01796bc38548cf56b500731d899541ef214ec4e3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571325"
---
# <span data-ttu-id="cab41-103">Функция JsVariantToValue</span><span class="sxs-lookup"><span data-stu-id="cab41-103">JsVariantToValue Function</span></span>
<span data-ttu-id="cab41-104">Создает значение JavaScript, которое является проекцией переданного `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="cab41-104">Creates a JavaScript value that is a projection of the passed in `VARIANT`.</span></span>  
  
## <span data-ttu-id="cab41-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cab41-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsVariantToValue(  
   _In_ VARIANT *variant,  
   _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="cab41-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="cab41-106">Parameters</span></span>  
 `variant`  
 <span data-ttu-id="cab41-107">`VARIANT`Для прогноза.</span><span class="sxs-lookup"><span data-stu-id="cab41-107">A `VARIANT` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="cab41-108">Значение JavaScript, которое является проекцией `VARIANT` .</span><span class="sxs-lookup"><span data-stu-id="cab41-108">A JavaScript value that is a projection of the `VARIANT`.</span></span>  
  
## <span data-ttu-id="cab41-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="cab41-109">Return Value</span></span>  
 <span data-ttu-id="cab41-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="cab41-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="cab41-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cab41-111">Remarks</span></span>  
 <span data-ttu-id="cab41-112">Проецируемое значение может использоваться сценарием для вызова объекта автоматизации COM из сценария.</span><span class="sxs-lookup"><span data-stu-id="cab41-112">The projected value can be used by script to call a COM automation object from script.</span></span> <span data-ttu-id="cab41-113">Узлы ответственны за принудительное использование правил COM Threading.</span><span class="sxs-lookup"><span data-stu-id="cab41-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="cab41-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="cab41-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="cab41-115">Требования</span><span class="sxs-lookup"><span data-stu-id="cab41-115">Requirements</span></span>  
 <span data-ttu-id="cab41-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="cab41-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="cab41-117">См. также</span><span class="sxs-lookup"><span data-stu-id="cab41-117">See Also</span></span>  
 [<span data-ttu-id="cab41-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="cab41-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)