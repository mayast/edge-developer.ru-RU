---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: bd9d10d5f281b2e8f0a5d0687235560c44edc170
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886439"
---
# <span data-ttu-id="a1a6b-104">0.9.430-Interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="a1a6b-104">0.9.430 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="a1a6b-105">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="a1a6b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a1a6b-106">Summary</span></span>

 <span data-ttu-id="a1a6b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="a1a6b-107">Members</span></span>                        | <span data-ttu-id="a1a6b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="a1a6b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a1a6b-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a1a6b-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="a1a6b-110">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-110">The uri of the requested navigation.</span></span>
[<span data-ttu-id="a1a6b-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a1a6b-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="a1a6b-112">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-112">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="a1a6b-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="a1a6b-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="a1a6b-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="a1a6b-115">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a1a6b-115">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="a1a6b-116">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-116">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="a1a6b-117">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="a1a6b-117">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="a1a6b-118">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-118">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="a1a6b-119">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="a1a6b-119">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="a1a6b-120">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-120">Set the Cancel property.</span></span>
[<span data-ttu-id="a1a6b-121">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a1a6b-121">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="a1a6b-122">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-122">The ID of the navigation.</span></span>

## <span data-ttu-id="a1a6b-123">Участников</span><span class="sxs-lookup"><span data-stu-id="a1a6b-123">Members</span></span>

#### <span data-ttu-id="a1a6b-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="a1a6b-124">get_Uri</span></span> 

<span data-ttu-id="a1a6b-125">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="a1a6b-126">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="a1a6b-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="a1a6b-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a1a6b-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="a1a6b-128">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="a1a6b-129">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="a1a6b-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="a1a6b-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="a1a6b-130">get_IsRedirected</span></span> 

<span data-ttu-id="a1a6b-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="a1a6b-132">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="a1a6b-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="a1a6b-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="a1a6b-133">get_RequestHeaders</span></span> 

<span data-ttu-id="a1a6b-134">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="a1a6b-135">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="a1a6b-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="a1a6b-136">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="a1a6b-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="a1a6b-137">get_Cancel</span></span> 

<span data-ttu-id="a1a6b-138">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="a1a6b-139">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="a1a6b-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="a1a6b-140">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="a1a6b-141">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="a1a6b-142">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="a1a6b-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="a1a6b-143">put_Cancel</span></span> 

<span data-ttu-id="a1a6b-144">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-144">Set the Cancel property.</span></span>

> <span data-ttu-id="a1a6b-145">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="a1a6b-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="a1a6b-146">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="a1a6b-146">get_NavigationId</span></span> 

<span data-ttu-id="a1a6b-147">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="a1a6b-147">The ID of the navigation.</span></span>

> <span data-ttu-id="a1a6b-148">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="a1a6b-148">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

