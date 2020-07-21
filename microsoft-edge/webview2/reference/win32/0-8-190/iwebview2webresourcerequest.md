---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: e9d84fbd459d56b82ab4b7d253526e517960c1db
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885725"
---
# <span data-ttu-id="a30fa-104">0.8.355-Interface IWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="a30fa-104">0.8.355 - interface IWebView2WebResourceRequest</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="a30fa-105">HTTP-запрос, используемый для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="a30fa-105">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="a30fa-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a30fa-106">Summary</span></span>

 <span data-ttu-id="a30fa-107">Участников</span><span class="sxs-lookup"><span data-stu-id="a30fa-107">Members</span></span>                        | <span data-ttu-id="a30fa-108">Описания</span><span class="sxs-lookup"><span data-stu-id="a30fa-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a30fa-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a30fa-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="a30fa-110">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="a30fa-110">The request URI.</span></span>
[<span data-ttu-id="a30fa-111">put_Uri</span><span class="sxs-lookup"><span data-stu-id="a30fa-111">put_Uri</span></span>](#put_uri) | <span data-ttu-id="a30fa-112">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="a30fa-112">Set the Uri property.</span></span>
[<span data-ttu-id="a30fa-113">get_Method</span><span class="sxs-lookup"><span data-stu-id="a30fa-113">get_Method</span></span>](#get_method) | <span data-ttu-id="a30fa-114">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="a30fa-114">The HTTP request method.</span></span>
[<span data-ttu-id="a30fa-115">put_Method</span><span class="sxs-lookup"><span data-stu-id="a30fa-115">put_Method</span></span>](#put_method) | <span data-ttu-id="a30fa-116">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="a30fa-116">Set the Method property.</span></span>
[<span data-ttu-id="a30fa-117">get_Content</span><span class="sxs-lookup"><span data-stu-id="a30fa-117">get_Content</span></span>](#get_content) | <span data-ttu-id="a30fa-118">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="a30fa-118">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="a30fa-119">put_Content</span><span class="sxs-lookup"><span data-stu-id="a30fa-119">put_Content</span></span>](#put_content) | <span data-ttu-id="a30fa-120">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="a30fa-120">Set the Content property.</span></span>
[<span data-ttu-id="a30fa-121">get_Headers</span><span class="sxs-lookup"><span data-stu-id="a30fa-121">get_Headers</span></span>](#get_headers) | <span data-ttu-id="a30fa-122">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="a30fa-122">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="a30fa-123">Участников</span><span class="sxs-lookup"><span data-stu-id="a30fa-123">Members</span></span>

#### <span data-ttu-id="a30fa-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a30fa-124">get_Uri</span></span> 

<span data-ttu-id="a30fa-125">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="a30fa-125">The request URI.</span></span>

> <span data-ttu-id="a30fa-126">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="a30fa-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="a30fa-127">put_Uri</span><span class="sxs-lookup"><span data-stu-id="a30fa-127">put_Uri</span></span> 

<span data-ttu-id="a30fa-128">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="a30fa-128">Set the Uri property.</span></span>

> <span data-ttu-id="a30fa-129">общедоступные значения HRESULT [put_Uri](#put_uri)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="a30fa-129">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="a30fa-130">get_Method</span><span class="sxs-lookup"><span data-stu-id="a30fa-130">get_Method</span></span> 

<span data-ttu-id="a30fa-131">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="a30fa-131">The HTTP request method.</span></span>

> <span data-ttu-id="a30fa-132">общедоступный [GET_METHOD](#get_method)HRESULT (метод LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="a30fa-132">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="a30fa-133">put_Method</span><span class="sxs-lookup"><span data-stu-id="a30fa-133">put_Method</span></span> 

<span data-ttu-id="a30fa-134">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="a30fa-134">Set the Method property.</span></span>

> <span data-ttu-id="a30fa-135">общедоступные значения HRESULT [put_Method](#put_method)(метод LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="a30fa-135">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="a30fa-136">get_Content</span><span class="sxs-lookup"><span data-stu-id="a30fa-136">get_Content</span></span> 

<span data-ttu-id="a30fa-137">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="a30fa-137">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="a30fa-138">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="a30fa-138">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="a30fa-139">Поместите здесь данные.</span><span class="sxs-lookup"><span data-stu-id="a30fa-139">POST data would be here.</span></span> <span data-ttu-id="a30fa-140">Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="a30fa-140">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="a30fa-141">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="a30fa-141">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="a30fa-142">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="a30fa-142">Null means no content data.</span></span> <span data-ttu-id="a30fa-143">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="a30fa-143">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="a30fa-144">put_Content</span><span class="sxs-lookup"><span data-stu-id="a30fa-144">put_Content</span></span> 

<span data-ttu-id="a30fa-145">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="a30fa-145">Set the Content property.</span></span>

> <span data-ttu-id="a30fa-146">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="a30fa-146">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="a30fa-147">get_Headers</span><span class="sxs-lookup"><span data-stu-id="a30fa-147">get_Headers</span></span> 

<span data-ttu-id="a30fa-148">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="a30fa-148">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="a30fa-149">общедоступные значения HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="a30fa-149">public HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* headers)</span></span>

