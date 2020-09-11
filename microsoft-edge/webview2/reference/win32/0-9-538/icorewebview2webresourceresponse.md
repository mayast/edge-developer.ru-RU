---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebResourceResponse
ms.openlocfilehash: f94aa86f589f49930de9186cdca4a6ae943d286f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011386"
---
# <span data-ttu-id="f2ad8-104">0.9.579-Interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="f2ad8-104">0.9.579 - interface ICoreWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="f2ad8-105">HTTP-ответ, используемый с событием WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="f2ad8-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f2ad8-106">Summary</span></span>

 <span data-ttu-id="f2ad8-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f2ad8-107">Members</span></span>                        | <span data-ttu-id="f2ad8-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f2ad8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f2ad8-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="f2ad8-109">get_Content</span></span>](#get_content) | <span data-ttu-id="f2ad8-110">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="f2ad8-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="f2ad8-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="f2ad8-112">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-112">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="f2ad8-113">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f2ad8-113">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="f2ad8-114">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-114">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="f2ad8-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f2ad8-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="f2ad8-116">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-116">The HTTP response status code.</span></span>
[<span data-ttu-id="f2ad8-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="f2ad8-117">put_Content</span></span>](#put_content) | <span data-ttu-id="f2ad8-118">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="f2ad8-118">Set the Content property.</span></span>
[<span data-ttu-id="f2ad8-119">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f2ad8-119">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="f2ad8-120">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-120">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="f2ad8-121">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f2ad8-121">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="f2ad8-122">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-122">Set the StatusCode property.</span></span>

## <span data-ttu-id="f2ad8-123">Участников</span><span class="sxs-lookup"><span data-stu-id="f2ad8-123">Members</span></span>

#### <span data-ttu-id="f2ad8-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="f2ad8-124">get_Content</span></span> 

<span data-ttu-id="f2ad8-125">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="f2ad8-126">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="f2ad8-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="f2ad8-127">Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="f2ad8-128">Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="f2ad8-129">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-129">Null means no content data.</span></span> <span data-ttu-id="f2ad8-130">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="f2ad8-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="f2ad8-131">get_Headers</span><span class="sxs-lookup"><span data-stu-id="f2ad8-131">get_Headers</span></span> 

<span data-ttu-id="f2ad8-132">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-132">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="f2ad8-133">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="f2ad8-133">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="f2ad8-134">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f2ad8-134">get_ReasonPhrase</span></span> 

<span data-ttu-id="f2ad8-135">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-135">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="f2ad8-136">общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="f2ad8-136">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="f2ad8-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f2ad8-137">get_StatusCode</span></span> 

<span data-ttu-id="f2ad8-138">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-138">The HTTP response status code.</span></span>

> <span data-ttu-id="f2ad8-139">общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="f2ad8-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="f2ad8-140">put_Content</span><span class="sxs-lookup"><span data-stu-id="f2ad8-140">put_Content</span></span> 

<span data-ttu-id="f2ad8-141">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="f2ad8-141">Set the Content property.</span></span>

> <span data-ttu-id="f2ad8-142">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="f2ad8-142">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="f2ad8-143">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="f2ad8-143">put_ReasonPhrase</span></span> 

<span data-ttu-id="f2ad8-144">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-144">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="f2ad8-145">общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="f2ad8-145">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="f2ad8-146">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="f2ad8-146">put_StatusCode</span></span> 

<span data-ttu-id="f2ad8-147">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="f2ad8-147">Set the StatusCode property.</span></span>

> <span data-ttu-id="f2ad8-148">общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="f2ad8-148">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

