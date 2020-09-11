---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: e7aad408372acbbd19ecab9d04312f21e2396e88
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012479"
---
# <span data-ttu-id="e930a-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="e930a-104">Microsoft.Web.WebView2.Core.CoreWebView2HttpHeadersCollectionIterator class</span></span> 

<span data-ttu-id="e930a-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e930a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e930a-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e930a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e930a-107">Итератор для коллекции заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="e930a-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="e930a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e930a-108">Summary</span></span>

 <span data-ttu-id="e930a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="e930a-109">Members</span></span>                        | <span data-ttu-id="e930a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="e930a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e930a-111">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="e930a-111">HasCurrentHeader</span></span>](#hascurrentheader) | <span data-ttu-id="e930a-112">Имеет значение true, если итератор не исходил из заголовков.</span><span class="sxs-lookup"><span data-stu-id="e930a-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="e930a-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="e930a-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="e930a-114">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e930a-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="e930a-115">Смотрите CoreWebView2HttpRequestHeaders и CoreWebView2HttpResponseHeaders.</span><span class="sxs-lookup"><span data-stu-id="e930a-115">See CoreWebView2HttpRequestHeaders and CoreWebView2HttpResponseHeaders.</span></span>

## <span data-ttu-id="e930a-116">Участников</span><span class="sxs-lookup"><span data-stu-id="e930a-116">Members</span></span>

#### <span data-ttu-id="e930a-117">HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="e930a-117">HasCurrentHeader</span></span> 

<span data-ttu-id="e930a-118">Имеет значение true, если итератор не исходил из заголовков.</span><span class="sxs-lookup"><span data-stu-id="e930a-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="e930a-119">Открытый логический [HasCurrentHeader](#hascurrentheader)</span><span class="sxs-lookup"><span data-stu-id="e930a-119">public bool [HasCurrentHeader](#hascurrentheader)</span></span>

<span data-ttu-id="e930a-120">Если коллекция, в которой находится итератор, является пустой или, если итератор пропало за ее пределами, это ложный.</span><span class="sxs-lookup"><span data-stu-id="e930a-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="e930a-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="e930a-121">MoveNext</span></span> 

<span data-ttu-id="e930a-122">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e930a-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="e930a-123">общедоступный bool [MoveNext](#movenext)()</span><span class="sxs-lookup"><span data-stu-id="e930a-123">public bool [MoveNext](#movenext)()</span></span>

<span data-ttu-id="e930a-124">При отсутствии заголовков HTTP для параметра hasNext будет задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e930a-124">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="e930a-125">После этого метод GetCurrentHeader завершается сбоем, если он вызывается.</span><span class="sxs-lookup"><span data-stu-id="e930a-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>

