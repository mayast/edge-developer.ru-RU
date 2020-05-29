---
description: Возвращает значение, указывающее, отключено ли выполнение сценария в среде выполнения.
title: Функция JsIsRuntimeExecutionDisabled | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsIsRuntimeExecutionDisabled
helpviewer_keywords:
- JsIsRuntimeExecutionDisabled function
ms.assetid: 77490280-fb84-4614-a1f0-6ac31e3bd607
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6968a31c9acab70589fe58c86cc566e631778c3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571357"
---
# <span data-ttu-id="edf70-103">Функция JsIsRuntimeExecutionDisabled</span><span class="sxs-lookup"><span data-stu-id="edf70-103">JsIsRuntimeExecutionDisabled Function</span></span>
<span data-ttu-id="edf70-104">Возвращает значение, указывающее, отключено ли выполнение сценария в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="edf70-104">Returns a value that indicates whether script execution is disabled in the runtime.</span></span>  
  
## <span data-ttu-id="edf70-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="edf70-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsIsRuntimeExecutionDisabled(    _In_ JsRuntimeHandle runtime,    _Out_ bool *isDisabled);  
```  
  
#### <span data-ttu-id="edf70-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="edf70-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="edf70-107">Задает среду выполнения для проверки того, отключено ли выполнение.</span><span class="sxs-lookup"><span data-stu-id="edf70-107">Specifies the runtime to check if execution is disabled.</span></span>  
  
 `isDisabled`  
 `true` <span data-ttu-id="edf70-108">, если выполнение отключено, `false` в противном случае.</span><span class="sxs-lookup"><span data-stu-id="edf70-108">if execution is disabled, `false` otherwise.</span></span>  
  
## <span data-ttu-id="edf70-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="edf70-109">Return Value</span></span>  
 `JsNoError` <span data-ttu-id="edf70-110">Если операция выполнена успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="edf70-110">if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="edf70-111">Требования</span><span class="sxs-lookup"><span data-stu-id="edf70-111">Requirements</span></span>  
 <span data-ttu-id="edf70-112">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="edf70-112">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="edf70-113">См. также</span><span class="sxs-lookup"><span data-stu-id="edf70-113">See Also</span></span>  
 [<span data-ttu-id="edf70-114">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="edf70-114">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)