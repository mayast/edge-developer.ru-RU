---
description: Обратный вызов функции.
title: JsNativeFunction typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 56ef6cdf-4ca9-4f7c-b953-e661addb1a8e
caps.latest.revision: 5
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c0b73a11d3a0b2ed0867ef001f3c29c5643132a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571354"
---
# <span data-ttu-id="53b05-103">JsNativeFunction typedef</span><span class="sxs-lookup"><span data-stu-id="53b05-103">JsNativeFunction Typedef</span></span>
<span data-ttu-id="53b05-104">Обратный вызов функции.</span><span class="sxs-lookup"><span data-stu-id="53b05-104">A function callback.</span></span>  
  
## <span data-ttu-id="53b05-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53b05-105">Syntax</span></span>  
  
```cpp  
typedef _Ret_maybenull_ JsValueRef (CALLBACK * JsNativeFunction)(  
   _In_ JsValueRef callee,  
   _In_ bool isConstructCall,  
   _In_ JsValueRef *arguments,  
   _In_ unsigned short argumentCount  
);  
```  
  
#### <span data-ttu-id="53b05-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53b05-106">Parameters</span></span>  
 <span data-ttu-id="53b05-107">Вызываемый абонент</span><span class="sxs-lookup"><span data-stu-id="53b05-107">callee</span></span>  
 <span data-ttu-id="53b05-108">`Function`Объект, представляющий вызываемую функцию.</span><span class="sxs-lookup"><span data-stu-id="53b05-108">A `Function` object that represents the function being invoked.</span></span>  
  
 <span data-ttu-id="53b05-109">isConstructCall</span><span class="sxs-lookup"><span data-stu-id="53b05-109">isConstructCall</span></span>  
 <span data-ttu-id="53b05-110">Показывает, является ли этот вызов регулярным или новым.</span><span class="sxs-lookup"><span data-stu-id="53b05-110">Indicates whether this is a regular call or a 'new' call.</span></span>  
  
 <span data-ttu-id="53b05-111">arguments</span><span class="sxs-lookup"><span data-stu-id="53b05-111">arguments</span></span>  
 <span data-ttu-id="53b05-112">Аргументы для вызова.</span><span class="sxs-lookup"><span data-stu-id="53b05-112">The arguments to the call.</span></span>  
  
 <span data-ttu-id="53b05-113">argumentCount</span><span class="sxs-lookup"><span data-stu-id="53b05-113">argumentCount</span></span>  
 <span data-ttu-id="53b05-114">Число аргументов.</span><span class="sxs-lookup"><span data-stu-id="53b05-114">The number of arguments.</span></span>  
  
## <span data-ttu-id="53b05-115">Значение свойства/возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53b05-115">Property Value/Return Value</span></span>  
 <span data-ttu-id="53b05-116">Результат звонка (если таковой имеется).</span><span class="sxs-lookup"><span data-stu-id="53b05-116">The result of the call, if any.</span></span>  
  
## <span data-ttu-id="53b05-117">Требования</span><span class="sxs-lookup"><span data-stu-id="53b05-117">Requirements</span></span>  
 <span data-ttu-id="53b05-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="53b05-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="53b05-119">См. также</span><span class="sxs-lookup"><span data-stu-id="53b05-119">See Also</span></span>  
 [<span data-ttu-id="53b05-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="53b05-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)