---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d6b51600479f47eebb09d5cff8fb096455fb1766
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654666"
---
# <span data-ttu-id="b3cc4-104">интерфейс ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="b3cc4-104">interface ICoreWebView2WebResourceResponse</span></span> 

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="b3cc4-105">HTTP-ответ, используемый с событием WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="b3cc4-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b3cc4-106">Summary</span></span>

 <span data-ttu-id="b3cc4-107">Участников</span><span class="sxs-lookup"><span data-stu-id="b3cc4-107">Members</span></span>                        | <span data-ttu-id="b3cc4-108">Описания</span><span class="sxs-lookup"><span data-stu-id="b3cc4-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b3cc4-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="b3cc4-109">get_Content</span></span>](#get_content) | <span data-ttu-id="b3cc4-110">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="b3cc4-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b3cc4-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="b3cc4-112">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="b3cc4-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b3cc4-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="b3cc4-114">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="b3cc4-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b3cc4-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="b3cc4-116">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-116">The HTTP response status code.</span></span>
[<span data-ttu-id="b3cc4-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="b3cc4-117">put_Content</span></span>](#put_content) | <span data-ttu-id="b3cc4-118">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="b3cc4-118">Set the Content property.</span></span>
[<span data-ttu-id="b3cc4-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b3cc4-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="b3cc4-120">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="b3cc4-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b3cc4-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="b3cc4-122">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="b3cc4-123">Участников</span><span class="sxs-lookup"><span data-stu-id="b3cc4-123">Members</span></span>

#### <span data-ttu-id="b3cc4-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="b3cc4-124">get_Content</span></span> 

<span data-ttu-id="b3cc4-125">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="b3cc4-126">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="b3cc4-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="b3cc4-127">Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="b3cc4-128">Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="b3cc4-129">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-129">Null means no content data.</span></span> <span data-ttu-id="b3cc4-130">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="b3cc4-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="b3cc4-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b3cc4-131">get_Headers</span></span> 

<span data-ttu-id="b3cc4-132">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="b3cc4-133">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="b3cc4-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="b3cc4-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b3cc4-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="b3cc4-135">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="b3cc4-136">общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="b3cc4-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="b3cc4-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b3cc4-137">get_StatusCode</span></span> 

<span data-ttu-id="b3cc4-138">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-138">The HTTP response status code.</span></span>

> <span data-ttu-id="b3cc4-139">общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="b3cc4-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="b3cc4-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="b3cc4-140">put_Content</span></span> 

<span data-ttu-id="b3cc4-141">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="b3cc4-141">Set the Content property.</span></span>

> <span data-ttu-id="b3cc4-142">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="b3cc4-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="b3cc4-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="b3cc4-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="b3cc4-144">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="b3cc4-145">общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="b3cc4-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="b3cc4-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="b3cc4-146">put_StatusCode</span></span> 

<span data-ttu-id="b3cc4-147">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="b3cc4-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="b3cc4-148">общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="b3cc4-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

