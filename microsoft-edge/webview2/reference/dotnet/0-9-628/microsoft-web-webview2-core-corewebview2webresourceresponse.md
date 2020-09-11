---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012429"
---
# <span data-ttu-id="b05c7-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="b05c7-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponse class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="b05c7-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b05c7-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b05c7-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b05c7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b05c7-107">HTTP-ответ, используемый с событием WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="b05c7-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="b05c7-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b05c7-108">Summary</span></span>

 <span data-ttu-id="b05c7-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b05c7-109">Members</span></span>                        | <span data-ttu-id="b05c7-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b05c7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b05c7-111">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b05c7-111">Content</span></span>](#content) | <span data-ttu-id="b05c7-112">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="b05c7-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="b05c7-113">Заголовки</span><span class="sxs-lookup"><span data-stu-id="b05c7-113">Headers</span></span>](#headers) | <span data-ttu-id="b05c7-114">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b05c7-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="b05c7-115">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b05c7-115">ReasonPhrase</span></span>](#reasonphrase) | <span data-ttu-id="b05c7-116">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b05c7-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="b05c7-117">StatusCode</span><span class="sxs-lookup"><span data-stu-id="b05c7-117">StatusCode</span></span>](#statuscode) | <span data-ttu-id="b05c7-118">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b05c7-118">The HTTP response status code.</span></span>

## <span data-ttu-id="b05c7-119">Участников</span><span class="sxs-lookup"><span data-stu-id="b05c7-119">Members</span></span>

#### <span data-ttu-id="b05c7-120">Содержимое</span><span class="sxs-lookup"><span data-stu-id="b05c7-120">Content</span></span> 

<span data-ttu-id="b05c7-121">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="b05c7-121">HTTP response content as stream.</span></span>

> <span data-ttu-id="b05c7-122">Общее [содержимое](#content) потока</span><span class="sxs-lookup"><span data-stu-id="b05c7-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="b05c7-123">Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="b05c7-123">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="b05c7-124">Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b05c7-124">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="b05c7-125">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b05c7-125">Null means no content data.</span></span> <span data-ttu-id="b05c7-126">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="b05c7-126">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="b05c7-127">Заголовки</span><span class="sxs-lookup"><span data-stu-id="b05c7-127">Headers</span></span> 

<span data-ttu-id="b05c7-128">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b05c7-128">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="b05c7-129">[заголовки](#headers) общедоступной [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md)</span><span class="sxs-lookup"><span data-stu-id="b05c7-129">public [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="b05c7-130">ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b05c7-130">ReasonPhrase</span></span> 

<span data-ttu-id="b05c7-131">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b05c7-131">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="b05c7-132">общедоступная строка [ReasonPhrase](#reasonphrase)</span><span class="sxs-lookup"><span data-stu-id="b05c7-132">public string [ReasonPhrase](#reasonphrase)</span></span>

#### <span data-ttu-id="b05c7-133">StatusCode</span><span class="sxs-lookup"><span data-stu-id="b05c7-133">StatusCode</span></span> 

<span data-ttu-id="b05c7-134">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b05c7-134">The HTTP response status code.</span></span>

> <span data-ttu-id="b05c7-135">Открытый целочисленный [StatusCode](#statuscode)</span><span class="sxs-lookup"><span data-stu-id="b05c7-135">public int [StatusCode](#statuscode)</span></span>

