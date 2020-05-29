---
description: Анализирует сценарий и возвращает функцию, которая представляет сценарий.
title: Функция JsParseScript | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseScript
helpviewer_keywords:
- JsParseScript function
ms.assetid: e9d0e363-7cbe-43eb-9dc0-1f47e586c9ab
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: dd224ef0e800f05e6e07580f545bc4af218b3498
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572485"
---
# <span data-ttu-id="8c92b-103">Функция JsParseScript</span><span class="sxs-lookup"><span data-stu-id="8c92b-103">JsParseScript Function</span></span>
<span data-ttu-id="8c92b-104">Анализирует сценарий и возвращает функцию, которая представляет сценарий.</span><span class="sxs-lookup"><span data-stu-id="8c92b-104">Parses a script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="8c92b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8c92b-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="8c92b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8c92b-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="8c92b-107">Сценарий для синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="8c92b-107">The script to parse.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="8c92b-108">Объект cookie, определяющий сценарий, который можно использовать для контекстно-отлаженных сценариев.</span><span class="sxs-lookup"><span data-stu-id="8c92b-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="8c92b-109">Расположение, из которого получен сценарий.</span><span class="sxs-lookup"><span data-stu-id="8c92b-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="8c92b-110">Функция, представляющая код сценария.</span><span class="sxs-lookup"><span data-stu-id="8c92b-110">A function representing the script code.</span></span>  
  
## <span data-ttu-id="8c92b-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="8c92b-111">Return Value</span></span>  
 <span data-ttu-id="8c92b-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8c92b-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="8c92b-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8c92b-113">Remarks</span></span>  
 <span data-ttu-id="8c92b-114">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="8c92b-114">Requires an active script context.</span></span>  
  
## <span data-ttu-id="8c92b-115">Требования</span><span class="sxs-lookup"><span data-stu-id="8c92b-115">Requirements</span></span>  
 <span data-ttu-id="8c92b-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="8c92b-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="8c92b-117">См. также</span><span class="sxs-lookup"><span data-stu-id="8c92b-117">See Also</span></span>  
 [<span data-ttu-id="8c92b-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="8c92b-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)