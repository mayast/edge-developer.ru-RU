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
ms.openlocfilehash: d3b3f4e78ef37ad2101a3a8f817279e999cea3e3
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697618"
---
# <span data-ttu-id="7a20d-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7a20d-104">Microsoft.Web.WebView2.Core.CoreWebView2NavigationCompletedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="7a20d-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7a20d-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7a20d-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="7a20d-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="7a20d-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7a20d-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7a20d-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="7a20d-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7a20d-109">Аргументы события для события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="7a20d-109">Event args for the NavigationCompleted event.</span></span>

## <span data-ttu-id="7a20d-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7a20d-110">Summary</span></span>

 <span data-ttu-id="7a20d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="7a20d-111">Members</span></span>                        | <span data-ttu-id="7a20d-112">Описания</span><span class="sxs-lookup"><span data-stu-id="7a20d-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a20d-113">Удачи</span><span class="sxs-lookup"><span data-stu-id="7a20d-113">IsSuccess</span></span>](#issuccess) | <span data-ttu-id="7a20d-114">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7a20d-114">True when the navigation is successful.</span></span>
[<span data-ttu-id="7a20d-115">NavigationId</span><span class="sxs-lookup"><span data-stu-id="7a20d-115">NavigationId</span></span>](#navigationid) | <span data-ttu-id="7a20d-116">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="7a20d-116">The ID of the navigation.</span></span>
[<span data-ttu-id="7a20d-117">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="7a20d-117">WebErrorStatus</span></span>](#weberrorstatus) | <span data-ttu-id="7a20d-118">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="7a20d-118">The error code if the navigation failed.</span></span>

## <span data-ttu-id="7a20d-119">Участников</span><span class="sxs-lookup"><span data-stu-id="7a20d-119">Members</span></span>

#### <span data-ttu-id="7a20d-120">Удачи</span><span class="sxs-lookup"><span data-stu-id="7a20d-120">IsSuccess</span></span> 

<span data-ttu-id="7a20d-121">Значение true, если навигация выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7a20d-121">True when the navigation is successful.</span></span>

> <span data-ttu-id="7a20d-122">общедоступный bool ( [успешно](#issuccess) )</span><span class="sxs-lookup"><span data-stu-id="7a20d-122">public bool [IsSuccess](#issuccess)</span></span>

<span data-ttu-id="7a20d-123">Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.</span><span class="sxs-lookup"><span data-stu-id="7a20d-123">This is false for a navigation that ended up in an error page (failures due to no network, DNS lookup failure, HTTP server responds with 4xx), but could also be false for additional things such as window.stop() called on navigated page.</span></span>

#### <span data-ttu-id="7a20d-124">NavigationId</span><span class="sxs-lookup"><span data-stu-id="7a20d-124">NavigationId</span></span> 

<span data-ttu-id="7a20d-125">Идентификатор навигации.</span><span class="sxs-lookup"><span data-stu-id="7a20d-125">The ID of the navigation.</span></span>

> <span data-ttu-id="7a20d-126">общедоступный ulong [NavigationId](#navigationid)</span><span class="sxs-lookup"><span data-stu-id="7a20d-126">public ulong [NavigationId](#navigationid)</span></span>

#### <span data-ttu-id="7a20d-127">WebErrorStatus</span><span class="sxs-lookup"><span data-stu-id="7a20d-127">WebErrorStatus</span></span> 

<span data-ttu-id="7a20d-128">Код ошибки, если навигация завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="7a20d-128">The error code if the navigation failed.</span></span>

> <span data-ttu-id="7a20d-129">общедоступная CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span><span class="sxs-lookup"><span data-stu-id="7a20d-129">public CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)</span></span>

