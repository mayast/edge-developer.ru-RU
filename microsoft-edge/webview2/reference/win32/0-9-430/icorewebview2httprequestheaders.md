---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 04a8bf376ad7649021c4ab1555c3090cce5b52fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885613"
---
# <span data-ttu-id="91356-104">0.9.430-Interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="91356-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="91356-105">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="91356-105">HTTP request headers.</span></span>

## <span data-ttu-id="91356-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="91356-106">Summary</span></span>

 <span data-ttu-id="91356-107">Участников</span><span class="sxs-lookup"><span data-stu-id="91356-107">Members</span></span>                        | <span data-ttu-id="91356-108">Описания</span><span class="sxs-lookup"><span data-stu-id="91356-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="91356-109">"Голова"</span><span class="sxs-lookup"><span data-stu-id="91356-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="91356-110">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="91356-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="91356-111">"Голова"</span><span class="sxs-lookup"><span data-stu-id="91356-111">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="91356-112">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="91356-112">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="91356-113">Contains</span><span class="sxs-lookup"><span data-stu-id="91356-113">Contains</span></span>](#contains) | <span data-ttu-id="91356-114">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="91356-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="91356-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="91356-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="91356-116">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="91356-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="91356-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="91356-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="91356-118">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="91356-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="91356-119">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="91356-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="91356-120">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="91356-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="91356-121">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="91356-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="91356-122">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="91356-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="91356-123">Участников</span><span class="sxs-lookup"><span data-stu-id="91356-123">Members</span></span>

#### <span data-ttu-id="91356-124">"Голова"</span><span class="sxs-lookup"><span data-stu-id="91356-124">GetHeader</span></span> 

<span data-ttu-id="91356-125">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="91356-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="91356-126">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="91356-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="91356-127">"Голова"</span><span class="sxs-lookup"><span data-stu-id="91356-127">GetHeaders</span></span> 

<span data-ttu-id="91356-128">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="91356-128">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="91356-129">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="91356-129">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="91356-130">Contains</span><span class="sxs-lookup"><span data-stu-id="91356-130">Contains</span></span> 

<span data-ttu-id="91356-131">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="91356-131">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="91356-132">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="91356-132">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="91356-133">SetHeader</span><span class="sxs-lookup"><span data-stu-id="91356-133">SetHeader</span></span> 

<span data-ttu-id="91356-134">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="91356-134">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="91356-135">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="91356-135">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="91356-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="91356-136">RemoveHeader</span></span> 

<span data-ttu-id="91356-137">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="91356-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="91356-138">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="91356-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="91356-139">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="91356-139">GetIterator</span></span> 

<span data-ttu-id="91356-140">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="91356-140">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="91356-141">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="91356-141">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

