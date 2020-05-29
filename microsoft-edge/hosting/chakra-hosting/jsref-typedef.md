---
description: Ссылка на объект, принадлежащий сборщику мусора Chakra.
title: JsRef typedef | Документы Microsoft
ms.custom: ''
ms.date: 01/18/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.tgt_pltfrm: ''
ms.topic: reference
ms.assetid: 6aafc39f-6b9c-457f-8bf0-48831bffe9b8
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: f5ce1ada67a4530ba57345b90c0b7deba6954c7c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572474"
---
# <span data-ttu-id="1b04a-103">JsRef typedef</span><span class="sxs-lookup"><span data-stu-id="1b04a-103">JsRef Typedef</span></span>
<span data-ttu-id="1b04a-104">Ссылка на объект, принадлежащий сборщику мусора Chakra.</span><span class="sxs-lookup"><span data-stu-id="1b04a-104">A reference to an object owned by the Chakra garbage collector.</span></span>  
  
## <span data-ttu-id="1b04a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1b04a-105">Syntax</span></span>  
  
```cpp  
typedef void *JsRef;  
```  
  
## <span data-ttu-id="1b04a-106">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1b04a-106">Remarks</span></span>  
 <span data-ttu-id="1b04a-107">Среда выполнения Chakra автоматически отслеживает ссылки JsRef, пока они хранятся в локальных переменных или в параметрах (например, в стеке).</span><span class="sxs-lookup"><span data-stu-id="1b04a-107">A Chakra runtime will automatically track JsRef references as long as they are on stored in local variables or in parameters (i.e. on the stack).</span></span> <span data-ttu-id="1b04a-108">Для хранения JsRef, не включенных в стек, требуется вызвать JsAddRef и JsRelease для управления жизненным циклом объекта, в противном случае сборщик мусора может высвободить объект, пока он все еще используется.</span><span class="sxs-lookup"><span data-stu-id="1b04a-108">Storing a JsRef somewhere other than on the stack requires calling JsAddRef and JsRelease to manage the lifetime of the object, otherwise the garbage collector may free the object while it is still in use.</span></span>  
  
## <span data-ttu-id="1b04a-109">Требования</span><span class="sxs-lookup"><span data-stu-id="1b04a-109">Requirements</span></span>  
 <span data-ttu-id="1b04a-110">**Верхний колонтитул:** jsrt. h</span><span class="sxs-lookup"><span data-stu-id="1b04a-110">**Header:** jsrt.h</span></span>  
  
## <span data-ttu-id="1b04a-111">См. также</span><span class="sxs-lookup"><span data-stu-id="1b04a-111">See Also</span></span>  
 [<span data-ttu-id="1b04a-112">Справочник (среда выполнения JavaScript)</span><span class="sxs-lookup"><span data-stu-id="1b04a-112">Reference (JavaScript Runtime)</span></span>](../chakra-hosting/reference-javascript-runtime.md)