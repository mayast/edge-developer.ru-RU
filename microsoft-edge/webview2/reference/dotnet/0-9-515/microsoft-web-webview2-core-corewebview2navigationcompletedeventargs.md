---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2a18fe9f8f79a109047d029affab8d84a6ef845c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654634"
---
# <span data-ttu-id="21c4d-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="21c4d-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

<span data-ttu-id="21c4d-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="21c4d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="21c4d-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="21c4d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="21c4d-107">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="21c4d-107">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="21c4d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="21c4d-108">Summary</span></span>

 <span data-ttu-id="21c4d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="21c4d-109">Members</span></span>                        | <span data-ttu-id="21c4d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="21c4d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="21c4d-111">Удачи</span><span class="sxs-lookup"><span data-stu-id="21c4d-111">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="21c4d-112">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="21c4d-112">True when the navigation is successful.</span></span>
[<span data-ttu-id="21c4d-113">NavigationId</span><span class="sxs-lookup"><span data-stu-id="21c4d-113">NavigationId</span></span>](#navigationid) | <span data-ttu-id="21c4d-114">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="21c4d-114">The ID of the navigation.</span></span>
[<span data-ttu-id="21c4d-115">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="21c4d-115">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="21c4d-116">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="21c4d-116">The error code if the navigation failed.</span></span>

## <span data-ttu-id="21c4d-117">Участников</span><span class="sxs-lookup"><span data-stu-id="21c4d-117">Members</span></span>

#### <span data-ttu-id="21c4d-118">Удачи</span><span class="sxs-lookup"><span data-stu-id="21c4d-118">IsSuccess</span></span> 

<span data-ttu-id="21c4d-119">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="21c4d-119">True when the navigation is successful.</span></span>

> <span data-ttu-id="21c4d-120">общедоступный bool ( [успешно](#issuccess) )</span><span class="sxs-lookup"><span data-stu-id="21c4d-120">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="21c4d-121">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="21c4d-121">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="21c4d-122">NavigationId</span><span class="sxs-lookup"><span data-stu-id="21c4d-122">NavigationId</span></span> 

<span data-ttu-id="21c4d-123">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="21c4d-123">The ID of the navigation.</span></span>

> <span data-ttu-id="21c4d-124">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="21c4d-124">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="21c4d-125">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="21c4d-125">WebErrorStatus</span></span> 

<span data-ttu-id="21c4d-126">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="21c4d-126">The error code if the navigation failed.</span></span>

> <span data-ttu-id="21c4d-127">общедоступная CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="21c4d-127">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

