---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: ebfb4aaf3f0c2b5531aaab3783572cf550bebf83
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012537"
---
# <span data-ttu-id="25f3c-104">интерфейс ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="25f3c-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="25f3c-105">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="25f3c-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="25f3c-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="25f3c-106">Summary</span></span>

 <span data-ttu-id="25f3c-107">Участников</span><span class="sxs-lookup"><span data-stu-id="25f3c-107">Members</span></span>                        | <span data-ttu-id="25f3c-108">Описания</span><span class="sxs-lookup"><span data-stu-id="25f3c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="25f3c-109">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="25f3c-109">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="25f3c-110">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="25f3c-110">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="25f3c-111">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="25f3c-111">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="25f3c-112">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="25f3c-112">True when the navigation is redirected.</span></span>
[<span data-ttu-id="25f3c-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="25f3c-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="25f3c-114">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="25f3c-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="25f3c-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="25f3c-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="25f3c-116">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="25f3c-116">The ID of the navigation.</span></span>
[<span data-ttu-id="25f3c-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="25f3c-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="25f3c-118">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="25f3c-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="25f3c-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="25f3c-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="25f3c-120">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="25f3c-120">The uri of the requested navigation.</span></span>
[<span data-ttu-id="25f3c-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="25f3c-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="25f3c-122">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="25f3c-122">Set the Cancel property.</span></span>

## <span data-ttu-id="25f3c-123">Участников</span><span class="sxs-lookup"><span data-stu-id="25f3c-123">Members</span></span>

#### <span data-ttu-id="25f3c-124">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="25f3c-124">get_Cancel</span></span> 

<span data-ttu-id="25f3c-125">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="25f3c-125">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="25f3c-126">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="25f3c-126">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="25f3c-127">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="25f3c-127">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="25f3c-128">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="25f3c-128">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="25f3c-129">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="25f3c-129">This means cookies can be set and used part of a request for the navigation.</span></span> <span data-ttu-id="25f3c-130">Отмена для навигации: пустая или переход по рамкам в srcdoc не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="25f3c-130">Cancellation for navigation to about:blank or frame navigation to srcdoc is not supported.</span></span> <span data-ttu-id="25f3c-131">Такие попытки будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="25f3c-131">Such attempts will be ignored.</span></span>

#### <span data-ttu-id="25f3c-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="25f3c-132">get_IsRedirected</span></span> 

<span data-ttu-id="25f3c-133">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="25f3c-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="25f3c-134">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="25f3c-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="25f3c-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="25f3c-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="25f3c-136">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="25f3c-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="25f3c-137">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="25f3c-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="25f3c-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="25f3c-138">get_NavigationId</span></span> 

<span data-ttu-id="25f3c-139">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="25f3c-139">The ID of the navigation.</span></span>

> <span data-ttu-id="25f3c-140">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* NavigationId)</span><span class="sxs-lookup"><span data-stu-id="25f3c-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigationId)</span></span>

#### <span data-ttu-id="25f3c-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="25f3c-141">get_RequestHeaders</span></span> 

<span data-ttu-id="25f3c-142">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="25f3c-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="25f3c-143">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="25f3c-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="25f3c-144">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="25f3c-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="25f3c-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="25f3c-145">get_Uri</span></span> 

<span data-ttu-id="25f3c-146">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="25f3c-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="25f3c-147">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="25f3c-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="25f3c-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="25f3c-148">put_Cancel</span></span> 

<span data-ttu-id="25f3c-149">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="25f3c-149">Set the Cancel property.</span></span>

> <span data-ttu-id="25f3c-150">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="25f3c-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

