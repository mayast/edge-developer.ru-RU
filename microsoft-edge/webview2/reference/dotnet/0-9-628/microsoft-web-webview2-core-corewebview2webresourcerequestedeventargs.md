---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 501483894a2abca58c5a1856ab587b93be904c8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012432"
---
# <span data-ttu-id="c9d63-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c9d63-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

<span data-ttu-id="c9d63-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c9d63-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c9d63-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="c9d63-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c9d63-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c9d63-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="c9d63-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c9d63-108">Summary</span></span>

 <span data-ttu-id="c9d63-109">Участников</span><span class="sxs-lookup"><span data-stu-id="c9d63-109">Members</span></span>                        | <span data-ttu-id="c9d63-110">Описания</span><span class="sxs-lookup"><span data-stu-id="c9d63-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c9d63-111">Запрос</span><span class="sxs-lookup"><span data-stu-id="c9d63-111">Request</span></span>](#request) | <span data-ttu-id="c9d63-112">Запрос на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="c9d63-112">The Web resource request.</span></span>
[<span data-ttu-id="c9d63-113">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="c9d63-113">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="c9d63-114">Контекст запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="c9d63-114">The web resource request context.</span></span>
[<span data-ttu-id="c9d63-115">Ответ</span><span class="sxs-lookup"><span data-stu-id="c9d63-115">Response</span></span>](#response) | <span data-ttu-id="c9d63-116">Заполнитель для объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="c9d63-116">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="c9d63-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c9d63-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="c9d63-118">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="c9d63-118">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="c9d63-119">Участников</span><span class="sxs-lookup"><span data-stu-id="c9d63-119">Members</span></span>

#### <span data-ttu-id="c9d63-120">Запрос</span><span class="sxs-lookup"><span data-stu-id="c9d63-120">Request</span></span> 

<span data-ttu-id="c9d63-121">Запрос на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="c9d63-121">The Web resource request.</span></span>

> <span data-ttu-id="c9d63-122">общедоступный [запрос](#request) [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md)</span><span class="sxs-lookup"><span data-stu-id="c9d63-122">public [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) [Request](#request)</span></span>

<span data-ttu-id="c9d63-123">Возможно, в объекте Request отсутствует часть заголовков, добавленных в разделе "сетевой стек".</span><span class="sxs-lookup"><span data-stu-id="c9d63-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="c9d63-124">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="c9d63-124">ResourceContext</span></span> 

<span data-ttu-id="c9d63-125">Контекст запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="c9d63-125">The web resource request context.</span></span>

> <span data-ttu-id="c9d63-126">общедоступная [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [разделе ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="c9d63-126">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="c9d63-127">Ответ</span><span class="sxs-lookup"><span data-stu-id="c9d63-127">Response</span></span> 

<span data-ttu-id="c9d63-128">Заполнитель для объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="c9d63-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="c9d63-129">[ответ](#response) на общедоступные [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md)</span><span class="sxs-lookup"><span data-stu-id="c9d63-129">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response)</span></span>

<span data-ttu-id="c9d63-130">Если этот объект задан, запрос на веб-ресурс будет выполнен с этим ответом.</span><span class="sxs-lookup"><span data-stu-id="c9d63-130">If this object is set, the web resource request will be completed with this response.</span></span> <span data-ttu-id="c9d63-131">Пустой объект ответа на веб-ресурс можно создать с помощью CreateWebResourceResponse и затем изменить для создания ответа.</span><span class="sxs-lookup"><span data-stu-id="c9d63-131">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>

#### <span data-ttu-id="c9d63-132">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="c9d63-132">GetDeferral</span></span> 

<span data-ttu-id="c9d63-133">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="c9d63-133">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="c9d63-134">общедоступный [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) - [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="c9d63-134">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="c9d63-135">Вы можете использовать объект CoreWebView2Deferral, чтобы выполнить запрос позже.</span><span class="sxs-lookup"><span data-stu-id="c9d63-135">You can use the CoreWebView2Deferral object to complete the request at a later time.</span></span>

