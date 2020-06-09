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
ms.openlocfilehash: 98e242ace5eb0ae5958ddb1eb6cd380d194294be
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697632"
---
# <span data-ttu-id="75a07-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="75a07-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationStartingEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="75a07-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="75a07-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="75a07-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="75a07-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="75a07-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="75a07-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="75a07-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="75a07-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="75a07-109">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="75a07-109">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="75a07-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="75a07-110">Summary</span></span>

 <span data-ttu-id="75a07-111">Участников</span><span class="sxs-lookup"><span data-stu-id="75a07-111">Members</span></span>                        | <span data-ttu-id="75a07-112">Описания</span><span class="sxs-lookup"><span data-stu-id="75a07-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="75a07-113">Отмена</span><span class="sxs-lookup"><span data-stu-id="75a07-113">Cancel</span></span>](#cancel) | <span data-ttu-id="75a07-114">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="75a07-114">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="75a07-115">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="75a07-115">IsRedirected</span></span>](#isredirected) | <span data-ttu-id="75a07-116">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="75a07-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="75a07-117">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="75a07-117">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="75a07-118">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="75a07-118">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="75a07-119">NavigationId</span><span class="sxs-lookup"><span data-stu-id="75a07-119">NavigationId</span></span>](#navigationid) | <span data-ttu-id="75a07-120">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="75a07-120">The ID of the navigation.</span></span>
[<span data-ttu-id="75a07-121">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="75a07-121">RequestHeaders</span></span>](#requestheaders) | <span data-ttu-id="75a07-122">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="75a07-122">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="75a07-123">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="75a07-123">Uri</span></span>](#uri) | <span data-ttu-id="75a07-124">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="75a07-124">The uri of the requested navigation.</span></span>

## <span data-ttu-id="75a07-125">Участников</span><span class="sxs-lookup"><span data-stu-id="75a07-125">Members</span></span>

#### <span data-ttu-id="75a07-126">Отмена</span><span class="sxs-lookup"><span data-stu-id="75a07-126">Cancel</span></span> 

<span data-ttu-id="75a07-127">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="75a07-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="75a07-128">[Отмена](#cancel) открытого bool</span><span class="sxs-lookup"><span data-stu-id="75a07-128">public bool [Cancel](#cancel)</span></span>

<span data-ttu-id="75a07-129">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="75a07-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="75a07-130">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="75a07-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="75a07-131">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="75a07-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="75a07-132">Redirect (перенаправление)</span><span class="sxs-lookup"><span data-stu-id="75a07-132">IsRedirected</span></span> 

<span data-ttu-id="75a07-133">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="75a07-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="75a07-134">общедоступный bool [перенаправленный](#isredirected)</span><span class="sxs-lookup"><span data-stu-id="75a07-134">public bool [IsRedirected](#isredirected)</span></span>

#### <span data-ttu-id="75a07-135">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="75a07-135">IsUserInitiated</span></span> 

<span data-ttu-id="75a07-136">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="75a07-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="75a07-137">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="75a07-137">public bool [IsUserInitiated](#isuserinitiated)</span></span>

#### <span data-ttu-id="75a07-138">NavigationId</span><span class="sxs-lookup"><span data-stu-id="75a07-138">NavigationId</span></span> 

<span data-ttu-id="75a07-139">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="75a07-139">The ID of the navigation.</span></span>

> <span data-ttu-id="75a07-140">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="75a07-140">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="75a07-141">RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="75a07-141">RequestHeaders</span></span> 

<span data-ttu-id="75a07-142">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="75a07-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="75a07-143">общедоступная HttpRequestHeaders [RequestHeaders](#requestheaders)</span><span class="sxs-lookup"><span data-stu-id="75a07-143">public HttpRequestHeaders [RequestHeaders](#requestheaders)</span></span>

<span data-ttu-id="75a07-144">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="75a07-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="75a07-145">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="75a07-145">Uri</span></span> 

<span data-ttu-id="75a07-146">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="75a07-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="75a07-147">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="75a07-147">public string [Uri](#uri)</span></span>

