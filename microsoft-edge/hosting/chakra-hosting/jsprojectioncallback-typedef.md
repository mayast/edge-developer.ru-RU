---
description: Обратный вызов JsRT, который должен вызываться с контекстом, передаваемым `JsProjectionEnqueueCallback` в нужном потоке.
title: JsProjectionCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 32f22d37-e57e-4196-b6cd-a3fc75bd0632
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: b30f9a7dc4671896eeacecbf58ef88f0383e9e7e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571345"
---
# <span data-ttu-id="3d2fc-103">JsProjectionCallback typedef</span><span class="sxs-lookup"><span data-stu-id="3d2fc-103">JsProjectionCallback Typedef</span></span>
<span data-ttu-id="3d2fc-104">Обратный вызов JsRT, который должен вызываться с контекстом, передаваемым `JsProjectionEnqueueCallback` в нужном потоке.</span><span class="sxs-lookup"><span data-stu-id="3d2fc-104">The JsRT callback which should be called with the context passed to `JsProjectionEnqueueCallback` on the correct thread.</span></span>  
  
## <span data-ttu-id="3d2fc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3d2fc-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsProjectionCallback)(  
  _In_ JsProjectionCallbackContext jsContext  
);  
```  
  
#### <span data-ttu-id="3d2fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d2fc-106">Parameters</span></span>  
 `jsContext`  
 <span data-ttu-id="3d2fc-107">Требуется вызов `JsSetProjectionEnqueueCallback` для приема обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="3d2fc-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
## <span data-ttu-id="3d2fc-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3d2fc-108">Remarks</span></span>  
 <span data-ttu-id="3d2fc-109">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="3d2fc-109">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="3d2fc-110">Требования</span><span class="sxs-lookup"><span data-stu-id="3d2fc-110">Requirements</span></span>  
 <span data-ttu-id="3d2fc-111">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="3d2fc-111">jsrt.h</span></span>  
  
## <span data-ttu-id="3d2fc-112">См. также</span><span class="sxs-lookup"><span data-stu-id="3d2fc-112">See Also</span></span>  
 [<span data-ttu-id="3d2fc-113">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="3d2fc-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)