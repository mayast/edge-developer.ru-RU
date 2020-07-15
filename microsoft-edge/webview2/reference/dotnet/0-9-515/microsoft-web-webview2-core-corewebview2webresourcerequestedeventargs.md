---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2f9fb899746922206ff3f6cbfd129d69389fd60e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879312"
---
# <span data-ttu-id="f326e-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f326e-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="f326e-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f326e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f326e-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="f326e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="f326e-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f326e-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f326e-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f326e-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f326e-109">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f326e-109">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="f326e-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f326e-110">Summary</span></span>

 <span data-ttu-id="f326e-111">Участников</span><span class="sxs-lookup"><span data-stu-id="f326e-111">Members</span></span>                        | <span data-ttu-id="f326e-112">Описания</span><span class="sxs-lookup"><span data-stu-id="f326e-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f326e-113">Запрос</span><span class="sxs-lookup"><span data-stu-id="f326e-113">Request</span></span>](#request) | <span data-ttu-id="f326e-114">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="f326e-114">The HTTP request.</span></span>
[<span data-ttu-id="f326e-115">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f326e-115">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="f326e-116">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f326e-116">The web resource request contexts.</span></span>
[<span data-ttu-id="f326e-117">Ответ</span><span class="sxs-lookup"><span data-stu-id="f326e-117">Response</span></span>](#response) | <span data-ttu-id="f326e-118">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="f326e-118">The HTTP response.</span></span>
[<span data-ttu-id="f326e-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f326e-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f326e-120">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="f326e-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="f326e-121">Участников</span><span class="sxs-lookup"><span data-stu-id="f326e-121">Members</span></span>

#### <span data-ttu-id="f326e-122">Запрос</span><span class="sxs-lookup"><span data-stu-id="f326e-122">Request</span></span> 

<span data-ttu-id="f326e-123">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="f326e-123">The HTTP request.</span></span>

> <span data-ttu-id="f326e-124">общедоступный [запрос](#request) HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="f326e-124">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="f326e-125">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="f326e-125">ResourceContext</span></span> 

<span data-ttu-id="f326e-126">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f326e-126">The web resource request contexts.</span></span>

> <span data-ttu-id="f326e-127">общедоступная [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [разделе ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="f326e-127">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="f326e-128">Ответ</span><span class="sxs-lookup"><span data-stu-id="f326e-128">Response</span></span> 

<span data-ttu-id="f326e-129">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="f326e-129">The HTTP response.</span></span>

> <span data-ttu-id="f326e-130">[ответ](#response) на общедоступные HttpResponseMessage</span><span class="sxs-lookup"><span data-stu-id="f326e-130">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="f326e-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f326e-131">GetDeferral</span></span> 

<span data-ttu-id="f326e-132">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="f326e-132">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="f326e-133">общедоступный [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) - [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="f326e-133">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="f326e-134">Вы можете использовать объект CoreWebView2Deferral для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="f326e-134">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

