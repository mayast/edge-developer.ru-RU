---
description: Контекст, переданный в обратный вызов приложения, JsProjectionEnqueueCallback из JsRT и затем передаваемый обратно в JsRT в указанном обратном вызове, в `JsProjectionCallback` приложении в правильном потоке.
title: JsProjectionCallbackContext typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 50c705c5-664f-4a1a-92f6-4882fc718ab1
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 58d4c74da13ae0dd269f3c101bbf3d2b95e77732
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571346"
---
# <span data-ttu-id="5ccf1-103">JsProjectionCallbackContext typedef</span><span class="sxs-lookup"><span data-stu-id="5ccf1-103">JsProjectionCallbackContext Typedef</span></span>
<span data-ttu-id="5ccf1-104">Контекст, переданный в обратный вызов приложения, JsProjectionEnqueueCallback из JsRT и затем передаваемый обратно в JsRT в указанном обратном вызове, в `JsProjectionCallback` приложении в правильном потоке.</span><span class="sxs-lookup"><span data-stu-id="5ccf1-104">The context passed into application callback, JsProjectionEnqueueCallback, from JsRT and then passed back to JsRT in the provided callback, `JsProjectionCallback`, by the application on the correct thread.</span></span>  
  
## <span data-ttu-id="5ccf1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5ccf1-105">Syntax</span></span>  
  
```cpp  
typedef void *JsProjectionCallbackContext;  
```  
  
## <span data-ttu-id="5ccf1-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="5ccf1-106">Remarks</span></span>  
 <span data-ttu-id="5ccf1-107">Требуется вызов `JsSetProjectionEnqueueCallback` для приема обратных вызовов.</span><span class="sxs-lookup"><span data-stu-id="5ccf1-107">Requires calling `JsSetProjectionEnqueueCallback` to receive callbacks.</span></span>  
  
 <span data-ttu-id="5ccf1-108">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="5ccf1-108">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="5ccf1-109">Требования</span><span class="sxs-lookup"><span data-stu-id="5ccf1-109">Requirements</span></span>  
 <span data-ttu-id="5ccf1-110">jsrt. h</span><span class="sxs-lookup"><span data-stu-id="5ccf1-110">jsrt.h</span></span>  
  
## <span data-ttu-id="5ccf1-111">См. также</span><span class="sxs-lookup"><span data-stu-id="5ccf1-111">See Also</span></span>  
 [<span data-ttu-id="5ccf1-112">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="5ccf1-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)