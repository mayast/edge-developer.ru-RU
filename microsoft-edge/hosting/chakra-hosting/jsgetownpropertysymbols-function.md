---
description: Возвращает список всех свойств символа в объекте.
title: Функция JsGetOwnPropertySymbols | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 57c431e3-de0b-4ed0-b750-87a86448daff
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7a7f4e88986a45fbccfae0c53e92ff2e5313991
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572518"
---
# <span data-ttu-id="be89a-103">Функция JsGetOwnPropertySymbols</span><span class="sxs-lookup"><span data-stu-id="be89a-103">JsGetOwnPropertySymbols Function</span></span>
<span data-ttu-id="be89a-104">Возвращает список всех свойств символа в объекте.</span><span class="sxs-lookup"><span data-stu-id="be89a-104">Gets the list of all symbol properties on the object.</span></span>  
  
## <span data-ttu-id="be89a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="be89a-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertySymbols(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertySymbols  
);  
```  
  
#### <span data-ttu-id="be89a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="be89a-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="be89a-107">Объект, из которого нужно получить символы свойств.</span><span class="sxs-lookup"><span data-stu-id="be89a-107">The object from which to get the property symbols.</span></span>  
  
 `propertySymbols`  
 <span data-ttu-id="be89a-108">Массив символов свойств.</span><span class="sxs-lookup"><span data-stu-id="be89a-108">An array of property symbols.</span></span>  
  
## <span data-ttu-id="be89a-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="be89a-109">Return Value</span></span>  
 <span data-ttu-id="be89a-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="be89a-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="be89a-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="be89a-111">Remarks</span></span>  
 <span data-ttu-id="be89a-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="be89a-112">Requires an active script context.</span></span>  
  
 <span data-ttu-id="be89a-113">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="be89a-113">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="be89a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="be89a-114">Requirements</span></span>  
 <span data-ttu-id="be89a-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="be89a-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="be89a-116">См. также</span><span class="sxs-lookup"><span data-stu-id="be89a-116">See Also</span></span>  
 [<span data-ttu-id="be89a-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="be89a-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)