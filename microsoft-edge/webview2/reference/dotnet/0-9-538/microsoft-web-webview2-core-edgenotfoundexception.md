---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: b4dc30ff741702d03796cb40e6ea6367ffdd0fc0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010105"
---
# <span data-ttu-id="ab306-104">класс 0.9.579-Microsoft. Web. WebView2. Core. EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ab306-104">0.9.579 - Microsoft.Web.WebView2.Core.EdgeNotFoundException class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="ab306-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ab306-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ab306-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="ab306-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

```
class Microsoft.Web.WebView2.Core.EdgeNotFoundException
  : public Exception
```

<span data-ttu-id="ab306-107">Исключение, возникающее при отсутствии установки Edge.</span><span class="sxs-lookup"><span data-stu-id="ab306-107">The exception that is thrown when an Edge installation is missing.</span></span>

## <span data-ttu-id="ab306-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ab306-108">Summary</span></span>

 <span data-ttu-id="ab306-109">Участников</span><span class="sxs-lookup"><span data-stu-id="ab306-109">Members</span></span>                        | <span data-ttu-id="ab306-110">Описания</span><span class="sxs-lookup"><span data-stu-id="ab306-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ab306-111">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ab306-111">EdgeNotFoundException</span></span>](#edgenotfoundexception) | <span data-ttu-id="ab306-112">Инициализирует новый экземпляр класса EdgeNotFoundException.</span><span class="sxs-lookup"><span data-stu-id="ab306-112">Initializes a new instance of the EdgeNotFoundException class.</span></span>
[<span data-ttu-id="ab306-113">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ab306-113">EdgeNotFoundException</span></span>](#edgenotfoundexception) | <span data-ttu-id="ab306-114">Инициализирует новый экземпляр класса EdgeNotFoundException ссылкой на внутреннее исключение, которое является причиной этого исключения.</span><span class="sxs-lookup"><span data-stu-id="ab306-114">Initializes a new instance of the EdgeNotFoundException class with a reference to the inner exception that is the cause of this exception.</span></span>
[<span data-ttu-id="ab306-115">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ab306-115">EdgeNotFoundException</span></span>](#edgenotfoundexception) | <span data-ttu-id="ab306-116">Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ab306-116">Initializes a new instance of the EdgeNotFoundException class with a specified error message.</span></span>
[<span data-ttu-id="ab306-117">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ab306-117">EdgeNotFoundException</span></span>](#edgenotfoundexception) | <span data-ttu-id="ab306-118">Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке и ссылкой на внутреннее исключение, которое является причиной этого исключения.</span><span class="sxs-lookup"><span data-stu-id="ab306-118">Initializes a new instance of the EdgeNotFoundException class with a specified error message and a reference to the inner exception that is the cause of this exception.</span></span>

## <span data-ttu-id="ab306-119">Участников</span><span class="sxs-lookup"><span data-stu-id="ab306-119">Members</span></span>

#### <span data-ttu-id="ab306-120">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ab306-120">EdgeNotFoundException</span></span> 

<span data-ttu-id="ab306-121">Инициализирует новый экземпляр класса EdgeNotFoundException.</span><span class="sxs-lookup"><span data-stu-id="ab306-121">Initializes a new instance of the EdgeNotFoundException class.</span></span>

> <span data-ttu-id="ab306-122">общедоступная [EdgeNotFoundException](#edgenotfoundexception)()</span><span class="sxs-lookup"><span data-stu-id="ab306-122">public [EdgeNotFoundException](#edgenotfoundexception)()</span></span>

#### <span data-ttu-id="ab306-123">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ab306-123">EdgeNotFoundException</span></span> 

<span data-ttu-id="ab306-124">Инициализирует новый экземпляр класса EdgeNotFoundException ссылкой на внутреннее исключение, которое является причиной этого исключения.</span><span class="sxs-lookup"><span data-stu-id="ab306-124">Initializes a new instance of the EdgeNotFoundException class with a reference to the inner exception that is the cause of this exception.</span></span>

> <span data-ttu-id="ab306-125">общедоступный [EdgeNotFoundException](#edgenotfoundexception)(внутренние исключения)</span><span class="sxs-lookup"><span data-stu-id="ab306-125">public [EdgeNotFoundException](#edgenotfoundexception)(Exception inner)</span></span>

##### <span data-ttu-id="ab306-126">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab306-126">Parameters</span></span>
* `inner` <span data-ttu-id="ab306-127">Исключение, вызвавшее текущее исключение.</span><span class="sxs-lookup"><span data-stu-id="ab306-127">The exception that is the cause of the current exception.</span></span>

#### <span data-ttu-id="ab306-128">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ab306-128">EdgeNotFoundException</span></span> 

<span data-ttu-id="ab306-129">Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ab306-129">Initializes a new instance of the EdgeNotFoundException class with a specified error message.</span></span>

> <span data-ttu-id="ab306-130">общедоступный [EdgeNotFoundException](#edgenotfoundexception)(строковое сообщение)</span><span class="sxs-lookup"><span data-stu-id="ab306-130">public [EdgeNotFoundException](#edgenotfoundexception)(string message)</span></span>

##### <span data-ttu-id="ab306-131">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab306-131">Parameters</span></span>
* `message` <span data-ttu-id="ab306-132">Сообщение об ошибке, объясняющее причину исключения.</span><span class="sxs-lookup"><span data-stu-id="ab306-132">The error message that explains the reason for the exception.</span></span>

#### <span data-ttu-id="ab306-133">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="ab306-133">EdgeNotFoundException</span></span> 

<span data-ttu-id="ab306-134">Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке и ссылкой на внутреннее исключение, которое является причиной этого исключения.</span><span class="sxs-lookup"><span data-stu-id="ab306-134">Initializes a new instance of the EdgeNotFoundException class with a specified error message and a reference to the inner exception that is the cause of this exception.</span></span>

> <span data-ttu-id="ab306-135">общедоступный [EdgeNotFoundException](#edgenotfoundexception)(строковое сообщение, исключение Inner)</span><span class="sxs-lookup"><span data-stu-id="ab306-135">public [EdgeNotFoundException](#edgenotfoundexception)(string message, Exception inner)</span></span>

##### <span data-ttu-id="ab306-136">Параметры</span><span class="sxs-lookup"><span data-stu-id="ab306-136">Parameters</span></span>
* `message` <span data-ttu-id="ab306-137">Сообщение об ошибке, объясняющее причину исключения.</span><span class="sxs-lookup"><span data-stu-id="ab306-137">The error message that explains the reason for the exception.</span></span> 

* `inner` <span data-ttu-id="ab306-138">Исключение, вызвавшее текущее исключение.</span><span class="sxs-lookup"><span data-stu-id="ab306-138">The exception that is the cause of the current exception.</span></span>

