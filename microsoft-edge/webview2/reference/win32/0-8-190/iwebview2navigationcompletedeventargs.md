---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 7c10e669b4caf13f43f858e343c9bad3da155518
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878416"
---
# <span data-ttu-id="2aab5-104">0.8.355-Interface IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2aab5-104">0.8.355 - interface IWebView2NavigationCompletedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="2aab5-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="2aab5-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="2aab5-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="2aab5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="2aab5-107">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="2aab5-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="2aab5-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2aab5-108">Summary</span></span>

 <span data-ttu-id="2aab5-109">Участников</span><span class="sxs-lookup"><span data-stu-id="2aab5-109">Members</span></span>                        | <span data-ttu-id="2aab5-110">Описания</span><span class="sxs-lookup"><span data-stu-id="2aab5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2aab5-111">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="2aab5-111">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="2aab5-112">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2aab5-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="2aab5-113">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="2aab5-113">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="2aab5-114">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="2aab5-114">The error code if the navigation failed.</span></span>

## <span data-ttu-id="2aab5-115">Участников</span><span class="sxs-lookup"><span data-stu-id="2aab5-115">Members</span></span>

#### <span data-ttu-id="2aab5-116">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="2aab5-116">get_IsSuccess</span></span> 

<span data-ttu-id="2aab5-117">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="2aab5-117">True when the navigation is successful.</span></span>

> <span data-ttu-id="2aab5-118">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="2aab5-118">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="2aab5-119">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="2aab5-119">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="2aab5-120">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="2aab5-120">get_WebErrorStatus</span></span> 

<span data-ttu-id="2aab5-121">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="2aab5-121">The error code if the navigation failed.</span></span>

> <span data-ttu-id="2aab5-122">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="2aab5-122">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>

