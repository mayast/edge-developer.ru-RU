---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f9d24d10d9487198988b4c6d3ad4a941a32dc396
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655021"
---
# <span data-ttu-id="56d5f-104">интерфейс ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="56d5f-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="56d5f-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="56d5f-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="56d5f-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="56d5f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="56d5f-107">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="56d5f-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="56d5f-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="56d5f-108">Summary</span></span>

 <span data-ttu-id="56d5f-109">Участников</span><span class="sxs-lookup"><span data-stu-id="56d5f-109">Members</span></span>                        | <span data-ttu-id="56d5f-110">Описания</span><span class="sxs-lookup"><span data-stu-id="56d5f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="56d5f-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="56d5f-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="56d5f-112">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="56d5f-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="56d5f-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="56d5f-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="56d5f-114">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="56d5f-114">The error code if the navigation failed.</span></span>
[<span data-ttu-id="56d5f-115">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="56d5f-115">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="56d5f-116">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="56d5f-116">The ID of the navigation.</span></span>

## <span data-ttu-id="56d5f-117">Участников</span><span class="sxs-lookup"><span data-stu-id="56d5f-117">Members</span></span>

#### <span data-ttu-id="56d5f-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="56d5f-118">get_IsSuccess</span></span> 

<span data-ttu-id="56d5f-119">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="56d5f-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="56d5f-120">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="56d5f-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="56d5f-121">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="56d5f-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="56d5f-122">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="56d5f-122">get_WebErrorStatus</span></span> 

<span data-ttu-id="56d5f-123">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="56d5f-123">The error code if the navigation failed.</span></span>

> <span data-ttu-id="56d5f-124">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="56d5f-124">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS \* CORE_WEBVIEW2_WEB_ERROR_STATUS)</span></span>

#### <span data-ttu-id="56d5f-125">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="56d5f-125">get_NavigationId</span></span> 

<span data-ttu-id="56d5f-126">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="56d5f-126">The ID of the navigation.</span></span>

> <span data-ttu-id="56d5f-127">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="56d5f-127">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

