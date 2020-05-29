---
description: Извлекает сведения о внешних данных индексированных свойств объекта.
title: Функция JsGetIndexedPropertiesExternalData | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 2c313163-3462-42fd-8dee-3dfb3ac7f43f
caps.latest.revision: 2
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 96fdcd4b6fe29ffc20a796983cc1de692c80a3f1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571387"
---
# <span data-ttu-id="aca01-103">Функция JsGetIndexedPropertiesExternalData</span><span class="sxs-lookup"><span data-stu-id="aca01-103">JsGetIndexedPropertiesExternalData Function</span></span>
<span data-ttu-id="aca01-104">Извлекает сведения о внешних данных индексированных свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="aca01-104">Retrieves an object's indexed properties external data information.</span></span>  
  
## <span data-ttu-id="aca01-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aca01-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsGetIndexedPropertiesExternalData(  
   _In_ JsValueRef object,  
   _Out_ void** data,  
   _Out_ JsTypedArrayType* arrayType,  
   _Out_ unsigned int* elementLength  
);  
```  
  
#### <span data-ttu-id="aca01-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="aca01-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="aca01-107">Объект.</span><span class="sxs-lookup"><span data-stu-id="aca01-107">The object.</span></span>  
  
 `data`  
 <span data-ttu-id="aca01-108">Резервное хранилище внешних данных для индексированных свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="aca01-108">The external data back store for the object's indexed properties.</span></span>  
  
 `arrayType`  
 <span data-ttu-id="aca01-109">Тип элемента массива во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="aca01-109">The array element type in external data.</span></span>  
  
 `elementLength`  
 <span data-ttu-id="aca01-110">Количество элементов массива во внешних данных.</span><span class="sxs-lookup"><span data-stu-id="aca01-110">The number of array elements in external data.</span></span>  
  
## <span data-ttu-id="aca01-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="aca01-111">Return Value</span></span>  
 <span data-ttu-id="aca01-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="aca01-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="aca01-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aca01-113">Remarks</span></span>  
 <span data-ttu-id="aca01-114">Этот API поддерживается только в режиме Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="aca01-114">This API is supported only in Microsoft Edge mode.</span></span>  
  
## <span data-ttu-id="aca01-115">Требования</span><span class="sxs-lookup"><span data-stu-id="aca01-115">Requirements</span></span>  
 <span data-ttu-id="aca01-116">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="aca01-116">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="aca01-117">См. также</span><span class="sxs-lookup"><span data-stu-id="aca01-117">See Also</span></span>  
 [<span data-ttu-id="aca01-118">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="aca01-118">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)