---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012412"
---
# <span data-ttu-id="49b88-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders</span><span class="sxs-lookup"><span data-stu-id="49b88-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpRequestHeaders class</span></span> 

<span data-ttu-id="49b88-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="49b88-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="49b88-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="49b88-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="49b88-107">Заголовки запросов HTTP.</span><span class="sxs-lookup"><span data-stu-id="49b88-107">HTTP request headers.</span></span>

## <span data-ttu-id="49b88-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="49b88-108">Summary</span></span>

 <span data-ttu-id="49b88-109">Участников</span><span class="sxs-lookup"><span data-stu-id="49b88-109">Members</span></span>                        | <span data-ttu-id="49b88-110">Описания</span><span class="sxs-lookup"><span data-stu-id="49b88-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49b88-111">Contains</span><span class="sxs-lookup"><span data-stu-id="49b88-111">Contains</span></span>](#contains) | <span data-ttu-id="49b88-112">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="49b88-112">Checks whether the headers contain an entry matching the header name.</span></span>
[<span data-ttu-id="49b88-113">"Голова"</span><span class="sxs-lookup"><span data-stu-id="49b88-113">GetHeader</span></span>](#getheader) | <span data-ttu-id="49b88-114">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="49b88-114">Gets the header value matching the name.</span></span>
[<span data-ttu-id="49b88-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="49b88-115">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="49b88-116">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="49b88-116">Gets the header value matching the name via an iterator.</span></span>
[<span data-ttu-id="49b88-117">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="49b88-117">GetIterator</span></span>](#getiterator) | <span data-ttu-id="49b88-118">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="49b88-118">Gets an iterator over the collection of request headers.</span></span>
[<span data-ttu-id="49b88-119">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="49b88-119">RemoveHeader</span></span>](#removeheader) | <span data-ttu-id="49b88-120">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="49b88-120">Removes header that matches the name.</span></span>
[<span data-ttu-id="49b88-121">SetHeader</span><span class="sxs-lookup"><span data-stu-id="49b88-121">SetHeader</span></span>](#setheader) | <span data-ttu-id="49b88-122">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="49b88-122">Adds or updates header that matches the name.</span></span>

<span data-ttu-id="49b88-123">Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="49b88-123">Used to inspect the HTTP request on WebResourceRequested event and NavigationStarting event.</span></span> <span data-ttu-id="49b88-124">Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="49b88-124">Note, you can modify the HTTP request headers from a WebResourceRequested event, but not from a NavigationStarting event.</span></span>

## <span data-ttu-id="49b88-125">Участников</span><span class="sxs-lookup"><span data-stu-id="49b88-125">Members</span></span>

#### <span data-ttu-id="49b88-126">Contains</span><span class="sxs-lookup"><span data-stu-id="49b88-126">Contains</span></span> 

<span data-ttu-id="49b88-127">Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.</span><span class="sxs-lookup"><span data-stu-id="49b88-127">Checks whether the headers contain an entry matching the header name.</span></span>

> <span data-ttu-id="49b88-128">общедоступный bool [имеет](#contains)(строковое имя)</span><span class="sxs-lookup"><span data-stu-id="49b88-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="49b88-129">"Голова"</span><span class="sxs-lookup"><span data-stu-id="49b88-129">GetHeader</span></span> 

<span data-ttu-id="49b88-130">Возвращает значение заголовка, совпадающее с именем.</span><span class="sxs-lookup"><span data-stu-id="49b88-130">Gets the header value matching the name.</span></span>

> <span data-ttu-id="49b88-131">[заголовок](#getheader)общедоступной строки (имя строки)</span><span class="sxs-lookup"><span data-stu-id="49b88-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="49b88-132">"Голова"</span><span class="sxs-lookup"><span data-stu-id="49b88-132">GetHeaders</span></span> 

<span data-ttu-id="49b88-133">Возвращает значение заголовка, совпадающее с именем через итератор.</span><span class="sxs-lookup"><span data-stu-id="49b88-133">Gets the header value matching the name via an iterator.</span></span>

> <span data-ttu-id="49b88-134">общедоступные CoreWebView2HttpHeadersCollectionIterator- [заголовки](#getheaders)(строковое имя)</span><span class="sxs-lookup"><span data-stu-id="49b88-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="49b88-135">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="49b88-135">GetIterator</span></span> 

<span data-ttu-id="49b88-136">Получает итератор на коллекцию заголовков запроса.</span><span class="sxs-lookup"><span data-stu-id="49b88-136">Gets an iterator over the collection of request headers.</span></span>

> <span data-ttu-id="49b88-137">Public CoreWebView2HttpHeadersCollectionIterator- [iterator](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="49b88-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>

#### <span data-ttu-id="49b88-138">RemoveHeader</span><span class="sxs-lookup"><span data-stu-id="49b88-138">RemoveHeader</span></span> 

<span data-ttu-id="49b88-139">Удаляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="49b88-139">Removes header that matches the name.</span></span>

> <span data-ttu-id="49b88-140">общедоступная void [RemoveHeader](#removeheader)(строковое имя)</span><span class="sxs-lookup"><span data-stu-id="49b88-140">public void [RemoveHeader](#removeheader)(string name)</span></span>

#### <span data-ttu-id="49b88-141">SetHeader</span><span class="sxs-lookup"><span data-stu-id="49b88-141">SetHeader</span></span> 

<span data-ttu-id="49b88-142">Добавляет или обновляет заголовок, соответствующий имени.</span><span class="sxs-lookup"><span data-stu-id="49b88-142">Adds or updates header that matches the name.</span></span>

> <span data-ttu-id="49b88-143">Public void [SetHeader](#setheader)(строковое имя, строковое значение)</span><span class="sxs-lookup"><span data-stu-id="49b88-143">public void [SetHeader](#setheader)(string name, string value)</span></span>

