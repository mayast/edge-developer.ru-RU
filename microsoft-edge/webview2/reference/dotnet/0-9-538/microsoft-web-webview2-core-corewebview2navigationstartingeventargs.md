---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 5f63cd8a9dc16ee82d77fe4b5a0b705eb79e7c6f
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010945"
---
# <span data-ttu-id="31fe6-104">класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="31fe6-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="31fe6-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="31fe6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="31fe6-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="31fe6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="31fe6-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="31fe6-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="31fe6-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="31fe6-108">Summary</span></span>

 <span data-ttu-id="31fe6-109">Участников</span><span class="sxs-lookup"><span data-stu-id="31fe6-109">Members</span></span>                        | <span data-ttu-id="31fe6-110">Описания</span><span class="sxs-lookup"><span data-stu-id="31fe6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="31fe6-111">Отмена</span><span class="sxs-lookup"><span data-stu-id="31fe6-111">Cancel</span></span>](#cancel) | <span data-ttu-id="31fe6-112">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="31fe6-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="31fe6-113">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="31fe6-113">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="31fe6-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="31fe6-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="31fe6-115">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="31fe6-115">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="31fe6-116">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="31fe6-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="31fe6-117">NavigationId</span><span class="sxs-lookup"><span data-stu-id="31fe6-117">NavigationId</span></span>](#navigationid) | <span data-ttu-id="31fe6-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="31fe6-118">The ID of the navigation.</span></span>
[<span data-ttu-id="31fe6-119">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="31fe6-119">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="31fe6-120">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="31fe6-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="31fe6-121">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="31fe6-121">Uri</span></span>](#uri) | <span data-ttu-id="31fe6-122">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="31fe6-122">The uri of the requested navigation.</span></span>

## <span data-ttu-id="31fe6-123">Участников</span><span class="sxs-lookup"><span data-stu-id="31fe6-123">Members</span></span>

#### <span data-ttu-id="31fe6-124">Отмена</span><span class="sxs-lookup"><span data-stu-id="31fe6-124">Cancel</span></span> 

<span data-ttu-id="31fe6-125">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="31fe6-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="31fe6-126">[Отмена](#cancel) открытого bool</span><span class="sxs-lookup"><span data-stu-id="31fe6-126">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="31fe6-127">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="31fe6-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="31fe6-128">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="31fe6-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="31fe6-129">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="31fe6-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="31fe6-130">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="31fe6-130">IsRedirected</span></span> 

<span data-ttu-id="31fe6-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="31fe6-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="31fe6-132">общедоступный bool [перенаправленный](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="31fe6-132">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="31fe6-133">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="31fe6-133">IsUserInitiated</span></span> 

<span data-ttu-id="31fe6-134">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="31fe6-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="31fe6-135">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="31fe6-135">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="31fe6-136">NavigationId</span><span class="sxs-lookup"><span data-stu-id="31fe6-136">NavigationId</span></span> 

<span data-ttu-id="31fe6-137">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="31fe6-137">The ID of the navigation.</span></span>

> <span data-ttu-id="31fe6-138">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="31fe6-138">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="31fe6-139">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="31fe6-139">RequestHeaders</span></span> 

<span data-ttu-id="31fe6-140">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="31fe6-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="31fe6-141">общедоступная HttpRequestHeaders [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="31fe6-141">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="31fe6-142">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="31fe6-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="31fe6-143">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="31fe6-143">Uri</span></span> 

<span data-ttu-id="31fe6-144">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="31fe6-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="31fe6-145">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="31fe6-145">public string [Uri](#uri)</span></span>

