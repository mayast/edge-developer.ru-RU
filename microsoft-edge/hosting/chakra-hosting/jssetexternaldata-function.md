---
description: Задает внешние данные для внешнего объекта.
title: Функция JsSetExternalData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSetExternalData
helpviewer_keywords:
- JsSetExternalData function
ms.assetid: 94e0ad34-67d7-4f7f-88a3-3b057ef5e4b9
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: cc638905786a1baa0a3d5f79bfa3792a764f358f
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572446"
---
# <span data-ttu-id="39a1a-103">Функция JsSetExternalData</span><span class="sxs-lookup"><span data-stu-id="39a1a-103">JsSetExternalData Function</span></span>
<span data-ttu-id="39a1a-104">Задает внешние данные для внешнего объекта.</span><span class="sxs-lookup"><span data-stu-id="39a1a-104">Sets the external data on an external object.</span></span>  
  
## <span data-ttu-id="39a1a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="39a1a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetExternalData(  
   _In_ JsValueRef object,  
   _In_opt_ void *externalData  
);  
```  
  
#### <span data-ttu-id="39a1a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="39a1a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="39a1a-107">Внешний объект.</span><span class="sxs-lookup"><span data-stu-id="39a1a-107">The external object.</span></span>  
  
 `externalData`  
 <span data-ttu-id="39a1a-108">Внешние данные, хранящиеся в объекте.</span><span class="sxs-lookup"><span data-stu-id="39a1a-108">The external data stored in the object.</span></span> <span data-ttu-id="39a1a-109">Может иметь значение null, если в объекте не хранятся внешние данные.</span><span class="sxs-lookup"><span data-stu-id="39a1a-109">Can be null if no external data is stored in the object.</span></span>  
  
## <span data-ttu-id="39a1a-110">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="39a1a-110">Return Value</span></span>  
 <span data-ttu-id="39a1a-111">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="39a1a-111">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="39a1a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="39a1a-112">Remarks</span></span>  
 <span data-ttu-id="39a1a-113">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="39a1a-113">Requires an active script context.</span></span>  
  
## <span data-ttu-id="39a1a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="39a1a-114">Requirements</span></span>  
 <span data-ttu-id="39a1a-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="39a1a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="39a1a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="39a1a-116">See Also</span></span>  
 [<span data-ttu-id="39a1a-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="39a1a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)