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
ms.openlocfilehash: c715a195a52d95e91095e006c71e50de46dc05e4
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699218"
---
# <span data-ttu-id="79c32-104">интерфейс ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="79c32-104">interface ICoreWebView2WebResourceRequest</span></span> 

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="79c32-105">HTTP-запрос, используемый для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="79c32-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="79c32-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="79c32-106">Summary</span></span>

 <span data-ttu-id="79c32-107">Участников</span><span class="sxs-lookup"><span data-stu-id="79c32-107">Members</span></span>                        | <span data-ttu-id="79c32-108">Описания</span><span class="sxs-lookup"><span data-stu-id="79c32-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="79c32-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="79c32-109">get_Content</span></span>](#get_content) | <span data-ttu-id="79c32-110">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="79c32-110">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="79c32-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="79c32-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="79c32-112">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="79c32-112">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="79c32-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="79c32-113">get_Method</span></span>](#get_method) | <span data-ttu-id="79c32-114">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="79c32-114">The HTTP request method.</span></span>
[<span data-ttu-id="79c32-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="79c32-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="79c32-116">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="79c32-116">The request URI.</span></span>
[<span data-ttu-id="79c32-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="79c32-117">put_Content</span></span>](#put_content) | <span data-ttu-id="79c32-118">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="79c32-118">Set the Content property.</span></span>
[<span data-ttu-id="79c32-119">put_Method</span><span class="sxs-lookup"><span data-stu-id="79c32-119">put_Method</span></span>](#put_method) | <span data-ttu-id="79c32-120">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="79c32-120">Set the Method property.</span></span>
[<span data-ttu-id="79c32-121">put_Uri</span><span class="sxs-lookup"><span data-stu-id="79c32-121">put_Uri</span></span>](#put_uri) | <span data-ttu-id="79c32-122">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="79c32-122">Set the Uri property.</span></span>

## <span data-ttu-id="79c32-123">Участников</span><span class="sxs-lookup"><span data-stu-id="79c32-123">Members</span></span>

#### <span data-ttu-id="79c32-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="79c32-124">get_Content</span></span> 

<span data-ttu-id="79c32-125">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="79c32-125">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="79c32-126">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="79c32-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="79c32-127">Поместите здесь данные.</span><span class="sxs-lookup"><span data-stu-id="79c32-127">POST data would be here.</span></span> <span data-ttu-id="79c32-128">Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="79c32-128">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="79c32-129">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="79c32-129">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="79c32-130">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="79c32-130">Null means no content data.</span></span> <span data-ttu-id="79c32-131">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="79c32-131">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="79c32-132">get_Headers</span><span class="sxs-lookup"><span data-stu-id="79c32-132">get_Headers</span></span> 

<span data-ttu-id="79c32-133">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="79c32-133">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="79c32-134">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="79c32-134">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="79c32-135">get_Method</span><span class="sxs-lookup"><span data-stu-id="79c32-135">get_Method</span></span> 

<span data-ttu-id="79c32-136">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="79c32-136">The HTTP request method.</span></span>

> <span data-ttu-id="79c32-137">общедоступный [GET_METHOD](#get_method)HRESULT (метод LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="79c32-137">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="79c32-138">get_Uri</span><span class="sxs-lookup"><span data-stu-id="79c32-138">get_Uri</span></span> 

<span data-ttu-id="79c32-139">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="79c32-139">The request URI.</span></span>

> <span data-ttu-id="79c32-140">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="79c32-140">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="79c32-141">put_Content</span><span class="sxs-lookup"><span data-stu-id="79c32-141">put_Content</span></span> 

<span data-ttu-id="79c32-142">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="79c32-142">Set the Content property.</span></span>

> <span data-ttu-id="79c32-143">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="79c32-143">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="79c32-144">put_Method</span><span class="sxs-lookup"><span data-stu-id="79c32-144">put_Method</span></span> 

<span data-ttu-id="79c32-145">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="79c32-145">Set the Method property.</span></span>

> <span data-ttu-id="79c32-146">общедоступные значения HRESULT [put_Method](#put_method)(метод LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="79c32-146">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="79c32-147">put_Uri</span><span class="sxs-lookup"><span data-stu-id="79c32-147">put_Uri</span></span> 

<span data-ttu-id="79c32-148">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="79c32-148">Set the Uri property.</span></span>

> <span data-ttu-id="79c32-149">общедоступные значения HRESULT [put_Uri](#put_uri)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="79c32-149">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

