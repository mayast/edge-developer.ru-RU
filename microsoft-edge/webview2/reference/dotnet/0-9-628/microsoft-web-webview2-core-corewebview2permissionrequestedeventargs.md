---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 87993559d4d70daef84cbd86a2305f09cc017aa9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012447"
---
# <span data-ttu-id="a0303-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a0303-104">Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

<span data-ttu-id="a0303-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a0303-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a0303-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a0303-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a0303-107">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="a0303-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="a0303-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a0303-108">Summary</span></span>

 <span data-ttu-id="a0303-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a0303-109">Members</span></span>                        | <span data-ttu-id="a0303-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a0303-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0303-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a0303-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="a0303-112">Значение true, если новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="a0303-112">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>
[<span data-ttu-id="a0303-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="a0303-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="a0303-114">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="a0303-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="a0303-115">Состояние</span><span class="sxs-lookup"><span data-stu-id="a0303-115">State</span></span>](#state) | <span data-ttu-id="a0303-116">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="a0303-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="a0303-117">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="a0303-117">Uri</span></span>](#uri) | <span data-ttu-id="a0303-118">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="a0303-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="a0303-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a0303-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="a0303-120">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="a0303-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="a0303-121">Участников</span><span class="sxs-lookup"><span data-stu-id="a0303-121">Members</span></span>

#### <span data-ttu-id="a0303-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="a0303-122">IsUserInitiated</span></span> 

<span data-ttu-id="a0303-123">Значение true, если новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.</span><span class="sxs-lookup"><span data-stu-id="a0303-123">True when the new window request was initiated through a user gesture such as clicking an anchor tag with target.</span></span>

> <span data-ttu-id="a0303-124">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="a0303-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="a0303-125">Заблокированный блочный блок "Edge" отключен для WebView, поэтому приложение может использовать этот флаг, чтобы заблокировать всплывающие окна, не инициированные пользователем.</span><span class="sxs-lookup"><span data-stu-id="a0303-125">The Edge popup blocker is disabled for WebView so the app can use this flag to block non-user initiated popups.</span></span>

#### <span data-ttu-id="a0303-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="a0303-126">PermissionKind</span></span> 

<span data-ttu-id="a0303-127">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="a0303-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="a0303-128">общедоступная CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="a0303-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="a0303-129">Состояние</span><span class="sxs-lookup"><span data-stu-id="a0303-129">State</span></span> 

<span data-ttu-id="a0303-130">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="a0303-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="a0303-131">[состояние](#state) общедоступной CoreWebView2PermissionState</span><span class="sxs-lookup"><span data-stu-id="a0303-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="a0303-132">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="a0303-132">whether the request is granted.</span></span>

<span data-ttu-id="a0303-133">По умолчанию используется значение CoreWebView2PermissionState. Default.</span><span class="sxs-lookup"><span data-stu-id="a0303-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="a0303-134">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="a0303-134">Uri</span></span> 

<span data-ttu-id="a0303-135">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="a0303-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="a0303-136">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="a0303-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="a0303-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="a0303-137">GetDeferral</span></span> 

<span data-ttu-id="a0303-138">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="a0303-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="a0303-139">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="a0303-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="a0303-140">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="a0303-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

