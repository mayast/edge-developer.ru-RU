---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: a8c988fdfee72ed22e74886b440819d7a9d6fe24
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010513"
---
# <span data-ttu-id="65f66-104">класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="65f66-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2WebResourceResponseReceivedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="65f66-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="65f66-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="65f66-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="65f66-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="65f66-107">Аргументы события для события WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="65f66-107">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="65f66-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="65f66-108">Summary</span></span>

 <span data-ttu-id="65f66-109">Участников</span><span class="sxs-lookup"><span data-stu-id="65f66-109">Members</span></span>                        | <span data-ttu-id="65f66-110">Описания</span><span class="sxs-lookup"><span data-stu-id="65f66-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="65f66-111">Запрос</span><span class="sxs-lookup"><span data-stu-id="65f66-111">Request</span></span>](#request) | <span data-ttu-id="65f66-112">Объект запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="65f66-112">Web resource request object.</span></span>
[<span data-ttu-id="65f66-113">Ответ</span><span class="sxs-lookup"><span data-stu-id="65f66-113">Response</span></span>](#response) | <span data-ttu-id="65f66-114">Объект ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="65f66-114">Web resource response object.</span></span>
[<span data-ttu-id="65f66-115">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="65f66-115">PopulateResponseContentAsync</span></span>](#populateresponsecontentasync) | <span data-ttu-id="65f66-116">Метод Async для запроса потока содержимого ответа.</span><span class="sxs-lookup"><span data-stu-id="65f66-116">Async method to request the Content stream of the response.</span></span>

## <span data-ttu-id="65f66-117">Участников</span><span class="sxs-lookup"><span data-stu-id="65f66-117">Members</span></span>

#### <span data-ttu-id="65f66-118">Запрос</span><span class="sxs-lookup"><span data-stu-id="65f66-118">Request</span></span> 

<span data-ttu-id="65f66-119">Объект запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="65f66-119">Web resource request object.</span></span>

> <span data-ttu-id="65f66-120">общедоступный [запрос](#request) HttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="65f66-120">public HttpRequestMessage [Request](#request)</span></span>

<span data-ttu-id="65f66-121">Все изменения, внесенные в этот объект, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="65f66-121">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="65f66-122">Ответ</span><span class="sxs-lookup"><span data-stu-id="65f66-122">Response</span></span> 

<span data-ttu-id="65f66-123">Объект ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="65f66-123">Web resource response object.</span></span>

> <span data-ttu-id="65f66-124">[ответ](#response) на общедоступные HttpResponseMessage</span><span class="sxs-lookup"><span data-stu-id="65f66-124">public HttpResponseMessage [Response](#response)</span></span>

<span data-ttu-id="65f66-125">Все изменения, внесенные в этот объект, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="65f66-125">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="65f66-126">PopulateResponseContentAsync</span><span class="sxs-lookup"><span data-stu-id="65f66-126">PopulateResponseContentAsync</span></span> 

<span data-ttu-id="65f66-127">Метод Async для запроса потока содержимого ответа.</span><span class="sxs-lookup"><span data-stu-id="65f66-127">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="65f66-128">Public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()</span><span class="sxs-lookup"><span data-stu-id="65f66-128">public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()</span></span>

