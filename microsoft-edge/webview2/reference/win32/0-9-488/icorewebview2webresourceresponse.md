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
ms.openlocfilehash: 5b80691f0e42be4cdea7c99b165bfe9cebf632dd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697933"
---
# <span data-ttu-id="66a8e-104">интерфейс ICoreWebView2WebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="66a8e-104">interface ICoreWebView2WebResourceResponse</span></span> 

> [!NOTE]
> <span data-ttu-id="66a8e-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="66a8e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="66a8e-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="66a8e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

<span data-ttu-id="66a8e-107">HTTP-ответ, используемый с событием WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="66a8e-107">An HTTP response used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="66a8e-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="66a8e-108">Summary</span></span>

 <span data-ttu-id="66a8e-109">Участников</span><span class="sxs-lookup"><span data-stu-id="66a8e-109">Members</span></span>                        | <span data-ttu-id="66a8e-110">Описания</span><span class="sxs-lookup"><span data-stu-id="66a8e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="66a8e-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="66a8e-111">get_Content</span></span>](#get_content) | <span data-ttu-id="66a8e-112">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="66a8e-112">HTTP response content as stream.</span></span>
[<span data-ttu-id="66a8e-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="66a8e-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="66a8e-114">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="66a8e-114">Overridden HTTP response headers.</span></span>
[<span data-ttu-id="66a8e-115">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="66a8e-115">get_ReasonPhrase</span></span>](#get_reasonphrase) | <span data-ttu-id="66a8e-116">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="66a8e-116">The HTTP response reason phrase.</span></span>
[<span data-ttu-id="66a8e-117">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="66a8e-117">get_StatusCode</span></span>](#get_statuscode) | <span data-ttu-id="66a8e-118">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="66a8e-118">The HTTP response status code.</span></span>
[<span data-ttu-id="66a8e-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="66a8e-119">put_Content</span></span>](#put_content) | <span data-ttu-id="66a8e-120">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="66a8e-120">Set the Content property.</span></span>
[<span data-ttu-id="66a8e-121">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="66a8e-121">put_ReasonPhrase</span></span>](#put_reasonphrase) | <span data-ttu-id="66a8e-122">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="66a8e-122">Set the ReasonPhrase property.</span></span>
[<span data-ttu-id="66a8e-123">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="66a8e-123">put_StatusCode</span></span>](#put_statuscode) | <span data-ttu-id="66a8e-124">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="66a8e-124">Set the StatusCode property.</span></span>

## <span data-ttu-id="66a8e-125">Участников</span><span class="sxs-lookup"><span data-stu-id="66a8e-125">Members</span></span>

#### <span data-ttu-id="66a8e-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="66a8e-126">get_Content</span></span> 

<span data-ttu-id="66a8e-127">Содержимое ответа HTTP в виде потока.</span><span class="sxs-lookup"><span data-stu-id="66a8e-127">HTTP response content as stream.</span></span>

> <span data-ttu-id="66a8e-128">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="66a8e-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="66a8e-129">Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="66a8e-129">Stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="66a8e-130">Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="66a8e-130">Stream should be agile or be created from a background thread to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="66a8e-131">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="66a8e-131">Null means no content data.</span></span> <span data-ttu-id="66a8e-132">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="66a8e-132">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="66a8e-133">get_Headers</span><span class="sxs-lookup"><span data-stu-id="66a8e-133">get_Headers</span></span> 

<span data-ttu-id="66a8e-134">Переопределенные заголовки HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="66a8e-134">Overridden HTTP response headers.</span></span>

> <span data-ttu-id="66a8e-135">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="66a8e-135">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="66a8e-136">get_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="66a8e-136">get_ReasonPhrase</span></span> 

<span data-ttu-id="66a8e-137">Фраза причина HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="66a8e-137">The HTTP response reason phrase.</span></span>

> <span data-ttu-id="66a8e-138">общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="66a8e-138">public HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR \* reasonPhrase)</span></span>

#### <span data-ttu-id="66a8e-139">get_StatusCode</span><span class="sxs-lookup"><span data-stu-id="66a8e-139">get_StatusCode</span></span> 

<span data-ttu-id="66a8e-140">Код состояния HTTP-ответа.</span><span class="sxs-lookup"><span data-stu-id="66a8e-140">The HTTP response status code.</span></span>

> <span data-ttu-id="66a8e-141">общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int \* StatusCode)</span><span class="sxs-lookup"><span data-stu-id="66a8e-141">public HRESULT [get_StatusCode](#get_statuscode)(int \* statusCode)</span></span>

#### <span data-ttu-id="66a8e-142">put_Content</span><span class="sxs-lookup"><span data-stu-id="66a8e-142">put_Content</span></span> 

<span data-ttu-id="66a8e-143">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="66a8e-143">Set the Content property.</span></span>

> <span data-ttu-id="66a8e-144">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="66a8e-144">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="66a8e-145">put_ReasonPhrase</span><span class="sxs-lookup"><span data-stu-id="66a8e-145">put_ReasonPhrase</span></span> 

<span data-ttu-id="66a8e-146">Задайте свойство ReasonPhrase.</span><span class="sxs-lookup"><span data-stu-id="66a8e-146">Set the ReasonPhrase property.</span></span>

> <span data-ttu-id="66a8e-147">общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)</span><span class="sxs-lookup"><span data-stu-id="66a8e-147">public HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR reasonPhrase)</span></span>

#### <span data-ttu-id="66a8e-148">put_StatusCode</span><span class="sxs-lookup"><span data-stu-id="66a8e-148">put_StatusCode</span></span> 

<span data-ttu-id="66a8e-149">Задайте Свойство StatusCode.</span><span class="sxs-lookup"><span data-stu-id="66a8e-149">Set the StatusCode property.</span></span>

> <span data-ttu-id="66a8e-150">общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)</span><span class="sxs-lookup"><span data-stu-id="66a8e-150">public HRESULT [put_StatusCode](#put_statuscode)(int statusCode)</span></span>

