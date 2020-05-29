---
description: Добавляет ссылку на объект, собранный сборщиком мусора.
title: Функция JsAddRef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsAddRef
helpviewer_keywords:
- JsAddRef function
ms.assetid: a7f3ed49-6a86-489a-abdf-c99428e79cae
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: bd02dded6dc2877228f22b4d2800e41a78163467
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571471"
---
# <span data-ttu-id="a6b0f-103">Функция JsAddRef</span><span class="sxs-lookup"><span data-stu-id="a6b0f-103">JsAddRef Function</span></span>
<span data-ttu-id="a6b0f-104">Добавляет ссылку на объект, собранный сборщиком мусора.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-104">Adds a reference to a garbage collected object.</span></span>  
  
## <span data-ttu-id="a6b0f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a6b0f-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsAddRef(  
   _In_ JsRef ref,  
   _Out_opt_ unsigned int *count  
);  
```  
  
#### <span data-ttu-id="a6b0f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a6b0f-106">Parameters</span></span>  
 `ref`  
 <span data-ttu-id="a6b0f-107">Объект, к которому нужно добавить ссылку.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-107">The object to add a reference to.</span></span>  
  
 `count`  
 <span data-ttu-id="a6b0f-108">Новая функция счетчика ссылок объекта (может передавать значение null).</span><span class="sxs-lookup"><span data-stu-id="a6b0f-108">The object's new reference count (can pass in null).</span></span>  
  
## <span data-ttu-id="a6b0f-109">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="a6b0f-109">Return Value</span></span>  
 <span data-ttu-id="a6b0f-110">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-110">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="a6b0f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a6b0f-111">Remarks</span></span>  
 <span data-ttu-id="a6b0f-112">Это необходимо вызвать только для `JsRef` дескрипторов, которые не будут храниться в стеке.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-112">This only needs to be called on `JsRef` handles that are not going to be stored somewhere on the stack.</span></span> <span data-ttu-id="a6b0f-113">Вызов `JsAddRef` гарантирует, что объект, на который `JsRef` указывает ссылка, не будет освобожден до `JsRelease` вызова.</span><span class="sxs-lookup"><span data-stu-id="a6b0f-113">Calling `JsAddRef` ensures that the object the `JsRef` refers to will not be freed until `JsRelease` is called.</span></span>  
  
## <span data-ttu-id="a6b0f-114">Требования</span><span class="sxs-lookup"><span data-stu-id="a6b0f-114">Requirements</span></span>  
 <span data-ttu-id="a6b0f-115">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="a6b0f-115">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="a6b0f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a6b0f-116">See Also</span></span>  
 [<span data-ttu-id="a6b0f-117">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="a6b0f-117">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)