---
description: Сравните два значения JavaScript на равенство.
title: Функция JsEquals | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEquals
helpviewer_keywords:
- JsEquals function
ms.assetid: 8377a7b6-12ff-43e4-8cc8-5a5a198a168b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 84416584a048512ab20754a3b59eb8ec255901c4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572535"
---
# <span data-ttu-id="90f93-103">Функция JsEquals</span><span class="sxs-lookup"><span data-stu-id="90f93-103">JsEquals Function</span></span>
<span data-ttu-id="90f93-104">Сравните два значения JavaScript на равенство.</span><span class="sxs-lookup"><span data-stu-id="90f93-104">Compare two JavaScript values for equality.</span></span>  
  
## <span data-ttu-id="90f93-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="90f93-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEquals(  
   _In_ JsValueRef object1,  
   _In_ JsValueRef object2,  
   _Out_ bool *result  
);  
```  
  
#### <span data-ttu-id="90f93-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="90f93-106">Parameters</span></span>  
 `object1`  
 <span data-ttu-id="90f93-107">Первый сравниваемый объект.</span><span class="sxs-lookup"><span data-stu-id="90f93-107">The first object to compare.</span></span>  
  
 `object2`  
 <span data-ttu-id="90f93-108">Второй сравниваемый объект.</span><span class="sxs-lookup"><span data-stu-id="90f93-108">The second object to compare.</span></span>  
  
 `result`  
 <span data-ttu-id="90f93-109">Равны ли значения.</span><span class="sxs-lookup"><span data-stu-id="90f93-109">Whether the values are equal.</span></span>  
  
## <span data-ttu-id="90f93-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="90f93-110">Return Value</span></span>  
 <span data-ttu-id="90f93-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="90f93-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="90f93-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="90f93-112">Remarks</span></span>  
 <span data-ttu-id="90f93-113">Эта функция эквивалентна `==` оператору в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="90f93-113">This function is equivalent to the `==` operator in Javascript.</span></span>  
  
 <span data-ttu-id="90f93-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="90f93-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="90f93-115">Требования</span><span class="sxs-lookup"><span data-stu-id="90f93-115">Requirements</span></span>  
 <span data-ttu-id="90f93-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="90f93-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="90f93-117">См. также</span><span class="sxs-lookup"><span data-stu-id="90f93-117">See Also</span></span>  
 [<span data-ttu-id="90f93-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="90f93-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)