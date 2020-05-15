---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 899a6f50db1d77f3f24524c5ccec139dcbdbcaf9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654685"
---
# <span data-ttu-id="67d74-104">интерфейс IWebView2WebResourceRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="67d74-104">interface IWebView2WebResourceRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="67d74-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="67d74-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="67d74-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="67d74-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="67d74-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="67d74-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="67d74-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="67d74-108">Summary</span></span>

 <span data-ttu-id="67d74-109">Участников</span><span class="sxs-lookup"><span data-stu-id="67d74-109">Members</span></span>                        | <span data-ttu-id="67d74-110">Описания</span><span class="sxs-lookup"><span data-stu-id="67d74-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67d74-111">get_Request</span><span class="sxs-lookup"><span data-stu-id="67d74-111">get_Request</span></span>](#get_request) | <span data-ttu-id="67d74-112">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="67d74-112">The HTTP request.</span></span>
[<span data-ttu-id="67d74-113">get_Response</span><span class="sxs-lookup"><span data-stu-id="67d74-113">get_Response</span></span>](#get_response) | <span data-ttu-id="67d74-114">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="67d74-114">The HTTP response.</span></span>
[<span data-ttu-id="67d74-115">put_Response</span><span class="sxs-lookup"><span data-stu-id="67d74-115">put_Response</span></span>](#put_response) | <span data-ttu-id="67d74-116">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="67d74-116">Set the Response property.</span></span>
[<span data-ttu-id="67d74-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="67d74-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="67d74-118">Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="67d74-118">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

## <span data-ttu-id="67d74-119">Участников</span><span class="sxs-lookup"><span data-stu-id="67d74-119">Members</span></span>

#### <span data-ttu-id="67d74-120">get_Request</span><span class="sxs-lookup"><span data-stu-id="67d74-120">get_Request</span></span> 

<span data-ttu-id="67d74-121">HTTP-запрос.</span><span class="sxs-lookup"><span data-stu-id="67d74-121">The HTTP request.</span></span>

> <span data-ttu-id="67d74-122">общедоступные значения HRESULT [get_Request](#get_request)(запрос[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="67d74-122">public HRESULT [get_Request](#get_request)([IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) \*\* request)</span></span>

#### <span data-ttu-id="67d74-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="67d74-123">get_Response</span></span> 

<span data-ttu-id="67d74-124">Ответ HTTP.</span><span class="sxs-lookup"><span data-stu-id="67d74-124">The HTTP response.</span></span>

> <span data-ttu-id="67d74-125">общедоступные значения HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="67d74-125">public HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

#### <span data-ttu-id="67d74-126">put_Response</span><span class="sxs-lookup"><span data-stu-id="67d74-126">put_Response</span></span> 

<span data-ttu-id="67d74-127">Задайте свойство Response (ответ).</span><span class="sxs-lookup"><span data-stu-id="67d74-127">Set the Response property.</span></span>

> <span data-ttu-id="67d74-128">общедоступные значения HRESULT [put_Response](#put_response)(ответ[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*)</span><span class="sxs-lookup"><span data-stu-id="67d74-128">public HRESULT [put_Response](#put_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* response)</span></span>

#### <span data-ttu-id="67d74-129">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="67d74-129">GetDeferral</span></span> 

<span data-ttu-id="67d74-130">Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.</span><span class="sxs-lookup"><span data-stu-id="67d74-130">Obtain an [IWebView2Deferral](IWebView2Deferral.md) object and put the event into a deferred state.</span></span>

> <span data-ttu-id="67d74-131">общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="67d74-131">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="67d74-132">Вы можете использовать объект [IWebView2Deferral](IWebView2Deferral.md) для выполнения сетевого запроса позже.</span><span class="sxs-lookup"><span data-stu-id="67d74-132">You can use the [IWebView2Deferral](IWebView2Deferral.md) object to complete the network request at a later time.</span></span>

