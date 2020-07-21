---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 656510998879e77c2e7797c700dacc5966299210
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884654"
---
# <span data-ttu-id="0e615-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0e615-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="0e615-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0e615-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0e615-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="0e615-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0e615-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="0e615-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="0e615-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0e615-108">Summary</span></span>

 <span data-ttu-id="0e615-109">Участников</span><span class="sxs-lookup"><span data-stu-id="0e615-109">Members</span></span>                        | <span data-ttu-id="0e615-110">Описания</span><span class="sxs-lookup"><span data-stu-id="0e615-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0e615-111">Запрос</span><span class="sxs-lookup"><span data-stu-id="0e615-111">Request</span></span>](#request) | <span data-ttu-id="0e615-112">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="0e615-112">The HTTP request.</span></span>
[<span data-ttu-id="0e615-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="0e615-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="0e615-114">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e615-114">The web resource request contexts.</span></span>
[<span data-ttu-id="0e615-115">Ответ</span><span class="sxs-lookup"><span data-stu-id="0e615-115">Response</span></span>](#response) | <span data-ttu-id="0e615-116">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="0e615-116">The HTTP response.</span></span>
[<span data-ttu-id="0e615-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0e615-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="0e615-118">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="0e615-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="0e615-119">Участников</span><span class="sxs-lookup"><span data-stu-id="0e615-119">Members</span></span>

#### <span data-ttu-id="0e615-120">Запрос</span><span class="sxs-lookup"><span data-stu-id="0e615-120">Request</span></span> 

<span data-ttu-id="0e615-121">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="0e615-121">The HTTP request.</span></span>

> <span data-ttu-id="0e615-122">общедоступный [запрос](#request) HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="0e615-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="0e615-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="0e615-123">ResourceContext</span></span> 

<span data-ttu-id="0e615-124">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0e615-124">The web resource request contexts.</span></span>

> <span data-ttu-id="0e615-125">общедоступная [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [разделе ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="0e615-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="0e615-126">Ответ</span><span class="sxs-lookup"><span data-stu-id="0e615-126">Response</span></span> 

<span data-ttu-id="0e615-127">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="0e615-127">The HTTP response.</span></span>

> <span data-ttu-id="0e615-128">[ответ](#response) на общедоступные HttpResponseMessage</span><span class="sxs-lookup"><span data-stu-id="0e615-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="0e615-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0e615-129">GetDeferral</span></span> 

<span data-ttu-id="0e615-130">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="0e615-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="0e615-131">общедоступный [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) - [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="0e615-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="0e615-132">Вы можете использовать объект CoreWebView2Deferral для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="0e615-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

