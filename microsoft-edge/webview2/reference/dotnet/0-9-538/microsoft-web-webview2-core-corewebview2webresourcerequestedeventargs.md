---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 3d85b1116a3f75058bda59f1c374700555b42a5e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699263"
---
# <span data-ttu-id="ade5a-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ade5a-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="ade5a-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="ade5a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="ade5a-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="ade5a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="ade5a-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="ade5a-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="ade5a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ade5a-108">Summary</span></span>

 <span data-ttu-id="ade5a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="ade5a-109">Members</span></span>                        | <span data-ttu-id="ade5a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="ade5a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ade5a-111">Запрос</span><span class="sxs-lookup"><span data-stu-id="ade5a-111">Request</span></span>](#request) | <span data-ttu-id="ade5a-112">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="ade5a-112">The HTTP request.</span></span>
[<span data-ttu-id="ade5a-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="ade5a-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="ade5a-114">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ade5a-114">The web resource request contexts.</span></span>
[<span data-ttu-id="ade5a-115">Ответ</span><span class="sxs-lookup"><span data-stu-id="ade5a-115">Response</span></span>](#response) | <span data-ttu-id="ade5a-116">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="ade5a-116">The HTTP response.</span></span>
[<span data-ttu-id="ade5a-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ade5a-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="ade5a-118">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="ade5a-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="ade5a-119">Участников</span><span class="sxs-lookup"><span data-stu-id="ade5a-119">Members</span></span>

#### <span data-ttu-id="ade5a-120">Запрос</span><span class="sxs-lookup"><span data-stu-id="ade5a-120">Request</span></span> 

<span data-ttu-id="ade5a-121">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="ade5a-121">The HTTP request.</span></span>

> <span data-ttu-id="ade5a-122">общедоступный [запрос](#request) HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="ade5a-122">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="ade5a-123">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="ade5a-123">ResourceContext</span></span> 

<span data-ttu-id="ade5a-124">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ade5a-124">The web resource request contexts.</span></span>

> <span data-ttu-id="ade5a-125">общедоступная [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [разделе ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="ade5a-125">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="ade5a-126">Ответ</span><span class="sxs-lookup"><span data-stu-id="ade5a-126">Response</span></span> 

<span data-ttu-id="ade5a-127">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="ade5a-127">The HTTP response.</span></span>

> <span data-ttu-id="ade5a-128">[ответ](#response) на общедоступные HttpResponseMessage</span><span class="sxs-lookup"><span data-stu-id="ade5a-128">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="ade5a-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="ade5a-129">GetDeferral</span></span> 

<span data-ttu-id="ade5a-130">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="ade5a-130">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="ade5a-131">общедоступный [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) - [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="ade5a-131">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="ade5a-132">Вы можете использовать объект CoreWebView2Deferral для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="ade5a-132">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

