---
description: Создает объект JavaScript `ArrayBuffer` для доступа к внешней памяти.
title: Функция JsCreateExternalArrayBuffer | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 4a02aaec-0f67-4bf9-b37c-71cdb1410ca4
caps.latest.revision: 3
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 376eedda18393436d9dce340753586bf32599b21
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571434"
---
# <span data-ttu-id="b1ae2-103">Функция JsCreateExternalArrayBuffer</span><span class="sxs-lookup"><span data-stu-id="b1ae2-103">JsCreateExternalArrayBuffer Function</span></span>
<span data-ttu-id="b1ae2-104">Создает объект JavaScript `ArrayBuffer` для доступа к внешней памяти.</span><span class="sxs-lookup"><span data-stu-id="b1ae2-104">Creates a Javascript `ArrayBuffer` object to access external memory.</span></span>
  
## <span data-ttu-id="b1ae2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b1ae2-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsCreateExternalArrayBuffer(  
  _Pre_maybenull_ _Pre_writable_byte_size_(byteLength) void *data,  
  _In_ unsigned int byteLength,  
  _In_opt_ JsFinalizeCallback finalizeCallback,  
  _In_opt_ void *callbackState,  
  _Out_ JsValueRef *result  
);  
  
```  
  
#### <span data-ttu-id="b1ae2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1ae2-106">Parameters</span></span>  
 `data`  
 <span data-ttu-id="b1ae2-107">Указатель на внешнюю память.</span><span class="sxs-lookup"><span data-stu-id="b1ae2-107">A pointer to the external memory.</span></span>  
  
 `byteLength`  
 <span data-ttu-id="b1ae2-108">Количество байтов во внешней памяти.</span><span class="sxs-lookup"><span data-stu-id="b1ae2-108">The number of bytes in the external memory.</span></span>  
  
 `finalizeCallback`  
 <span data-ttu-id="b1ae2-109">Обратный вызов для завершения работы объекта.</span><span class="sxs-lookup"><span data-stu-id="b1ae2-109">A callback for when the object is finalized.</span></span> <span data-ttu-id="b1ae2-110">Может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="b1ae2-110">May be null.</span></span>  
  
 `callbackState`  
 <span data-ttu-id="b1ae2-111">Указанное пользователем состояние, которое будет возвращено в finalizeCallback.</span><span class="sxs-lookup"><span data-stu-id="b1ae2-111">User provided state that will be passed back to finalizeCallback.</span></span>  
  
 `result`  
 <span data-ttu-id="b1ae2-112">Новый `ArrayBuffer` объект.</span><span class="sxs-lookup"><span data-stu-id="b1ae2-112">The new `ArrayBuffer` object.</span></span>  
  
## <span data-ttu-id="b1ae2-113">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="b1ae2-113">Return Value</span></span>  
 <span data-ttu-id="b1ae2-114">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b1ae2-114">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="b1ae2-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b1ae2-115">Remarks</span></span>  
 <span data-ttu-id="b1ae2-116">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="b1ae2-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="b1ae2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b1ae2-117">Requirements</span></span>  
 <span data-ttu-id="b1ae2-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="b1ae2-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="b1ae2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b1ae2-119">See Also</span></span>  
 [<span data-ttu-id="b1ae2-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="b1ae2-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)