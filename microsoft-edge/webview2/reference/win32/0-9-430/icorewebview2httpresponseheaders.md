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
ms.openlocfilehash: b23b724977b9d164c48dc99d0da2e64d61539549
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654975"
---
# <span data-ttu-id="d3ce3-104">интерфейс ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="d3ce3-104">interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="d3ce3-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d3ce3-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="d3ce3-107">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-107">HTTP response headers.</span></span>

## <span data-ttu-id="d3ce3-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d3ce3-108">Summary</span></span>

 <span data-ttu-id="d3ce3-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d3ce3-109">Members</span></span>                        | <span data-ttu-id="d3ce3-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d3ce3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d3ce3-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="d3ce3-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="d3ce3-112">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="d3ce3-113">Contains</span><span class="sxs-lookup"><span data-stu-id="d3ce3-113">Contains</span></span>](#contains) | <span data-ttu-id="d3ce3-114">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="d3ce3-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="d3ce3-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="d3ce3-116">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="d3ce3-117">"Голова"</span><span class="sxs-lookup"><span data-stu-id="d3ce3-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="d3ce3-118">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="d3ce3-119">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="d3ce3-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="d3ce3-120">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="d3ce3-121">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="d3ce3-122">Участников</span><span class="sxs-lookup"><span data-stu-id="d3ce3-122">Members</span></span>

#### <span data-ttu-id="d3ce3-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="d3ce3-123">AppendHeader</span></span> 

<span data-ttu-id="d3ce3-124">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="d3ce3-125">общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d3ce3-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="d3ce3-126">Contains</span><span class="sxs-lookup"><span data-stu-id="d3ce3-126">Contains</span></span> 

<span data-ttu-id="d3ce3-127">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="d3ce3-128">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="d3ce3-128">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="d3ce3-129">"Голова"</span><span class="sxs-lookup"><span data-stu-id="d3ce3-129">GetHeader</span></span> 

<span data-ttu-id="d3ce3-130">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="d3ce3-131">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="d3ce3-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="d3ce3-132">"Голова"</span><span class="sxs-lookup"><span data-stu-id="d3ce3-132">GetHeaders</span></span> 

<span data-ttu-id="d3ce3-133">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="d3ce3-134">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="d3ce3-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="d3ce3-135">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="d3ce3-135">GetIterator</span></span> 

<span data-ttu-id="d3ce3-136">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="d3ce3-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="d3ce3-137">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="d3ce3-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

