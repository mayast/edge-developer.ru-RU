---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 61f731a948dee970731ba3dbe83426cbb40eb831
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884003"
---
# <span data-ttu-id="19f4a-104">0.9.430-Interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="19f4a-104">0.9.430 - interface ICoreWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="19f4a-105">HTTP-ответ, используемый с событием WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="19f4a-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="19f4a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="19f4a-106">Summary</span></span>

 <span data-ttu-id="19f4a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="19f4a-107">Members</span></span>                        | <span data-ttu-id="19f4a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="19f4a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="19f4a-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="19f4a-109">get_Content</span></span>](#get_content) | <span data-ttu-id="19f4a-110">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="19f4a-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="19f4a-111">put_Content</span><span class="sxs-lookup"><span data-stu-id="19f4a-111">put_Content</span></span>](#put_content) | <span data-ttu-id="19f4a-112">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="19f4a-112">Set the Content property.</span></span>
[<span data-ttu-id="19f4a-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="19f4a-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="19f4a-114">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="19f4a-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="19f4a-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="19f4a-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="19f4a-116">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="19f4a-116">The HTTP response status code.</span></span>
[<span data-ttu-id="19f4a-117">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="19f4a-117">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="19f4a-118">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="19f4a-118">Set the StatusCode property.</span></span>
[<span data-ttu-id="19f4a-119">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="19f4a-119">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="19f4a-120">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="19f4a-120">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="19f4a-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="19f4a-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="19f4a-122">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="19f4a-122">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="19f4a-123">Участников</span><span class="sxs-lookup"><span data-stu-id="19f4a-123">Members</span></span>

#### <span data-ttu-id="19f4a-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="19f4a-124">get_Content</span></span> 

<span data-ttu-id="19f4a-125">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="19f4a-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="19f4a-126">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="19f4a-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="19f4a-127">Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="19f4a-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="19f4a-128">Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="19f4a-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="19f4a-129">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="19f4a-129">Null means no content data.</span></span> <span data-ttu-id="19f4a-130">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="19f4a-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="19f4a-131">put_Content</span><span class="sxs-lookup"><span data-stu-id="19f4a-131">put_Content</span></span> 

<span data-ttu-id="19f4a-132">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="19f4a-132">Set the Content property.</span></span>

> <span data-ttu-id="19f4a-133">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="19f4a-133">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="19f4a-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="19f4a-134">get_Headers</span></span> 

<span data-ttu-id="19f4a-135">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="19f4a-135">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="19f4a-136">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="19f4a-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="19f4a-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="19f4a-137">get_StatusCode</span></span> 

<span data-ttu-id="19f4a-138">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="19f4a-138">The HTTP response status code.</span></span>

> <span data-ttu-id="19f4a-139">общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="19f4a-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="19f4a-140">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="19f4a-140">put_StatusCode</span></span> 

<span data-ttu-id="19f4a-141">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="19f4a-141">Set the StatusCode property.</span></span>

> <span data-ttu-id="19f4a-142">общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="19f4a-142">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="19f4a-143">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="19f4a-143">get_ReasonPhrase</span></span> 

<span data-ttu-id="19f4a-144">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="19f4a-144">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="19f4a-145">общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="19f4a-145">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="19f4a-146">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="19f4a-146">put_ReasonPhrase</span></span> 

<span data-ttu-id="19f4a-147">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="19f4a-147">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="19f4a-148">общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="19f4a-148">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

