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
ms.openlocfilehash: 072ce10e7ac1f34238278366c3e8799a3268cb0b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697534"
---
# <span data-ttu-id="4d1e3-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4d1e3-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="4d1e3-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4d1e3-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="4d1e3-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4d1e3-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4d1e3-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="4d1e3-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4d1e3-109">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-109">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="4d1e3-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4d1e3-110">Summary</span></span>

 <span data-ttu-id="4d1e3-111">Участников</span><span class="sxs-lookup"><span data-stu-id="4d1e3-111">Members</span></span>                        | <span data-ttu-id="4d1e3-112">Описания</span><span class="sxs-lookup"><span data-stu-id="4d1e3-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4d1e3-113">Запрос</span><span class="sxs-lookup"><span data-stu-id="4d1e3-113">Request</span></span>](#request) | <span data-ttu-id="4d1e3-114">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-114">The HTTP request.</span></span>
[<span data-ttu-id="4d1e3-115">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="4d1e3-115">ResourceContext</span></span>](#resourcecontext) | <span data-ttu-id="4d1e3-116">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-116">The web resource request contexts.</span></span>
[<span data-ttu-id="4d1e3-117">Ответ</span><span class="sxs-lookup"><span data-stu-id="4d1e3-117">Response</span></span>](#response) | <span data-ttu-id="4d1e3-118">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-118">The HTTP response.</span></span>
[<span data-ttu-id="4d1e3-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4d1e3-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4d1e3-120">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-120">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

## <span data-ttu-id="4d1e3-121">Участников</span><span class="sxs-lookup"><span data-stu-id="4d1e3-121">Members</span></span>

#### <span data-ttu-id="4d1e3-122">Запрос</span><span class="sxs-lookup"><span data-stu-id="4d1e3-122">Request</span></span> 

<span data-ttu-id="4d1e3-123">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-123">The HTTP request.</span></span>

> <span data-ttu-id="4d1e3-124">общедоступный [запрос](#request) HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="4d1e3-124">public HttpRequestMessage [Request](#request)</span></span>

#### <span data-ttu-id="4d1e3-125">ResourceContext</span><span class="sxs-lookup"><span data-stu-id="4d1e3-125">ResourceContext</span></span> 

<span data-ttu-id="4d1e3-126">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-126">The web resource request contexts.</span></span>

> <span data-ttu-id="4d1e3-127">общедоступная [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [разделе ResourceContext](#resourcecontext)</span><span class="sxs-lookup"><span data-stu-id="4d1e3-127">public [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [ResourceContext](#resourcecontext)</span></span>

#### <span data-ttu-id="4d1e3-128">Ответ</span><span class="sxs-lookup"><span data-stu-id="4d1e3-128">Response</span></span> 

<span data-ttu-id="4d1e3-129">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-129">The HTTP response.</span></span>

> <span data-ttu-id="4d1e3-130">[ответ](#response) на общедоступные HttpResponseMessage</span><span class="sxs-lookup"><span data-stu-id="4d1e3-130">public HttpResponseMessage [Response](#response)</span></span>

#### <span data-ttu-id="4d1e3-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4d1e3-131">GetDeferral</span></span> 

<span data-ttu-id="4d1e3-132">Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-132">Obtain a CoreWebView2Deferral object and put the event into a deferred state.</span></span>

> <span data-ttu-id="4d1e3-133">общедоступный [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) - [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="4d1e3-133">public [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="4d1e3-134">Вы можете использовать объект CoreWebView2Deferral для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="4d1e3-134">You can use the CoreWebView2Deferral object to complete the network request at a later time.</span></span>

