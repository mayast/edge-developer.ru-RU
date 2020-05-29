---
description: Создает логическое значение из `bool` значения.
title: Функция JsBoolToBoolean | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsBoolToBoolean
helpviewer_keywords:
- JsBoolToBoolean function
ms.assetid: 24322ea3-0638-40a3-9b4c-fc912ebed3ff
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f795bdd02a2a21dc4a0c8948a76ef817d6e0fac6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571466"
---
# <span data-ttu-id="84660-103">Функция JsBoolToBoolean</span><span class="sxs-lookup"><span data-stu-id="84660-103">JsBoolToBoolean Function</span></span>
<span data-ttu-id="84660-104">Создает логическое значение из `bool` значения.</span><span class="sxs-lookup"><span data-stu-id="84660-104">Creates a Boolean value from a `bool` value.</span></span>  
  
## <span data-ttu-id="84660-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="84660-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode JsBoolToBoolean(  
   _In_ bool value,  
   _Out_ JsValueRef *booleanValue  
);  
```  
  
#### <span data-ttu-id="84660-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84660-106">Parameters</span></span>  
 `value`  
 <span data-ttu-id="84660-107">Преобразуемое значение.</span><span class="sxs-lookup"><span data-stu-id="84660-107">The value to be converted.</span></span>  
  
 `booleanValue`  
 <span data-ttu-id="84660-108">Преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="84660-108">The converted value.</span></span>  
  
## <span data-ttu-id="84660-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="84660-109">Return Value</span></span>  
 <span data-ttu-id="84660-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="84660-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="84660-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="84660-111">Remarks</span></span>  
 <span data-ttu-id="84660-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="84660-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="84660-113">Требования</span><span class="sxs-lookup"><span data-stu-id="84660-113">Requirements</span></span>  
 <span data-ttu-id="84660-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="84660-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="84660-115">См. также</span><span class="sxs-lookup"><span data-stu-id="84660-115">See Also</span></span>  
 [<span data-ttu-id="84660-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="84660-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)