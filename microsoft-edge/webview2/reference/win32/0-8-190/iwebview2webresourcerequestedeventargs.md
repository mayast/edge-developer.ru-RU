---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 40474d6b1169467022e5bb47e82eba3883edc2aa
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878101"
---
# <span data-ttu-id="aaa7c-104">0.8.355-Interface IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="aaa7c-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="aaa7c-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="aaa7c-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="aaa7c-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="aaa7c-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="aaa7c-108">Summary</span></span>

 <span data-ttu-id="aaa7c-109">Участников</span><span class="sxs-lookup"><span data-stu-id="aaa7c-109">Members</span></span>                        | <span data-ttu-id="aaa7c-110">Описания</span><span class="sxs-lookup"><span data-stu-id="aaa7c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aaa7c-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="aaa7c-111">get_Request</span></span>](#get_request) | <span data-ttu-id="aaa7c-112">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-112">The HTTP request.</span></span>
[<span data-ttu-id="aaa7c-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="aaa7c-113">get_Response</span></span>](#get_response) | <span data-ttu-id="aaa7c-114">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-114">The HTTP response.</span></span>
[<span data-ttu-id="aaa7c-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="aaa7c-115">put_Response</span></span>](#put_response) | <span data-ttu-id="aaa7c-116">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="aaa7c-116">Set the Response property.</span></span>
[<span data-ttu-id="aaa7c-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="aaa7c-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="aaa7c-118">Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-118">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="aaa7c-119">Участников</span><span class="sxs-lookup"><span data-stu-id="aaa7c-119">Members</span></span>

#### <span data-ttu-id="aaa7c-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="aaa7c-120">get_Request</span></span> 

<span data-ttu-id="aaa7c-121">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-121">The HTTP request.</span></span>

> <span data-ttu-id="aaa7c-122">общедоступные значения HRESULT [get_Request](#get_request)(запрос[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="aaa7c-122">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="aaa7c-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="aaa7c-123">get_Response</span></span> 

<span data-ttu-id="aaa7c-124">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-124">The HTTP response.</span></span>

> <span data-ttu-id="aaa7c-125">общедоступные значения HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="aaa7c-125">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="aaa7c-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="aaa7c-126">put_Response</span></span> 

<span data-ttu-id="aaa7c-127">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="aaa7c-127">Set the Response property.</span></span>

> <span data-ttu-id="aaa7c-128">общедоступные значения HRESULT [put_Response](#put_response)(ответ[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="aaa7c-128">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="aaa7c-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="aaa7c-129">GetDeferral</span></span> 

<span data-ttu-id="aaa7c-130">Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-130">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="aaa7c-131">общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="aaa7c-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="aaa7c-132">Вы можете использовать объект [IWebView2Deferral](IWebView2Deferral.md) для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="aaa7c-132">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>

