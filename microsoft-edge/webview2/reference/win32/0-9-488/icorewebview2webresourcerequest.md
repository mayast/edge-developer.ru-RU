---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b60df5b7493ab095c6e71f7d28dbb6ec78d39052
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883772"
---
# <span data-ttu-id="2d053-104">0.9.515-Interface ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="2d053-104">0.9.515 - interface ICoreWebView2WebResourceRequest</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="2d053-105">HTTP-запрос, используемый для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2d053-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="2d053-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2d053-106">Summary</span></span>

 <span data-ttu-id="2d053-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2d053-107">Members</span></span>                        | <span data-ttu-id="2d053-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2d053-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2d053-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="2d053-109">get_Content</span></span>](#get_content) | <span data-ttu-id="2d053-110">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="2d053-110">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="2d053-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="2d053-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="2d053-112">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="2d053-112">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="2d053-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="2d053-113">get_Method</span></span>](#get_method) | <span data-ttu-id="2d053-114">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="2d053-114">The HTTP request method.</span></span>
[<span data-ttu-id="2d053-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2d053-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2d053-116">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="2d053-116">The request URI.</span></span>
[<span data-ttu-id="2d053-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="2d053-117">put_Content</span></span>](#put_content) | <span data-ttu-id="2d053-118">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="2d053-118">Set the Content property.</span></span>
[<span data-ttu-id="2d053-119">put_Method</span><span class="sxs-lookup"><span data-stu-id="2d053-119">put_Method</span></span>](#put_method) | <span data-ttu-id="2d053-120">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="2d053-120">Set the Method property.</span></span>
[<span data-ttu-id="2d053-121">put_Uri</span><span class="sxs-lookup"><span data-stu-id="2d053-121">put_Uri</span></span>](#put_uri) | <span data-ttu-id="2d053-122">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="2d053-122">Set the Uri property.</span></span>

## <span data-ttu-id="2d053-123">Участников</span><span class="sxs-lookup"><span data-stu-id="2d053-123">Members</span></span>

#### <span data-ttu-id="2d053-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="2d053-124">get_Content</span></span> 

<span data-ttu-id="2d053-125">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="2d053-125">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="2d053-126">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="2d053-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="2d053-127">Поместите здесь данные.</span><span class="sxs-lookup"><span data-stu-id="2d053-127">POST data would be here.</span></span> <span data-ttu-id="2d053-128">Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="2d053-128">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="2d053-129">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2d053-129">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="2d053-130">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="2d053-130">Null means no content data.</span></span> <span data-ttu-id="2d053-131">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="2d053-131">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="2d053-132">get_Headers</span><span class="sxs-lookup"><span data-stu-id="2d053-132">get_Headers</span></span> 

<span data-ttu-id="2d053-133">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="2d053-133">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="2d053-134">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="2d053-134">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="2d053-135">get_Method</span><span class="sxs-lookup"><span data-stu-id="2d053-135">get_Method</span></span> 

<span data-ttu-id="2d053-136">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="2d053-136">The HTTP request method.</span></span>

> <span data-ttu-id="2d053-137">общедоступный [GET_METHOD](#get_method)HRESULT (метод LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="2d053-137">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="2d053-138">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2d053-138">get_Uri</span></span> 

<span data-ttu-id="2d053-139">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="2d053-139">The request URI.</span></span>

> <span data-ttu-id="2d053-140">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2d053-140">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2d053-141">put_Content</span><span class="sxs-lookup"><span data-stu-id="2d053-141">put_Content</span></span> 

<span data-ttu-id="2d053-142">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="2d053-142">Set the Content property.</span></span>

> <span data-ttu-id="2d053-143">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="2d053-143">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="2d053-144">put_Method</span><span class="sxs-lookup"><span data-stu-id="2d053-144">put_Method</span></span> 

<span data-ttu-id="2d053-145">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="2d053-145">Set the Method property.</span></span>

> <span data-ttu-id="2d053-146">общедоступные значения HRESULT [put_Method](#put_method)(метод LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2d053-146">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="2d053-147">put_Uri</span><span class="sxs-lookup"><span data-stu-id="2d053-147">put_Uri</span></span> 

<span data-ttu-id="2d053-148">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="2d053-148">Set the Uri property.</span></span>

> <span data-ttu-id="2d053-149">общедоступные значения HRESULT [put_Uri](#put_uri)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2d053-149">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

