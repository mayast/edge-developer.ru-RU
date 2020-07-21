---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 5996f0eff4db17530750eb39c7693ea0f8496a4d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885900"
---
# <span data-ttu-id="3cd25-104">0.8.355-Interface IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="3cd25-104">0.8.355 - interface IWebView2NavigationStartingEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="3cd25-105">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3cd25-105">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="3cd25-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3cd25-106">Summary</span></span>

 <span data-ttu-id="3cd25-107">Участников</span><span class="sxs-lookup"><span data-stu-id="3cd25-107">Members</span></span>                        | <span data-ttu-id="3cd25-108">Описания</span><span class="sxs-lookup"><span data-stu-id="3cd25-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3cd25-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="3cd25-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="3cd25-110">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="3cd25-110">The uri of the requested navigation.</span></span>
[<span data-ttu-id="3cd25-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="3cd25-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="3cd25-112">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="3cd25-112">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="3cd25-113">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="3cd25-113">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="3cd25-114">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="3cd25-114">True when the navigation is redirected.</span></span>
[<span data-ttu-id="3cd25-115">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3cd25-115">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="3cd25-116">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="3cd25-116">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="3cd25-117">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="3cd25-117">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="3cd25-118">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="3cd25-118">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="3cd25-119">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="3cd25-119">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="3cd25-120">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="3cd25-120">Set the Cancel property.</span></span>

## <span data-ttu-id="3cd25-121">Участников</span><span class="sxs-lookup"><span data-stu-id="3cd25-121">Members</span></span>

#### <span data-ttu-id="3cd25-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="3cd25-122">get_Uri</span></span> 

<span data-ttu-id="3cd25-123">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="3cd25-123">The uri of the requested navigation.</span></span>

> <span data-ttu-id="3cd25-124">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="3cd25-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="3cd25-125">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="3cd25-125">get_IsUserInitiated</span></span> 

<span data-ttu-id="3cd25-126">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="3cd25-126">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="3cd25-127">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="3cd25-127">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="3cd25-128">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="3cd25-128">get_IsRedirected</span></span> 

<span data-ttu-id="3cd25-129">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="3cd25-129">True when the navigation is redirected.</span></span>

> <span data-ttu-id="3cd25-130">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="3cd25-130">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="3cd25-131">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="3cd25-131">get_RequestHeaders</span></span> 

<span data-ttu-id="3cd25-132">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="3cd25-132">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="3cd25-133">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="3cd25-133">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="3cd25-134">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="3cd25-134">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="3cd25-135">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="3cd25-135">get_Cancel</span></span> 

<span data-ttu-id="3cd25-136">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="3cd25-136">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="3cd25-137">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="3cd25-137">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="3cd25-138">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="3cd25-138">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="3cd25-139">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="3cd25-139">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="3cd25-140">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="3cd25-140">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="3cd25-141">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="3cd25-141">put_Cancel</span></span> 

<span data-ttu-id="3cd25-142">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="3cd25-142">Set the Cancel property.</span></span>

> <span data-ttu-id="3cd25-143">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="3cd25-143">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

