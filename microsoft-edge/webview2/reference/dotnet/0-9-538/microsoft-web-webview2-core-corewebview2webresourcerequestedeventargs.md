---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 2282b36d3b7dfcca83f84ed50a976d4e6622ce07
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010126"
---
# <span data-ttu-id="eb5ac-104">класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="eb5ac-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="eb5ac-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="eb5ac-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="eb5ac-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="eb5ac-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="eb5ac-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="eb5ac-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="eb5ac-108">Summary</span></span>

 <span data-ttu-id="eb5ac-109">Участников</span><span class="sxs-lookup"><span data-stu-id="eb5ac-109">Members</span></span>                        | <span data-ttu-id="eb5ac-110">Описания</span><span class="sxs-lookup"><span data-stu-id="eb5ac-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eb5ac-111">Запрос</span><span class="sxs-lookup"><span data-stu-id="eb5ac-111">Request</span></span>](#request) | <span data-ttu-id="eb5ac-112">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-112">The HTTP request.</span></span>
[<span data-ttu-id="eb5ac-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="eb5ac-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="eb5ac-114">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-114">The web resource request contexts.</span></span>
[<span data-ttu-id="eb5ac-115">Ответ</span><span class="sxs-lookup"><span data-stu-id="eb5ac-115">Response</span></span>](#response) | <span data-ttu-id="eb5ac-116">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-116">The HTTP response.</span></span>
[<span data-ttu-id="eb5ac-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="eb5ac-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="eb5ac-118">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="eb5ac-119">Участников</span><span class="sxs-lookup"><span data-stu-id="eb5ac-119">Members</span></span>

#### <span data-ttu-id="eb5ac-120">Запрос</span><span class="sxs-lookup"><span data-stu-id="eb5ac-120">Request</span></span> 

<span data-ttu-id="eb5ac-121">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-121">The HTTP request.</span></span>

> <span data-ttu-id="eb5ac-122">общедоступный [запрос](#request) HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="eb5ac-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="eb5ac-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="eb5ac-123">ResourceContext</span></span> 

<span data-ttu-id="eb5ac-124">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-124">The web resource request contexts.</span></span>

> <span data-ttu-id="eb5ac-125">общедоступная [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [разделе ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="eb5ac-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="eb5ac-126">Ответ</span><span class="sxs-lookup"><span data-stu-id="eb5ac-126">Response</span></span> 

<span data-ttu-id="eb5ac-127">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-127">The HTTP response.</span></span>

> <span data-ttu-id="eb5ac-128">[ответ](#response) на общедоступные HttpResponseMessage</span><span class="sxs-lookup"><span data-stu-id="eb5ac-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="eb5ac-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="eb5ac-129">GetDeferral</span></span> 

<span data-ttu-id="eb5ac-130">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="eb5ac-131">общедоступный [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) - [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="eb5ac-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="eb5ac-132">Вы можете использовать объект CoreWebView2Deferral для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="eb5ac-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

