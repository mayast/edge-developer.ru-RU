---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: cdea3b4d4643e6f14e546eb9edd27bf1534beadd
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877352"
---
# <span data-ttu-id="96966-104">0.9.515-Interface ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="96966-104">0.9.515 - interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="96966-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="96966-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="96966-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="96966-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="96966-107">HTTP-запрос, используемый для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="96966-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="96966-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="96966-108">Summary</span></span>

 <span data-ttu-id="96966-109">Участников</span><span class="sxs-lookup"><span data-stu-id="96966-109">Members</span></span>                        | <span data-ttu-id="96966-110">Описания</span><span class="sxs-lookup"><span data-stu-id="96966-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="96966-111">get_Content</span><span class="sxs-lookup"><span data-stu-id="96966-111">get_Content</span></span>](#get_content) | <span data-ttu-id="96966-112">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="96966-112">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="96966-113">get_Headers</span><span class="sxs-lookup"><span data-stu-id="96966-113">get_Headers</span></span>](#get_headers) | <span data-ttu-id="96966-114">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="96966-114">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="96966-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="96966-115">get_Method</span></span>](#get_method) | <span data-ttu-id="96966-116">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="96966-116">The HTTP request method.</span></span>
[<span data-ttu-id="96966-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="96966-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="96966-118">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="96966-118">The request URI.</span></span>
[<span data-ttu-id="96966-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="96966-119">put_Content</span></span>](#put_content) | <span data-ttu-id="96966-120">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="96966-120">Set the Content property.</span></span>
[<span data-ttu-id="96966-121">put_Method</span><span class="sxs-lookup"><span data-stu-id="96966-121">put_Method</span></span>](#put_method) | <span data-ttu-id="96966-122">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="96966-122">Set the Method property.</span></span>
[<span data-ttu-id="96966-123">put_Uri</span><span class="sxs-lookup"><span data-stu-id="96966-123">put_Uri</span></span>](#put_uri) | <span data-ttu-id="96966-124">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="96966-124">Set the Uri property.</span></span>

## <span data-ttu-id="96966-125">Участников</span><span class="sxs-lookup"><span data-stu-id="96966-125">Members</span></span>

#### <span data-ttu-id="96966-126">get_Content</span><span class="sxs-lookup"><span data-stu-id="96966-126">get_Content</span></span> 

<span data-ttu-id="96966-127">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="96966-127">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="96966-128">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="96966-128">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="96966-129">Поместите здесь данные.</span><span class="sxs-lookup"><span data-stu-id="96966-129">POST data would be here.</span></span> <span data-ttu-id="96966-130">Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="96966-130">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="96966-131">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="96966-131">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="96966-132">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="96966-132">Null means no content data.</span></span> <span data-ttu-id="96966-133">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="96966-133">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="96966-134">get_Headers</span><span class="sxs-lookup"><span data-stu-id="96966-134">get_Headers</span></span> 

<span data-ttu-id="96966-135">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="96966-135">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="96966-136">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="96966-136">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="96966-137">get_Method</span><span class="sxs-lookup"><span data-stu-id="96966-137">get_Method</span></span> 

<span data-ttu-id="96966-138">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="96966-138">The HTTP request method.</span></span>

> <span data-ttu-id="96966-139">общедоступный [GET_METHOD](#get_method)HRESULT (метод LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="96966-139">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="96966-140">get_Uri</span><span class="sxs-lookup"><span data-stu-id="96966-140">get_Uri</span></span> 

<span data-ttu-id="96966-141">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="96966-141">The request URI.</span></span>

> <span data-ttu-id="96966-142">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="96966-142">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="96966-143">put_Content</span><span class="sxs-lookup"><span data-stu-id="96966-143">put_Content</span></span> 

<span data-ttu-id="96966-144">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="96966-144">Set the Content property.</span></span>

> <span data-ttu-id="96966-145">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="96966-145">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="96966-146">put_Method</span><span class="sxs-lookup"><span data-stu-id="96966-146">put_Method</span></span> 

<span data-ttu-id="96966-147">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="96966-147">Set the Method property.</span></span>

> <span data-ttu-id="96966-148">общедоступные значения HRESULT [put_Method](#put_method)(метод LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="96966-148">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="96966-149">put_Uri</span><span class="sxs-lookup"><span data-stu-id="96966-149">put_Uri</span></span> 

<span data-ttu-id="96966-150">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="96966-150">Set the Uri property.</span></span>

> <span data-ttu-id="96966-151">общедоступные значения HRESULT [put_Uri](#put_uri)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="96966-151">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

