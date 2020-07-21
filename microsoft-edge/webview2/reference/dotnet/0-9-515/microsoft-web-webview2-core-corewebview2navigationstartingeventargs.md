---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2f129f36502ccc404da74904c73c4bdab1d9f472
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886376"
---
# <span data-ttu-id="57d19-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="57d19-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="57d19-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="57d19-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="57d19-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="57d19-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="57d19-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57d19-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="57d19-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="57d19-108">Summary</span></span>

 <span data-ttu-id="57d19-109">Участников</span><span class="sxs-lookup"><span data-stu-id="57d19-109">Members</span></span>                        | <span data-ttu-id="57d19-110">Описания</span><span class="sxs-lookup"><span data-stu-id="57d19-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="57d19-111">Отмена</span><span class="sxs-lookup"><span data-stu-id="57d19-111">Cancel</span></span>](#cancel) | <span data-ttu-id="57d19-112">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="57d19-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="57d19-113">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="57d19-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="57d19-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="57d19-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="57d19-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="57d19-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="57d19-116">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="57d19-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="57d19-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="57d19-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="57d19-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="57d19-118">The ID of the navigation.</span></span>
[<span data-ttu-id="57d19-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="57d19-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="57d19-120">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="57d19-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="57d19-121">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="57d19-121">Uri</span></span>](#uri) | <span data-ttu-id="57d19-122">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="57d19-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="57d19-123">Участников</span><span class="sxs-lookup"><span data-stu-id="57d19-123">Members</span></span>

#### <span data-ttu-id="57d19-124">Отмена</span><span class="sxs-lookup"><span data-stu-id="57d19-124">Cancel</span></span> 

<span data-ttu-id="57d19-125">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="57d19-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="57d19-126">[Отмена](#cancel) открытого bool</span><span class="sxs-lookup"><span data-stu-id="57d19-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="57d19-127">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="57d19-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="57d19-128">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="57d19-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="57d19-129">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="57d19-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="57d19-130">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="57d19-130">IsRedirected</span></span> 

<span data-ttu-id="57d19-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="57d19-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="57d19-132">общедоступный bool [перенаправленный](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="57d19-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="57d19-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="57d19-133">IsUserInitiated</span></span> 

<span data-ttu-id="57d19-134">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="57d19-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="57d19-135">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="57d19-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="57d19-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="57d19-136">NavigationId</span></span> 

<span data-ttu-id="57d19-137">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="57d19-137">The ID of the navigation.</span></span>

> <span data-ttu-id="57d19-138">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="57d19-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="57d19-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="57d19-139">RequestHeaders</span></span> 

<span data-ttu-id="57d19-140">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="57d19-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="57d19-141">общедоступная HttpRequestHeaders [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="57d19-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="57d19-142">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="57d19-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="57d19-143">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="57d19-143">Uri</span></span> 

<span data-ttu-id="57d19-144">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="57d19-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="57d19-145">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="57d19-145">public string [Uri](#uri)</span></span>

