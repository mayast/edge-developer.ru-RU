---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 21c78d88237e525f6e0ff8d9c604cd023209599c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654709"
---
# <span data-ttu-id="dc072-104">интерфейс ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="dc072-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="dc072-105">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="dc072-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="dc072-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="dc072-106">Summary</span></span>

 <span data-ttu-id="dc072-107">Участников</span><span class="sxs-lookup"><span data-stu-id="dc072-107">Members</span></span>                        | <span data-ttu-id="dc072-108">Описания</span><span class="sxs-lookup"><span data-stu-id="dc072-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="dc072-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="dc072-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="dc072-110">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dc072-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="dc072-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="dc072-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="dc072-112">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="dc072-112">The ID of the navigation.</span></span>
[<span data-ttu-id="dc072-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="dc072-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="dc072-114">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="dc072-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="dc072-115">Участников</span><span class="sxs-lookup"><span data-stu-id="dc072-115">Members</span></span>

#### <span data-ttu-id="dc072-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="dc072-116">get_IsSuccess</span></span> 

<span data-ttu-id="dc072-117">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="dc072-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="dc072-118">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="dc072-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="dc072-119">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="dc072-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="dc072-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="dc072-120">get_NavigationId</span></span> 

<span data-ttu-id="dc072-121">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="dc072-121">The ID of the navigation.</span></span>

> <span data-ttu-id="dc072-122">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="dc072-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="dc072-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="dc072-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="dc072-124">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="dc072-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="dc072-125">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="dc072-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

