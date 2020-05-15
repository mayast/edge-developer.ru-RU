---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 201b9af4a5838c9537014864c31cd2121f9dfe76
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654649"
---
# <span data-ttu-id="b01f9-104">интерфейс ICoreWebView2WebResourceRequest</span><span class="sxs-lookup"><span data-stu-id="b01f9-104">interface ICoreWebView2WebResourceRequest</span></span> 

> [!NOTE]
> <span data-ttu-id="b01f9-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b01f9-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b01f9-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="b01f9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

<span data-ttu-id="b01f9-107">HTTP-запрос, используемый для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="b01f9-107">An HTTP request used with the WebResourceRequested event.</span></span>

## <span data-ttu-id="b01f9-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b01f9-108">Summary</span></span>

 <span data-ttu-id="b01f9-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b01f9-109">Members</span></span>                        | <span data-ttu-id="b01f9-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b01f9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b01f9-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b01f9-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="b01f9-112">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="b01f9-112">The request URI.</span></span>
[<span data-ttu-id="b01f9-113">put_Uri</span><span class="sxs-lookup"><span data-stu-id="b01f9-113">put_Uri</span></span>](#put_uri) | <span data-ttu-id="b01f9-114">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="b01f9-114">Set the Uri property.</span></span>
[<span data-ttu-id="b01f9-115">get_Method</span><span class="sxs-lookup"><span data-stu-id="b01f9-115">get_Method</span></span>](#get_method) | <span data-ttu-id="b01f9-116">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="b01f9-116">The HTTP request method.</span></span>
[<span data-ttu-id="b01f9-117">put_Method</span><span class="sxs-lookup"><span data-stu-id="b01f9-117">put_Method</span></span>](#put_method) | <span data-ttu-id="b01f9-118">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="b01f9-118">Set the Method property.</span></span>
[<span data-ttu-id="b01f9-119">get_Content</span><span class="sxs-lookup"><span data-stu-id="b01f9-119">get_Content</span></span>](#get_content) | <span data-ttu-id="b01f9-120">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="b01f9-120">The HTTP request message body as stream.</span></span>
[<span data-ttu-id="b01f9-121">put_Content</span><span class="sxs-lookup"><span data-stu-id="b01f9-121">put_Content</span></span>](#put_content) | <span data-ttu-id="b01f9-122">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="b01f9-122">Set the Content property.</span></span>
[<span data-ttu-id="b01f9-123">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b01f9-123">get_Headers</span></span>](#get_headers) | <span data-ttu-id="b01f9-124">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="b01f9-124">The mutable HTTP request headers.</span></span>

## <span data-ttu-id="b01f9-125">Участников</span><span class="sxs-lookup"><span data-stu-id="b01f9-125">Members</span></span>

#### <span data-ttu-id="b01f9-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="b01f9-126">get_Uri</span></span> 

<span data-ttu-id="b01f9-127">URI запроса.</span><span class="sxs-lookup"><span data-stu-id="b01f9-127">The request URI.</span></span>

> <span data-ttu-id="b01f9-128">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="b01f9-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="b01f9-129">put_Uri</span><span class="sxs-lookup"><span data-stu-id="b01f9-129">put_Uri</span></span> 

<span data-ttu-id="b01f9-130">Задайте свойство URI.</span><span class="sxs-lookup"><span data-stu-id="b01f9-130">Set the Uri property.</span></span>

> <span data-ttu-id="b01f9-131">общедоступные значения HRESULT [put_Uri](#put_uri)(URI LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b01f9-131">public HRESULT [put_Uri](#put_uri)(LPCWSTR uri)</span></span>

#### <span data-ttu-id="b01f9-132">get_Method</span><span class="sxs-lookup"><span data-stu-id="b01f9-132">get_Method</span></span> 

<span data-ttu-id="b01f9-133">Метод HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="b01f9-133">The HTTP request method.</span></span>

> <span data-ttu-id="b01f9-134">общедоступный [GET_METHOD](#get_method)HRESULT (метод LPWSTR \*)</span><span class="sxs-lookup"><span data-stu-id="b01f9-134">public HRESULT [get_Method](#get_method)(LPWSTR \* method)</span></span>

#### <span data-ttu-id="b01f9-135">put_Method</span><span class="sxs-lookup"><span data-stu-id="b01f9-135">put_Method</span></span> 

<span data-ttu-id="b01f9-136">Задайте свойство Method.</span><span class="sxs-lookup"><span data-stu-id="b01f9-136">Set the Method property.</span></span>

> <span data-ttu-id="b01f9-137">общедоступные значения HRESULT [put_Method](#put_method)(метод LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b01f9-137">public HRESULT [put_Method](#put_method)(LPCWSTR method)</span></span>

#### <span data-ttu-id="b01f9-138">get_Content</span><span class="sxs-lookup"><span data-stu-id="b01f9-138">get_Content</span></span> 

<span data-ttu-id="b01f9-139">Текст сообщения HTTP-запроса в виде потока.</span><span class="sxs-lookup"><span data-stu-id="b01f9-139">The HTTP request message body as stream.</span></span>

> <span data-ttu-id="b01f9-140">общедоступные значения HRESULT [get_Content](#get_content)(IStream \* \* содержимое)</span><span class="sxs-lookup"><span data-stu-id="b01f9-140">public HRESULT [get_Content](#get_content)(IStream \*\* content)</span></span>

<span data-ttu-id="b01f9-141">Поместите здесь данные.</span><span class="sxs-lookup"><span data-stu-id="b01f9-141">POST data would be here.</span></span> <span data-ttu-id="b01f9-142">Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа.</span><span class="sxs-lookup"><span data-stu-id="b01f9-142">If a stream is set, which will override the message body, the stream must have all the content data available by the time this response's WebResourceRequested event deferral is completed.</span></span> <span data-ttu-id="b01f9-143">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b01f9-143">Stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span> <span data-ttu-id="b01f9-144">NULL означает, что данные содержимого отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="b01f9-144">Null means no content data.</span></span> <span data-ttu-id="b01f9-145">Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).</span><span class="sxs-lookup"><span data-stu-id="b01f9-145">IStream semantics apply (return S_OK to Read calls until all data is exhausted)</span></span>

#### <span data-ttu-id="b01f9-146">put_Content</span><span class="sxs-lookup"><span data-stu-id="b01f9-146">put_Content</span></span> 

<span data-ttu-id="b01f9-147">Задайте свойство Content (содержимое).</span><span class="sxs-lookup"><span data-stu-id="b01f9-147">Set the Content property.</span></span>

> <span data-ttu-id="b01f9-148">общедоступные значения HRESULT [put_Content](#put_content)(IStream \* Content)</span><span class="sxs-lookup"><span data-stu-id="b01f9-148">public HRESULT [put_Content](#put_content)(IStream \* content)</span></span>

#### <span data-ttu-id="b01f9-149">get_Headers</span><span class="sxs-lookup"><span data-stu-id="b01f9-149">get_Headers</span></span> 

<span data-ttu-id="b01f9-150">Изменяющиеся заголовки HTTP-запроса.</span><span class="sxs-lookup"><span data-stu-id="b01f9-150">The mutable HTTP request headers.</span></span>

> <span data-ttu-id="b01f9-151">общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* headers)</span><span class="sxs-lookup"><span data-stu-id="b01f9-151">public HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* headers)</span></span>

