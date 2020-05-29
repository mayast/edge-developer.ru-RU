---
description: Создает контекст сценария для выполнения сценариев.
title: Функция JsCreateContext | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsCreateContext
helpviewer_keywords:
- JsCreateContext function
ms.assetid: aceca043-2c73-4029-a06c-8ad6695109cf
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 06bd4c4780a8c7610ebc95cfc0da058306ce5b78
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571443"
---
# <span data-ttu-id="bf559-103">Функция JsCreateContext</span><span class="sxs-lookup"><span data-stu-id="bf559-103">JsCreateContext Function</span></span>
<span data-ttu-id="bf559-104">Создает контекст сценария для выполнения сценариев.</span><span class="sxs-lookup"><span data-stu-id="bf559-104">Creates a script context for running scripts.</span></span>  
  
## <span data-ttu-id="bf559-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bf559-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _Out_ JsContextRef *newContext);  
  
// Legacy mode signature  
STDAPI_(JsErrorCode) JsCreateContext(  
   _In_ JsRuntimeHandle runtime,  
   _In_ IDebugApplication *debugApplication,  
   _Out_ JsContextRef *newContext  
);  
```  
  
#### <span data-ttu-id="bf559-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf559-106">Parameters</span></span>  
 `runtime`  
 <span data-ttu-id="bf559-107">Среда выполнения, в которой создается контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="bf559-107">The runtime the script context is being created in.</span></span>  
  
 `debugApplication`  
 <span data-ttu-id="bf559-108">Отладочное приложение, используемое для отладки.</span><span class="sxs-lookup"><span data-stu-id="bf559-108">The debug application to use for debugging.</span></span> <span data-ttu-id="bf559-109">Этот параметр может иметь значение null, в этом случае отладка не включена для контекста.</span><span class="sxs-lookup"><span data-stu-id="bf559-109">This parameter can be null, in which case debugging is not enabled for the context.</span></span>  
  
 `newContext`  
 <span data-ttu-id="bf559-110">Созданный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="bf559-110">The created script context.</span></span>  
  
## <span data-ttu-id="bf559-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="bf559-111">Return Value</span></span>  
 <span data-ttu-id="bf559-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="bf559-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bf559-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bf559-113">Remarks</span></span>  
 <span data-ttu-id="bf559-114">Каждый контекст сценария имеет собственный глобальный объект, который изолирован от всех остальных контекстов сценария.</span><span class="sxs-lookup"><span data-stu-id="bf559-114">Each script context has its own global object that is isolated from all other script contexts.</span></span>  
  
 <span data-ttu-id="bf559-115">`debugApplication`В режиме Microsoft Edge этот параметр не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bf559-115">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="bf559-116">Дополнительные сведения об использовании этого API в режиме Microsoft EDGE можно найти в разделе [назначение Microsoft EDGE и устаревших ядер](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="bf559-116">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="bf559-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bf559-117">Requirements</span></span>  
 <span data-ttu-id="bf559-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bf559-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bf559-119">См. также</span><span class="sxs-lookup"><span data-stu-id="bf559-119">See Also</span></span>  
 [<span data-ttu-id="bf559-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bf559-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)