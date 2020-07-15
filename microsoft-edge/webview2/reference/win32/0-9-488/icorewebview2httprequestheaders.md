---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2587a3e07869076be659e29d484a647b74c2bd7f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880551"
---
# <span data-ttu-id="eff0e-104">0.9.515-Interface ICoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="eff0e-104">0.9.515 - interface ICoreWebView2HttpRequestHeaders</span></span> 

> [!NOTE]
> <span data-ttu-id="eff0e-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="eff0e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="eff0e-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="eff0e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

<span data-ttu-id="eff0e-107">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="eff0e-107">HTTP request headers.</span></span>

## <span data-ttu-id="eff0e-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="eff0e-108">Summary</span></span>

 <span data-ttu-id="eff0e-109">Участников</span><span class="sxs-lookup"><span data-stu-id="eff0e-109">Members</span></span>                        | <span data-ttu-id="eff0e-110">Описания</span><span class="sxs-lookup"><span data-stu-id="eff0e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eff0e-111">Contains</span><span class="sxs-lookup"><span data-stu-id="eff0e-111">Contains</span></span>](#contains) | <span data-ttu-id="eff0e-112">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="eff0e-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="eff0e-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="eff0e-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="eff0e-114">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="eff0e-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="eff0e-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="eff0e-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="eff0e-116">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="eff0e-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="eff0e-117">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="eff0e-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="eff0e-118">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="eff0e-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="eff0e-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="eff0e-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="eff0e-120">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="eff0e-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="eff0e-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="eff0e-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="eff0e-122">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="eff0e-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="eff0e-123">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="eff0e-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="eff0e-124">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="eff0e-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="eff0e-125">Участников</span><span class="sxs-lookup"><span data-stu-id="eff0e-125">Members</span></span>

#### <span data-ttu-id="eff0e-126">Contains</span><span class="sxs-lookup"><span data-stu-id="eff0e-126">Contains</span></span> 

<span data-ttu-id="eff0e-127">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="eff0e-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="eff0e-128">общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool \* Contains)</span><span class="sxs-lookup"><span data-stu-id="eff0e-128">public HRESULT [Contains](#contains)(LPCWSTR name, BOOL \* contains)</span></span>

#### <span data-ttu-id="eff0e-129">"Голова"</span><span class="sxs-lookup"><span data-stu-id="eff0e-129">GetHeader</span></span> 

<span data-ttu-id="eff0e-130">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="eff0e-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="eff0e-131">общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR \* Value)</span><span class="sxs-lookup"><span data-stu-id="eff0e-131">public HRESULT [GetHeader](#getheader)(LPCWSTR name, LPWSTR \* value)</span></span>

#### <span data-ttu-id="eff0e-132">"Голова"</span><span class="sxs-lookup"><span data-stu-id="eff0e-132">GetHeaders</span></span> 

<span data-ttu-id="eff0e-133">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="eff0e-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="eff0e-134">общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \* итератор)</span><span class="sxs-lookup"><span data-stu-id="eff0e-134">public HRESULT [GetHeaders](#getheaders)(LPCWSTR name, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="eff0e-135">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="eff0e-135">GetIterator</span></span> 

<span data-ttu-id="eff0e-136">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="eff0e-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="eff0e-137">общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \* \*)</span><span class="sxs-lookup"><span data-stu-id="eff0e-137">public HRESULT [GetIterator](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) \*\* iterator)</span></span>

#### <span data-ttu-id="eff0e-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="eff0e-138">RemoveHeader</span></span> 

<span data-ttu-id="eff0e-139">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="eff0e-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="eff0e-140">общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="eff0e-140">public HRESULT [RemoveHeader](#removeheader)(LPCWSTR name)</span></span>

#### <span data-ttu-id="eff0e-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="eff0e-141">SetHeader</span></span> 

<span data-ttu-id="eff0e-142">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="eff0e-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="eff0e-143">общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="eff0e-143">public HRESULT [SetHeader](#setheader)(LPCWSTR name, LPCWSTR value)</span></span>

