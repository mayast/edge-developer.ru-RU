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
ms.openlocfilehash: aea00f37f28034e1b7a33d4fd11c5ed78f779d00
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654908"
---
# <span data-ttu-id="19269-104">интерфейс IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="19269-104">interface IWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="19269-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="19269-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="19269-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="19269-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="19269-107">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="19269-107">HTTP request headers.</span></span>

## <span data-ttu-id="19269-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="19269-108">Summary</span></span>

 <span data-ttu-id="19269-109">Участников</span><span class="sxs-lookup"><span data-stu-id="19269-109">Members</span></span>                        | <span data-ttu-id="19269-110">Описания</span><span class="sxs-lookup"><span data-stu-id="19269-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="19269-111">"Голова"</span><span class="sxs-lookup"><span data-stu-id="19269-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="19269-112">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="19269-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="19269-113">Contains</span><span class="sxs-lookup"><span data-stu-id="19269-113">Contains</span></span>](#contains) | <span data-ttu-id="19269-114">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="19269-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="19269-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="19269-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="19269-116">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="19269-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="19269-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="19269-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="19269-118">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="19269-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="19269-119">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="19269-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="19269-120">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="19269-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="19269-121">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="19269-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="19269-122">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="19269-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="19269-123">Участников</span><span class="sxs-lookup"><span data-stu-id="19269-123">Members</span></span>

#### <span data-ttu-id="19269-124">"Голова"</span><span class="sxs-lookup"><span data-stu-id="19269-124">GetHeader</span></span> 

<span data-ttu-id="19269-125">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="19269-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="19269-126">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="19269-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="19269-127">Contains</span><span class="sxs-lookup"><span data-stu-id="19269-127">Contains</span></span> 

<span data-ttu-id="19269-128">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="19269-128">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="19269-129">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="19269-129">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="19269-130">SetHeader</span><span class="sxs-lookup"><span data-stu-id="19269-130">SetHeader</span></span> 

<span data-ttu-id="19269-131">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="19269-131">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="19269-132">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="19269-132">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="19269-133">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="19269-133">RemoveHeader</span></span> 

<span data-ttu-id="19269-134">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="19269-134">Removes header that matches the name.</span></span>

> <span data-ttu-id="19269-135">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="19269-135">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="19269-136">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="19269-136">GetIterator</span></span> 

<span data-ttu-id="19269-137">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="19269-137">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="19269-138">общедоступный HRESULT- [итератор](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="19269-138">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

