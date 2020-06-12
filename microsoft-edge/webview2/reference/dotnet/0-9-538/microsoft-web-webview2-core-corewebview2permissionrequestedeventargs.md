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
ms.openlocfilehash: 58d87d1815b81969c4424eacfcec26ffe425192e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699134"
---
# <span data-ttu-id="5dd52-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5dd52-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="5dd52-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="5dd52-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="5dd52-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="5dd52-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="5dd52-107">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="5dd52-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="5dd52-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5dd52-108">Summary</span></span>

 <span data-ttu-id="5dd52-109">Участников</span><span class="sxs-lookup"><span data-stu-id="5dd52-109">Members</span></span>                        | <span data-ttu-id="5dd52-110">Описания</span><span class="sxs-lookup"><span data-stu-id="5dd52-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5dd52-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="5dd52-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="5dd52-112">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="5dd52-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="5dd52-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="5dd52-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="5dd52-114">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="5dd52-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="5dd52-115">Состояние</span><span class="sxs-lookup"><span data-stu-id="5dd52-115">State</span></span>](#state) | <span data-ttu-id="5dd52-116">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="5dd52-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="5dd52-117">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="5dd52-117">Uri</span></span>](#uri) | <span data-ttu-id="5dd52-118">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="5dd52-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="5dd52-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="5dd52-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="5dd52-120">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="5dd52-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="5dd52-121">Участников</span><span class="sxs-lookup"><span data-stu-id="5dd52-121">Members</span></span>

#### <span data-ttu-id="5dd52-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="5dd52-122">IsUserInitiated</span></span> 

<span data-ttu-id="5dd52-123">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="5dd52-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="5dd52-124">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="5dd52-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="5dd52-125">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="5dd52-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="5dd52-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="5dd52-126">PermissionKind</span></span> 

<span data-ttu-id="5dd52-127">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="5dd52-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="5dd52-128">общедоступная CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="5dd52-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="5dd52-129">Состояние</span><span class="sxs-lookup"><span data-stu-id="5dd52-129">State</span></span> 

<span data-ttu-id="5dd52-130">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="5dd52-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="5dd52-131">[состояние](#state) общедоступной CoreWebView2PermissionState</span><span class="sxs-lookup"><span data-stu-id="5dd52-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="5dd52-132">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="5dd52-132">whether the request is granted.</span></span>

<span data-ttu-id="5dd52-133">По умолчанию используется значение CoreWebView2PermissionState. Default.</span><span class="sxs-lookup"><span data-stu-id="5dd52-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="5dd52-134">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="5dd52-134">Uri</span></span> 

<span data-ttu-id="5dd52-135">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="5dd52-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="5dd52-136">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="5dd52-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="5dd52-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="5dd52-137">GetDeferral</span></span> 

<span data-ttu-id="5dd52-138">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="5dd52-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="5dd52-139">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="5dd52-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="5dd52-140">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="5dd52-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>
