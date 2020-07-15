---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9aa44483fc824f8a26af6293f031c58d681de624
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880474"
---
# <span data-ttu-id="49e59-104">0.9.515-Interface ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="49e59-104">0.9.515 - interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="49e59-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="49e59-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="49e59-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="49e59-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="49e59-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="49e59-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="49e59-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="49e59-108">Summary</span></span>

 <span data-ttu-id="49e59-109">Участников</span><span class="sxs-lookup"><span data-stu-id="49e59-109">Members</span></span>                        | <span data-ttu-id="49e59-110">Описания</span><span class="sxs-lookup"><span data-stu-id="49e59-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49e59-111">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="49e59-111">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="49e59-112">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="49e59-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="49e59-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="49e59-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="49e59-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="49e59-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="49e59-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="49e59-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="49e59-116">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="49e59-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="49e59-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="49e59-117">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="49e59-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="49e59-118">The ID of the navigation.</span></span>
[<span data-ttu-id="49e59-119">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="49e59-119">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="49e59-120">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="49e59-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="49e59-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="49e59-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="49e59-122">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="49e59-122">The uri of the requested navigation.</span></span>
[<span data-ttu-id="49e59-123">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="49e59-123">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="49e59-124">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="49e59-124">Set the Cancel property.</span></span>

## <span data-ttu-id="49e59-125">Участников</span><span class="sxs-lookup"><span data-stu-id="49e59-125">Members</span></span>

#### <span data-ttu-id="49e59-126">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="49e59-126">get_Cancel</span></span> 

<span data-ttu-id="49e59-127">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="49e59-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="49e59-128">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="49e59-128">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="49e59-129">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="49e59-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="49e59-130">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="49e59-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="49e59-131">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="49e59-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="49e59-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="49e59-132">get_IsRedirected</span></span> 

<span data-ttu-id="49e59-133">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="49e59-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="49e59-134">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="49e59-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="49e59-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="49e59-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="49e59-136">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="49e59-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="49e59-137">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="49e59-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="49e59-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="49e59-138">get_NavigationId</span></span> 

<span data-ttu-id="49e59-139">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="49e59-139">The ID of the navigation.</span></span>

> <span data-ttu-id="49e59-140">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="49e59-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="49e59-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="49e59-141">get_RequestHeaders</span></span> 

<span data-ttu-id="49e59-142">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="49e59-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="49e59-143">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="49e59-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="49e59-144">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="49e59-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="49e59-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="49e59-145">get_Uri</span></span> 

<span data-ttu-id="49e59-146">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="49e59-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="49e59-147">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="49e59-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="49e59-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="49e59-148">put_Cancel</span></span> 

<span data-ttu-id="49e59-149">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="49e59-149">Set the Cancel property.</span></span>

> <span data-ttu-id="49e59-150">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="49e59-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

