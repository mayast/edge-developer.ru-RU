---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 2d0660616de0c234b1535b2af127843fea3a3a53
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012427"
---
# <span data-ttu-id="b2147-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b2147-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseReceivedEventArgs class</span></span> 

<span data-ttu-id="b2147-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b2147-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b2147-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b2147-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b2147-107">Аргументы события для события WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="b2147-107">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="b2147-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b2147-108">Summary</span></span>

 <span data-ttu-id="b2147-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b2147-109">Members</span></span>                        | <span data-ttu-id="b2147-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b2147-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b2147-111">Запрос</span><span class="sxs-lookup"><span data-stu-id="b2147-111">Request</span></span>](#request) | <span data-ttu-id="b2147-112">Объект запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2147-112">Web resource request object.</span></span>
[<span data-ttu-id="b2147-113">Ответ</span><span class="sxs-lookup"><span data-stu-id="b2147-113">Response</span></span>](#response) | <span data-ttu-id="b2147-114">Объект ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="b2147-114">Web resource response object.</span></span>
[<span data-ttu-id="b2147-115">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="b2147-115">PopulateResponseContentAsync</span></span>](#populateresponsecontentasync) | <span data-ttu-id="b2147-116">Метод Async для запроса потока содержимого ответа.</span><span class="sxs-lookup"><span data-stu-id="b2147-116">Async method to request the Content stream of the response.</span></span>

## <span data-ttu-id="b2147-117">Участников</span><span class="sxs-lookup"><span data-stu-id="b2147-117">Members</span></span>

#### <span data-ttu-id="b2147-118">Запрос</span><span class="sxs-lookup"><span data-stu-id="b2147-118">Request</span></span> 

<span data-ttu-id="b2147-119">Объект запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="b2147-119">Web resource request object.</span></span>

> <span data-ttu-id="b2147-120">общедоступный [запрос](#request) [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md)</span><span class="sxs-lookup"><span data-stu-id="b2147-120">public [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md) [Request](#request)</span></span>

<span data-ttu-id="b2147-121">Все изменения, внесенные в этот объект, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="b2147-121">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="b2147-122">Ответ</span><span class="sxs-lookup"><span data-stu-id="b2147-122">Response</span></span> 

<span data-ttu-id="b2147-123">Объект ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="b2147-123">Web resource response object.</span></span>

> <span data-ttu-id="b2147-124">[ответ](#response) на общедоступные [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md)</span><span class="sxs-lookup"><span data-stu-id="b2147-124">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [Response](#response)</span></span>

<span data-ttu-id="b2147-125">Все изменения, внесенные в этот объект, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="b2147-125">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="b2147-126">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="b2147-126">PopulateResponseContentAsync</span></span> 

<span data-ttu-id="b2147-127">Метод Async для запроса потока содержимого ответа.</span><span class="sxs-lookup"><span data-stu-id="b2147-127">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="b2147-128">Public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()</span><span class="sxs-lookup"><span data-stu-id="b2147-128">public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()</span></span>

