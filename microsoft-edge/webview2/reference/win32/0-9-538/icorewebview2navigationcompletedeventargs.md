---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: 482137fd0ffa10c60381d5b0f3dc3d7db6f9fdf7
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011295"
---
# <span data-ttu-id="ac2d0-104">0.9.579-Interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ac2d0-104">0.9.579 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="ac2d0-105">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="ac2d0-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="ac2d0-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ac2d0-106">Summary</span></span>

 <span data-ttu-id="ac2d0-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ac2d0-107">Members</span></span>                        | <span data-ttu-id="ac2d0-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ac2d0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ac2d0-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="ac2d0-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="ac2d0-110">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ac2d0-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="ac2d0-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="ac2d0-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="ac2d0-112">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="ac2d0-112">The ID of the navigation.</span></span>
[<span data-ttu-id="ac2d0-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="ac2d0-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="ac2d0-114">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="ac2d0-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="ac2d0-115">Участников</span><span class="sxs-lookup"><span data-stu-id="ac2d0-115">Members</span></span>

#### <span data-ttu-id="ac2d0-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="ac2d0-116">get_IsSuccess</span></span> 

<span data-ttu-id="ac2d0-117">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ac2d0-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="ac2d0-118">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="ac2d0-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="ac2d0-119">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="ac2d0-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="ac2d0-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="ac2d0-120">get_NavigationId</span></span> 

<span data-ttu-id="ac2d0-121">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="ac2d0-121">The ID of the navigation.</span></span>

> <span data-ttu-id="ac2d0-122">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="ac2d0-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="ac2d0-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="ac2d0-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="ac2d0-124">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="ac2d0-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="ac2d0-125">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="ac2d0-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

