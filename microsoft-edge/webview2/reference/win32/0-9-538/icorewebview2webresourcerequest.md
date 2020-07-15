---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebResourceRequest
ms.openlocfilehash: 4ce5b04d2349c2ad63e68e9977fa9b9bcea7efec
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879291"
---
# <span data-ttu-id="2783b-104">интерфейс ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="2783b-104">interface ICoreWebView2WebResourceRequest</span></span> 

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="2783b-105">HTTP-запрос, используемый для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="2783b-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="2783b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2783b-106">Summary</span></span>

 <span data-ttu-id="2783b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2783b-107">Members</span></span>                        | <span data-ttu-id="2783b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2783b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2783b-109">get_Content</span><span class="sxs-lookup"><span data-stu-id="2783b-109">get_Content</span></span>](#get_content) | <span data-ttu-id="2783b-110">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="2783b-110">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="2783b-111">get_Headers</span><span class="sxs-lookup"><span data-stu-id="2783b-111">get_Headers</span></span>](#get_headers) | <span data-ttu-id="2783b-112">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="2783b-112">The mutable HTTP request headers.</span></span>
[<span data-ttu-id="2783b-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="2783b-113">get_Method</span></span>](#get_method) | <span data-ttu-id="2783b-114">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="2783b-114">The HTTP request method.</span></span>
[<span data-ttu-id="2783b-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2783b-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2783b-116">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="2783b-116">The request URI.</span></span>
[<span data-ttu-id="2783b-117">put_Content</span><span class="sxs-lookup"><span data-stu-id="2783b-117">put_Content</span></span>](#put_content) | <span data-ttu-id="2783b-118">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="2783b-118">Set the Content property.</span></span>
[<span data-ttu-id="2783b-119">put_Method</span><span class="sxs-lookup"><span data-stu-id="2783b-119">put_Method</span></span>](#put_method) | <span data-ttu-id="2783b-120">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="2783b-120">Set the Method property.</span></span>
[<span data-ttu-id="2783b-121">put_Uri</span><span class="sxs-lookup"><span data-stu-id="2783b-121">put_Uri</span></span>](#put_uri) | <span data-ttu-id="2783b-122">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="2783b-122">Set the Uri property.</span></span>

## <span data-ttu-id="2783b-123">Участников</span><span class="sxs-lookup"><span data-stu-id="2783b-123">Members</span></span>

#### <span data-ttu-id="2783b-124">get_Content</span><span class="sxs-lookup"><span data-stu-id="2783b-124">get_Content</span></span> 

<span data-ttu-id="2783b-125">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="2783b-125">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="2783b-126">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="2783b-126">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="2783b-127">Поместите здесь данные.</span><span class="sxs-lookup"><span data-stu-id="2783b-127">POST data would be here.</span></span> <span data-ttu-id="2783b-128">Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="2783b-128">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="2783b-129">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="2783b-129">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="2783b-130">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="2783b-130">Null means no content data.</span></span> <span data-ttu-id="2783b-131">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="2783b-131">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="2783b-132">get_Headers</span><span class="sxs-lookup"><span data-stu-id="2783b-132">get_Headers</span></span> 

<span data-ttu-id="2783b-133">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="2783b-133">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="2783b-134">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="2783b-134">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* headers)</span></span>

#### <span data-ttu-id="2783b-135">get_Method</span><span class="sxs-lookup"><span data-stu-id="2783b-135">get_Method</span></span> 

<span data-ttu-id="2783b-136">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="2783b-136">The HTTP request method.</span></span>

> <span data-ttu-id="2783b-137">общедоступный [GET_METHOD](#get_method)HRESULT (метод LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="2783b-137">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="2783b-138">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2783b-138">get_Uri</span></span> 

<span data-ttu-id="2783b-139">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="2783b-139">The request URI.</span></span>

> <span data-ttu-id="2783b-140">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2783b-140">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2783b-141">put_Content</span><span class="sxs-lookup"><span data-stu-id="2783b-141">put_Content</span></span> 

<span data-ttu-id="2783b-142">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="2783b-142">Set the Content property.</span></span>

> <span data-ttu-id="2783b-143">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="2783b-143">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="2783b-144">put_Method</span><span class="sxs-lookup"><span data-stu-id="2783b-144">put_Method</span></span> 

<span data-ttu-id="2783b-145">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="2783b-145">Set the Method property.</span></span>

> <span data-ttu-id="2783b-146">общедоступные значения HRESULT [put_Method](#put_method)(метод LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2783b-146">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="2783b-147">put_Uri</span><span class="sxs-lookup"><span data-stu-id="2783b-147">put_Uri</span></span> 

<span data-ttu-id="2783b-148">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="2783b-148">Set the Uri property.</span></span>

> <span data-ttu-id="2783b-149">общедоступные значения HRESULT [put_Uri](#put_uri)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="2783b-149">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

