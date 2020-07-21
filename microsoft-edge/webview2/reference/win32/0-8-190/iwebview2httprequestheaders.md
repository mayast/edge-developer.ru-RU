---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 1e0148c0d1e27cb4f1c52fb6ad55cc2e7613a94b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885970"
---
# <span data-ttu-id="1d4e2-104">0.8.355-Interface IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="1d4e2-104">0.8.355 - interface IWebView2HttpRequestHeaders</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="1d4e2-105">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-105">HTTP request headers.</span></span>

## <span data-ttu-id="1d4e2-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1d4e2-106">Summary</span></span>

 <span data-ttu-id="1d4e2-107">Участников</span><span class="sxs-lookup"><span data-stu-id="1d4e2-107">Members</span></span>                        | <span data-ttu-id="1d4e2-108">Описания</span><span class="sxs-lookup"><span data-stu-id="1d4e2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1d4e2-109">"Голова"</span><span class="sxs-lookup"><span data-stu-id="1d4e2-109">GetHeader</span></span>](#getheader) | <span data-ttu-id="1d4e2-110">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-110">Gets the header value matching the name.</span></span>
[<span data-ttu-id="1d4e2-111">Contains</span><span class="sxs-lookup"><span data-stu-id="1d4e2-111">Contains</span></span>](#contains) | <span data-ttu-id="1d4e2-112">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="1d4e2-113">SetHeader</span><span class="sxs-lookup"><span data-stu-id="1d4e2-113">SetHeader</span></span>](#setheader) | <span data-ttu-id="1d4e2-114">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-114">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="1d4e2-115">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="1d4e2-115">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="1d4e2-116">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-116">Removes header that matches the name.</span></span>
[<span data-ttu-id="1d4e2-117">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="1d4e2-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="1d4e2-118">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-118">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="1d4e2-119">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-119">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="1d4e2-120">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-120">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="1d4e2-121">Участников</span><span class="sxs-lookup"><span data-stu-id="1d4e2-121">Members</span></span>

#### <span data-ttu-id="1d4e2-122">"Голова"</span><span class="sxs-lookup"><span data-stu-id="1d4e2-122">GetHeader</span></span> 

<span data-ttu-id="1d4e2-123">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-123">Gets the header value matching the name.</span></span>

> <span data-ttu-id="1d4e2-124">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="1d4e2-124">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="1d4e2-125">Contains</span><span class="sxs-lookup"><span data-stu-id="1d4e2-125">Contains</span></span> 

<span data-ttu-id="1d4e2-126">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-126">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="1d4e2-127">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="1d4e2-127">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="1d4e2-128">SetHeader</span><span class="sxs-lookup"><span data-stu-id="1d4e2-128">SetHeader</span></span> 

<span data-ttu-id="1d4e2-129">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-129">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="1d4e2-130">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="1d4e2-130">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="1d4e2-131">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="1d4e2-131">RemoveHeader</span></span> 

<span data-ttu-id="1d4e2-132">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-132">Removes header that matches the name.</span></span>

> <span data-ttu-id="1d4e2-133">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="1d4e2-133">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="1d4e2-134">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="1d4e2-134">GetIterator</span></span> 

<span data-ttu-id="1d4e2-135">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="1d4e2-135">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="1d4e2-136">общедоступный HRESULT- [итератор](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="1d4e2-136">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

