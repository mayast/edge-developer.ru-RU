---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 82c94869a84165de4c3b8d09937d6ea5d1f79256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885690"
---
# <span data-ttu-id="792be-104">0.8.355-Interface IWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="792be-104">0.8.355 - interface IWebView2WebResourceResponse</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="792be-105">HTTP-ответ, используемый с событием WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="792be-105">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="792be-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="792be-106">Summary</span></span>

 <span data-ttu-id="792be-107">Участников</span><span class="sxs-lookup"><span data-stu-id="792be-107">Members</span></span>                        | <span data-ttu-id="792be-108">Описания</span><span class="sxs-lookup"><span data-stu-id="792be-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="792be-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="792be-109">get_Content</span></span>](#get_content) | <span data-ttu-id="792be-110">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="792be-110">HTTP response content as stream.</span></span>
[<span data-ttu-id="792be-111">put_Content</span><span class="sxs-lookup"><span data-stu-id="792be-111">put_Content</span></span>](#put_content) | <span data-ttu-id="792be-112">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="792be-112">Set the Content property.</span></span>
[<span data-ttu-id="792be-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="792be-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="792be-114">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="792be-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="792be-115">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="792be-115">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="792be-116">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="792be-116">The HTTP response status code.</span></span>
[<span data-ttu-id="792be-117">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="792be-117">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="792be-118">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="792be-118">Set the StatusCode property.</span></span>
[<span data-ttu-id="792be-119">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="792be-119">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="792be-120">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="792be-120">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="792be-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="792be-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="792be-122">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="792be-122">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="792be-123">Участников</span><span class="sxs-lookup"><span data-stu-id="792be-123">Members</span></span>

#### <span data-ttu-id="792be-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="792be-124">get_Content</span></span> 

<span data-ttu-id="792be-125">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="792be-125">HTTP response content as stream.</span></span>

> <span data-ttu-id="792be-126">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="792be-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="792be-127">Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="792be-127">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="792be-128">Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="792be-128">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="792be-129">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="792be-129">Null means no content data.</span></span> <span data-ttu-id="792be-130">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="792be-130">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="792be-131">put_Content</span><span class="sxs-lookup"><span data-stu-id="792be-131">put_Content</span></span> 

<span data-ttu-id="792be-132">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="792be-132">Set the Content property.</span></span>

> <span data-ttu-id="792be-133">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="792be-133">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="792be-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="792be-134">get_Headers</span></span> 

<span data-ttu-id="792be-135">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="792be-135">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="792be-136">общедоступные значения HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="792be-136">public HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="792be-137">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="792be-137">get_StatusCode</span></span> 

<span data-ttu-id="792be-138">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="792be-138">The HTTP response status code.</span></span>

> <span data-ttu-id="792be-139">общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="792be-139">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="792be-140">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="792be-140">put_StatusCode</span></span> 

<span data-ttu-id="792be-141">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="792be-141">Set the StatusCode property.</span></span>

> <span data-ttu-id="792be-142">общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="792be-142">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="792be-143">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="792be-143">get_ReasonPhrase</span></span> 

<span data-ttu-id="792be-144">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="792be-144">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="792be-145">общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="792be-145">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="792be-146">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="792be-146">put_ReasonPhrase</span></span> 

<span data-ttu-id="792be-147">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="792be-147">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="792be-148">общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="792be-148">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

