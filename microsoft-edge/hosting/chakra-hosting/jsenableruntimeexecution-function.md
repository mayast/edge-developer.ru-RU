---
description: 'Включает выполнение сценария в среде выполнения. '
title: Функция JsEnableRuntimeExecution | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsEnableRuntimeExecution
helpviewer_keywords:
- JsEnableRuntimeExecution function
ms.assetid: daa2036b-aef6-497d-a8ce-5a006b6ed13f
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd8071fd3c120d1c2029a3c7a3d9c39e68c4cfd2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572541"
---
# <span data-ttu-id="02202-103">Функция JsEnableRuntimeExecution</span><span class="sxs-lookup"><span data-stu-id="02202-103">JsEnableRuntimeExecution Function</span></span>
<span data-ttu-id="02202-104">Включает выполнение сценария в среде выполнения.</span><span class="sxs-lookup"><span data-stu-id="02202-104">Enables script execution in a runtime.</span></span>  
  
## <span data-ttu-id="02202-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="02202-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsEnableRuntimeExecution(  
   _In_ JsRuntimeHandle runtime  
);  
```  
  
#### <span data-ttu-id="02202-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="02202-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="02202-107">Среда выполнения, которая должна быть включена.</span><span class="sxs-lookup"><span data-stu-id="02202-107">The runtime to be enabled.</span></span>  
  
## <span data-ttu-id="02202-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="02202-108">Return Value</span></span>  
 <span data-ttu-id="02202-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="02202-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="02202-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="02202-110">Remarks</span></span>  
 <span data-ttu-id="02202-111">Включение выполнения сценария в среде выполнения, в которой уже включено выполнение сценария, — это No-Op.</span><span class="sxs-lookup"><span data-stu-id="02202-111">Enabling script execution in a runtime that already has script execution enabled is a no-op.</span></span>  
  
## <span data-ttu-id="02202-112">Требования</span><span class="sxs-lookup"><span data-stu-id="02202-112">Requirements</span></span>  
 <span data-ttu-id="02202-113">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="02202-113">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="02202-114">См. также</span><span class="sxs-lookup"><span data-stu-id="02202-114">See Also</span></span>  
 [<span data-ttu-id="02202-115">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="02202-115">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)