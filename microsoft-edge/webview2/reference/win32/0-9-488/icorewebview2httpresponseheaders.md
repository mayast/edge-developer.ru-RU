---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 356f8bfc235e522ef5e976baf61f8c9017766a3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880537"
---
# <span data-ttu-id="37469-104">0.9.515-Interface ICoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="37469-104">0.9.515 - interface ICoreWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="37469-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="37469-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="37469-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="37469-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="37469-107">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="37469-107">HTTP response headers.</span></span>

## <span data-ttu-id="37469-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="37469-108">Summary</span></span>

 <span data-ttu-id="37469-109">Участников</span><span class="sxs-lookup"><span data-stu-id="37469-109">Members</span></span>                        | <span data-ttu-id="37469-110">Описания</span><span class="sxs-lookup"><span data-stu-id="37469-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="37469-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="37469-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="37469-112">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="37469-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="37469-113">Contains</span><span class="sxs-lookup"><span data-stu-id="37469-113">Contains</span></span>](#contains) | <span data-ttu-id="37469-114">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="37469-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="37469-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="37469-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="37469-116">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="37469-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="37469-117">"Голова"</span><span class="sxs-lookup"><span data-stu-id="37469-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="37469-118">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="37469-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="37469-119">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="37469-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="37469-120">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="37469-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="37469-121">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="37469-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="37469-122">Участников</span><span class="sxs-lookup"><span data-stu-id="37469-122">Members</span></span>

#### <span data-ttu-id="37469-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="37469-123">AppendHeader</span></span> 

<span data-ttu-id="37469-124">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="37469-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="37469-125">общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="37469-125">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name, LPCWSTR value)</span></span>

#### <span data-ttu-id="37469-126">Contains</span><span class="sxs-lookup"><span data-stu-id="37469-126">Contains</span></span> 

<span data-ttu-id="37469-127">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="37469-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="37469-128">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="37469-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="37469-129">"Голова"</span><span class="sxs-lookup"><span data-stu-id="37469-129">GetHeader</span></span> 

<span data-ttu-id="37469-130">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="37469-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="37469-131">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="37469-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="37469-132">"Голова"</span><span class="sxs-lookup"><span data-stu-id="37469-132">GetHeaders</span></span> 

<span data-ttu-id="37469-133">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="37469-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="37469-134">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="37469-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="37469-135">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="37469-135">GetIterator</span></span> 

<span data-ttu-id="37469-136">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="37469-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="37469-137">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="37469-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

