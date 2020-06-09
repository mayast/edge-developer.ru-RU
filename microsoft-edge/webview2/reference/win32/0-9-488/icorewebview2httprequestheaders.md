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
ms.openlocfilehash: effceb6fafb062b1747f39876b8d2a5e02721aa8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697275"
---
# <span data-ttu-id="b8bba-104">интерфейс ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="b8bba-104">interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="b8bba-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b8bba-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b8bba-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="b8bba-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="b8bba-107">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="b8bba-107">HTTP request headers.</span></span>

## <span data-ttu-id="b8bba-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b8bba-108">Summary</span></span>

 <span data-ttu-id="b8bba-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b8bba-109">Members</span></span>                        | <span data-ttu-id="b8bba-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b8bba-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b8bba-111">Contains</span><span class="sxs-lookup"><span data-stu-id="b8bba-111">Contains</span></span>](#contains) | <span data-ttu-id="b8bba-112">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="b8bba-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="b8bba-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="b8bba-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="b8bba-114">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="b8bba-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="b8bba-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="b8bba-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="b8bba-116">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="b8bba-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="b8bba-117">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="b8bba-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="b8bba-118">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="b8bba-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="b8bba-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="b8bba-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="b8bba-120">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="b8bba-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="b8bba-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="b8bba-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="b8bba-122">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="b8bba-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="b8bba-123">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="b8bba-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="b8bba-124">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="b8bba-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="b8bba-125">Участников</span><span class="sxs-lookup"><span data-stu-id="b8bba-125">Members</span></span>

#### <span data-ttu-id="b8bba-126">Contains</span><span class="sxs-lookup"><span data-stu-id="b8bba-126">Contains</span></span> 

<span data-ttu-id="b8bba-127">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="b8bba-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="b8bba-128">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="b8bba-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="b8bba-129">"Голова"</span><span class="sxs-lookup"><span data-stu-id="b8bba-129">GetHeader</span></span> 

<span data-ttu-id="b8bba-130">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="b8bba-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="b8bba-131">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="b8bba-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="b8bba-132">"Голова"</span><span class="sxs-lookup"><span data-stu-id="b8bba-132">GetHeaders</span></span> 

<span data-ttu-id="b8bba-133">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="b8bba-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="b8bba-134">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="b8bba-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="b8bba-135">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="b8bba-135">GetIterator</span></span> 

<span data-ttu-id="b8bba-136">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="b8bba-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="b8bba-137">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="b8bba-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="b8bba-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="b8bba-138">RemoveHeader</span></span> 

<span data-ttu-id="b8bba-139">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="b8bba-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="b8bba-140">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b8bba-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="b8bba-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="b8bba-141">SetHeader</span></span> 

<span data-ttu-id="b8bba-142">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="b8bba-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="b8bba-143">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b8bba-143">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

