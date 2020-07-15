---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: cd692de6aaa3dc694fb2fe149411e5fd64de1ee2
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878871"
---
# <span data-ttu-id="c5063-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="c5063-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="c5063-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c5063-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c5063-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="c5063-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c5063-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="c5063-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="c5063-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c5063-108">Summary</span></span>

 <span data-ttu-id="c5063-109">Участников</span><span class="sxs-lookup"><span data-stu-id="c5063-109">Members</span></span>                        | <span data-ttu-id="c5063-110">Описания</span><span class="sxs-lookup"><span data-stu-id="c5063-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c5063-111">Отмена</span><span class="sxs-lookup"><span data-stu-id="c5063-111">Cancel</span></span>](#cancel) | <span data-ttu-id="c5063-112">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="c5063-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="c5063-113">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="c5063-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="c5063-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="c5063-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="c5063-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c5063-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="c5063-116">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="c5063-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="c5063-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="c5063-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="c5063-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="c5063-118">The ID of the navigation.</span></span>
[<span data-ttu-id="c5063-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="c5063-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="c5063-120">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="c5063-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="c5063-121">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="c5063-121">Uri</span></span>](#uri) | <span data-ttu-id="c5063-122">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="c5063-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="c5063-123">Участников</span><span class="sxs-lookup"><span data-stu-id="c5063-123">Members</span></span>

#### <span data-ttu-id="c5063-124">Отмена</span><span class="sxs-lookup"><span data-stu-id="c5063-124">Cancel</span></span> 

<span data-ttu-id="c5063-125">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="c5063-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="c5063-126">[Отмена](#cancel) открытого bool</span><span class="sxs-lookup"><span data-stu-id="c5063-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="c5063-127">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="c5063-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="c5063-128">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="c5063-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="c5063-129">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="c5063-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="c5063-130">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="c5063-130">IsRedirected</span></span> 

<span data-ttu-id="c5063-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="c5063-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="c5063-132">общедоступный bool [перенаправленный](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="c5063-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="c5063-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="c5063-133">IsUserInitiated</span></span> 

<span data-ttu-id="c5063-134">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="c5063-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="c5063-135">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="c5063-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="c5063-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="c5063-136">NavigationId</span></span> 

<span data-ttu-id="c5063-137">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="c5063-137">The ID of the navigation.</span></span>

> <span data-ttu-id="c5063-138">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="c5063-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="c5063-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="c5063-139">RequestHeaders</span></span> 

<span data-ttu-id="c5063-140">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="c5063-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="c5063-141">общедоступная HttpRequestHeaders [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="c5063-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="c5063-142">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="c5063-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="c5063-143">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="c5063-143">Uri</span></span> 

<span data-ttu-id="c5063-144">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="c5063-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="c5063-145">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="c5063-145">public string [Uri](#uri)</span></span>

