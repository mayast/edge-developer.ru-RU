---
description: Выполняет сериализацию проанализированного сценария в буфер, чем может быть повторно использован.
title: Функция JsSerializeScript | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
f1_keywords:
- jsrt/JsSerializeScript
helpviewer_keywords:
- JsSerializeScript function
ms.assetid: ca42c194-e1c1-407d-b542-b9d494e3ac4e
caps.latest.revision: 12
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1b45067fddb7ea4dff02e527e460db1270011c61
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572453"
---
# <span data-ttu-id="85c78-103">Функция JsSerializeScript</span><span class="sxs-lookup"><span data-stu-id="85c78-103">JsSerializeScript Function</span></span>
<span data-ttu-id="85c78-104">Выполняет сериализацию проанализированного сценария в буфер, чем может быть повторно использован.</span><span class="sxs-lookup"><span data-stu-id="85c78-104">Serializes a parsed script to a buffer than can be reused.</span></span>  
  
## <span data-ttu-id="85c78-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="85c78-105">Syntax</span></span>  
  
```cpp  
STDAPI_(JsErrorCode) JsSerializeScript(  
   _In_z_ const wchar_t *script,  
   _Out_writes_to_opt_(*bufferSize,  
   *bufferSize) BYTE *buffer,  
   _Inout_ unsigned long *bufferSize  
);  
```  
  
#### <span data-ttu-id="85c78-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="85c78-106">Parameters</span></span>  
 `script`  
 <span data-ttu-id="85c78-107">Сценарий, который нужно сериализовать.</span><span class="sxs-lookup"><span data-stu-id="85c78-107">The script to serialize.</span></span>  
  
 `buffer`  
 <span data-ttu-id="85c78-108">Буфер, в который будет помещен сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="85c78-108">The buffer to put the serialized script into.</span></span> <span data-ttu-id="85c78-109">Может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="85c78-109">Can be null.</span></span>  
  
 `bufferSize`  
 <span data-ttu-id="85c78-110">На входе — размер буфера в байтах; при выходе — размер буфера (в байтах), который должен хранить сериализованный сценарий.</span><span class="sxs-lookup"><span data-stu-id="85c78-110">On entry, the size of the buffer, in bytes; on exit, the size of the buffer, in bytes, required to hold the serialized script.</span></span>  
  
## <span data-ttu-id="85c78-111">Возвращенное значение</span><span class="sxs-lookup"><span data-stu-id="85c78-111">Return Value</span></span>  
 <span data-ttu-id="85c78-112">Код `JsNoError` , если операция завершилась успешно, код ошибки в противном случае.</span><span class="sxs-lookup"><span data-stu-id="85c78-112">The code `JsNoError` if the operation succeeded, a failure code otherwise.</span></span>  
  
## <span data-ttu-id="85c78-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="85c78-113">Remarks</span></span>  
 `JsSerializeScript` <span data-ttu-id="85c78-114">анализирует сценарий и сохраняет проанализированную форму сценария в формате, не зависящем от среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="85c78-114">parses a script and then stores the parsed form of the script in a runtime-independent format.</span></span> <span data-ttu-id="85c78-115">Сериализованный сценарий затем можно десериализовать в любой среде выполнения, не требуя повторного синтаксического анализа сценария.</span><span class="sxs-lookup"><span data-stu-id="85c78-115">The serialized script then can be deserialized in any runtime without requiring the script to be re-parsed.</span></span>  
  
 <span data-ttu-id="85c78-116">Требуется активный контекст сценария.</span><span class="sxs-lookup"><span data-stu-id="85c78-116">Requires an active script context.</span></span>  
  
## <span data-ttu-id="85c78-117">Требования</span><span class="sxs-lookup"><span data-stu-id="85c78-117">Requirements</span></span>  
 <span data-ttu-id="85c78-118">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="85c78-118">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="85c78-119">См. также</span><span class="sxs-lookup"><span data-stu-id="85c78-119">See Also</span></span>  
 [<span data-ttu-id="85c78-120">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="85c78-120">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)