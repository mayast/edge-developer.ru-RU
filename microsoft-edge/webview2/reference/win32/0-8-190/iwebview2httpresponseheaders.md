---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 077c85b2458c2cf843c4d2f0548d17ec01ba4751
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885963"
---
# <span data-ttu-id="ad818-104">0.8.355-Interface IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="ad818-104">0.8.355 - interface IWebView2HttpResponseHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="ad818-105">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="ad818-105">HTTP response headers.</span></span>

## <span data-ttu-id="ad818-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ad818-106">Summary</span></span>

 <span data-ttu-id="ad818-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ad818-107">Members</span></span>                        | <span data-ttu-id="ad818-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ad818-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ad818-109">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="ad818-109">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="ad818-110">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="ad818-110">Appends header line with name and value.</span></span>
[<span data-ttu-id="ad818-111">Contains</span><span class="sxs-lookup"><span data-stu-id="ad818-111">Contains</span></span>](#contains) | <span data-ttu-id="ad818-112">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="ad818-112">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="ad818-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="ad818-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="ad818-114">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="ad818-114">Gets the header values matching the name.</span></span>
[<span data-ttu-id="ad818-115">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="ad818-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="ad818-116">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="ad818-116">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="ad818-117">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="ad818-117">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="ad818-118">Участников</span><span class="sxs-lookup"><span data-stu-id="ad818-118">Members</span></span>

#### <span data-ttu-id="ad818-119">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="ad818-119">AppendHeader</span></span> 

<span data-ttu-id="ad818-120">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="ad818-120">Appends header line with name and value.</span></span>

> <span data-ttu-id="ad818-121">общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="ad818-121">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="ad818-122">Contains</span><span class="sxs-lookup"><span data-stu-id="ad818-122">Contains</span></span> 

<span data-ttu-id="ad818-123">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="ad818-123">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="ad818-124">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="ad818-124">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="ad818-125">"Голова"</span><span class="sxs-lookup"><span data-stu-id="ad818-125">GetHeaders</span></span> 

<span data-ttu-id="ad818-126">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="ad818-126">Gets the header values matching the name.</span></span>

> <span data-ttu-id="ad818-127">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="ad818-127">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="ad818-128">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="ad818-128">GetIterator</span></span> 

<span data-ttu-id="ad818-129">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="ad818-129">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="ad818-130">общедоступный HRESULT- [итератор](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="ad818-130">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

