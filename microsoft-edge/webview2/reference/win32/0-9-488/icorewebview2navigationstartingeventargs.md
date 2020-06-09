---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d56f40a9780313c79f421559eaf54750828542a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697191"
---
# <span data-ttu-id="1717a-104">интерфейс ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="1717a-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="1717a-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1717a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1717a-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="1717a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="1717a-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="1717a-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="1717a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1717a-108">Summary</span></span>

 <span data-ttu-id="1717a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="1717a-109">Members</span></span>                        | <span data-ttu-id="1717a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="1717a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1717a-111">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="1717a-111">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="1717a-112">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="1717a-112">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="1717a-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="1717a-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="1717a-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="1717a-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="1717a-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="1717a-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="1717a-116">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="1717a-116">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="1717a-117">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="1717a-117">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="1717a-118">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="1717a-118">The ID of the navigation.</span></span>
[<span data-ttu-id="1717a-119">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="1717a-119">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="1717a-120">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="1717a-120">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="1717a-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="1717a-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="1717a-122">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="1717a-122">The uri of the requested navigation.</span></span>
[<span data-ttu-id="1717a-123">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="1717a-123">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="1717a-124">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="1717a-124">Set the Cancel property.</span></span>

## <span data-ttu-id="1717a-125">Участников</span><span class="sxs-lookup"><span data-stu-id="1717a-125">Members</span></span>

#### <span data-ttu-id="1717a-126">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="1717a-126">get_Cancel</span></span> 

<span data-ttu-id="1717a-127">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="1717a-127">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="1717a-128">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="1717a-128">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="1717a-129">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="1717a-129">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="1717a-130">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="1717a-130">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="1717a-131">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="1717a-131">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="1717a-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="1717a-132">get_IsRedirected</span></span> 

<span data-ttu-id="1717a-133">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="1717a-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="1717a-134">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="1717a-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="1717a-135">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="1717a-135">get_IsUserInitiated</span></span> 

<span data-ttu-id="1717a-136">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="1717a-136">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="1717a-137">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="1717a-137">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="1717a-138">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="1717a-138">get_NavigationId</span></span> 

<span data-ttu-id="1717a-139">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="1717a-139">The ID of the navigation.</span></span>

> <span data-ttu-id="1717a-140">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="1717a-140">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="1717a-141">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="1717a-141">get_RequestHeaders</span></span> 

<span data-ttu-id="1717a-142">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="1717a-142">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="1717a-143">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="1717a-143">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="1717a-144">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="1717a-144">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="1717a-145">get_Uri</span><span class="sxs-lookup"><span data-stu-id="1717a-145">get_Uri</span></span> 

<span data-ttu-id="1717a-146">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="1717a-146">The uri of the requested navigation.</span></span>

> <span data-ttu-id="1717a-147">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="1717a-147">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="1717a-148">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="1717a-148">put_Cancel</span></span> 

<span data-ttu-id="1717a-149">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="1717a-149">Set the Cancel property.</span></span>

> <span data-ttu-id="1717a-150">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="1717a-150">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

