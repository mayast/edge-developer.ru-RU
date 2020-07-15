---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c2ac2e499e6bbd49f411a001e061af72fda524b5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877884"
---
# <span data-ttu-id="75fd9-104">0.9.430-Interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="75fd9-104">0.9.430 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="75fd9-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="75fd9-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="75fd9-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="75fd9-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="75fd9-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="75fd9-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="75fd9-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="75fd9-108">Summary</span></span>

 <span data-ttu-id="75fd9-109">Участников</span><span class="sxs-lookup"><span data-stu-id="75fd9-109">Members</span></span>                        | <span data-ttu-id="75fd9-110">Описания</span><span class="sxs-lookup"><span data-stu-id="75fd9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="75fd9-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="75fd9-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="75fd9-112">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="75fd9-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="75fd9-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="75fd9-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="75fd9-114">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="75fd9-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="75fd9-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="75fd9-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="75fd9-116">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="75fd9-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="75fd9-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="75fd9-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="75fd9-118">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="75fd9-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="75fd9-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="75fd9-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="75fd9-120">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="75fd9-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="75fd9-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="75fd9-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="75fd9-122">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="75fd9-122">Set the Cancel property.</span></span>
[<span data-ttu-id="75fd9-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="75fd9-123">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="75fd9-124">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="75fd9-124">The ID of the navigation.</span></span>

## <span data-ttu-id="75fd9-125">Участников</span><span class="sxs-lookup"><span data-stu-id="75fd9-125">Members</span></span>

#### <span data-ttu-id="75fd9-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="75fd9-126">get_Uri</span></span> 

<span data-ttu-id="75fd9-127">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="75fd9-127">The uri of the requested navigation.</span></span>

> <span data-ttu-id="75fd9-128">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="75fd9-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="75fd9-129">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="75fd9-129">get_IsUserInitiated</span></span> 

<span data-ttu-id="75fd9-130">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="75fd9-130">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="75fd9-131">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="75fd9-131">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="75fd9-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="75fd9-132">get_IsRedirected</span></span> 

<span data-ttu-id="75fd9-133">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="75fd9-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="75fd9-134">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="75fd9-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="75fd9-135">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="75fd9-135">get_RequestHeaders</span></span> 

<span data-ttu-id="75fd9-136">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="75fd9-136">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="75fd9-137">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="75fd9-137">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="75fd9-138">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="75fd9-138">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="75fd9-139">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="75fd9-139">get_Cancel</span></span> 

<span data-ttu-id="75fd9-140">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="75fd9-140">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="75fd9-141">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="75fd9-141">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="75fd9-142">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="75fd9-142">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="75fd9-143">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="75fd9-143">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="75fd9-144">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="75fd9-144">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="75fd9-145">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="75fd9-145">put_Cancel</span></span> 

<span data-ttu-id="75fd9-146">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="75fd9-146">Set the Cancel property.</span></span>

> <span data-ttu-id="75fd9-147">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="75fd9-147">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="75fd9-148">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="75fd9-148">get_NavigationId</span></span> 

<span data-ttu-id="75fd9-149">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="75fd9-149">The ID of the navigation.</span></span>

> <span data-ttu-id="75fd9-150">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="75fd9-150">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

