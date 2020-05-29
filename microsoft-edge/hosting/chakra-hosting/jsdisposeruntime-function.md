---
description: Уничтожает среду выполнения.
title: Функция JsDisposeRuntime | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDisposeRuntime
helpviewer_keywords:
- JsDisposeRuntime function
ms.assetid: 0aefde3f-7250-48be-afc5-53ea85c12f30
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 89166249616c265ce75ebc43a01c838d607bdd08
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572542"
---
# <span data-ttu-id="76eab-103">Функция JsDisposeRuntime</span><span class="sxs-lookup"><span data-stu-id="76eab-103">JsDisposeRuntime Function</span></span>
<span data-ttu-id="76eab-104">Уничтожает среду выполнения.</span><span class="sxs-lookup"><span data-stu-id="76eab-104">Disposes a runtime.</span></span>  
  
## <span data-ttu-id="76eab-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="76eab-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDisposeRuntime(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="76eab-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="76eab-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="76eab-107">Среда выполнения для удаления.</span><span class="sxs-lookup"><span data-stu-id="76eab-107">The runtime to dispose.</span></span>  
  
## <span data-ttu-id="76eab-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="76eab-108">Return Value</span></span>  
 <span data-ttu-id="76eab-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="76eab-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="76eab-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76eab-110">Remarks</span></span>  
 <span data-ttu-id="76eab-111">После удаления среды выполнения все ресурсы, которыми владеет она, недопустимы и не могут использоваться.</span><span class="sxs-lookup"><span data-stu-id="76eab-111">Once a runtime has been disposed, all resources owned by it are invalid and cannot be used.</span></span> <span data-ttu-id="76eab-112">Если среда выполнения активна (то есть она должна быть актуальной в конкретном потоке), она не может быть удалена.</span><span class="sxs-lookup"><span data-stu-id="76eab-112">If the runtime is active (i.e. it is set to be current on a particular thread), it cannot be disposed.</span></span>  
  
## <span data-ttu-id="76eab-113">Требования</span><span class="sxs-lookup"><span data-stu-id="76eab-113">Requirements</span></span>  
 <span data-ttu-id="76eab-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="76eab-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="76eab-115">См. также</span><span class="sxs-lookup"><span data-stu-id="76eab-115">See Also</span></span>  
 [<span data-ttu-id="76eab-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="76eab-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)