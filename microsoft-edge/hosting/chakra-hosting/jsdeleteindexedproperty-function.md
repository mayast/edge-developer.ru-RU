---
description: Удаление значения по указанному индексу объекта.
title: Функция JsDeleteIndexedProperty | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsDeleteIndexedProperty
helpviewer_keywords:
- JsDeleteIndexedProperty function
ms.assetid: cc876839-2ecd-41a8-82d0-c19b3de944e3
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 6148a9c59105749a78ece73578d4b840501c6ecc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571407"
---
# <span data-ttu-id="bc9fb-103">Функция JsDeleteIndexedProperty</span><span class="sxs-lookup"><span data-stu-id="bc9fb-103">JsDeleteIndexedProperty Function</span></span>
<span data-ttu-id="bc9fb-104">Удаление значения по указанному индексу объекта.</span><span class="sxs-lookup"><span data-stu-id="bc9fb-104">Delete the value at the specified index of an object.</span></span>  
  
## <span data-ttu-id="bc9fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bc9fb-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsDeleteIndexedProperty(  
   _In_ JsValueRef object,  
   _In_ JsValueRef index  
);  
```  
  
#### <span data-ttu-id="bc9fb-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc9fb-106">Parameters</span></span>  
 `object`  
 <span data-ttu-id="bc9fb-107">Объект для работы.</span><span class="sxs-lookup"><span data-stu-id="bc9fb-107">The object to operate on.</span></span>  
  
 `index`  
 <span data-ttu-id="bc9fb-108">Индекс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bc9fb-108">The index to delete.</span></span>  
  
## <span data-ttu-id="bc9fb-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="bc9fb-109">Return Value</span></span>  
 <span data-ttu-id="bc9fb-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="bc9fb-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="bc9fb-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bc9fb-111">Remarks</span></span>  
 <span data-ttu-id="bc9fb-112">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="bc9fb-112">Requires an active script context.</span></span>  
  
## <span data-ttu-id="bc9fb-113">Требования</span><span class="sxs-lookup"><span data-stu-id="bc9fb-113">Requirements</span></span>  
 <span data-ttu-id="bc9fb-114">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="bc9fb-114">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="bc9fb-115">См. также</span><span class="sxs-lookup"><span data-stu-id="bc9fb-115">See Also</span></span>  
 [<span data-ttu-id="bc9fb-116">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="bc9fb-116">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)