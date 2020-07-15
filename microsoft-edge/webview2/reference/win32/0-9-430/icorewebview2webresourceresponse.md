---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c0c33bab95f8d2c7908864b1869bc9a186216ef9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877548"
---
# <span data-ttu-id="3eaea-104">0.9.430-Interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="3eaea-104">0.9.430 - interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="3eaea-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="3eaea-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="3eaea-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="3eaea-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="3eaea-107">HTTP-ответ, используемый с событием WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="3eaea-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="3eaea-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3eaea-108">Summary</span></span>

 <span data-ttu-id="3eaea-109">Участников</span><span class="sxs-lookup"><span data-stu-id="3eaea-109">Members</span></span>                        | <span data-ttu-id="3eaea-110">Описания</span><span class="sxs-lookup"><span data-stu-id="3eaea-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3eaea-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="3eaea-111">get_Content</span></span>](#get_content) | <span data-ttu-id="3eaea-112">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="3eaea-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="3eaea-113">put_Content</span><span class="sxs-lookup"><span data-stu-id="3eaea-113">put_Content</span></span>](#put_content) | <span data-ttu-id="3eaea-114">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="3eaea-114">Set the Content property.</span></span>
[<span data-ttu-id="3eaea-115">get_Headers</span><span class="sxs-lookup"><span data-stu-id="3eaea-115">get_Headers</span></span>](#get_headers) | <span data-ttu-id="3eaea-116">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="3eaea-116">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="3eaea-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3eaea-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="3eaea-118">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="3eaea-118">The HTTP response status code.</span></span>
[<span data-ttu-id="3eaea-119">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3eaea-119">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="3eaea-120">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="3eaea-120">Set the StatusCode property.</span></span>
[<span data-ttu-id="3eaea-121">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3eaea-121">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="3eaea-122">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="3eaea-122">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="3eaea-123">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3eaea-123">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="3eaea-124">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="3eaea-124">Set the ReasonPhrase property.</span></span>

## <span data-ttu-id="3eaea-125">Участников</span><span class="sxs-lookup"><span data-stu-id="3eaea-125">Members</span></span>

#### <span data-ttu-id="3eaea-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="3eaea-126">get_Content</span></span> 

<span data-ttu-id="3eaea-127">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="3eaea-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="3eaea-128">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="3eaea-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="3eaea-129">Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="3eaea-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="3eaea-130">Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="3eaea-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="3eaea-131">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="3eaea-131">Null means no content data.</span></span> <span data-ttu-id="3eaea-132">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="3eaea-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="3eaea-133">put_Content</span><span class="sxs-lookup"><span data-stu-id="3eaea-133">put_Content</span></span> 

<span data-ttu-id="3eaea-134">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="3eaea-134">Set the Content property.</span></span>

> <span data-ttu-id="3eaea-135">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="3eaea-135">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="3eaea-136">get_Headers</span><span class="sxs-lookup"><span data-stu-id="3eaea-136">get_Headers</span></span> 

<span data-ttu-id="3eaea-137">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="3eaea-137">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="3eaea-138">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="3eaea-138">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="3eaea-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3eaea-139">get_StatusCode</span></span> 

<span data-ttu-id="3eaea-140">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="3eaea-140">The HTTP response status code.</span></span>

> <span data-ttu-id="3eaea-141">общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="3eaea-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="3eaea-142">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="3eaea-142">put_StatusCode</span></span> 

<span data-ttu-id="3eaea-143">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="3eaea-143">Set the StatusCode property.</span></span>

> <span data-ttu-id="3eaea-144">общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="3eaea-144">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

#### <span data-ttu-id="3eaea-145">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3eaea-145">get_ReasonPhrase</span></span> 

<span data-ttu-id="3eaea-146">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="3eaea-146">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="3eaea-147">общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="3eaea-147">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="3eaea-148">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="3eaea-148">put_ReasonPhrase</span></span> 

<span data-ttu-id="3eaea-149">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="3eaea-149">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="3eaea-150">общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="3eaea-150">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

