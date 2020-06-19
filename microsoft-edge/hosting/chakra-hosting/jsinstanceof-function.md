---
description: Выполняет `instanceof` проверку оператора JavaScript.
title: Функция JsInstanceOf | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 94399a62-b996-4fd2-82ce-1c26e7a4da08
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4d9bf2e4c3da9f83fdf7c0ef4e2c31df04670420
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10751977"
---
# <span data-ttu-id="43e4b-103">Функция JsInstanceOf</span><span class="sxs-lookup"><span data-stu-id="43e4b-103">JsInstanceOf Function</span></span>
<span data-ttu-id="43e4b-104">Выполняет `instanceof` проверку оператора JavaScript.</span><span class="sxs-lookup"><span data-stu-id="43e4b-104">Performs JavaScript `instanceof` operator test.</span></span>  
  
## <span data-ttu-id="43e4b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="43e4b-105">Syntax</span></span>  
  
```cpp  
JsInstanceOf(   
  _In_ JsValueRef object,  
  _In_ JsValueRef constructor,  
  _Out_ bool *result  
);  
  
```  
  
#### <span data-ttu-id="43e4b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="43e4b-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="43e4b-107">Проверяемый объект.</span><span class="sxs-lookup"><span data-stu-id="43e4b-107">The object to test.</span></span>  
  
 `constructor`  
 <span data-ttu-id="43e4b-108">Функция конструктора для проверки.</span><span class="sxs-lookup"><span data-stu-id="43e4b-108">The constructor function to test against.</span></span>  
  
 `result`  
 <span data-ttu-id="43e4b-109">Значение, определяющее, имеет ли instanceof конструктор Object.</span><span class="sxs-lookup"><span data-stu-id="43e4b-109">Whether the "object instanceof constructor" is true.</span></span>  
  
## <span data-ttu-id="43e4b-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="43e4b-110">Return Value</span></span>  
 <span data-ttu-id="43e4b-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="43e4b-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="43e4b-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43e4b-112">Remarks</span></span>  
 <span data-ttu-id="43e4b-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="43e4b-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="43e4b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="43e4b-114">Requirements</span></span>  
 <span data-ttu-id="43e4b-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="43e4b-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="43e4b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="43e4b-116">See Also</span></span>  
 [<span data-ttu-id="43e4b-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="43e4b-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)