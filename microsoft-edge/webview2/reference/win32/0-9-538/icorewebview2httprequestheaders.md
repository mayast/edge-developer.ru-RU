---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 903355ff04463ad86f1e25771f5f321f7d0df479
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879165"
---
# <span data-ttu-id="98c81-104">интерфейс ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="98c81-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="98c81-105">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="98c81-105">HTTP request headers.</span></span>

## <span data-ttu-id="98c81-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="98c81-106">Summary</span></span>

 <span data-ttu-id="98c81-107">Участников</span><span class="sxs-lookup"><span data-stu-id="98c81-107">Members</span></span>                        | <span data-ttu-id="98c81-108">Описания</span><span class="sxs-lookup"><span data-stu-id="98c81-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="98c81-109">Contains</span><span class="sxs-lookup"><span data-stu-id="98c81-109">Contains</span></span>](#contains) | <span data-ttu-id="98c81-110">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="98c81-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="98c81-111">"Голова"</span><span class="sxs-lookup"><span data-stu-id="98c81-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="98c81-112">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="98c81-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="98c81-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="98c81-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="98c81-114">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="98c81-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="98c81-115">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="98c81-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="98c81-116">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="98c81-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="98c81-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="98c81-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="98c81-118">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="98c81-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="98c81-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="98c81-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="98c81-120">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="98c81-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="98c81-121">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="98c81-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="98c81-122">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="98c81-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="98c81-123">Участников</span><span class="sxs-lookup"><span data-stu-id="98c81-123">Members</span></span>

#### <span data-ttu-id="98c81-124">Contains</span><span class="sxs-lookup"><span data-stu-id="98c81-124">Contains</span></span> 

<span data-ttu-id="98c81-125">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="98c81-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="98c81-126">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="98c81-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="98c81-127">"Голова"</span><span class="sxs-lookup"><span data-stu-id="98c81-127">GetHeader</span></span> 

<span data-ttu-id="98c81-128">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="98c81-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="98c81-129">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="98c81-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="98c81-130">"Голова"</span><span class="sxs-lookup"><span data-stu-id="98c81-130">GetHeaders</span></span> 

<span data-ttu-id="98c81-131">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="98c81-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="98c81-132">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="98c81-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="98c81-133">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="98c81-133">GetIterator</span></span> 

<span data-ttu-id="98c81-134">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="98c81-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="98c81-135">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="98c81-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="98c81-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="98c81-136">RemoveHeader</span></span> 

<span data-ttu-id="98c81-137">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="98c81-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="98c81-138">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="98c81-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="98c81-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="98c81-139">SetHeader</span></span> 

<span data-ttu-id="98c81-140">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="98c81-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="98c81-141">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="98c81-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

