---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: fc65d857f11a77a1d3629d40266f0453acadaa7b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886313"
---
# <span data-ttu-id="53b74-104">класс 0.9.515-Microsoft. Web. WebView2. Core. EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="53b74-104">0.9.515 - Microsoft.Web.WebView2.Core.EdgeNotFoundException class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="53b74-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="53b74-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="53b74-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="53b74-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

```
class Microsoft.Web.WebView2.Core.EdgeNotFoundException
  : public Exception
```

<span data-ttu-id="53b74-107">Исключение, возникающее при отсутствии установки Edge.</span><span class="sxs-lookup"><span data-stu-id="53b74-107">The exception that is thrown when an Edge installation is missing.</span></span>

## <span data-ttu-id="53b74-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="53b74-108">Summary</span></span>

 <span data-ttu-id="53b74-109">Участников</span><span class="sxs-lookup"><span data-stu-id="53b74-109">Members</span></span>                        | <span data-ttu-id="53b74-110">Описания</span><span class="sxs-lookup"><span data-stu-id="53b74-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="53b74-111">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="53b74-111">EdgeNotFoundException</span></span>](#edgenotfoundexception) | <span data-ttu-id="53b74-112">Инициализирует новый экземпляр класса EdgeNotFoundException.</span><span class="sxs-lookup"><span data-stu-id="53b74-112">Initializes a new instance of the EdgeNotFoundException class.</span></span>
[<span data-ttu-id="53b74-113">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="53b74-113">EdgeNotFoundException</span></span>](#edgenotfoundexception) | <span data-ttu-id="53b74-114">Инициализирует новый экземпляр класса EdgeNotFoundException ссылкой на внутреннее исключение, которое является причиной этого исключения.</span><span class="sxs-lookup"><span data-stu-id="53b74-114">Initializes a new instance of the EdgeNotFoundException class with a reference to the inner exception that is the cause of this exception.</span></span>
[<span data-ttu-id="53b74-115">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="53b74-115">EdgeNotFoundException</span></span>](#edgenotfoundexception) | <span data-ttu-id="53b74-116">Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке.</span><span class="sxs-lookup"><span data-stu-id="53b74-116">Initializes a new instance of the EdgeNotFoundException class with a specified error message.</span></span>
[<span data-ttu-id="53b74-117">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="53b74-117">EdgeNotFoundException</span></span>](#edgenotfoundexception) | <span data-ttu-id="53b74-118">Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке и ссылкой на внутреннее исключение, которое является причиной этого исключения.</span><span class="sxs-lookup"><span data-stu-id="53b74-118">Initializes a new instance of the EdgeNotFoundException class with a specified error message and a reference to the inner exception that is the cause of this exception.</span></span>

## <span data-ttu-id="53b74-119">Участников</span><span class="sxs-lookup"><span data-stu-id="53b74-119">Members</span></span>

#### <span data-ttu-id="53b74-120">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="53b74-120">EdgeNotFoundException</span></span> 

<span data-ttu-id="53b74-121">Инициализирует новый экземпляр класса EdgeNotFoundException.</span><span class="sxs-lookup"><span data-stu-id="53b74-121">Initializes a new instance of the EdgeNotFoundException class.</span></span>

> <span data-ttu-id="53b74-122">общедоступная [EdgeNotFoundException](#edgenotfoundexception)()</span><span class="sxs-lookup"><span data-stu-id="53b74-122">public [EdgeNotFoundException](#edgenotfoundexception)()</span></span>

#### <span data-ttu-id="53b74-123">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="53b74-123">EdgeNotFoundException</span></span> 

<span data-ttu-id="53b74-124">Инициализирует новый экземпляр класса EdgeNotFoundException ссылкой на внутреннее исключение, которое является причиной этого исключения.</span><span class="sxs-lookup"><span data-stu-id="53b74-124">Initializes a new instance of the EdgeNotFoundException class with a reference to the inner exception that is the cause of this exception.</span></span>

> <span data-ttu-id="53b74-125">общедоступный [EdgeNotFoundException](#edgenotfoundexception)(внутренние исключения)</span><span class="sxs-lookup"><span data-stu-id="53b74-125">public [EdgeNotFoundException](#edgenotfoundexception)(Exception inner)</span></span>

##### <span data-ttu-id="53b74-126">Параметры</span><span class="sxs-lookup"><span data-stu-id="53b74-126">Parameters</span></span>
* `inner` <span data-ttu-id="53b74-127">Исключение, вызвавшее текущее исключение.</span><span class="sxs-lookup"><span data-stu-id="53b74-127">The exception that is the cause of the current exception.</span></span>

#### <span data-ttu-id="53b74-128">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="53b74-128">EdgeNotFoundException</span></span> 

<span data-ttu-id="53b74-129">Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке.</span><span class="sxs-lookup"><span data-stu-id="53b74-129">Initializes a new instance of the EdgeNotFoundException class with a specified error message.</span></span>

> <span data-ttu-id="53b74-130">общедоступный [EdgeNotFoundException](#edgenotfoundexception)(строковое сообщение)</span><span class="sxs-lookup"><span data-stu-id="53b74-130">public [EdgeNotFoundException](#edgenotfoundexception)(string message)</span></span>

##### <span data-ttu-id="53b74-131">Параметры</span><span class="sxs-lookup"><span data-stu-id="53b74-131">Parameters</span></span>
* `message` <span data-ttu-id="53b74-132">Сообщение об ошибке, объясняющее причину исключения.</span><span class="sxs-lookup"><span data-stu-id="53b74-132">The error message that explains the reason for the exception.</span></span>

#### <span data-ttu-id="53b74-133">EdgeNotFoundException</span><span class="sxs-lookup"><span data-stu-id="53b74-133">EdgeNotFoundException</span></span> 

<span data-ttu-id="53b74-134">Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке и ссылкой на внутреннее исключение, которое является причиной этого исключения.</span><span class="sxs-lookup"><span data-stu-id="53b74-134">Initializes a new instance of the EdgeNotFoundException class with a specified error message and a reference to the inner exception that is the cause of this exception.</span></span>

> <span data-ttu-id="53b74-135">общедоступный [EdgeNotFoundException](#edgenotfoundexception)(строковое сообщение, исключение Inner)</span><span class="sxs-lookup"><span data-stu-id="53b74-135">public [EdgeNotFoundException](#edgenotfoundexception)(string message, Exception inner)</span></span>

##### <span data-ttu-id="53b74-136">Параметры</span><span class="sxs-lookup"><span data-stu-id="53b74-136">Parameters</span></span>
* `message` <span data-ttu-id="53b74-137">Сообщение об ошибке, объясняющее причину исключения.</span><span class="sxs-lookup"><span data-stu-id="53b74-137">The error message that explains the reason for the exception.</span></span> 

* `inner` <span data-ttu-id="53b74-138">Исключение, вызвавшее текущее исключение.</span><span class="sxs-lookup"><span data-stu-id="53b74-138">The exception that is the cause of the current exception.</span></span>

