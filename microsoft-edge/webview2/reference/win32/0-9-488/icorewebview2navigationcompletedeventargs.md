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
ms.openlocfilehash: 83f55e19c8c8c0f2fb075ff47e95e34be27c6602
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697338"
---
# <span data-ttu-id="09293-104">интерфейс ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="09293-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="09293-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="09293-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="09293-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="09293-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="09293-107">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="09293-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="09293-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="09293-108">Summary</span></span>

 <span data-ttu-id="09293-109">Участников</span><span class="sxs-lookup"><span data-stu-id="09293-109">Members</span></span>                        | <span data-ttu-id="09293-110">Описания</span><span class="sxs-lookup"><span data-stu-id="09293-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09293-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="09293-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="09293-112">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="09293-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="09293-113">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="09293-113">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="09293-114">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="09293-114">The ID of the navigation.</span></span>
[<span data-ttu-id="09293-115">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="09293-115">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="09293-116">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="09293-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="09293-117">Участников</span><span class="sxs-lookup"><span data-stu-id="09293-117">Members</span></span>

#### <span data-ttu-id="09293-118">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="09293-118">get_IsSuccess</span></span> 

<span data-ttu-id="09293-119">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="09293-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="09293-120">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="09293-120">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="09293-121">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="09293-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="09293-122">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="09293-122">get_NavigationId</span></span> 

<span data-ttu-id="09293-123">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="09293-123">The ID of the navigation.</span></span>

> <span data-ttu-id="09293-124">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span><span class="sxs-lookup"><span data-stu-id="09293-124">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigation_id)</span></span>

#### <span data-ttu-id="09293-125">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="09293-125">get_WebErrorStatus</span></span> 

<span data-ttu-id="09293-126">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="09293-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="09293-127">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="09293-127">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* COREWEBVIEW2_WEB_ERROR_STATUS)</span></span>

