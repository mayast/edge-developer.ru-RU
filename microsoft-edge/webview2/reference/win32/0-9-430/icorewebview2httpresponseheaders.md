---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 321d18a726ac19db92018cb27d31867029991cf0
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886222"
---
# <span data-ttu-id="b2c6a-104">0.9.430-Interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="b2c6a-104">0.9.430 - interface ICoreWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="b2c6a-105">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-105">HTTP response headers.</span></span>

## <span data-ttu-id="b2c6a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b2c6a-106">Summary</span></span>

 <span data-ttu-id="b2c6a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="b2c6a-107">Members</span></span>                        | <span data-ttu-id="b2c6a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="b2c6a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b2c6a-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="b2c6a-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="b2c6a-110">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="b2c6a-111">Contains</span><span class="sxs-lookup"><span data-stu-id="b2c6a-111">Contains</span></span>](#contains) | <span data-ttu-id="b2c6a-112">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="b2c6a-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="b2c6a-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="b2c6a-114">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-114">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="b2c6a-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="b2c6a-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="b2c6a-116">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="b2c6a-117">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="b2c6a-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="b2c6a-118">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="b2c6a-119">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="b2c6a-120">Участников</span><span class="sxs-lookup"><span data-stu-id="b2c6a-120">Members</span></span>

#### <span data-ttu-id="b2c6a-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="b2c6a-121">AppendHeader</span></span> 

<span data-ttu-id="b2c6a-122">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="b2c6a-123">общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b2c6a-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="b2c6a-124">Contains</span><span class="sxs-lookup"><span data-stu-id="b2c6a-124">Contains</span></span> 

<span data-ttu-id="b2c6a-125">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="b2c6a-126">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="b2c6a-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="b2c6a-127">"Голова"</span><span class="sxs-lookup"><span data-stu-id="b2c6a-127">GetHeader</span></span> 

<span data-ttu-id="b2c6a-128">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-128">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="b2c6a-129">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="b2c6a-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="b2c6a-130">"Голова"</span><span class="sxs-lookup"><span data-stu-id="b2c6a-130">GetHeaders</span></span> 

<span data-ttu-id="b2c6a-131">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-131">Gets the header values matching the name.</span></span>

> <span data-ttu-id="b2c6a-132">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="b2c6a-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="b2c6a-133">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="b2c6a-133">GetIterator</span></span> 

<span data-ttu-id="b2c6a-134">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="b2c6a-134">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="b2c6a-135">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="b2c6a-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

