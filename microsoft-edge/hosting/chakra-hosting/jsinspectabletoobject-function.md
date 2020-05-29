---
description: Создает значение JavaScript, которое является проекцией переданного `IInspectable` указателя.
title: Функция JsInspectableToObject | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: dd0ad567-2ba8-4a63-bee4-2c6ff5ce9fa9
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 26ce17eb3abcefcf9a1f0cc773e9fe4c3aaf05cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571367"
---
# <span data-ttu-id="16fb3-103">Функция JsInspectableToObject</span><span class="sxs-lookup"><span data-stu-id="16fb3-103">JsInspectableToObject Function</span></span>
<span data-ttu-id="16fb3-104">Создает значение JavaScript, которое является проекцией переданного `IInspectable` указателя.</span><span class="sxs-lookup"><span data-stu-id="16fb3-104">Creates a JavaScript value that is a projection of the passed in `IInspectable` pointer.</span></span>  
  
## <span data-ttu-id="16fb3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16fb3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsInspectableToObject(  
        _In_ IInspectable  *inspectable,  
        _Out_ JsValueRef *value  
);  
```  
  
#### <span data-ttu-id="16fb3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="16fb3-106">Parameters</span></span>  
 `inspectable`  
 <span data-ttu-id="16fb3-107">`IInspectable`Для прогноза.</span><span class="sxs-lookup"><span data-stu-id="16fb3-107">A `IInspectable` to be projected.</span></span>  
  
 `value`  
 <span data-ttu-id="16fb3-108">Значение JavaScript, которое является проекцией `IInspectable` .</span><span class="sxs-lookup"><span data-stu-id="16fb3-108">A JavaScript value that is a projection of the `IInspectable`.</span></span>  
  
## <span data-ttu-id="16fb3-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="16fb3-109">Return Value</span></span>  
 <span data-ttu-id="16fb3-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="16fb3-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="16fb3-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16fb3-111">Remarks</span></span>  
 <span data-ttu-id="16fb3-112">Проецируемое значение может использоваться сценарием для вызова объекта WinRT.</span><span class="sxs-lookup"><span data-stu-id="16fb3-112">The projected value can be used by script to call a WinRT object.</span></span> <span data-ttu-id="16fb3-113">Узлы ответственны за принудительное использование правил COM Threading.</span><span class="sxs-lookup"><span data-stu-id="16fb3-113">Hosts are responsible for enforcing COM threading rules.</span></span>  
  
 <span data-ttu-id="16fb3-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="16fb3-114">Requires an active script context.</span></span>  
  
 <span data-ttu-id="16fb3-115">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="16fb3-115">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="16fb3-116">Требования</span><span class="sxs-lookup"><span data-stu-id="16fb3-116">Requirements</span></span>  
 <span data-ttu-id="16fb3-117">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="16fb3-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="16fb3-118">См. также</span><span class="sxs-lookup"><span data-stu-id="16fb3-118">See Also</span></span>  
 [<span data-ttu-id="16fb3-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="16fb3-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)