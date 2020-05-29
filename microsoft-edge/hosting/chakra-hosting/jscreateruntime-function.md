---
description: Создает новую среду выполнения.
title: Функция JsCreateRuntime | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateRuntime
helpviewer_keywords:
- JsCreateRuntime function
ms.assetid: 92d09b89-6593-4d73-a562-88f9fec10228
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d25c1b46354be1fda0ce906dc68c3643989fe2c6
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571423"
---
# <span data-ttu-id="2a183-103">Функция JsCreateRuntime</span><span class="sxs-lookup"><span data-stu-id="2a183-103">JsCreateRuntime Function</span></span>
<span data-ttu-id="2a183-104">Создает новую среду выполнения.</span><span class="sxs-lookup"><span data-stu-id="2a183-104">Creates a new runtime.</span></span>
  
## <span data-ttu-id="2a183-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2a183-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateRuntime(  
   _In_ JsRuntimeAttributes attributes,  
   _In_ JsRuntimeVersion version,  
   _In_opt_ JsThreadServiceCallback threadService,  
   _Out_ JsRuntimeHandle *runtime  
);  
```  
  
#### <span data-ttu-id="2a183-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a183-106">Parameters</span></span>  
 `attributes`  
 <span data-ttu-id="2a183-107">Атрибуты создаваемой среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="2a183-107">The attributes of the runtime to be created.</span></span>  
  
 `version`  
 <span data-ttu-id="2a183-108">Версия среды выполнения, которую нужно создать.</span><span class="sxs-lookup"><span data-stu-id="2a183-108">The version of the runtime to be created.</span></span>  
  
 `threadService`  
 <span data-ttu-id="2a183-109">Служба потока для среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="2a183-109">The thread service for the runtime.</span></span> <span data-ttu-id="2a183-110">Может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="2a183-110">Can be null.</span></span>  
  
 `runtime`  
 <span data-ttu-id="2a183-111">Среда выполнения создана.</span><span class="sxs-lookup"><span data-stu-id="2a183-111">The runtime created.</span></span>  
  
## <span data-ttu-id="2a183-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="2a183-112">Return Value</span></span>  
 <span data-ttu-id="2a183-113">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="2a183-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="2a183-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2a183-114">Remarks</span></span>  
 <span data-ttu-id="2a183-115">`version`В режиме Microsoft Edge этот параметр не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="2a183-115">The `version` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="2a183-116">Дополнительные сведения об использовании этого API в режиме Microsoft EDGE можно найти в разделе [назначение Microsoft EDGE и устаревших ядер](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="2a183-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="2a183-117">Требования</span><span class="sxs-lookup"><span data-stu-id="2a183-117">Requirements</span></span>  
 <span data-ttu-id="2a183-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="2a183-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="2a183-119">См. также</span><span class="sxs-lookup"><span data-stu-id="2a183-119">See Also</span></span>  
 [<span data-ttu-id="2a183-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="2a183-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)