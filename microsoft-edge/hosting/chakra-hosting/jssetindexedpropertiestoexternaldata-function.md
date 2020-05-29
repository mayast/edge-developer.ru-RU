---
description: Задает для индексированных свойств объекта внешние данные. Внешние данные будут использоваться в качестве резервного хранилища для индексированных свойств объекта и доступны как типизированный массив.
title: Функция JsSetIndexedPropertiesToExternalData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: cee2d86d-ed42-4acb-86ef-95a67e63d0d6
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c1aed6e194b1dc1c35f403626a7b6c02a7752ffb
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572443"
---
# <span data-ttu-id="b8d76-104">Функция JsSetIndexedPropertiesToExternalData</span><span class="sxs-lookup"><span data-stu-id="b8d76-104">JsSetIndexedPropertiesToExternalData Function</span></span>
<span data-ttu-id="b8d76-105">Задает для индексированных свойств объекта внешние данные.</span><span class="sxs-lookup"><span data-stu-id="b8d76-105">Sets an object's indexed properties to external data.</span></span> <span data-ttu-id="b8d76-106">Внешние данные будут использоваться в качестве резервного хранилища для индексированных свойств объекта и доступны как типизированный массив.</span><span class="sxs-lookup"><span data-stu-id="b8d76-106">The external data will be used as back store for the object's indexed properties and accessed like a typed array.</span></span>  
  
## <span data-ttu-id="b8d76-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b8d76-107">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSetIndexedPropertiesToExternalData(  
   _In_ JsValueRef object,  
   _In_ void* data,  
   _In_ JsTypedArrayType arrayType,  
   _In_ unsigned int elementLength  
);  
```  
  
#### <span data-ttu-id="b8d76-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8d76-108">Parameters</span></span>  
 `object`  
 <span data-ttu-id="b8d76-109">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="b8d76-109">The object to operate on.</span></span>  
  
 `data`  
 <span data-ttu-id="b8d76-110">Внешние данные, которые будут использоваться в качестве резервного хранилища для индексированных свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="b8d76-110">The external data to be used as back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="b8d76-111">Тип элемента массива во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="b8d76-111">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="b8d76-112">Количество элементов массива во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="b8d76-112">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="b8d76-113">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="b8d76-113">Return Value</span></span>  
 <span data-ttu-id="b8d76-114">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b8d76-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b8d76-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b8d76-115">Remarks</span></span>  
 <span data-ttu-id="b8d76-116">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="b8d76-116">Requires an active script context.</span></span>  
  
 <span data-ttu-id="b8d76-117">Этот API поддерживается только в режиме EdgeHTML.</span><span class="sxs-lookup"><span data-stu-id="b8d76-117">This API is supported only in EdgeHTML mode.</span></span>  
  
## <span data-ttu-id="b8d76-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b8d76-118">Requirements</span></span>  
 <span data-ttu-id="b8d76-119">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b8d76-119">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b8d76-120">См. также</span><span class="sxs-lookup"><span data-stu-id="b8d76-120">See Also</span></span>  
 [<span data-ttu-id="b8d76-121">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b8d76-121">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)