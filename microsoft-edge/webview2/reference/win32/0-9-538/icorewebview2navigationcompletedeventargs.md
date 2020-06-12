---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 11d7e5ffef11a445c55cd4a9d70fcbbb8087c024
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699231"
---
# <span data-ttu-id="2c6d9-104">интерфейс ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2c6d9-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="2c6d9-105">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2c6d9-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="2c6d9-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2c6d9-106">Summary</span></span>

 <span data-ttu-id="2c6d9-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2c6d9-107">Members</span></span>                        | <span data-ttu-id="2c6d9-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2c6d9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2c6d9-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="2c6d9-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="2c6d9-110">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2c6d9-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="2c6d9-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="2c6d9-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="2c6d9-112">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="2c6d9-112">The ID of the navigation.</span></span>
[<span data-ttu-id="2c6d9-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="2c6d9-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="2c6d9-114">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="2c6d9-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="2c6d9-115">Участников</span><span class="sxs-lookup"><span data-stu-id="2c6d9-115">Members</span></span>

#### <span data-ttu-id="2c6d9-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="2c6d9-116">get_IsSuccess</span></span> 

<span data-ttu-id="2c6d9-117">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2c6d9-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="2c6d9-118">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="2c6d9-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="2c6d9-119">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="2c6d9-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="2c6d9-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="2c6d9-120">get_NavigationId</span></span> 

<span data-ttu-id="2c6d9-121">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="2c6d9-121">The ID of the navigation.</span></span>

> <span data-ttu-id="2c6d9-122">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="2c6d9-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="2c6d9-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="2c6d9-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="2c6d9-124">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="2c6d9-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="2c6d9-125">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="2c6d9-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>
