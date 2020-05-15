---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b0b868b99d3f77679b3684a20e7744d7a22fd715
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654808"
---
# <span data-ttu-id="02019-104">интерфейс ICoreWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="02019-104">interface ICoreWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="02019-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="02019-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="02019-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="02019-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="02019-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="02019-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="02019-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="02019-108">Summary</span></span>

 <span data-ttu-id="02019-109">Участников</span><span class="sxs-lookup"><span data-stu-id="02019-109">Members</span></span>                        | <span data-ttu-id="02019-110">Описания</span><span class="sxs-lookup"><span data-stu-id="02019-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="02019-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="02019-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="02019-112">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="02019-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="02019-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="02019-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="02019-114">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="02019-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="02019-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="02019-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="02019-116">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="02019-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="02019-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="02019-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="02019-118">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="02019-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="02019-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="02019-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="02019-120">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="02019-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="02019-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="02019-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="02019-122">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="02019-122">Set the Cancel property.</span></span>
[<span data-ttu-id="02019-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="02019-123">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="02019-124">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="02019-124">The ID of the navigation.</span></span>

## <span data-ttu-id="02019-125">Участников</span><span class="sxs-lookup"><span data-stu-id="02019-125">Members</span></span>

#### <span data-ttu-id="02019-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="02019-126">get_Uri</span></span> 

<span data-ttu-id="02019-127">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="02019-127">The uri of the requested navigation.</span></span>

> <span data-ttu-id="02019-128">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="02019-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="02019-129">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="02019-129">get_IsUserInitiated</span></span> 

<span data-ttu-id="02019-130">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="02019-130">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="02019-131">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="02019-131">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="02019-132">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="02019-132">get_IsRedirected</span></span> 

<span data-ttu-id="02019-133">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="02019-133">True when the navigation is redirected.</span></span>

> <span data-ttu-id="02019-134">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="02019-134">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="02019-135">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="02019-135">get_RequestHeaders</span></span> 

<span data-ttu-id="02019-136">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="02019-136">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="02019-137">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="02019-137">public HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="02019-138">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="02019-138">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="02019-139">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="02019-139">get_Cancel</span></span> 

<span data-ttu-id="02019-140">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="02019-140">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="02019-141">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="02019-141">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="02019-142">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="02019-142">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="02019-143">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="02019-143">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="02019-144">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="02019-144">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="02019-145">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="02019-145">put_Cancel</span></span> 

<span data-ttu-id="02019-146">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="02019-146">Set the Cancel property.</span></span>

> <span data-ttu-id="02019-147">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="02019-147">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

#### <span data-ttu-id="02019-148">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="02019-148">get_NavigationId</span></span> 

<span data-ttu-id="02019-149">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="02019-149">The ID of the navigation.</span></span>

> <span data-ttu-id="02019-150">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="02019-150">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

