---
description: Указывает среде выполнения, что она должна выполнить все необходимые действия.
title: Функция JsIdle | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIdle
helpviewer_keywords:
- JsIdle function
ms.assetid: 372d1c62-8e19-4886-aa33-364cabc09bba
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 4da7148bf7daa3db983ab8f5bba622bfe0b19466
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572492"
---
# <span data-ttu-id="e710a-103">Функция JsIdle</span><span class="sxs-lookup"><span data-stu-id="e710a-103">JsIdle Function</span></span>
<span data-ttu-id="e710a-104">Указывает среде выполнения, что она должна выполнить все необходимые действия.</span><span class="sxs-lookup"><span data-stu-id="e710a-104">Tells the runtime to do any idle processing it need to do.</span></span>  
  
## <span data-ttu-id="e710a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e710a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIdle(  
   _Out_opt_ unsigned int *nextIdleTick  
);  
```  
  
#### <span data-ttu-id="e710a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e710a-106">Parameters</span></span>  
 `nextIdleTick`  
 <span data-ttu-id="e710a-107">Следующий системный Квант, если у вас есть больше времени на работу.</span><span class="sxs-lookup"><span data-stu-id="e710a-107">The next system tick when there will be more idle work to do.</span></span> <span data-ttu-id="e710a-108">Может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="e710a-108">Can be null.</span></span> <span data-ttu-id="e710a-109">Возвращает максимальное количество тактов в случае отсутствия предстоящих усилий.</span><span class="sxs-lookup"><span data-stu-id="e710a-109">Returns the maximum number of ticks if there no upcoming idle work to do.</span></span>  
  
## <span data-ttu-id="e710a-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="e710a-110">Return Value</span></span>  
 <span data-ttu-id="e710a-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e710a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="e710a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e710a-112">Remarks</span></span>  
 <span data-ttu-id="e710a-113">Если для текущей среды выполнения включена обработка простаивающих ресурсов, при звонке `JsIdle` сообщается о текущей среде выполнения, когда узел бездействует и что среда выполнения может выполнять задачи по очистке памяти.</span><span class="sxs-lookup"><span data-stu-id="e710a-113">If idle processing has been enabled for the current runtime, calling `JsIdle` will inform the current runtime that the host is idle and that the runtime can perform memory cleanup tasks.</span></span>  
  
 `JsIdle` <span data-ttu-id="e710a-114">также может возвращать число системных тактов, пока не будет более простой работы, чтобы среда выполнения работала.</span><span class="sxs-lookup"><span data-stu-id="e710a-114">can also return the number of system ticks until there will be more idle work for the runtime to do.</span></span> <span data-ttu-id="e710a-115">Вызов `JsIdle` до того, как это число тактов пройдет, не будет работать.</span><span class="sxs-lookup"><span data-stu-id="e710a-115">Calling `JsIdle` before this number of ticks has passed will do no work.</span></span>  
  
 <span data-ttu-id="e710a-116">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="e710a-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="e710a-117">Требования</span><span class="sxs-lookup"><span data-stu-id="e710a-117">Requirements</span></span>  
 <span data-ttu-id="e710a-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="e710a-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="e710a-119">См. также</span><span class="sxs-lookup"><span data-stu-id="e710a-119">See Also</span></span>  
 [<span data-ttu-id="e710a-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="e710a-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)