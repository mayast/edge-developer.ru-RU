---
description: Освобождает ссылку на объект, собранный сборщиком мусора.
title: Функция JsRelease | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRelease
helpviewer_keywords:
- JsRelease function
ms.assetid: 8714fd0b-5b66-48e0-927e-7b93af6cde7b
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 134ba16509b6c2f0c232214d7efba4d8c8915d43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572473"
---
# <span data-ttu-id="db260-103">Функция JsRelease</span><span class="sxs-lookup"><span data-stu-id="db260-103">JsRelease Function</span></span>
<span data-ttu-id="db260-104">Освобождает ссылку на объект, собранный сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="db260-104">Releases a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="db260-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="db260-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRelease(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="db260-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="db260-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="db260-107">Объект, к которому нужно добавить ссылку.</span><span class="sxs-lookup"><span data-stu-id="db260-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="db260-108">Новая функция счетчика ссылок объекта (может передавать значение null).</span><span class="sxs-lookup"><span data-stu-id="db260-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="db260-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="db260-109">Return Value</span></span>  
 <span data-ttu-id="db260-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="db260-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="db260-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="db260-111">Remarks</span></span>  
 <span data-ttu-id="db260-112">Удаляет ссылку на `JsRef` созданный маркер `JsAddRef` .</span><span class="sxs-lookup"><span data-stu-id="db260-112">Removes a reference to a `JsRef` handle that was created by `JsAddRef`.</span></span>  
  
## <span data-ttu-id="db260-113">Требования</span><span class="sxs-lookup"><span data-stu-id="db260-113">Requirements</span></span>  
 <span data-ttu-id="db260-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="db260-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="db260-115">См. также</span><span class="sxs-lookup"><span data-stu-id="db260-115">See Also</span></span>  
 [<span data-ttu-id="db260-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="db260-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)