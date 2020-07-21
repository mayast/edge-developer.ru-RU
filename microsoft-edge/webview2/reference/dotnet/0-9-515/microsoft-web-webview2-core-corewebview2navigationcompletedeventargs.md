---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e2e973e2ee1817decd24bbc1d0dc3daa9709795c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885081"
---
# <span data-ttu-id="f419b-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f419b-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="f419b-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f419b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f419b-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f419b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f419b-107">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f419b-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="f419b-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f419b-108">Summary</span></span>

 <span data-ttu-id="f419b-109">Участников</span><span class="sxs-lookup"><span data-stu-id="f419b-109">Members</span></span>                        | <span data-ttu-id="f419b-110">Описания</span><span class="sxs-lookup"><span data-stu-id="f419b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f419b-111">Удачи</span><span class="sxs-lookup"><span data-stu-id="f419b-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="f419b-112">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f419b-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="f419b-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="f419b-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="f419b-114">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="f419b-114">The ID of the navigation.</span></span>
[<span data-ttu-id="f419b-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="f419b-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="f419b-116">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="f419b-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="f419b-117">Участников</span><span class="sxs-lookup"><span data-stu-id="f419b-117">Members</span></span>

#### <span data-ttu-id="f419b-118">Удачи</span><span class="sxs-lookup"><span data-stu-id="f419b-118">IsSuccess</span></span> 

<span data-ttu-id="f419b-119">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="f419b-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="f419b-120">общедоступный bool ( [успешно](#issuccess) )</span><span class="sxs-lookup"><span data-stu-id="f419b-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="f419b-121">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="f419b-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="f419b-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="f419b-122">NavigationId</span></span> 

<span data-ttu-id="f419b-123">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="f419b-123">The ID of the navigation.</span></span>

> <span data-ttu-id="f419b-124">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="f419b-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="f419b-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="f419b-125">WebErrorStatus</span></span> 

<span data-ttu-id="f419b-126">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="f419b-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="f419b-127">общедоступная CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="f419b-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

