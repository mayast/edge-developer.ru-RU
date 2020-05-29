---
description: Ссылка на контекст сценария.
title: JsContextRef typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8586bfcc-bb24-430d-a6f2-1a3b3e34ec2e
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 80e4b5034079f4f0d26da070bd209aa41bf3475f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571457"
---
# <span data-ttu-id="12ff6-103">JsContextRef typedef</span><span class="sxs-lookup"><span data-stu-id="12ff6-103">JsContextRef Typedef</span></span>
<span data-ttu-id="12ff6-104">Ссылка на контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="12ff6-104">A reference to a script context.</span></span>  
  
## <span data-ttu-id="12ff6-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="12ff6-105">Syntax</span></span>  
  
```cpp  
typedef JsRef JsContextRef;  
```  
  
## <span data-ttu-id="12ff6-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="12ff6-106">Remarks</span></span>  
 <span data-ttu-id="12ff6-107">Каждый контекст сценария имеет собственный глобальный объект, отличный от глобального объекта в других контекстах сценария.</span><span class="sxs-lookup"><span data-stu-id="12ff6-107">Each script context contains its own global object, distinct from the global object in other script contexts.</span></span>  
  
 <span data-ttu-id="12ff6-108">Для многих API размещения Chakra требуется контекст сценария "активный", который можно настроить с помощью `JsSetCurrentContext` .</span><span class="sxs-lookup"><span data-stu-id="12ff6-108">Many Chakra hosting APIs require an "active" script context, which can be set using `JsSetCurrentContext`.</span></span> <span data-ttu-id="12ff6-109">API размещения Chakra, для которых требуется задать текущий контекст, запомните о том, что они будут явно указаны в документации.</span><span class="sxs-lookup"><span data-stu-id="12ff6-109">Chakra hosting APIs that require a current context to be set will note that explicitly in their documentation.</span></span>  
  
## <span data-ttu-id="12ff6-110">Требования</span><span class="sxs-lookup"><span data-stu-id="12ff6-110">Requirements</span></span>  
 <span data-ttu-id="12ff6-111">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="12ff6-111">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="12ff6-112">См. также</span><span class="sxs-lookup"><span data-stu-id="12ff6-112">See Also</span></span>  
 [<span data-ttu-id="12ff6-113">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="12ff6-113">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)