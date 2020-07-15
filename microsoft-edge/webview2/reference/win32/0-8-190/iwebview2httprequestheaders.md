---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 162d6dde904868ad6a4864b81c0ca76d50638c06
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878458"
---
# <span data-ttu-id="61c49-104">0.8.355-Interface IWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="61c49-104">0.8.355 - interface IWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="61c49-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="61c49-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="61c49-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="61c49-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="61c49-107">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="61c49-107">HTTP request headers.</span></span>

## <span data-ttu-id="61c49-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="61c49-108">Summary</span></span>

 <span data-ttu-id="61c49-109">Участников</span><span class="sxs-lookup"><span data-stu-id="61c49-109">Members</span></span>                        | <span data-ttu-id="61c49-110">Описания</span><span class="sxs-lookup"><span data-stu-id="61c49-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="61c49-111">"Голова"</span><span class="sxs-lookup"><span data-stu-id="61c49-111">GetHeader</span></span>](#getheader) | <span data-ttu-id="61c49-112">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="61c49-112">Gets the header value matching the name.</span></span>
[<span data-ttu-id="61c49-113">Contains</span><span class="sxs-lookup"><span data-stu-id="61c49-113">Contains</span></span>](#contains) | <span data-ttu-id="61c49-114">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="61c49-114">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="61c49-115">SetHeader</span><span class="sxs-lookup"><span data-stu-id="61c49-115">SetHeader</span></span>](#setheader) | <span data-ttu-id="61c49-116">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="61c49-116">Adds or updates header that matches the name.</span></span>
[<span data-ttu-id="61c49-117">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="61c49-117">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="61c49-118">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="61c49-118">Removes header that matches the name.</span></span>
[<span data-ttu-id="61c49-119">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="61c49-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="61c49-120">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="61c49-120">Gets an iterator over the collection of request headers.</span></span>

<span data-ttu-id="61c49-121">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="61c49-121">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="61c49-122">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="61c49-122">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="61c49-123">Участников</span><span class="sxs-lookup"><span data-stu-id="61c49-123">Members</span></span>

#### <span data-ttu-id="61c49-124">"Голова"</span><span class="sxs-lookup"><span data-stu-id="61c49-124">GetHeader</span></span> 

<span data-ttu-id="61c49-125">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="61c49-125">Gets the header value matching the name.</span></span>

> <span data-ttu-id="61c49-126">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="61c49-126">public HRESULT [GetHeader](#getheader)(LPCWSTR name,LPWSTR \* value)</span></span>

#### <span data-ttu-id="61c49-127">Contains</span><span class="sxs-lookup"><span data-stu-id="61c49-127">Contains</span></span> 

<span data-ttu-id="61c49-128">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="61c49-128">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="61c49-129">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="61c49-129">public HRESULT [Contains](#contains)(LPCWSTR name,BOOL \* contains)</span></span>

#### <span data-ttu-id="61c49-130">SetHeader</span><span class="sxs-lookup"><span data-stu-id="61c49-130">SetHeader</span></span> 

<span data-ttu-id="61c49-131">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="61c49-131">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="61c49-132">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="61c49-132">public HRESULT [SetHeader](#setheader)(LPCWSTR name,LPCWSTR value)</span></span>

#### <span data-ttu-id="61c49-133">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="61c49-133">RemoveHeader</span></span> 

<span data-ttu-id="61c49-134">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="61c49-134">Removes header that matches the name.</span></span>

> <span data-ttu-id="61c49-135">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="61c49-135">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="61c49-136">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="61c49-136">GetIterator</span></span> 

<span data-ttu-id="61c49-137">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="61c49-137">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="61c49-138">общедоступный HRESULT- [итератор](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="61c49-138">public HRESULT [GetIterator](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) \*\* iterator)</span></span>

