---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ea3936ac1267fa085f62db843f5cac3fad2635b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879788"
---
# <span data-ttu-id="e7159-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="e7159-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="e7159-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e7159-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e7159-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="e7159-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="e7159-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e7159-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e7159-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e7159-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e7159-109">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="e7159-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="e7159-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e7159-110">Summary</span></span>

 <span data-ttu-id="e7159-111">Участников</span><span class="sxs-lookup"><span data-stu-id="e7159-111">Members</span></span>                        | <span data-ttu-id="e7159-112">Описания</span><span class="sxs-lookup"><span data-stu-id="e7159-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e7159-113">Отмена</span><span class="sxs-lookup"><span data-stu-id="e7159-113">Cancel</span></span>](#cancel) | <span data-ttu-id="e7159-114">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="e7159-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="e7159-115">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="e7159-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="e7159-116">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="e7159-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="e7159-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e7159-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="e7159-118">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="e7159-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="e7159-119">NavigationId</span><span class="sxs-lookup"><span data-stu-id="e7159-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="e7159-120">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="e7159-120">The ID of the navigation.</span></span>
[<span data-ttu-id="e7159-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="e7159-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="e7159-122">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="e7159-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="e7159-123">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="e7159-123">Uri</span></span>](#uri) | <span data-ttu-id="e7159-124">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="e7159-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="e7159-125">Участников</span><span class="sxs-lookup"><span data-stu-id="e7159-125">Members</span></span>

#### <span data-ttu-id="e7159-126">Отмена</span><span class="sxs-lookup"><span data-stu-id="e7159-126">Cancel</span></span> 

<span data-ttu-id="e7159-127">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="e7159-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="e7159-128">[Отмена](#cancel) открытого bool</span><span class="sxs-lookup"><span data-stu-id="e7159-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="e7159-129">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="e7159-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="e7159-130">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="e7159-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="e7159-131">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="e7159-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="e7159-132">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="e7159-132">IsRedirected</span></span> 

<span data-ttu-id="e7159-133">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="e7159-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="e7159-134">общедоступный bool [перенаправленный](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="e7159-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="e7159-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e7159-135">IsUserInitiated</span></span> 

<span data-ttu-id="e7159-136">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="e7159-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="e7159-137">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="e7159-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="e7159-138">NavigationId</span><span class="sxs-lookup"><span data-stu-id="e7159-138">NavigationId</span></span> 

<span data-ttu-id="e7159-139">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="e7159-139">The ID of the navigation.</span></span>

> <span data-ttu-id="e7159-140">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="e7159-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="e7159-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="e7159-141">RequestHeaders</span></span> 

<span data-ttu-id="e7159-142">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="e7159-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="e7159-143">общедоступная HttpRequestHeaders [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="e7159-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="e7159-144">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="e7159-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="e7159-145">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="e7159-145">Uri</span></span> 

<span data-ttu-id="e7159-146">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="e7159-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="e7159-147">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="e7159-147">public string [Uri](#uri)</span></span>

