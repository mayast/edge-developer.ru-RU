---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 69bf9eeae4b6736ac6df6ddaa9594b7438cbf58c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654686"
---
# <span data-ttu-id="d4a48-104">интерфейс IWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="d4a48-104">interface IWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="d4a48-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d4a48-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d4a48-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="d4a48-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="d4a48-107">HTTP-запрос, используемый для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d4a48-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="d4a48-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d4a48-108">Summary</span></span>

 <span data-ttu-id="d4a48-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d4a48-109">Members</span></span>                        | <span data-ttu-id="d4a48-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d4a48-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d4a48-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="d4a48-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="d4a48-112">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="d4a48-112">The request URI.</span></span>
[<span data-ttu-id="d4a48-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="d4a48-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="d4a48-114">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="d4a48-114">Set the Uri property.</span></span>
[<span data-ttu-id="d4a48-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="d4a48-115">get_Method</span></span>](#get_method) | <span data-ttu-id="d4a48-116">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="d4a48-116">The HTTP request method.</span></span>
[<span data-ttu-id="d4a48-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="d4a48-117">put_Method</span></span>](#put_method) | <span data-ttu-id="d4a48-118">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="d4a48-118">Set the Method property.</span></span>
[<span data-ttu-id="d4a48-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="d4a48-119">get_Content</span></span>](#get_content) | <span data-ttu-id="d4a48-120">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="d4a48-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="d4a48-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="d4a48-121">put_Content</span></span>](#put_content) | <span data-ttu-id="d4a48-122">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="d4a48-122">Set the Content property.</span></span>
[<span data-ttu-id="d4a48-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="d4a48-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="d4a48-124">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="d4a48-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="d4a48-125">Участников</span><span class="sxs-lookup"><span data-stu-id="d4a48-125">Members</span></span>

#### <span data-ttu-id="d4a48-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="d4a48-126">get_Uri</span></span> 

<span data-ttu-id="d4a48-127">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="d4a48-127">The request URI.</span></span>

> <span data-ttu-id="d4a48-128">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="d4a48-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="d4a48-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="d4a48-129">put_Uri</span></span> 

<span data-ttu-id="d4a48-130">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="d4a48-130">Set the Uri property.</span></span>

> <span data-ttu-id="d4a48-131">общедоступные значения HRESULT [put_Uri](#put_uri)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d4a48-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="d4a48-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="d4a48-132">get_Method</span></span> 

<span data-ttu-id="d4a48-133">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="d4a48-133">The HTTP request method.</span></span>

> <span data-ttu-id="d4a48-134">общедоступный [GET_METHOD](#get_method)HRESULT (метод LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="d4a48-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="d4a48-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="d4a48-135">put_Method</span></span> 

<span data-ttu-id="d4a48-136">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="d4a48-136">Set the Method property.</span></span>

> <span data-ttu-id="d4a48-137">общедоступные значения HRESULT [put_Method](#put_method)(метод LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d4a48-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="d4a48-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="d4a48-138">get_Content</span></span> 

<span data-ttu-id="d4a48-139">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="d4a48-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="d4a48-140">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="d4a48-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="d4a48-141">Поместите здесь данные.</span><span class="sxs-lookup"><span data-stu-id="d4a48-141">POST data would be here.</span></span> <span data-ttu-id="d4a48-142">Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="d4a48-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="d4a48-143">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="d4a48-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="d4a48-144">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="d4a48-144">Null means no content data.</span></span> <span data-ttu-id="d4a48-145">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="d4a48-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="d4a48-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="d4a48-146">put_Content</span></span> 

<span data-ttu-id="d4a48-147">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="d4a48-147">Set the Content property.</span></span>

> <span data-ttu-id="d4a48-148">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="d4a48-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="d4a48-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="d4a48-149">get_Headers</span></span> 

<span data-ttu-id="d4a48-150">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="d4a48-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="d4a48-151">общедоступные значения HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="d4a48-151">public HRESULT [get_Headers](#get_headers)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* headers)</span></span>

