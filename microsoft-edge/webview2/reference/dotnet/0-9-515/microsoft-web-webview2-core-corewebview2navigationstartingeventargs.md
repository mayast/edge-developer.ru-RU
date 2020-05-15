---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8b7ac3ab27cf5a2d9e80a77eabc488599820a02f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655046"
---
# <span data-ttu-id="77499-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="77499-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="77499-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="77499-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="77499-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="77499-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="77499-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="77499-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="77499-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="77499-108">Summary</span></span>

 <span data-ttu-id="77499-109">Участников</span><span class="sxs-lookup"><span data-stu-id="77499-109">Members</span></span>                        | <span data-ttu-id="77499-110">Описания</span><span class="sxs-lookup"><span data-stu-id="77499-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="77499-111">Отмена</span><span class="sxs-lookup"><span data-stu-id="77499-111">Cancel</span></span>](#cancel) | <span data-ttu-id="77499-112">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="77499-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="77499-113">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="77499-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="77499-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="77499-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="77499-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="77499-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="77499-116">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="77499-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="77499-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="77499-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="77499-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="77499-118">The ID of the navigation.</span></span>
[<span data-ttu-id="77499-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="77499-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="77499-120">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="77499-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="77499-121">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="77499-121">Uri</span></span>](#uri) | <span data-ttu-id="77499-122">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="77499-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="77499-123">Участников</span><span class="sxs-lookup"><span data-stu-id="77499-123">Members</span></span>

#### <span data-ttu-id="77499-124">Отмена</span><span class="sxs-lookup"><span data-stu-id="77499-124">Cancel</span></span> 

<span data-ttu-id="77499-125">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="77499-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="77499-126">[Отмена](#cancel) открытого bool</span><span class="sxs-lookup"><span data-stu-id="77499-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="77499-127">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="77499-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="77499-128">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="77499-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="77499-129">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="77499-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="77499-130">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="77499-130">IsRedirected</span></span> 

<span data-ttu-id="77499-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="77499-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="77499-132">общедоступный bool [перенаправленный](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="77499-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="77499-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="77499-133">IsUserInitiated</span></span> 

<span data-ttu-id="77499-134">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="77499-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="77499-135">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="77499-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="77499-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="77499-136">NavigationId</span></span> 

<span data-ttu-id="77499-137">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="77499-137">The ID of the navigation.</span></span>

> <span data-ttu-id="77499-138">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="77499-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="77499-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="77499-139">RequestHeaders</span></span> 

<span data-ttu-id="77499-140">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="77499-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="77499-141">общедоступная HttpRequestHeaders [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="77499-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="77499-142">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="77499-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="77499-143">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="77499-143">Uri</span></span> 

<span data-ttu-id="77499-144">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="77499-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="77499-145">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="77499-145">public string [Uri](#uri)</span></span>

