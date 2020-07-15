---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 826cdf960a20e32b8e0fa6b5a8ddad720ac137a6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877583"
---
# <span data-ttu-id="7e57a-104">0.9.430-Interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7e57a-104">0.9.430 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7e57a-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7e57a-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7e57a-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="7e57a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="7e57a-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="7e57a-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="7e57a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7e57a-108">Summary</span></span>

 <span data-ttu-id="7e57a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7e57a-109">Members</span></span>                        | <span data-ttu-id="7e57a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7e57a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7e57a-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="7e57a-111">get_Request</span></span>](#get_request) | <span data-ttu-id="7e57a-112">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="7e57a-112">The HTTP request.</span></span>
[<span data-ttu-id="7e57a-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="7e57a-113">get_Response</span></span>](#get_response) | <span data-ttu-id="7e57a-114">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="7e57a-114">The HTTP response.</span></span>
[<span data-ttu-id="7e57a-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="7e57a-115">put_Response</span></span>](#put_response) | <span data-ttu-id="7e57a-116">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="7e57a-116">Set the Response property.</span></span>
[<span data-ttu-id="7e57a-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7e57a-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="7e57a-118">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="7e57a-118">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="7e57a-119">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="7e57a-119">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="7e57a-120">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e57a-120">The web resource request contexts.</span></span>

## <span data-ttu-id="7e57a-121">Участников</span><span class="sxs-lookup"><span data-stu-id="7e57a-121">Members</span></span>

#### <span data-ttu-id="7e57a-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="7e57a-122">get_Request</span></span> 

<span data-ttu-id="7e57a-123">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="7e57a-123">The HTTP request.</span></span>

> <span data-ttu-id="7e57a-124">общедоступные значения HRESULT [get_Request](#get_request)(запрос[ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="7e57a-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="7e57a-125">get_Response</span><span class="sxs-lookup"><span data-stu-id="7e57a-125">get_Response</span></span> 

<span data-ttu-id="7e57a-126">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="7e57a-126">The HTTP response.</span></span>

> <span data-ttu-id="7e57a-127">общедоступные значения HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="7e57a-127">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="7e57a-128">put_Response</span><span class="sxs-lookup"><span data-stu-id="7e57a-128">put_Response</span></span> 

<span data-ttu-id="7e57a-129">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="7e57a-129">Set the Response property.</span></span>

> <span data-ttu-id="7e57a-130">общедоступные значения HRESULT [put_Response](#put_response)(ответ[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="7e57a-130">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="7e57a-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="7e57a-131">GetDeferral</span></span> 

<span data-ttu-id="7e57a-132">Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="7e57a-132">Obtain an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="7e57a-133">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="7e57a-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="7e57a-134">Вы можете использовать объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="7e57a-134">You can use the [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="7e57a-135">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="7e57a-135">get_ResourceContext</span></span> 

<span data-ttu-id="7e57a-136">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7e57a-136">The web resource request contexts.</span></span>

> <span data-ttu-id="7e57a-137">общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* контекст)</span><span class="sxs-lookup"><span data-stu-id="7e57a-137">public HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

