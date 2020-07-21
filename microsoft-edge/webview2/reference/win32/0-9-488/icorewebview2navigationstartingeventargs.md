---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a9219266412c2872d9236ef93ce0e03e2dd5f7f2
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886399"
---
# <span data-ttu-id="7eff9-104">0.9.515-Interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="7eff9-104">0.9.515 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="7eff9-105">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="7eff9-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="7eff9-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7eff9-106">Summary</span></span>

 <span data-ttu-id="7eff9-107">Участников</span><span class="sxs-lookup"><span data-stu-id="7eff9-107">Members</span></span>                        | <span data-ttu-id="7eff9-108">Описания</span><span class="sxs-lookup"><span data-stu-id="7eff9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7eff9-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="7eff9-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="7eff9-110">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="7eff9-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="7eff9-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="7eff9-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="7eff9-112">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="7eff9-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="7eff9-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7eff9-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="7eff9-114">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="7eff9-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="7eff9-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7eff9-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="7eff9-116">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="7eff9-116">The ID of the navigation.</span></span>
[<span data-ttu-id="7eff9-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="7eff9-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="7eff9-118">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="7eff9-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="7eff9-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7eff9-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="7eff9-120">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="7eff9-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="7eff9-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="7eff9-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="7eff9-122">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="7eff9-122">Set the Cancel property.</span></span>

## <span data-ttu-id="7eff9-123">Участников</span><span class="sxs-lookup"><span data-stu-id="7eff9-123">Members</span></span>

#### <span data-ttu-id="7eff9-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="7eff9-124">get_Cancel</span></span> 

<span data-ttu-id="7eff9-125">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="7eff9-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="7eff9-126">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="7eff9-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="7eff9-127">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="7eff9-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="7eff9-128">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="7eff9-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="7eff9-129">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="7eff9-129">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="7eff9-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="7eff9-130">get_IsRedirected</span></span> 

<span data-ttu-id="7eff9-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="7eff9-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="7eff9-132">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="7eff9-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="7eff9-133">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="7eff9-133">get_IsUserInitiated</span></span> 

<span data-ttu-id="7eff9-134">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="7eff9-134">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="7eff9-135">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="7eff9-135">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="7eff9-136">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="7eff9-136">get_NavigationId</span></span> 

<span data-ttu-id="7eff9-137">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="7eff9-137">The ID of the navigation.</span></span>

> <span data-ttu-id="7eff9-138">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="7eff9-138">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="7eff9-139">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="7eff9-139">get_RequestHeaders</span></span> 

<span data-ttu-id="7eff9-140">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="7eff9-140">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="7eff9-141">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="7eff9-141">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="7eff9-142">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="7eff9-142">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="7eff9-143">get_Uri</span><span class="sxs-lookup"><span data-stu-id="7eff9-143">get_Uri</span></span> 

<span data-ttu-id="7eff9-144">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="7eff9-144">The uri of the requested navigation.</span></span>

> <span data-ttu-id="7eff9-145">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="7eff9-145">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="7eff9-146">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="7eff9-146">put_Cancel</span></span> 

<span data-ttu-id="7eff9-147">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="7eff9-147">Set the Cancel property.</span></span>

> <span data-ttu-id="7eff9-148">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="7eff9-148">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

