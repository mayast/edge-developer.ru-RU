---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: aa5206be13790fd7a783f2afb4471de90fc8f2ae
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885720"
---
# <span data-ttu-id="2c35e-104">0.8.355-Interface IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2c35e-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="2c35e-105">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2c35e-105">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="2c35e-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2c35e-106">Summary</span></span>

 <span data-ttu-id="2c35e-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2c35e-107">Members</span></span>                        | <span data-ttu-id="2c35e-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2c35e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2c35e-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="2c35e-109">get_Request</span></span>](#get_request) | <span data-ttu-id="2c35e-110">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="2c35e-110">The HTTP request.</span></span>
[<span data-ttu-id="2c35e-111">get_Response</span><span class="sxs-lookup"><span data-stu-id="2c35e-111">get_Response</span></span>](#get_response) | <span data-ttu-id="2c35e-112">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="2c35e-112">The HTTP response.</span></span>
[<span data-ttu-id="2c35e-113">put_Response</span><span class="sxs-lookup"><span data-stu-id="2c35e-113">put_Response</span></span>](#put_response) | <span data-ttu-id="2c35e-114">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="2c35e-114">Set the Response property.</span></span>
[<span data-ttu-id="2c35e-115">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2c35e-115">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2c35e-116">Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="2c35e-116">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="2c35e-117">Участников</span><span class="sxs-lookup"><span data-stu-id="2c35e-117">Members</span></span>

#### <span data-ttu-id="2c35e-118">get_Request</span><span class="sxs-lookup"><span data-stu-id="2c35e-118">get_Request</span></span> 

<span data-ttu-id="2c35e-119">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="2c35e-119">The HTTP request.</span></span>

> <span data-ttu-id="2c35e-120">общедоступные значения HRESULT [get_Request](#get_request)(запрос[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="2c35e-120">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="2c35e-121">get_Response</span><span class="sxs-lookup"><span data-stu-id="2c35e-121">get_Response</span></span> 

<span data-ttu-id="2c35e-122">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="2c35e-122">The HTTP response.</span></span>

> <span data-ttu-id="2c35e-123">общедоступные значения HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="2c35e-123">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="2c35e-124">put_Response</span><span class="sxs-lookup"><span data-stu-id="2c35e-124">put_Response</span></span> 

<span data-ttu-id="2c35e-125">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="2c35e-125">Set the Response property.</span></span>

> <span data-ttu-id="2c35e-126">общедоступные значения HRESULT [put_Response](#put_response)(ответ[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="2c35e-126">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="2c35e-127">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2c35e-127">GetDeferral</span></span> 

<span data-ttu-id="2c35e-128">Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="2c35e-128">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="2c35e-129">общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="2c35e-129">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2c35e-130">Вы можете использовать объект [IWebView2Deferral](IWebView2Deferral.md) для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="2c35e-130">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>

