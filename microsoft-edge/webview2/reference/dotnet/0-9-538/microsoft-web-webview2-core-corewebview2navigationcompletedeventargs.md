---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 01102cc9aa9d6fbec7f4d223e1115892dabe2899
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010973"
---
# <span data-ttu-id="56131-104">класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="56131-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="56131-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="56131-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="56131-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="56131-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="56131-107">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="56131-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="56131-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="56131-108">Summary</span></span>

 <span data-ttu-id="56131-109">Участников</span><span class="sxs-lookup"><span data-stu-id="56131-109">Members</span></span>                        | <span data-ttu-id="56131-110">Описания</span><span class="sxs-lookup"><span data-stu-id="56131-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="56131-111">Удачи</span><span class="sxs-lookup"><span data-stu-id="56131-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="56131-112">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="56131-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="56131-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="56131-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="56131-114">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="56131-114">The ID of the navigation.</span></span>
[<span data-ttu-id="56131-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="56131-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="56131-116">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="56131-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="56131-117">Участников</span><span class="sxs-lookup"><span data-stu-id="56131-117">Members</span></span>

#### <span data-ttu-id="56131-118">Удачи</span><span class="sxs-lookup"><span data-stu-id="56131-118">IsSuccess</span></span> 

<span data-ttu-id="56131-119">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="56131-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="56131-120">общедоступный bool ( [успешно](#issuccess) )</span><span class="sxs-lookup"><span data-stu-id="56131-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="56131-121">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="56131-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="56131-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="56131-122">NavigationId</span></span> 

<span data-ttu-id="56131-123">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="56131-123">The ID of the navigation.</span></span>

> <span data-ttu-id="56131-124">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="56131-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="56131-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="56131-125">WebErrorStatus</span></span> 

<span data-ttu-id="56131-126">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="56131-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="56131-127">общедоступная CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="56131-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

