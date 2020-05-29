---
description: Обратный вызов финализатора.
title: JsFinalizeCallback typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: aa7a0269-b9d4-4717-97ac-8da7eb6ced15
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d2ee2c2c11e85094010cd15be59aa7ac587b614f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572533"
---
# <span data-ttu-id="580f0-103">JsFinalizeCallback typedef</span><span class="sxs-lookup"><span data-stu-id="580f0-103">JsFinalizeCallback Typedef</span></span>
<span data-ttu-id="580f0-104">Обратный вызов финализатора.</span><span class="sxs-lookup"><span data-stu-id="580f0-104">A finalizer callback.</span></span>  
  
## <span data-ttu-id="580f0-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="580f0-105">Syntax</span></span>  
  
```cpp  
typedef void (CALLBACK *JsFinalizeCallback)(  
   _In_opt_ void *data  
);  
```  
  
#### <span data-ttu-id="580f0-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="580f0-106">Parameters</span></span>  
 <span data-ttu-id="580f0-107">data</span><span class="sxs-lookup"><span data-stu-id="580f0-107">data</span></span>  
 <span data-ttu-id="580f0-108">Внешние данные, которые были переданы при создании финализации объекта.</span><span class="sxs-lookup"><span data-stu-id="580f0-108">The external data that was passed in when creating the object being finalized.</span></span>  
  
## <span data-ttu-id="580f0-109">Требования</span><span class="sxs-lookup"><span data-stu-id="580f0-109">Requirements</span></span>  
 <span data-ttu-id="580f0-110">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="580f0-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="580f0-111">См. также</span><span class="sxs-lookup"><span data-stu-id="580f0-111">See Also</span></span>  
 [<span data-ttu-id="580f0-112">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="580f0-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)