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
ms.openlocfilehash: 0f3564fa96bc1c13527cbf3b26ce92114d44eae4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654822"
---
# <span data-ttu-id="c0259-104">интерфейс IWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="c0259-104">interface IWebView2HttpResponseHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="c0259-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="c0259-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="c0259-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="c0259-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpResponseHeaders
  : public IUnknown
```

<span data-ttu-id="c0259-107">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="c0259-107">HTTP response headers.</span></span>

## <span data-ttu-id="c0259-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c0259-108">Summary</span></span>

 <span data-ttu-id="c0259-109">Участников</span><span class="sxs-lookup"><span data-stu-id="c0259-109">Members</span></span>                        | <span data-ttu-id="c0259-110">Описания</span><span class="sxs-lookup"><span data-stu-id="c0259-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0259-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="c0259-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="c0259-112">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="c0259-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="c0259-113">Contains</span><span class="sxs-lookup"><span data-stu-id="c0259-113">Contains</span></span>](#contains) | <span data-ttu-id="c0259-114">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="c0259-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="c0259-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="c0259-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="c0259-116">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="c0259-116">Gets the header values matching the name.</span></span>
[<span data-ttu-id="c0259-117">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="c0259-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="c0259-118">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="c0259-118">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="c0259-119">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="c0259-119">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="c0259-120">Участников</span><span class="sxs-lookup"><span data-stu-id="c0259-120">Members</span></span>

#### <span data-ttu-id="c0259-121">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="c0259-121">AppendHeader</span></span> 

<span data-ttu-id="c0259-122">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="c0259-122">Appends header line with name and value.</span></span>

> <span data-ttu-id="c0259-123">общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="c0259-123">public HRESULT [AppendHeader](#appendheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="c0259-124">Contains</span><span class="sxs-lookup"><span data-stu-id="c0259-124">Contains</span></span> 

<span data-ttu-id="c0259-125">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="c0259-125">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="c0259-126">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="c0259-126">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="c0259-127">"Голова"</span><span class="sxs-lookup"><span data-stu-id="c0259-127">GetHeaders</span></span> 

<span data-ttu-id="c0259-128">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="c0259-128">Gets the header values matching the name.</span></span>

> <span data-ttu-id="c0259-129">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="c0259-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="c0259-130">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="c0259-130">GetIterator</span></span> 

<span data-ttu-id="c0259-131">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="c0259-131">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="c0259-132">общедоступный HRESULT- [итератор](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="c0259-132">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

