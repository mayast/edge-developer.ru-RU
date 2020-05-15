---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9f04e05ef77801a571771257f4a5e48077c373fd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654759"
---
# <span data-ttu-id="ea23d-104">интерфейс ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="ea23d-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="ea23d-105">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="ea23d-105">HTTP request headers.</span></span>

## <span data-ttu-id="ea23d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ea23d-106">Summary</span></span>

 <span data-ttu-id="ea23d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ea23d-107">Members</span></span>                        | <span data-ttu-id="ea23d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ea23d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ea23d-109">Contains</span><span class="sxs-lookup"><span data-stu-id="ea23d-109">Contains</span></span>](#contains) | <span data-ttu-id="ea23d-110">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="ea23d-110">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="ea23d-111">"Голова"</span><span class="sxs-lookup"><span data-stu-id="ea23d-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="ea23d-112">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="ea23d-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="ea23d-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="ea23d-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="ea23d-114">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="ea23d-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="ea23d-115">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="ea23d-115">GetIterator</span></span>](#getiterator) | <span data-ttu-id="ea23d-116">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="ea23d-116">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="ea23d-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="ea23d-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="ea23d-118">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="ea23d-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="ea23d-119">SetHeader</span><span class="sxs-lookup"><span data-stu-id="ea23d-119">SetHeader</span></span>](#setheader) | <span data-ttu-id="ea23d-120">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="ea23d-120">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="ea23d-121">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ea23d-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="ea23d-122">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="ea23d-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="ea23d-123">Участников</span><span class="sxs-lookup"><span data-stu-id="ea23d-123">Members</span></span>

#### <span data-ttu-id="ea23d-124">Contains</span><span class="sxs-lookup"><span data-stu-id="ea23d-124">Contains</span></span> 

<span data-ttu-id="ea23d-125">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="ea23d-125">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="ea23d-126">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="ea23d-126">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="ea23d-127">"Голова"</span><span class="sxs-lookup"><span data-stu-id="ea23d-127">GetHeader</span></span> 

<span data-ttu-id="ea23d-128">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="ea23d-128">Gets the header value matching the name.</span></span>

> <span data-ttu-id="ea23d-129">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="ea23d-129">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="ea23d-130">"Голова"</span><span class="sxs-lookup"><span data-stu-id="ea23d-130">GetHeaders</span></span> 

<span data-ttu-id="ea23d-131">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="ea23d-131">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="ea23d-132">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="ea23d-132">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="ea23d-133">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="ea23d-133">GetIterator</span></span> 

<span data-ttu-id="ea23d-134">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="ea23d-134">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="ea23d-135">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="ea23d-135">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="ea23d-136">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="ea23d-136">RemoveHeader</span></span> 

<span data-ttu-id="ea23d-137">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="ea23d-137">Removes header that matches the name.</span></span>

> <span data-ttu-id="ea23d-138">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="ea23d-138">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="ea23d-139">SetHeader</span><span class="sxs-lookup"><span data-stu-id="ea23d-139">SetHeader</span></span> 

<span data-ttu-id="ea23d-140">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="ea23d-140">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="ea23d-141">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="ea23d-141">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

