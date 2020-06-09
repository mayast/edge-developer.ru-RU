---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 7072a25636efb638fcb42c593aa6cc77e990965a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699214"
---
# <span data-ttu-id="e7c20-104">интерфейс ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="e7c20-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="e7c20-105">HTTP-ответ, используемый с событием WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="e7c20-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="e7c20-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e7c20-106">Summary</span></span>

 <span data-ttu-id="e7c20-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e7c20-107">Members</span></span>                        | <span data-ttu-id="e7c20-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e7c20-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e7c20-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="e7c20-109">get_Content</span></span>](#get_content) | <span data-ttu-id="e7c20-110">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="e7c20-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="e7c20-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="e7c20-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="e7c20-112">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="e7c20-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="e7c20-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="e7c20-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="e7c20-114">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="e7c20-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="e7c20-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="e7c20-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="e7c20-116">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="e7c20-116">The HTTP response status code.</span></span>
[<span data-ttu-id="e7c20-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="e7c20-117">put_Content</span></span>](#put_content) | <span data-ttu-id="e7c20-118">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="e7c20-118">Set the Content property.</span></span>
[<span data-ttu-id="e7c20-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="e7c20-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="e7c20-120">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="e7c20-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="e7c20-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="e7c20-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="e7c20-122">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="e7c20-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="e7c20-123">Участников</span><span class="sxs-lookup"><span data-stu-id="e7c20-123">Members</span></span>

#### <span data-ttu-id="e7c20-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="e7c20-124">get_Content</span></span> 

<span data-ttu-id="e7c20-125">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="e7c20-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="e7c20-126">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="e7c20-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="e7c20-127">Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="e7c20-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="e7c20-128">Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e7c20-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="e7c20-129">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="e7c20-129">Null means no content data.</span></span> <span data-ttu-id="e7c20-130">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="e7c20-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="e7c20-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="e7c20-131">get_Headers</span></span> 

<span data-ttu-id="e7c20-132">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="e7c20-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="e7c20-133">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="e7c20-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="e7c20-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="e7c20-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="e7c20-135">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="e7c20-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="e7c20-136">общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="e7c20-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="e7c20-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="e7c20-137">get_StatusCode</span></span> 

<span data-ttu-id="e7c20-138">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="e7c20-138">The HTTP response status code.</span></span>

> <span data-ttu-id="e7c20-139">общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="e7c20-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="e7c20-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="e7c20-140">put_Content</span></span> 

<span data-ttu-id="e7c20-141">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="e7c20-141">Set the Content property.</span></span>

> <span data-ttu-id="e7c20-142">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="e7c20-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="e7c20-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="e7c20-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="e7c20-144">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="e7c20-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="e7c20-145">общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="e7c20-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="e7c20-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="e7c20-146">put_StatusCode</span></span> 

<span data-ttu-id="e7c20-147">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="e7c20-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="e7c20-148">общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="e7c20-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

