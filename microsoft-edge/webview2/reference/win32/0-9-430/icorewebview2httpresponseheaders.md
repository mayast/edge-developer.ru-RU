---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 44f7477eaa81198ef64d332faa0c3a22225d5ea4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880973"
---
# <span data-ttu-id="8496c-104">0.9.430-Interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="8496c-104">0.9.430 - interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="8496c-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="8496c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="8496c-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="8496c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="8496c-107">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="8496c-107">HTTP response headers.</span></span>

## <span data-ttu-id="8496c-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8496c-108">Summary</span></span>

 <span data-ttu-id="8496c-109">Участников</span><span class="sxs-lookup"><span data-stu-id="8496c-109">Members</span></span>                        | <span data-ttu-id="8496c-110">Описания</span><span class="sxs-lookup"><span data-stu-id="8496c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8496c-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="8496c-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="8496c-112">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="8496c-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="8496c-113">Contains</span><span class="sxs-lookup"><span data-stu-id="8496c-113">Contains</span></span>](#contains) | <span data-ttu-id="8496c-114">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="8496c-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="8496c-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="8496c-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="8496c-116">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="8496c-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="8496c-117">"Голова"</span><span class="sxs-lookup"><span data-stu-id="8496c-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="8496c-118">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="8496c-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="8496c-119">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="8496c-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="8496c-120">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="8496c-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="8496c-121">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="8496c-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="8496c-122">Участников</span><span class="sxs-lookup"><span data-stu-id="8496c-122">Members</span></span>

#### <span data-ttu-id="8496c-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="8496c-123">AppendHeader</span></span> 

<span data-ttu-id="8496c-124">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="8496c-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="8496c-125">общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="8496c-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="8496c-126">Contains</span><span class="sxs-lookup"><span data-stu-id="8496c-126">Contains</span></span> 

<span data-ttu-id="8496c-127">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="8496c-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="8496c-128">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="8496c-128">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="8496c-129">"Голова"</span><span class="sxs-lookup"><span data-stu-id="8496c-129">GetHeader</span></span> 

<span data-ttu-id="8496c-130">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="8496c-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="8496c-131">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="8496c-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="8496c-132">"Голова"</span><span class="sxs-lookup"><span data-stu-id="8496c-132">GetHeaders</span></span> 

<span data-ttu-id="8496c-133">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="8496c-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="8496c-134">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="8496c-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="8496c-135">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="8496c-135">GetIterator</span></span> 

<span data-ttu-id="8496c-136">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="8496c-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="8496c-137">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="8496c-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

