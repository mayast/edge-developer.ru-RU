---
description: Определяет, имеет ли объект индексированные свойства во внешних данных.
title: Функция JsHasIndexedPropertiesExternalData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: c676db20-3ef1-4f84-8b26-3e06fe0ab2bf
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c7f9f87b19016b3d837b637219eec936a11211e9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572500"
---
# <span data-ttu-id="28789-103">Функция JsHasIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="28789-103">JsHasIndexedPropertiesExternalData Function</span></span>
<span data-ttu-id="28789-104">Определяет, имеет ли объект индексированные свойства во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="28789-104">Determines whether an object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="28789-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="28789-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsHasIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ bool* value  
);  
```  
  
#### <span data-ttu-id="28789-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="28789-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="28789-107">Объект.</span><span class="sxs-lookup"><span data-stu-id="28789-107">The object.</span></span>  
  
 `value`  
 <span data-ttu-id="28789-108">Имеет ли объект индексированные свойства во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="28789-108">Whether the object has its indexed properties in external data.</span></span>  
  
## <span data-ttu-id="28789-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="28789-109">Return Value</span></span>  
 <span data-ttu-id="28789-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="28789-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="28789-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="28789-111">Remarks</span></span>  
 <span data-ttu-id="28789-112">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="28789-112">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="28789-113">Требования</span><span class="sxs-lookup"><span data-stu-id="28789-113">Requirements</span></span>  
 <span data-ttu-id="28789-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="28789-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="28789-115">См. также</span><span class="sxs-lookup"><span data-stu-id="28789-115">See Also</span></span>  
 [<span data-ttu-id="28789-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="28789-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)