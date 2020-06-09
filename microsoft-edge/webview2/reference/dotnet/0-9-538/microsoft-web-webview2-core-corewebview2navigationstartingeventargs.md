---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 58ca180e73c3e4644e466e13c4059f32102f1896
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699136"
---
# <span data-ttu-id="0be9d-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="0be9d-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="0be9d-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="0be9d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="0be9d-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="0be9d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="0be9d-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0be9d-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="0be9d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0be9d-108">Summary</span></span>

 <span data-ttu-id="0be9d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="0be9d-109">Members</span></span>                        | <span data-ttu-id="0be9d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="0be9d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0be9d-111">Отмена</span><span class="sxs-lookup"><span data-stu-id="0be9d-111">Cancel</span></span>](#cancel) | <span data-ttu-id="0be9d-112">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="0be9d-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="0be9d-113">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="0be9d-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="0be9d-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="0be9d-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="0be9d-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0be9d-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="0be9d-116">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="0be9d-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="0be9d-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="0be9d-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="0be9d-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="0be9d-118">The ID of the navigation.</span></span>
[<span data-ttu-id="0be9d-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="0be9d-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="0be9d-120">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="0be9d-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="0be9d-121">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="0be9d-121">Uri</span></span>](#uri) | <span data-ttu-id="0be9d-122">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="0be9d-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="0be9d-123">Участников</span><span class="sxs-lookup"><span data-stu-id="0be9d-123">Members</span></span>

#### <span data-ttu-id="0be9d-124">Отмена</span><span class="sxs-lookup"><span data-stu-id="0be9d-124">Cancel</span></span> 

<span data-ttu-id="0be9d-125">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="0be9d-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="0be9d-126">[Отмена](#cancel) открытого bool</span><span class="sxs-lookup"><span data-stu-id="0be9d-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="0be9d-127">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="0be9d-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="0be9d-128">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="0be9d-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="0be9d-129">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="0be9d-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="0be9d-130">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="0be9d-130">IsRedirected</span></span> 

<span data-ttu-id="0be9d-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="0be9d-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="0be9d-132">общедоступный bool [перенаправленный](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="0be9d-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="0be9d-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0be9d-133">IsUserInitiated</span></span> 

<span data-ttu-id="0be9d-134">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="0be9d-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="0be9d-135">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="0be9d-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="0be9d-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="0be9d-136">NavigationId</span></span> 

<span data-ttu-id="0be9d-137">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="0be9d-137">The ID of the navigation.</span></span>

> <span data-ttu-id="0be9d-138">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="0be9d-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="0be9d-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="0be9d-139">RequestHeaders</span></span> 

<span data-ttu-id="0be9d-140">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="0be9d-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="0be9d-141">общедоступная HttpRequestHeaders [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="0be9d-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="0be9d-142">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="0be9d-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="0be9d-143">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="0be9d-143">Uri</span></span> 

<span data-ttu-id="0be9d-144">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="0be9d-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="0be9d-145">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="0be9d-145">public string [Uri](#uri)</span></span>

