---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 5c8d164b24995cc31070232dd9b1a2d88fc16cec
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012433"
---
# <span data-ttu-id="304fe-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="304fe-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequest class</span></span> 

<span data-ttu-id="304fe-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="304fe-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="304fe-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="304fe-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="304fe-107">HTTP-запрос, используемый для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="304fe-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="304fe-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="304fe-108">Summary</span></span>

 <span data-ttu-id="304fe-109">Участников</span><span class="sxs-lookup"><span data-stu-id="304fe-109">Members</span></span>                        | <span data-ttu-id="304fe-110">Описания</span><span class="sxs-lookup"><span data-stu-id="304fe-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="304fe-111">Содержимое</span><span class="sxs-lookup"><span data-stu-id="304fe-111">Content</span></span>](#content) | <span data-ttu-id="304fe-112">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="304fe-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="304fe-113">Заголовки</span><span class="sxs-lookup"><span data-stu-id="304fe-113">Headers</span></span>](#headers) | <span data-ttu-id="304fe-114">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="304fe-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="304fe-115">Метод</span><span class="sxs-lookup"><span data-stu-id="304fe-115">Method</span></span>](#method) | <span data-ttu-id="304fe-116">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="304fe-116">The HTTP request method.</span></span>
[<span data-ttu-id="304fe-117">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="304fe-117">Uri</span></span>](#uri) | <span data-ttu-id="304fe-118">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="304fe-118">The request URI.</span></span>

## <span data-ttu-id="304fe-119">Участников</span><span class="sxs-lookup"><span data-stu-id="304fe-119">Members</span></span>

#### <span data-ttu-id="304fe-120">Содержимое</span><span class="sxs-lookup"><span data-stu-id="304fe-120">Content</span></span> 

<span data-ttu-id="304fe-121">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="304fe-121">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="304fe-122">Общее [содержимое](#content) потока</span><span class="sxs-lookup"><span data-stu-id="304fe-122">public Stream [Content](#content)</span></span>

<span data-ttu-id="304fe-123">Поместите здесь данные.</span><span class="sxs-lookup"><span data-stu-id="304fe-123">POST data would be here.</span></span> <span data-ttu-id="304fe-124">Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="304fe-124">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="304fe-125">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="304fe-125">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="304fe-126">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="304fe-126">Null means no content data.</span></span> <span data-ttu-id="304fe-127">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="304fe-127">IStream semantics apply (return S_OK to Read calls until all data is exhausted).</span></span>

#### <span data-ttu-id="304fe-128">Заголовки</span><span class="sxs-lookup"><span data-stu-id="304fe-128">Headers</span></span> 

<span data-ttu-id="304fe-129">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="304fe-129">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="304fe-130">[заголовки](#headers) общедоступной [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md)</span><span class="sxs-lookup"><span data-stu-id="304fe-130">public [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md) [Headers](#headers)</span></span>

#### <span data-ttu-id="304fe-131">Метод</span><span class="sxs-lookup"><span data-stu-id="304fe-131">Method</span></span> 

<span data-ttu-id="304fe-132">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="304fe-132">The HTTP request method.</span></span>

> <span data-ttu-id="304fe-133">[метод](#method) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="304fe-133">public string [Method](#method)</span></span>

#### <span data-ttu-id="304fe-134">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="304fe-134">Uri</span></span> 

<span data-ttu-id="304fe-135">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="304fe-135">The request URI.</span></span>

> <span data-ttu-id="304fe-136">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="304fe-136">public string [Uri](#uri)</span></span>

