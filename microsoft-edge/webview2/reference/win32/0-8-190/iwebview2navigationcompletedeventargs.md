---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: b496c37949e934fadf0af736059566edcab9f5c3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885935"
---
# <span data-ttu-id="b4b8b-104">0.8.355-Interface IWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b4b8b-104">0.8.355 - interface IWebView2NavigationCompletedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NavigationCompletedEventArgs
  : public IUnknown
```

<span data-ttu-id="b4b8b-105">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="b4b8b-105">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="b4b8b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b4b8b-106">Summary</span></span>

 <span data-ttu-id="b4b8b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="b4b8b-107">Members</span></span>                        | <span data-ttu-id="b4b8b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="b4b8b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b4b8b-109">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="b4b8b-109">get_IsSuccess</span></span>](#get_issuccess) | <span data-ttu-id="b4b8b-110">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b4b8b-110">True when the navigation is successful.</span></span>
[<span data-ttu-id="b4b8b-111">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="b4b8b-111">get_WebErrorStatus</span></span>](#get_weberrorstatus) | <span data-ttu-id="b4b8b-112">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="b4b8b-112">The error code if the navigation failed.</span></span>

## <span data-ttu-id="b4b8b-113">Участников</span><span class="sxs-lookup"><span data-stu-id="b4b8b-113">Members</span></span>

#### <span data-ttu-id="b4b8b-114">get_IsSuccess</span><span class="sxs-lookup"><span data-stu-id="b4b8b-114">get_IsSuccess</span></span> 

<span data-ttu-id="b4b8b-115">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="b4b8b-115">True when the navigation is successful.</span></span>

> <span data-ttu-id="b4b8b-116">общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool \* "успешно")</span><span class="sxs-lookup"><span data-stu-id="b4b8b-116">public HRESULT [get_IsSuccess](#get_issuccess)(BOOL \* isSuccess)</span></span>

<span data-ttu-id="b4b8b-117">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="b4b8b-117">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="b4b8b-118">get_WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="b4b8b-118">get_WebErrorStatus</span></span> 

<span data-ttu-id="b4b8b-119">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="b4b8b-119">The error code if the navigation failed.</span></span>

> <span data-ttu-id="b4b8b-120">общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span><span class="sxs-lookup"><span data-stu-id="b4b8b-120">public HRESULT [get_WebErrorStatus](#get_weberrorstatus)(WEBVIEW2_WEB_ERROR_STATUS \* WEBVIEW2_WEB_ERROR_STATUS)</span></span>

