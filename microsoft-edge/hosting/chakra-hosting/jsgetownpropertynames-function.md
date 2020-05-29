---
description: Получает список всех свойств объекта.
title: Функция JsGetOwnPropertyNames | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsGetOwnPropertyNames
helpviewer_keywords:
- JsGetOwnPropertyNames function
ms.assetid: 0c17ea06-b17f-4ea3-ad04-1259a4d1b6de
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 5355caab864724d72fdb2c7abb3dc70e39662b55
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572517"
---
# <span data-ttu-id="80c57-103">Функция JsGetOwnPropertyNames</span><span class="sxs-lookup"><span data-stu-id="80c57-103">JsGetOwnPropertyNames Function</span></span>
<span data-ttu-id="80c57-104">Получает список всех свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="80c57-104">Gets the list of all properties on the object.</span></span>  
  
## <span data-ttu-id="80c57-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="80c57-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetOwnPropertyNames(  
   _In_ JsValueRef object,  
   _Out_ JsValueRef *propertyNames  
);  
```  
  
#### <span data-ttu-id="80c57-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="80c57-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="80c57-107">Объект, из которого нужно получить имена свойств.</span><span class="sxs-lookup"><span data-stu-id="80c57-107">The object from which to get the property names.</span></span>  
  
 `propertyNames`  
 <span data-ttu-id="80c57-108">Массив имен свойств.</span><span class="sxs-lookup"><span data-stu-id="80c57-108">An array of property names.</span></span>  
  
## <span data-ttu-id="80c57-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="80c57-109">Return Value</span></span>  
 <span data-ttu-id="80c57-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="80c57-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="80c57-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="80c57-111">Remarks</span></span>  
 <span data-ttu-id="80c57-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="80c57-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="80c57-113">Требования</span><span class="sxs-lookup"><span data-stu-id="80c57-113">Requirements</span></span>  
 <span data-ttu-id="80c57-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="80c57-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="80c57-115">См. также</span><span class="sxs-lookup"><span data-stu-id="80c57-115">See Also</span></span>  
 [<span data-ttu-id="80c57-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="80c57-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)