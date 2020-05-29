---
description: Пространство имен WinRT Project.
title: Функция JsProjectWinRTNamespace | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 8a23c154-df4b-4ce3-9fef-f41f90acdb87
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c4d63727b3d25bbb346fee7179ae0d942ae37008
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571340"
---
# <span data-ttu-id="d94f2-103">Функция JsProjectWinRTNamespace</span><span class="sxs-lookup"><span data-stu-id="d94f2-103">JsProjectWinRTNamespace Function</span></span>
<span data-ttu-id="d94f2-104">Пространство имен WinRT Project.</span><span class="sxs-lookup"><span data-stu-id="d94f2-104">Project a WinRT namespace.</span></span>  
  
## <span data-ttu-id="d94f2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d94f2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode)  
   JsProjectWinRTNamespace(  
   _In_z_ const wchar_t *namespaceName  
);  
```  
  
#### <span data-ttu-id="d94f2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d94f2-106">Parameters</span></span>  
 `namespaceName`  
 <span data-ttu-id="d94f2-107">Пространство имен WinRT для проецирования.</span><span class="sxs-lookup"><span data-stu-id="d94f2-107">The WinRT namespace to be projected.</span></span>  
  
## <span data-ttu-id="d94f2-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="d94f2-108">Return Value</span></span>  
 <span data-ttu-id="d94f2-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d94f2-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="d94f2-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d94f2-110">Remarks</span></span>  
 <span data-ttu-id="d94f2-111">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="d94f2-111">Requires an active script context.</span></span>  
  
 <span data-ttu-id="d94f2-112">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="d94f2-112">This API is supported only in EdgeHTML mode.</span></span>  
  
> [!NOTE]
>  <span data-ttu-id="d94f2-113">WinRT — это название платформы для универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="d94f2-113">WinRT was the platform name before Universal Windows Platform (UWP).</span></span>  
  
## <span data-ttu-id="d94f2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="d94f2-114">Requirements</span></span>  
 <span data-ttu-id="d94f2-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="d94f2-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="d94f2-116">См. также</span><span class="sxs-lookup"><span data-stu-id="d94f2-116">See Also</span></span>  
 [<span data-ttu-id="d94f2-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="d94f2-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)