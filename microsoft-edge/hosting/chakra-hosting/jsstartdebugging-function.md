---
description: Запускает отладку в текущем контексте.
title: Функция JsStartDebugging | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsStartDebugging
helpviewer_keywords:
- JsStartDebugging function
ms.assetid: c48ba02d-6d47-466f-a970-02f087d525f3
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 2c94a6f36ad72bfb9354c85d98ae0b5b4e9c77fb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572340"
---
# <span data-ttu-id="08e54-103">Функция JsStartDebugging</span><span class="sxs-lookup"><span data-stu-id="08e54-103">JsStartDebugging Function</span></span>
<span data-ttu-id="08e54-104">Запускает отладку в текущем контексте.</span><span class="sxs-lookup"><span data-stu-id="08e54-104">Starts debugging in the current context.</span></span>  
  
## <span data-ttu-id="08e54-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="08e54-105">Syntax</span></span>  
  
```cpp  
// Microsoft Edge mode signature  
STDAPI_(JsErrorCode) JsStartDebugging();  
  
// Legacy mode signature  
STDAPI_(JsErrorCode)  JsStartDebugging(  
   _In_ IDebugApplication *debugApplication  
);  
```  
  
#### <span data-ttu-id="08e54-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="08e54-106">Parameters</span></span>  
 `debugApplication`  
 <span data-ttu-id="08e54-107">Отладочное приложение, используемое для отладки.</span><span class="sxs-lookup"><span data-stu-id="08e54-107">The debug application to use for debugging.</span></span>  
  
## <span data-ttu-id="08e54-108">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="08e54-108">Return Value</span></span>  
 <span data-ttu-id="08e54-109">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="08e54-109">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="08e54-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="08e54-110">Remarks</span></span>  
 <span data-ttu-id="08e54-111">`CoInitializeEx`Для использования этого API необходимо, чтобы узел вызывался по `COINIT_MULTITHREADED` `COINIT_APARTMENTTHREADED` крайней мере один раз.</span><span class="sxs-lookup"><span data-stu-id="08e54-111">The host should make sure that `CoInitializeEx` is called with `COINIT_MULTITHREADED` or `COINIT_APARTMENTTHREADED` at least once before using this API</span></span>  
  
 <span data-ttu-id="08e54-112">`debugApplication`В режиме Microsoft Edge этот параметр не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="08e54-112">The `debugApplication` parameter is not supported in Microsoft Edge mode.</span></span> <span data-ttu-id="08e54-113">Дополнительные сведения об использовании этого API в режиме Microsoft EDGE можно найти в разделе [назначение Microsoft EDGE и устаревших ядер](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span><span class="sxs-lookup"><span data-stu-id="08e54-113">For more information on using this API in Microsoft Edge mode, see [Targeting Microsoft Edge vs. Legacy Engines](../chakra-hosting/targeting-edge-vs-legacy-engines-in-jsrt-apis.md).</span></span>  
  
## <span data-ttu-id="08e54-114">Требования</span><span class="sxs-lookup"><span data-stu-id="08e54-114">Requirements</span></span>  
 <span data-ttu-id="08e54-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="08e54-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="08e54-116">См. также</span><span class="sxs-lookup"><span data-stu-id="08e54-116">See Also</span></span>  
 [<span data-ttu-id="08e54-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="08e54-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)