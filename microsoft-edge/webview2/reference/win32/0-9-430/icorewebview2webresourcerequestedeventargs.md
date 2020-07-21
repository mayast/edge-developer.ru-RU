---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 00aaddcc732076e4f7aa808b04132641fe7fe969
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886446"
---
# <span data-ttu-id="9ce9e-104">0.9.430-Interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9ce9e-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="9ce9e-105">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="9ce9e-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9ce9e-106">Summary</span></span>

 <span data-ttu-id="9ce9e-107">Участников</span><span class="sxs-lookup"><span data-stu-id="9ce9e-107">Members</span></span>                        | <span data-ttu-id="9ce9e-108">Описания</span><span class="sxs-lookup"><span data-stu-id="9ce9e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9ce9e-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="9ce9e-109">get_Request</span></span>](#get_request) | <span data-ttu-id="9ce9e-110">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-110">The HTTP request.</span></span>
[<span data-ttu-id="9ce9e-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="9ce9e-111">get_Response</span></span>](#get_response) | <span data-ttu-id="9ce9e-112">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-112">The HTTP response.</span></span>
[<span data-ttu-id="9ce9e-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="9ce9e-113">put_Response</span></span>](#put_response) | <span data-ttu-id="9ce9e-114">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="9ce9e-114">Set the Response property.</span></span>
[<span data-ttu-id="9ce9e-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9ce9e-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="9ce9e-116">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-116">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="9ce9e-117">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9ce9e-117">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="9ce9e-118">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-118">The web resource request contexts.</span></span>

## <span data-ttu-id="9ce9e-119">Участников</span><span class="sxs-lookup"><span data-stu-id="9ce9e-119">Members</span></span>

#### <span data-ttu-id="9ce9e-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="9ce9e-120">get_Request</span></span> 

<span data-ttu-id="9ce9e-121">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-121">The HTTP request.</span></span>

> <span data-ttu-id="9ce9e-122">общедоступные значения HRESULT [get_Request](#get_request)(запрос[ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="9ce9e-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="9ce9e-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="9ce9e-123">get_Response</span></span> 

<span data-ttu-id="9ce9e-124">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-124">The HTTP response.</span></span>

> <span data-ttu-id="9ce9e-125">общедоступные значения HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="9ce9e-125">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="9ce9e-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="9ce9e-126">put_Response</span></span> 

<span data-ttu-id="9ce9e-127">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="9ce9e-127">Set the Response property.</span></span>

> <span data-ttu-id="9ce9e-128">общедоступные значения HRESULT [put_Response](#put_response)(ответ[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="9ce9e-128">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="9ce9e-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="9ce9e-129">GetDeferral</span></span> 

<span data-ttu-id="9ce9e-130">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-130">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="9ce9e-131">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="9ce9e-131">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="9ce9e-132">Вы можете использовать объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-132">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="9ce9e-133">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="9ce9e-133">get_ResourceContext</span></span> 

<span data-ttu-id="9ce9e-134">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ce9e-134">The web resource request contexts.</span></span>

> <span data-ttu-id="9ce9e-135">общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* контекст)</span><span class="sxs-lookup"><span data-stu-id="9ce9e-135">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

