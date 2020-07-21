---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 44fc4f47aa10a7e409ac584cb75b750048056e47
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886529"
---
# <span data-ttu-id="fafcd-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="fafcd-104">Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseReceivedEventArgs class</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="fafcd-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fafcd-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fafcd-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="fafcd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fafcd-107">Аргументы события для события WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="fafcd-107">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="fafcd-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fafcd-108">Summary</span></span>

 <span data-ttu-id="fafcd-109">Участников</span><span class="sxs-lookup"><span data-stu-id="fafcd-109">Members</span></span>                        | <span data-ttu-id="fafcd-110">Описания</span><span class="sxs-lookup"><span data-stu-id="fafcd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fafcd-111">Запрос</span><span class="sxs-lookup"><span data-stu-id="fafcd-111">Request</span></span>](#request) | <span data-ttu-id="fafcd-112">Объект запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="fafcd-112">Web resource request object.</span></span>
[<span data-ttu-id="fafcd-113">Ответ</span><span class="sxs-lookup"><span data-stu-id="fafcd-113">Response</span></span>](#response) | <span data-ttu-id="fafcd-114">Объект ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="fafcd-114">Web resource response object.</span></span>
[<span data-ttu-id="fafcd-115">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="fafcd-115">PopulateResponseContentAsync</span></span>](#populateresponsecontentasync) | <span data-ttu-id="fafcd-116">Метод Async для запроса потока содержимого ответа.</span><span class="sxs-lookup"><span data-stu-id="fafcd-116">Async method to request the Content stream of the response.</span></span>

## <span data-ttu-id="fafcd-117">Участников</span><span class="sxs-lookup"><span data-stu-id="fafcd-117">Members</span></span>

#### <span data-ttu-id="fafcd-118">Запрос</span><span class="sxs-lookup"><span data-stu-id="fafcd-118">Request</span></span> 

<span data-ttu-id="fafcd-119">Объект запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="fafcd-119">Web resource request object.</span></span>

> <span data-ttu-id="fafcd-120">общедоступный [запрос](#request) HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="fafcd-120">public HttpRequestMessage [Request](#request)</span></span>

<span data-ttu-id="fafcd-121">Все изменения, внесенные в этот объект, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="fafcd-121">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="fafcd-122">Ответ</span><span class="sxs-lookup"><span data-stu-id="fafcd-122">Response</span></span> 

<span data-ttu-id="fafcd-123">Объект ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="fafcd-123">Web resource response object.</span></span>

> <span data-ttu-id="fafcd-124">[ответ](#response) на общедоступные HttpResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fafcd-124">public HttpResponseMessage [Response](#response)</span></span>

<span data-ttu-id="fafcd-125">Все изменения, внесенные в этот объект, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="fafcd-125">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="fafcd-126">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="fafcd-126">PopulateResponseContentAsync</span></span> 

<span data-ttu-id="fafcd-127">Метод Async для запроса потока содержимого ответа.</span><span class="sxs-lookup"><span data-stu-id="fafcd-127">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="fafcd-128">Public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()</span><span class="sxs-lookup"><span data-stu-id="fafcd-128">public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()</span></span>

