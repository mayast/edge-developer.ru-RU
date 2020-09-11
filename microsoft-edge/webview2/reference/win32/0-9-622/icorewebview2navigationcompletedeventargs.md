---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NavigationCompletedEventArgs
ms.openlocfilehash: b45920cfdab8a01d1288fbaf566748545b8a2c98
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012461"
---
# <span data-ttu-id="055de-104">интерфейс ICoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="055de-104">interface ICoreWebView2NavigationCompletedEventArgs</span></span> 

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="055de-105">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="055de-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="055de-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="055de-106">Summary</span></span>

 <span data-ttu-id="055de-107">Участников</span><span class="sxs-lookup"><span data-stu-id="055de-107">Members</span></span>                        | <span data-ttu-id="055de-108">Описания</span><span class="sxs-lookup"><span data-stu-id="055de-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="055de-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="055de-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="055de-110">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="055de-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="055de-111">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="055de-111">get_NavigationId</span></span>](#get_navigationid) | <span data-ttu-id="055de-112">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="055de-112">The ID of the navigation.</span></span>
[<span data-ttu-id="055de-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="055de-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="055de-114">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="055de-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="055de-115">Участников</span><span class="sxs-lookup"><span data-stu-id="055de-115">Members</span></span>

#### <span data-ttu-id="055de-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="055de-116">get_IsSuccess</span></span> 

<span data-ttu-id="055de-117">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="055de-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="055de-118">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="055de-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="055de-119">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных сценариев, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="055de-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional scenarios such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="055de-120">get_NavigationId</span><span class="sxs-lookup"><span data-stu-id="055de-120">get_NavigationId</span></span> 

<span data-ttu-id="055de-121">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="055de-121">The ID of the navigation.</span></span>

> <span data-ttu-id="055de-122">общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* NavigationId)</span><span class="sxs-lookup"><span data-stu-id="055de-122">public HRESULT [get_NavigationId](#get_navigationid)(UINT64 \* navigationId)</span></span>

#### <span data-ttu-id="055de-123">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="055de-123">get_WebErrorStatus</span></span> 

<span data-ttu-id="055de-124">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="055de-124">The error code if the navigation failed.</span></span>

> <span data-ttu-id="055de-125">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* WebErrorStatus)</span><span class="sxs-lookup"><span data-stu-id="055de-125">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(COREWEBVIEW2_WEB_ERROR_STATUS \* webErrorStatus)</span></span>

