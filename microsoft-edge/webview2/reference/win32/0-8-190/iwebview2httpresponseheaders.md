---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 48a04ea60dff4cf9b6b52377927ee9085fb8bea2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878437"
---
# <span data-ttu-id="93801-104">0.8.355-Interface IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="93801-104">0.8.355 - interface IWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="93801-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="93801-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="93801-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="93801-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="93801-107">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="93801-107">HTTP response headers.</span></span>

## <span data-ttu-id="93801-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="93801-108">Summary</span></span>

 <span data-ttu-id="93801-109">Участников</span><span class="sxs-lookup"><span data-stu-id="93801-109">Members</span></span>                        | <span data-ttu-id="93801-110">Описания</span><span class="sxs-lookup"><span data-stu-id="93801-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="93801-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="93801-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="93801-112">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="93801-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="93801-113">Contains</span><span class="sxs-lookup"><span data-stu-id="93801-113">Contains</span></span>](#contains) | <span data-ttu-id="93801-114">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="93801-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="93801-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="93801-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="93801-116">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="93801-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="93801-117">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="93801-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="93801-118">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="93801-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="93801-119">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="93801-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="93801-120">Участников</span><span class="sxs-lookup"><span data-stu-id="93801-120">Members</span></span>

#### <span data-ttu-id="93801-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="93801-121">AppendHeader</span></span> 

<span data-ttu-id="93801-122">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="93801-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="93801-123">общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="93801-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="93801-124">Contains</span><span class="sxs-lookup"><span data-stu-id="93801-124">Contains</span></span> 

<span data-ttu-id="93801-125">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="93801-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="93801-126">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="93801-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="93801-127">"Голова"</span><span class="sxs-lookup"><span data-stu-id="93801-127">GetHeaders</span></span> 

<span data-ttu-id="93801-128">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="93801-128">Gets the header values matching the name.</span></span>

> <span data-ttu-id="93801-129">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="93801-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="93801-130">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="93801-130">GetIterator</span></span> 

<span data-ttu-id="93801-131">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="93801-131">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="93801-132">общедоступный HRESULT- [итератор](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="93801-132">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

