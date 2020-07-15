---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c13d0625669d6303c115c3d415d12278cfbe8320
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880502"
---
# <span data-ttu-id="49187-104">0.9.515-Interface ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="49187-104">0.9.515 - interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="49187-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="49187-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="49187-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="49187-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="49187-107">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="49187-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="49187-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="49187-108">Summary</span></span>

 <span data-ttu-id="49187-109">Участников</span><span class="sxs-lookup"><span data-stu-id="49187-109">Members</span></span>                        | <span data-ttu-id="49187-110">Описания</span><span class="sxs-lookup"><span data-stu-id="49187-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49187-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="49187-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="49187-112">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="49187-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="49187-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="49187-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="49187-114">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="49187-114">The ID of the navigation.</span></span>
[<span data-ttu-id="49187-115">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="49187-115">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="49187-116">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="49187-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="49187-117">Участников</span><span class="sxs-lookup"><span data-stu-id="49187-117">Members</span></span>

#### <span data-ttu-id="49187-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="49187-118">get_IsSuccess</span></span> 

<span data-ttu-id="49187-119">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="49187-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="49187-120">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="49187-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="49187-121">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="49187-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="49187-122">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="49187-122">get_NavigationId</span></span> 

<span data-ttu-id="49187-123">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="49187-123">The ID of the navigation.</span></span>

> <span data-ttu-id="49187-124">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="49187-124">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="49187-125">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="49187-125">get_WebErrorStatus</span></span> 

<span data-ttu-id="49187-126">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="49187-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="49187-127">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="49187-127">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

