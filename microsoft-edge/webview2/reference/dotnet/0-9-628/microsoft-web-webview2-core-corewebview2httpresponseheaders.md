---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 51218283460975421859c65da8a43553767ad216
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012476"
---
# <span data-ttu-id="8b2d6-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders</span><span class="sxs-lookup"><span data-stu-id="8b2d6-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpResponseHeaders class</span></span> 

<span data-ttu-id="8b2d6-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8b2d6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8b2d6-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="8b2d6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8b2d6-107">Заголовки ответа HTTP.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-107">HTTP response headers.</span></span>

## <span data-ttu-id="8b2d6-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8b2d6-108">Summary</span></span>

 <span data-ttu-id="8b2d6-109">Участников</span><span class="sxs-lookup"><span data-stu-id="8b2d6-109">Members</span></span>                        | <span data-ttu-id="8b2d6-110">Описания</span><span class="sxs-lookup"><span data-stu-id="8b2d6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8b2d6-111">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="8b2d6-111">AppendHeader</span></span>](#appendheader) | <span data-ttu-id="8b2d6-112">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-112">Appends header line with name and value.</span></span>
[<span data-ttu-id="8b2d6-113">Contains</span><span class="sxs-lookup"><span data-stu-id="8b2d6-113">Contains</span></span>](#contains) | <span data-ttu-id="8b2d6-114">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-114">Checks whether the headers contain entries matching the header name.</span></span>
[<span data-ttu-id="8b2d6-115">"Голова"</span><span class="sxs-lookup"><span data-stu-id="8b2d6-115">GetHeader</span></span>](#getheader) | <span data-ttu-id="8b2d6-116">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-116">Gets the first header value in the collection matching the name.</span></span>
[<span data-ttu-id="8b2d6-117">"Голова"</span><span class="sxs-lookup"><span data-stu-id="8b2d6-117">GetHeaders</span></span>](#getheaders) | <span data-ttu-id="8b2d6-118">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-118">Gets the header values matching the name.</span></span>
[<span data-ttu-id="8b2d6-119">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="8b2d6-119">GetIterator</span></span>](#getiterator) | <span data-ttu-id="8b2d6-120">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-120">Gets an iterator over the collection of entire response headers.</span></span>

<span data-ttu-id="8b2d6-121">Используется для создания WebResourceResponse для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-121">Used to construct a WebResourceResponse for the WebResourceRequested event.</span></span>

## <span data-ttu-id="8b2d6-122">Участников</span><span class="sxs-lookup"><span data-stu-id="8b2d6-122">Members</span></span>

#### <span data-ttu-id="8b2d6-123">AppendHeader</span><span class="sxs-lookup"><span data-stu-id="8b2d6-123">AppendHeader</span></span> 

<span data-ttu-id="8b2d6-124">Добавляет строку заголовка с именем и значением.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-124">Appends header line with name and value.</span></span>

> <span data-ttu-id="8b2d6-125">Public void [AppendHeader](#appendheader)(строковое имя, строковое значение)</span><span class="sxs-lookup"><span data-stu-id="8b2d6-125">public void [AppendHeader](#appendheader)(string name, string value)</span></span>

#### <span data-ttu-id="8b2d6-126">Contains</span><span class="sxs-lookup"><span data-stu-id="8b2d6-126">Contains</span></span> 

<span data-ttu-id="8b2d6-127">Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-127">Checks whether the headers contain entries matching the header name.</span></span>

> <span data-ttu-id="8b2d6-128">общедоступный bool [имеет](#contains)(строковое имя)</span><span class="sxs-lookup"><span data-stu-id="8b2d6-128">public bool [Contains](#contains)(string name)</span></span>

#### <span data-ttu-id="8b2d6-129">"Голова"</span><span class="sxs-lookup"><span data-stu-id="8b2d6-129">GetHeader</span></span> 

<span data-ttu-id="8b2d6-130">Возвращает значение первого заголовка в коллекции, соответствующее имени.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-130">Gets the first header value in the collection matching the name.</span></span>

> <span data-ttu-id="8b2d6-131">[заголовок](#getheader)общедоступной строки (имя строки)</span><span class="sxs-lookup"><span data-stu-id="8b2d6-131">public string [GetHeader](#getheader)(string name)</span></span>

#### <span data-ttu-id="8b2d6-132">"Голова"</span><span class="sxs-lookup"><span data-stu-id="8b2d6-132">GetHeaders</span></span> 

<span data-ttu-id="8b2d6-133">Возвращает значения заголовков, соответствующие имени.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-133">Gets the header values matching the name.</span></span>

> <span data-ttu-id="8b2d6-134">общедоступные CoreWebView2HttpHeadersCollectionIterator- [заголовки](#getheaders)(строковое имя)</span><span class="sxs-lookup"><span data-stu-id="8b2d6-134">public CoreWebView2HttpHeadersCollectionIterator [GetHeaders](#getheaders)(string name)</span></span>

#### <span data-ttu-id="8b2d6-135">Реверсивный итератор</span><span class="sxs-lookup"><span data-stu-id="8b2d6-135">GetIterator</span></span> 

<span data-ttu-id="8b2d6-136">Получает итератор на коллекцию всех заголовков ответа.</span><span class="sxs-lookup"><span data-stu-id="8b2d6-136">Gets an iterator over the collection of entire response headers.</span></span>

> <span data-ttu-id="8b2d6-137">Public CoreWebView2HttpHeadersCollectionIterator- [iterator](#getiterator)()</span><span class="sxs-lookup"><span data-stu-id="8b2d6-137">public CoreWebView2HttpHeadersCollectionIterator [GetIterator](#getiterator)()</span></span>

