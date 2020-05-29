---
description: Тип события обратного вызова выделения.
title: Перечисление JsMemoryEventType | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsMemoryEventType
helpviewer_keywords:
- JsMemoryEventType enumeration
ms.assetid: b4b176b6-b536-472e-8999-95b681a1df55
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1e9833777ed8fe5a19fd2a1487715296279f7351
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571353"
---
# <span data-ttu-id="f2a8c-103">Перечисление JsMemoryEventType</span><span class="sxs-lookup"><span data-stu-id="f2a8c-103">JsMemoryEventType Enumeration</span></span>
<span data-ttu-id="f2a8c-104">Тип события обратного вызова выделения.</span><span class="sxs-lookup"><span data-stu-id="f2a8c-104">Allocation callback event type.</span></span>  
  
## <span data-ttu-id="f2a8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f2a8c-105">Syntax</span></span>  
  
```cpp  
enum JsMemoryEventType;  
```  
  
## <span data-ttu-id="f2a8c-106">Участников</span><span class="sxs-lookup"><span data-stu-id="f2a8c-106">Members</span></span>  
  
### <span data-ttu-id="f2a8c-107">Данные</span><span class="sxs-lookup"><span data-stu-id="f2a8c-107">Values</span></span>  
  
|<span data-ttu-id="f2a8c-108">Имя</span><span class="sxs-lookup"><span data-stu-id="f2a8c-108">Name</span></span>|<span data-ttu-id="f2a8c-109">Описание</span><span class="sxs-lookup"><span data-stu-id="f2a8c-109">Description</span></span>|  
|----------|-----------------|  
|`JsMemoryAllocate`|<span data-ttu-id="f2a8c-110">Указывает на запрос выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="f2a8c-110">Indicates a request for memory allocation.</span></span>|  
|`JsMemoryFailure`|<span data-ttu-id="f2a8c-111">Указывает на сбой выделения.</span><span class="sxs-lookup"><span data-stu-id="f2a8c-111">Indicates a failed allocation event.</span></span>|  
|`JsMemoryFree`|<span data-ttu-id="f2a8c-112">Указывает на событие освобождения памяти.</span><span class="sxs-lookup"><span data-stu-id="f2a8c-112">Indicates a memory freeing event.</span></span>|  
  
## <span data-ttu-id="f2a8c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="f2a8c-113">Requirements</span></span>  
 <span data-ttu-id="f2a8c-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="f2a8c-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="f2a8c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="f2a8c-115">See Also</span></span>  
 [<span data-ttu-id="f2a8c-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="f2a8c-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)