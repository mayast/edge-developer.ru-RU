---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 70a7d997dfd89b6d9bb8eb8af9a87ff0a130b69f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880306"
---
# <span data-ttu-id="be498-104">0.9.515-Interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="be498-104">0.9.515 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="be498-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="be498-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="be498-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="be498-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="be498-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="be498-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="be498-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="be498-108">Summary</span></span>

 <span data-ttu-id="be498-109">Участников</span><span class="sxs-lookup"><span data-stu-id="be498-109">Members</span></span>                        | <span data-ttu-id="be498-110">Описания</span><span class="sxs-lookup"><span data-stu-id="be498-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="be498-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="be498-111">get_Request</span></span>](#get_request) | <span data-ttu-id="be498-112">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="be498-112">The HTTP request.</span></span>
[<span data-ttu-id="be498-113">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="be498-113">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="be498-114">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be498-114">The web resource request contexts.</span></span>
[<span data-ttu-id="be498-115">get_Response</span><span class="sxs-lookup"><span data-stu-id="be498-115">get_Response</span></span>](#get_response) | <span data-ttu-id="be498-116">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="be498-116">The HTTP response.</span></span>
[<span data-ttu-id="be498-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="be498-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="be498-118">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="be498-118">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="be498-119">put_Response</span><span class="sxs-lookup"><span data-stu-id="be498-119">put_Response</span></span>](#put_response) | <span data-ttu-id="be498-120">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="be498-120">Set the Response property.</span></span>

## <span data-ttu-id="be498-121">Участников</span><span class="sxs-lookup"><span data-stu-id="be498-121">Members</span></span>

#### <span data-ttu-id="be498-122">get_Request</span><span class="sxs-lookup"><span data-stu-id="be498-122">get_Request</span></span> 

<span data-ttu-id="be498-123">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="be498-123">The HTTP request.</span></span>

> <span data-ttu-id="be498-124">общедоступные значения HRESULT [get_Request](#get_request)(запрос[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="be498-124">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

#### <span data-ttu-id="be498-125">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="be498-125">get_ResourceContext</span></span> 

<span data-ttu-id="be498-126">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="be498-126">The web resource request contexts.</span></span>

> <span data-ttu-id="be498-127">общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* контекст)</span><span class="sxs-lookup"><span data-stu-id="be498-127">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="be498-128">get_Response</span><span class="sxs-lookup"><span data-stu-id="be498-128">get_Response</span></span> 

<span data-ttu-id="be498-129">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="be498-129">The HTTP response.</span></span>

> <span data-ttu-id="be498-130">общедоступные значения HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="be498-130">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

#### <span data-ttu-id="be498-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="be498-131">GetDeferral</span></span> 

<span data-ttu-id="be498-132">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="be498-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="be498-133">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="be498-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="be498-134">Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="be498-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the network request at a later time.</span></span>

#### <span data-ttu-id="be498-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="be498-135">put_Response</span></span> 

<span data-ttu-id="be498-136">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="be498-136">Set the Response property.</span></span>

> <span data-ttu-id="be498-137">общедоступные значения HRESULT [put_Response](#put_response)(ответ[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="be498-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

