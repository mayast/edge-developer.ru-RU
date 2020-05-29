---
description: Анализирует сериализованный сценарий и возвращает функцию, которая представляет сценарий.
title: Функция JsParseSerializedScript | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsParseSerializedScript
helpviewer_keywords:
- JsParseSerializedScript function
ms.assetid: 40d0c7c4-fd5b-46ed-9e65-38c2db2fc859
caps.latest.revision: 13
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a778a007e69f15063d23cc55f999144ab55a306c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572484"
---
# <span data-ttu-id="9dba3-103">Функция JsParseSerializedScript</span><span class="sxs-lookup"><span data-stu-id="9dba3-103">JsParseSerializedScript Function</span></span>
<span data-ttu-id="9dba3-104">Анализирует сериализованный сценарий и возвращает функцию, которая представляет сценарий.</span><span class="sxs-lookup"><span data-stu-id="9dba3-104">Parses a serialized script and returns a function representing the script.</span></span>  
  
## <span data-ttu-id="9dba3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9dba3-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsParseSerializedScript(  
   _In_z_ const wchar_t *script,  
   _In_ BYTE *buffer,  
   _In_ JsSourceContext sourceContext,  
   _In_z_ const wchar_t *sourceUrl,  
   _Out_ JsValueRef *result  
);  
```  
  
#### <span data-ttu-id="9dba3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9dba3-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="9dba3-107">Сценарий для синтаксического анализа.</span><span class="sxs-lookup"><span data-stu-id="9dba3-107">The script to parse.</span></span>  
  
 `buffer`  
 <span data-ttu-id="9dba3-108">Сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="9dba3-108">The serialized script.</span></span>  
  
 `sourceContext`  
 <span data-ttu-id="9dba3-109">Объект cookie, определяющий сценарий, который можно использовать для контекстно-отлаженных сценариев.</span><span class="sxs-lookup"><span data-stu-id="9dba3-109">A cookie identifying the script that can be used by debuggable script contexts.</span></span>  
  
 `sourceUrl`  
 <span data-ttu-id="9dba3-110">Расположение, из которого получен сценарий.</span><span class="sxs-lookup"><span data-stu-id="9dba3-110">The location the script came from.</span></span>  
  
 `result`  
 <span data-ttu-id="9dba3-111">Функция, представляющая код сценария.</span><span class="sxs-lookup"><span data-stu-id="9dba3-111">A function representing the script code.</span></span>  
  
## <span data-ttu-id="9dba3-112">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="9dba3-112">Return Value</span></span>  
 <span data-ttu-id="9dba3-113">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9dba3-113">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="9dba3-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9dba3-114">Remarks</span></span>  
 <span data-ttu-id="9dba3-115">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="9dba3-115">Requires an active script context.</span></span>  
  
 <span data-ttu-id="9dba3-116">Буфер не сохраняется в памяти обработчиком сценариев, поэтому ваш код должен поддерживать его, пока он может использоваться для выполнения сценариев.</span><span class="sxs-lookup"><span data-stu-id="9dba3-116">The buffer is not persisted in memory by the scripting engine, so your code must keep it alive for as long as it might be used to execute scripts.</span></span>  
  
## <span data-ttu-id="9dba3-117">Требования</span><span class="sxs-lookup"><span data-stu-id="9dba3-117">Requirements</span></span>  
 <span data-ttu-id="9dba3-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="9dba3-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="9dba3-119">См. также</span><span class="sxs-lookup"><span data-stu-id="9dba3-119">See Also</span></span>  
 [<span data-ttu-id="9dba3-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="9dba3-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)