---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 7a59511e9d899fe4a66f2671f67f7c7cd7f101df
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011323"
---
# <span data-ttu-id="baa2e-104">0.9.579-Interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="baa2e-104">0.9.579 - interface ICoreWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="baa2e-105">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="baa2e-105">HTTP request headers.</span></span>

## <span data-ttu-id="baa2e-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="baa2e-106">Summary</span></span>

 <span data-ttu-id="baa2e-107">Участников</span><span class="sxs-lookup"><span data-stu-id="baa2e-107">Members</span></span>                        | <span data-ttu-id="baa2e-108">Описания</span><span class="sxs-lookup"><span data-stu-id="baa2e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="baa2e-109">Contains</span><span class="sxs-lookup"><span data-stu-id="baa2e-109">Contains</span></span>](#contains) | <span data-ttu-id="baa2e-110">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="baa2e-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="baa2e-111">"Голова"</span><span class="sxs-lookup"><span data-stu-id="baa2e-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="baa2e-112">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="baa2e-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="baa2e-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="baa2e-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="baa2e-114">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="baa2e-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="baa2e-115">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="baa2e-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="baa2e-116">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="baa2e-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="baa2e-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="baa2e-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="baa2e-118">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="baa2e-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="baa2e-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="baa2e-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="baa2e-120">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="baa2e-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="baa2e-121">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="baa2e-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="baa2e-122">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="baa2e-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="baa2e-123">Участников</span><span class="sxs-lookup"><span data-stu-id="baa2e-123">Members</span></span>

#### <span data-ttu-id="baa2e-124">Contains</span><span class="sxs-lookup"><span data-stu-id="baa2e-124">Contains</span></span> 

<span data-ttu-id="baa2e-125">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="baa2e-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="baa2e-126">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="baa2e-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="baa2e-127">"Голова"</span><span class="sxs-lookup"><span data-stu-id="baa2e-127">GetHeader</span></span> 

<span data-ttu-id="baa2e-128">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="baa2e-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="baa2e-129">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="baa2e-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="baa2e-130">"Голова"</span><span class="sxs-lookup"><span data-stu-id="baa2e-130">GetHeaders</span></span> 

<span data-ttu-id="baa2e-131">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="baa2e-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="baa2e-132">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="baa2e-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="baa2e-133">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="baa2e-133">GetIterator</span></span> 

<span data-ttu-id="baa2e-134">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="baa2e-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="baa2e-135">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="baa2e-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="baa2e-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="baa2e-136">RemoveHeader</span></span> 

<span data-ttu-id="baa2e-137">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="baa2e-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="baa2e-138">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="baa2e-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="baa2e-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="baa2e-139">SetHeader</span></span> 

<span data-ttu-id="baa2e-140">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="baa2e-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="baa2e-141">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="baa2e-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

