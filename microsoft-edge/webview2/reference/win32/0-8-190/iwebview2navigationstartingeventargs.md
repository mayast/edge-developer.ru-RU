---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 8bc625d12cc3b3ebe06970fd282dd8f60bcabd22
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878402"
---
# <span data-ttu-id="f3a79-104">0.8.355-Interface IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="f3a79-104">0.8.355 - interface IWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="f3a79-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="f3a79-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="f3a79-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="f3a79-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="f3a79-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f3a79-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="f3a79-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f3a79-108">Summary</span></span>

 <span data-ttu-id="f3a79-109">Участников</span><span class="sxs-lookup"><span data-stu-id="f3a79-109">Members</span></span>                        | <span data-ttu-id="f3a79-110">Описания</span><span class="sxs-lookup"><span data-stu-id="f3a79-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f3a79-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f3a79-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="f3a79-112">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="f3a79-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="f3a79-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f3a79-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="f3a79-114">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="f3a79-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="f3a79-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="f3a79-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="f3a79-116">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="f3a79-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="f3a79-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="f3a79-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="f3a79-118">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="f3a79-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="f3a79-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="f3a79-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="f3a79-120">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="f3a79-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="f3a79-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="f3a79-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="f3a79-122">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="f3a79-122">Set the Cancel property.</span></span>

## <span data-ttu-id="f3a79-123">Участников</span><span class="sxs-lookup"><span data-stu-id="f3a79-123">Members</span></span>

#### <span data-ttu-id="f3a79-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f3a79-124">get_Uri</span></span> 

<span data-ttu-id="f3a79-125">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="f3a79-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="f3a79-126">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="f3a79-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="f3a79-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="f3a79-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="f3a79-128">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="f3a79-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="f3a79-129">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="f3a79-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="f3a79-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="f3a79-130">get_IsRedirected</span></span> 

<span data-ttu-id="f3a79-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="f3a79-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="f3a79-132">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="f3a79-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="f3a79-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="f3a79-133">get_RequestHeaders</span></span> 

<span data-ttu-id="f3a79-134">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="f3a79-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="f3a79-135">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="f3a79-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="f3a79-136">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="f3a79-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="f3a79-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="f3a79-137">get_Cancel</span></span> 

<span data-ttu-id="f3a79-138">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="f3a79-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="f3a79-139">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="f3a79-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="f3a79-140">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="f3a79-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="f3a79-141">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="f3a79-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="f3a79-142">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="f3a79-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="f3a79-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="f3a79-143">put_Cancel</span></span> 

<span data-ttu-id="f3a79-144">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="f3a79-144">Set the Cancel property.</span></span>

> <span data-ttu-id="f3a79-145">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="f3a79-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

