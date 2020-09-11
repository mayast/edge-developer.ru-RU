---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 1b80b42bc26316d1fcc8ac74656f24cb0db75bae
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012450"
---
# <span data-ttu-id="535c4-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="535c4-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

<span data-ttu-id="535c4-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="535c4-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="535c4-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="535c4-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="535c4-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="535c4-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="535c4-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="535c4-108">Summary</span></span>

 <span data-ttu-id="535c4-109">Участников</span><span class="sxs-lookup"><span data-stu-id="535c4-109">Members</span></span>                        | <span data-ttu-id="535c4-110">Описания</span><span class="sxs-lookup"><span data-stu-id="535c4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="535c4-111">Отмена</span><span class="sxs-lookup"><span data-stu-id="535c4-111">Cancel</span></span>](#cancel) | <span data-ttu-id="535c4-112">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="535c4-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="535c4-113">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="535c4-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="535c4-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="535c4-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="535c4-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="535c4-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="535c4-116">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="535c4-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="535c4-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="535c4-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="535c4-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="535c4-118">The ID of the navigation.</span></span>
[<span data-ttu-id="535c4-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="535c4-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="535c4-120">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="535c4-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="535c4-121">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="535c4-121">Uri</span></span>](#uri) | <span data-ttu-id="535c4-122">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="535c4-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="535c4-123">Участников</span><span class="sxs-lookup"><span data-stu-id="535c4-123">Members</span></span>

#### <span data-ttu-id="535c4-124">Отмена</span><span class="sxs-lookup"><span data-stu-id="535c4-124">Cancel</span></span> 

<span data-ttu-id="535c4-125">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="535c4-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="535c4-126">[Отмена](#cancel) открытого bool</span><span class="sxs-lookup"><span data-stu-id="535c4-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="535c4-127">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="535c4-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="535c4-128">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="535c4-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="535c4-129">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="535c4-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="535c4-130">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="535c4-130">IsRedirected</span></span> 

<span data-ttu-id="535c4-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="535c4-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="535c4-132">общедоступный bool [перенаправленный](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="535c4-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="535c4-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="535c4-133">IsUserInitiated</span></span> 

<span data-ttu-id="535c4-134">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="535c4-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="535c4-135">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="535c4-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="535c4-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="535c4-136">NavigationId</span></span> 

<span data-ttu-id="535c4-137">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="535c4-137">The ID of the navigation.</span></span>

> <span data-ttu-id="535c4-138">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="535c4-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="535c4-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="535c4-139">RequestHeaders</span></span> 

<span data-ttu-id="535c4-140">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="535c4-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="535c4-141">общедоступная CoreWebView2HttpRequestHeaders [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="535c4-141">public CoreWebView2HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="535c4-142">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="535c4-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="535c4-143">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="535c4-143">Uri</span></span> 

<span data-ttu-id="535c4-144">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="535c4-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="535c4-145">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="535c4-145">public string [Uri](#uri)</span></span>

