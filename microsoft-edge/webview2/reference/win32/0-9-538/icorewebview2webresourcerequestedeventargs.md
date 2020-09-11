---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 2e55a43282a7548acefdb0b1ed1b8cac2254ef21
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010392"
---
# <span data-ttu-id="2e0c4-104">0.9.579-Interface ICoreWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2e0c4-104">0.9.579 - interface ICoreWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="2e0c4-105">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="2e0c4-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2e0c4-106">Summary</span></span>

 <span data-ttu-id="2e0c4-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2e0c4-107">Members</span></span>                        | <span data-ttu-id="2e0c4-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2e0c4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2e0c4-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="2e0c4-109">get_Request</span></span>](#get_request) | <span data-ttu-id="2e0c4-110">Запрос на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-110">The Web resource request.</span></span>
[<span data-ttu-id="2e0c4-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2e0c4-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="2e0c4-112">Контекст запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-112">The web resource request context.</span></span>
[<span data-ttu-id="2e0c4-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="2e0c4-113">get_Response</span></span>](#get_response) | <span data-ttu-id="2e0c4-114">Заполнитель для объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-114">A placeholder for the web resource response object.</span></span>
[<span data-ttu-id="2e0c4-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2e0c4-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2e0c4-116">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-116">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>
[<span data-ttu-id="2e0c4-117">put_Response</span><span class="sxs-lookup"><span data-stu-id="2e0c4-117">put_Response</span></span>](#put_response) | <span data-ttu-id="2e0c4-118">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="2e0c4-118">Set the Response property.</span></span>

## <span data-ttu-id="2e0c4-119">Участников</span><span class="sxs-lookup"><span data-stu-id="2e0c4-119">Members</span></span>

#### <span data-ttu-id="2e0c4-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="2e0c4-120">get_Request</span></span> 

<span data-ttu-id="2e0c4-121">Запрос на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-121">The Web resource request.</span></span>

> <span data-ttu-id="2e0c4-122">общедоступные значения HRESULT [get_Request](#get_request)(запрос[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="2e0c4-122">public HRESULT [get_Request](#get_request)([ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) \*\* request)</span></span>

<span data-ttu-id="2e0c4-123">Возможно, в объекте Request отсутствует часть заголовков, добавленных в разделе "сетевой стек".</span><span class="sxs-lookup"><span data-stu-id="2e0c4-123">The request object may be missing some headers that are added by network stack later on.</span></span>

#### <span data-ttu-id="2e0c4-124">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="2e0c4-124">get_ResourceContext</span></span> 

<span data-ttu-id="2e0c4-125">Контекст запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-125">The web resource request context.</span></span>

> <span data-ttu-id="2e0c4-126">общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* контекст)</span><span class="sxs-lookup"><span data-stu-id="2e0c4-126">public HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

#### <span data-ttu-id="2e0c4-127">get_Response</span><span class="sxs-lookup"><span data-stu-id="2e0c4-127">get_Response</span></span> 

<span data-ttu-id="2e0c4-128">Заполнитель для объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-128">A placeholder for the web resource response object.</span></span>

> <span data-ttu-id="2e0c4-129">общедоступные значения HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="2e0c4-129">public HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*\* response)</span></span>

<span data-ttu-id="2e0c4-130">Если этот объект задан, запрос на веб-ресурс будет выполнен с этим ответом.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-130">If this object is set, the web resource request will be completed with this response.</span></span>

#### <span data-ttu-id="2e0c4-131">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2e0c4-131">GetDeferral</span></span> 

<span data-ttu-id="2e0c4-132">Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-132">Obtain an [ICoreWebView2Deferral](icorewebview2deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="2e0c4-133">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="2e0c4-133">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2e0c4-134">Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) , чтобы выполнить запрос позже.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-134">You can use the [ICoreWebView2Deferral](icorewebview2deferral.md) object to complete the request at a later time.</span></span>

#### <span data-ttu-id="2e0c4-135">put_Response</span><span class="sxs-lookup"><span data-stu-id="2e0c4-135">put_Response</span></span> 

<span data-ttu-id="2e0c4-136">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="2e0c4-136">Set the Response property.</span></span>

> <span data-ttu-id="2e0c4-137">общедоступные значения HRESULT [put_Response](#put_response)(ответ[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="2e0c4-137">public HRESULT [put_Response](#put_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) \* response)</span></span>

<span data-ttu-id="2e0c4-138">Пустой объект ответа на веб-ресурс можно создать с помощью CreateWebResourceResponse и затем изменить для создания ответа.</span><span class="sxs-lookup"><span data-stu-id="2e0c4-138">An empty Web resource response object can be created with CreateWebResourceResponse and then modified to construct the response.</span></span>

