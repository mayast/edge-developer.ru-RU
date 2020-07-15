---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 7a649944686df4d425141d5d22c03c5874572d1a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877345"
---
# <span data-ttu-id="bdd14-104">0.9.515-Interface ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="bdd14-104">0.9.515 - interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="bdd14-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="bdd14-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="bdd14-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="bdd14-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="bdd14-107">HTTP-ответ, используемый с событием WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="bdd14-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="bdd14-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="bdd14-108">Summary</span></span>

 <span data-ttu-id="bdd14-109">Участников</span><span class="sxs-lookup"><span data-stu-id="bdd14-109">Members</span></span>                        | <span data-ttu-id="bdd14-110">Описания</span><span class="sxs-lookup"><span data-stu-id="bdd14-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="bdd14-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="bdd14-111">get_Content</span></span>](#get_content) | <span data-ttu-id="bdd14-112">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="bdd14-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="bdd14-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="bdd14-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="bdd14-114">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="bdd14-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="bdd14-115">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="bdd14-115">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="bdd14-116">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="bdd14-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="bdd14-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="bdd14-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="bdd14-118">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="bdd14-118">The HTTP response status code.</span></span>
[<span data-ttu-id="bdd14-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="bdd14-119">put_Content</span></span>](#put_content) | <span data-ttu-id="bdd14-120">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="bdd14-120">Set the Content property.</span></span>
[<span data-ttu-id="bdd14-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="bdd14-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="bdd14-122">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="bdd14-122">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="bdd14-123">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="bdd14-123">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="bdd14-124">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="bdd14-124">Set the StatusCode property.</span></span>

## <span data-ttu-id="bdd14-125">Участников</span><span class="sxs-lookup"><span data-stu-id="bdd14-125">Members</span></span>

#### <span data-ttu-id="bdd14-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="bdd14-126">get_Content</span></span> 

<span data-ttu-id="bdd14-127">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="bdd14-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="bdd14-128">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="bdd14-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="bdd14-129">Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="bdd14-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="bdd14-130">Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bdd14-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="bdd14-131">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="bdd14-131">Null means no content data.</span></span> <span data-ttu-id="bdd14-132">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="bdd14-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="bdd14-133">get_Headers</span><span class="sxs-lookup"><span data-stu-id="bdd14-133">get_Headers</span></span> 

<span data-ttu-id="bdd14-134">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="bdd14-134">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="bdd14-135">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="bdd14-135">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="bdd14-136">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="bdd14-136">get_ReasonPhrase</span></span> 

<span data-ttu-id="bdd14-137">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="bdd14-137">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="bdd14-138">общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="bdd14-138">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="bdd14-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="bdd14-139">get_StatusCode</span></span> 

<span data-ttu-id="bdd14-140">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="bdd14-140">The HTTP response status code.</span></span>

> <span data-ttu-id="bdd14-141">общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="bdd14-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="bdd14-142">put_Content</span><span class="sxs-lookup"><span data-stu-id="bdd14-142">put_Content</span></span> 

<span data-ttu-id="bdd14-143">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="bdd14-143">Set the Content property.</span></span>

> <span data-ttu-id="bdd14-144">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="bdd14-144">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="bdd14-145">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="bdd14-145">put_ReasonPhrase</span></span> 

<span data-ttu-id="bdd14-146">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="bdd14-146">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="bdd14-147">общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="bdd14-147">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="bdd14-148">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="bdd14-148">put_StatusCode</span></span> 

<span data-ttu-id="bdd14-149">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="bdd14-149">Set the StatusCode property.</span></span>

> <span data-ttu-id="bdd14-150">общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="bdd14-150">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

