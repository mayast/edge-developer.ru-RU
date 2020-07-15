---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 3613ed9b2ef562e8760de1a88322ef028ddf4ca9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879221"
---
# <span data-ttu-id="85bae-104">интерфейс ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="85bae-104">interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="85bae-105">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="85bae-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="85bae-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="85bae-106">Summary</span></span>

 <span data-ttu-id="85bae-107">Участников</span><span class="sxs-lookup"><span data-stu-id="85bae-107">Members</span></span>                        | <span data-ttu-id="85bae-108">Описания</span><span class="sxs-lookup"><span data-stu-id="85bae-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="85bae-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="85bae-109">get_Request</span></span>](#get_request) | <span data-ttu-id="85bae-110">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="85bae-110">The HTTP request.</span></span>
[<span data-ttu-id="85bae-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="85bae-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="85bae-112">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85bae-112">The web resource request contexts.</span></span>
[<span data-ttu-id="85bae-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="85bae-113">get_Response</span></span>](#get_response) | <span data-ttu-id="85bae-114">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="85bae-114">The HTTP response.</span></span>
[<span data-ttu-id="85bae-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="85bae-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="85bae-116">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="85bae-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="85bae-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="85bae-117">put_Response</span></span>](#put_response) | <span data-ttu-id="85bae-118">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="85bae-118">Set the Response property.</span></span>

## <span data-ttu-id="85bae-119">Участников</span><span class="sxs-lookup"><span data-stu-id="85bae-119">Members</span></span>

#### <span data-ttu-id="85bae-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="85bae-120">get_Request</span></span> 

<span data-ttu-id="85bae-121">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="85bae-121">The HTTP request.</span></span>

> <span data-ttu-id="85bae-122">общедоступные значения HRESULT [get_Request](#get_request)(запрос[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="85bae-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="85bae-123">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="85bae-123">get_ResourceContext</span></span> 

<span data-ttu-id="85bae-124">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85bae-124">The web resource request contexts.</span></span>

> <span data-ttu-id="85bae-125">общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* контекст)</span><span class="sxs-lookup"><span data-stu-id="85bae-125">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="85bae-126">get_Response</span><span class="sxs-lookup"><span data-stu-id="85bae-126">get_Response</span></span> 

<span data-ttu-id="85bae-127">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="85bae-127">The HTTP response.</span></span>

> <span data-ttu-id="85bae-128">общедоступные значения HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="85bae-128">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="85bae-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="85bae-129">GetDeferral</span></span> 

<span data-ttu-id="85bae-130">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="85bae-130">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="85bae-131">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="85bae-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="85bae-132">Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="85bae-132">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="85bae-133">put_Response</span><span class="sxs-lookup"><span data-stu-id="85bae-133">put_Response</span></span> 

<span data-ttu-id="85bae-134">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="85bae-134">Set the Response property.</span></span>

> <span data-ttu-id="85bae-135">общедоступные значения HRESULT [put_Response](#put_response)(ответ[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="85bae-135">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

