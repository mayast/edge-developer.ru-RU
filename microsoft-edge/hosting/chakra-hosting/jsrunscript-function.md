---
description: Выполнение сценария.
title: Функция JsRunScript | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsRunScript
helpviewer_keywords:
- JsRunScript function
ms.assetid: 8d6b8c9a-af3a-4e21-a330-5a6b535423a3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 49a06e4e6ad0c04e124b76f31d38b2e362e03f99
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572471"
---
# <span data-ttu-id="ac393-103">Функция JsRunScript</span><span class="sxs-lookup"><span data-stu-id="ac393-103">JsRunScript Function</span></span>
<span data-ttu-id="ac393-104">Выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="ac393-104">Executes a script.</span></span>  
  
## <span data-ttu-id="ac393-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac393-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsRunScript(  
   _In_z_ const wchar_t *script,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="ac393-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac393-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="ac393-107">Сценарий, который необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="ac393-107">The script to run.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="ac393-108">Объект cookie, определяющий сценарий, который можно использовать для контекстно-отлаженных сценариев.</span><span class="sxs-lookup"><span data-stu-id="ac393-108">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="ac393-109">Расположение, из которого получен сценарий.</span><span class="sxs-lookup"><span data-stu-id="ac393-109">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="ac393-110">Результат сценария, если таковой имеется.</span><span class="sxs-lookup"><span data-stu-id="ac393-110">The result of the script, if any.</span></span> <span data-ttu-id="ac393-111">Этот параметр может быть равен null.</span><span class="sxs-lookup"><span data-stu-id="ac393-111">This parameter can be null.</span></span>  
  
## <span data-ttu-id="ac393-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="ac393-112">Return Value</span></span>  
 <span data-ttu-id="ac393-113">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ac393-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="ac393-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac393-114">Remarks</span></span>  
 <span data-ttu-id="ac393-115">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="ac393-115">Requires an active script context.</span></span>  
  
## <span data-ttu-id="ac393-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ac393-116">Requirements</span></span>  
 <span data-ttu-id="ac393-117">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="ac393-117">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="ac393-118">См. также</span><span class="sxs-lookup"><span data-stu-id="ac393-118">See Also</span></span>  
 [<span data-ttu-id="ac393-119">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="ac393-119">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)