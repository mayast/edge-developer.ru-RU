---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 099a022fef47beca0e0163e6e0e070aa37520a06
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883730"
---
# <span data-ttu-id="aef69-104">0.9.430-Interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="aef69-104">0.9.430 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="aef69-105">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="aef69-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="aef69-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="aef69-106">Summary</span></span>

 <span data-ttu-id="aef69-107">Участников</span><span class="sxs-lookup"><span data-stu-id="aef69-107">Members</span></span>                        | <span data-ttu-id="aef69-108">Описания</span><span class="sxs-lookup"><span data-stu-id="aef69-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aef69-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="aef69-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="aef69-110">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aef69-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="aef69-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="aef69-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="aef69-112">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="aef69-112">The error code if the navigation failed.</span></span>
[<span data-ttu-id="aef69-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="aef69-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="aef69-114">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="aef69-114">The ID of the navigation.</span></span>

## <span data-ttu-id="aef69-115">Участников</span><span class="sxs-lookup"><span data-stu-id="aef69-115">Members</span></span>

#### <span data-ttu-id="aef69-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="aef69-116">get_IsSuccess</span></span> 

<span data-ttu-id="aef69-117">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="aef69-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="aef69-118">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="aef69-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="aef69-119">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="aef69-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="aef69-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="aef69-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="aef69-121">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="aef69-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="aef69-122">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="aef69-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="aef69-123">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="aef69-123">get_NavigationId</span></span> 

<span data-ttu-id="aef69-124">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="aef69-124">The ID of the navigation.</span></span>

> <span data-ttu-id="aef69-125">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="aef69-125">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

