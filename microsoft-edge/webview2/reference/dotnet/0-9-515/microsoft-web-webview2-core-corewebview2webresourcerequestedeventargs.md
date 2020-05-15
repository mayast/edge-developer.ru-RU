---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9210a4b70d0e2edf30cbaad906f57b360688dfe8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654703"
---
# <span data-ttu-id="64258-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="64258-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="64258-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="64258-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="64258-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="64258-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="64258-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="64258-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="64258-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="64258-108">Summary</span></span>

 <span data-ttu-id="64258-109">Участников</span><span class="sxs-lookup"><span data-stu-id="64258-109">Members</span></span>                        | <span data-ttu-id="64258-110">Описания</span><span class="sxs-lookup"><span data-stu-id="64258-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64258-111">Запрос</span><span class="sxs-lookup"><span data-stu-id="64258-111">Request</span></span>](#request) | <span data-ttu-id="64258-112">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="64258-112">The HTTP request.</span></span>
[<span data-ttu-id="64258-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="64258-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="64258-114">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64258-114">The web resource request contexts.</span></span>
[<span data-ttu-id="64258-115">Ответ</span><span class="sxs-lookup"><span data-stu-id="64258-115">Response</span></span>](#response) | <span data-ttu-id="64258-116">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="64258-116">The HTTP response.</span></span>
[<span data-ttu-id="64258-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="64258-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="64258-118">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="64258-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="64258-119">Участников</span><span class="sxs-lookup"><span data-stu-id="64258-119">Members</span></span>

#### <span data-ttu-id="64258-120">Запрос</span><span class="sxs-lookup"><span data-stu-id="64258-120">Request</span></span> 

<span data-ttu-id="64258-121">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="64258-121">The HTTP request.</span></span>

> <span data-ttu-id="64258-122">общедоступный [запрос](#request) HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="64258-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="64258-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="64258-123">ResourceContext</span></span> 

<span data-ttu-id="64258-124">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="64258-124">The web resource request contexts.</span></span>

> <span data-ttu-id="64258-125">общедоступная [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [разделе ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="64258-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="64258-126">Ответ</span><span class="sxs-lookup"><span data-stu-id="64258-126">Response</span></span> 

<span data-ttu-id="64258-127">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="64258-127">The HTTP response.</span></span>

> <span data-ttu-id="64258-128">[ответ](#response) на общедоступные HttpResponseMessage</span><span class="sxs-lookup"><span data-stu-id="64258-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="64258-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="64258-129">GetDeferral</span></span> 

<span data-ttu-id="64258-130">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="64258-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="64258-131">общедоступный [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) - [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="64258-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="64258-132">Вы можете использовать объект CoreWebView2Deferral для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="64258-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

