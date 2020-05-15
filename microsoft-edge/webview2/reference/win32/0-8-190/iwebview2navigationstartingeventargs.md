---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: ee6886e32b32f4da4bbdc04fe6e866210a76488b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655058"
---
# <span data-ttu-id="10a84-104">интерфейс IWebView2NavigationStartingEventArgs</span><span class="sxs-lookup"><span data-stu-id="10a84-104">interface IWebView2NavigationStartingEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="10a84-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="10a84-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="10a84-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="10a84-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

<span data-ttu-id="10a84-107">Аргументы события для события NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10a84-107">Event args for the NavigationStarting event.</span></span>

## <span data-ttu-id="10a84-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="10a84-108">Summary</span></span>

 <span data-ttu-id="10a84-109">Участников</span><span class="sxs-lookup"><span data-stu-id="10a84-109">Members</span></span>                        | <span data-ttu-id="10a84-110">Описания</span><span class="sxs-lookup"><span data-stu-id="10a84-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10a84-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="10a84-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="10a84-112">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="10a84-112">The uri of the requested navigation.</span></span>
[<span data-ttu-id="10a84-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="10a84-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="10a84-114">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="10a84-114">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>
[<span data-ttu-id="10a84-115">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="10a84-115">get_IsRedirected</span></span>](#get_isredirected) | <span data-ttu-id="10a84-116">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="10a84-116">True when the navigation is redirected.</span></span>
[<span data-ttu-id="10a84-117">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="10a84-117">get_RequestHeaders</span></span>](#get_requestheaders) | <span data-ttu-id="10a84-118">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="10a84-118">The HTTP request headers for the navigation.</span></span>
[<span data-ttu-id="10a84-119">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="10a84-119">get_Cancel</span></span>](#get_cancel) | <span data-ttu-id="10a84-120">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="10a84-120">The host may set this flag to cancel the navigation.</span></span>
[<span data-ttu-id="10a84-121">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="10a84-121">put_Cancel</span></span>](#put_cancel) | <span data-ttu-id="10a84-122">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="10a84-122">Set the Cancel property.</span></span>

## <span data-ttu-id="10a84-123">Участников</span><span class="sxs-lookup"><span data-stu-id="10a84-123">Members</span></span>

#### <span data-ttu-id="10a84-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="10a84-124">get_Uri</span></span> 

<span data-ttu-id="10a84-125">URI запрошенной навигации.</span><span class="sxs-lookup"><span data-stu-id="10a84-125">The uri of the requested navigation.</span></span>

> <span data-ttu-id="10a84-126">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="10a84-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="10a84-127">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="10a84-127">get_IsUserInitiated</span></span> 

<span data-ttu-id="10a84-128">Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.</span><span class="sxs-lookup"><span data-stu-id="10a84-128">True when the navigation was initiated through a user gesture as opposed to programmatic navigation.</span></span>

> <span data-ttu-id="10a84-129">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="10a84-129">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

#### <span data-ttu-id="10a84-130">get_IsRedirected</span><span class="sxs-lookup"><span data-stu-id="10a84-130">get_IsRedirected</span></span> 

<span data-ttu-id="10a84-131">Значение true, если перенаправлять навигацию.</span><span class="sxs-lookup"><span data-stu-id="10a84-131">True when the navigation is redirected.</span></span>

> <span data-ttu-id="10a84-132">общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool \* Redirect)</span><span class="sxs-lookup"><span data-stu-id="10a84-132">public HRESULT [get_IsRedirected](#get_isredirected)(BOOL \* isRedirected)</span></span>

#### <span data-ttu-id="10a84-133">get_RequestHeaders</span><span class="sxs-lookup"><span data-stu-id="10a84-133">get_RequestHeaders</span></span> 

<span data-ttu-id="10a84-134">Заголовки HTTP-запроса для навигации.</span><span class="sxs-lookup"><span data-stu-id="10a84-134">The HTTP request headers for the navigation.</span></span>

> <span data-ttu-id="10a84-135">общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \* \* RequestHeaders)</span><span class="sxs-lookup"><span data-stu-id="10a84-135">public HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) \*\* requestHeaders)</span></span>

<span data-ttu-id="10a84-136">Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="10a84-136">Note, you cannot modify the HTTP request headers in a NavigationStarting event.</span></span>

#### <span data-ttu-id="10a84-137">get_Cancel</span><span class="sxs-lookup"><span data-stu-id="10a84-137">get_Cancel</span></span> 

<span data-ttu-id="10a84-138">Ведущее приложение может установить этот флаг, чтобы отменить навигацию.</span><span class="sxs-lookup"><span data-stu-id="10a84-138">The host may set this flag to cancel the navigation.</span></span>

> <span data-ttu-id="10a84-139">общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool \* Cancel)</span><span class="sxs-lookup"><span data-stu-id="10a84-139">public HRESULT [get_Cancel](#get_cancel)(BOOL \* cancel)</span></span>

<span data-ttu-id="10a84-140">Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным.</span><span class="sxs-lookup"><span data-stu-id="10a84-140">If set, it will be as if the navigation never happened and the current page's content will be intact.</span></span> <span data-ttu-id="10a84-141">По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы.</span><span class="sxs-lookup"><span data-stu-id="10a84-141">For performance reasons, GET HTTP requests may happen, while the host is responding.</span></span> <span data-ttu-id="10a84-142">Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.</span><span class="sxs-lookup"><span data-stu-id="10a84-142">This means cookies can be set and used part of a request for the navigation.</span></span>

#### <span data-ttu-id="10a84-143">put_Cancel</span><span class="sxs-lookup"><span data-stu-id="10a84-143">put_Cancel</span></span> 

<span data-ttu-id="10a84-144">Задайте свойство Cancel.</span><span class="sxs-lookup"><span data-stu-id="10a84-144">Set the Cancel property.</span></span>

> <span data-ttu-id="10a84-145">общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)</span><span class="sxs-lookup"><span data-stu-id="10a84-145">public HRESULT [put_Cancel](#put_cancel)(BOOL cancel)</span></span>

