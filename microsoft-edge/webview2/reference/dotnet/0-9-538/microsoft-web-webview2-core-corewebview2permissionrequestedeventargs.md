---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: ede6cef20a1a0f5fcd0780376b5ddec07bf05d26
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878801"
---
# <span data-ttu-id="fedbd-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="fedbd-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="fedbd-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="fedbd-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="fedbd-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="fedbd-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="fedbd-107">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="fedbd-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="fedbd-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fedbd-108">Summary</span></span>

 <span data-ttu-id="fedbd-109">Участников</span><span class="sxs-lookup"><span data-stu-id="fedbd-109">Members</span></span>                        | <span data-ttu-id="fedbd-110">Описания</span><span class="sxs-lookup"><span data-stu-id="fedbd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fedbd-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="fedbd-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="fedbd-112">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="fedbd-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="fedbd-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="fedbd-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="fedbd-114">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="fedbd-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="fedbd-115">Состояние</span><span class="sxs-lookup"><span data-stu-id="fedbd-115">State</span></span>](#state) | <span data-ttu-id="fedbd-116">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="fedbd-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="fedbd-117">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="fedbd-117">Uri</span></span>](#uri) | <span data-ttu-id="fedbd-118">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="fedbd-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="fedbd-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="fedbd-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="fedbd-120">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="fedbd-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="fedbd-121">Участников</span><span class="sxs-lookup"><span data-stu-id="fedbd-121">Members</span></span>

#### <span data-ttu-id="fedbd-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="fedbd-122">IsUserInitiated</span></span> 

<span data-ttu-id="fedbd-123">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="fedbd-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="fedbd-124">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="fedbd-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="fedbd-125">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="fedbd-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="fedbd-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="fedbd-126">PermissionKind</span></span> 

<span data-ttu-id="fedbd-127">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="fedbd-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="fedbd-128">общедоступная CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="fedbd-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="fedbd-129">Состояние</span><span class="sxs-lookup"><span data-stu-id="fedbd-129">State</span></span> 

<span data-ttu-id="fedbd-130">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="fedbd-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="fedbd-131">[состояние](#state) общедоступной CoreWebView2PermissionState</span><span class="sxs-lookup"><span data-stu-id="fedbd-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="fedbd-132">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="fedbd-132">whether the request is granted.</span></span>

<span data-ttu-id="fedbd-133">По умолчанию используется значение CoreWebView2PermissionState. Default.</span><span class="sxs-lookup"><span data-stu-id="fedbd-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="fedbd-134">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="fedbd-134">Uri</span></span> 

<span data-ttu-id="fedbd-135">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="fedbd-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="fedbd-136">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="fedbd-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="fedbd-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="fedbd-137">GetDeferral</span></span> 

<span data-ttu-id="fedbd-138">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="fedbd-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="fedbd-139">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="fedbd-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="fedbd-140">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="fedbd-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

