---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a67c5c267178ea873cd12d8a22dea7409b260d52
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880999"
---
# <span data-ttu-id="f8376-104">0.9.430-Interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="f8376-104">0.9.430 - interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="f8376-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="f8376-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="f8376-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="f8376-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="f8376-107">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="f8376-107">HTTP request headers.</span></span>

## <span data-ttu-id="f8376-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f8376-108">Summary</span></span>

 <span data-ttu-id="f8376-109">Участников</span><span class="sxs-lookup"><span data-stu-id="f8376-109">Members</span></span>                        | <span data-ttu-id="f8376-110">Описания</span><span class="sxs-lookup"><span data-stu-id="f8376-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f8376-111">"Голова"</span><span class="sxs-lookup"><span data-stu-id="f8376-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="f8376-112">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="f8376-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="f8376-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="f8376-113">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="f8376-114">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="f8376-114">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="f8376-115">Contains</span><span class="sxs-lookup"><span data-stu-id="f8376-115">Contains</span></span>](#contains) | <span data-ttu-id="f8376-116">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="f8376-116">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="f8376-117">SetHeader</span><span class="sxs-lookup"><span data-stu-id="f8376-117">SetHeader</span></span>](#setheader) | <span data-ttu-id="f8376-118">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="f8376-118">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="f8376-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="f8376-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="f8376-120">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="f8376-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="f8376-121">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="f8376-121">GetIterator</span></span>](#getiterator) | <span data-ttu-id="f8376-122">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="f8376-122">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="f8376-123">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f8376-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="f8376-124">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f8376-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="f8376-125">Участников</span><span class="sxs-lookup"><span data-stu-id="f8376-125">Members</span></span>

#### <span data-ttu-id="f8376-126">"Голова"</span><span class="sxs-lookup"><span data-stu-id="f8376-126">GetHeader</span></span> 

<span data-ttu-id="f8376-127">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="f8376-127">Gets the header value matching the name.</span></span>

> <span data-ttu-id="f8376-128">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="f8376-128">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="f8376-129">"Голова"</span><span class="sxs-lookup"><span data-stu-id="f8376-129">GetHeaders</span></span> 

<span data-ttu-id="f8376-130">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="f8376-130">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="f8376-131">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="f8376-131">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="f8376-132">Contains</span><span class="sxs-lookup"><span data-stu-id="f8376-132">Contains</span></span> 

<span data-ttu-id="f8376-133">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="f8376-133">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="f8376-134">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="f8376-134">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="f8376-135">SetHeader</span><span class="sxs-lookup"><span data-stu-id="f8376-135">SetHeader</span></span> 

<span data-ttu-id="f8376-136">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="f8376-136">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="f8376-137">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="f8376-137">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="f8376-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="f8376-138">RemoveHeader</span></span> 

<span data-ttu-id="f8376-139">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="f8376-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="f8376-140">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="f8376-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="f8376-141">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="f8376-141">GetIterator</span></span> 

<span data-ttu-id="f8376-142">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="f8376-142">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="f8376-143">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="f8376-143">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

