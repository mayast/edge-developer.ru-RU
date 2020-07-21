---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2bfa4559824c9bb397648249ead8fa8cb60c281c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884633"
---
# <span data-ttu-id="8db1c-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8db1c-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="8db1c-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8db1c-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8db1c-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="8db1c-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8db1c-107">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="8db1c-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="8db1c-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8db1c-108">Summary</span></span>

 <span data-ttu-id="8db1c-109">Участников</span><span class="sxs-lookup"><span data-stu-id="8db1c-109">Members</span></span>                        | <span data-ttu-id="8db1c-110">Описания</span><span class="sxs-lookup"><span data-stu-id="8db1c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8db1c-111">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="8db1c-111">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="8db1c-112">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="8db1c-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="8db1c-113">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="8db1c-113">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="8db1c-114">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="8db1c-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="8db1c-115">Состояние</span><span class="sxs-lookup"><span data-stu-id="8db1c-115">State</span></span>](#state) | <span data-ttu-id="8db1c-116">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="8db1c-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="8db1c-117">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="8db1c-117">Uri</span></span>](#uri) | <span data-ttu-id="8db1c-118">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="8db1c-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="8db1c-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8db1c-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="8db1c-120">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="8db1c-120">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="8db1c-121">Участников</span><span class="sxs-lookup"><span data-stu-id="8db1c-121">Members</span></span>

#### <span data-ttu-id="8db1c-122">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="8db1c-122">IsUserInitiated</span></span> 

<span data-ttu-id="8db1c-123">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="8db1c-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="8db1c-124">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="8db1c-124">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="8db1c-125">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="8db1c-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="8db1c-126">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="8db1c-126">PermissionKind</span></span> 

<span data-ttu-id="8db1c-127">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="8db1c-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="8db1c-128">общедоступная CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="8db1c-128">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="8db1c-129">Состояние</span><span class="sxs-lookup"><span data-stu-id="8db1c-129">State</span></span> 

<span data-ttu-id="8db1c-130">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="8db1c-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="8db1c-131">[состояние](#state) общедоступной CoreWebView2PermissionState</span><span class="sxs-lookup"><span data-stu-id="8db1c-131">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="8db1c-132">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="8db1c-132">whether the request is granted.</span></span>

<span data-ttu-id="8db1c-133">По умолчанию используется значение CoreWebView2PermissionState. Default.</span><span class="sxs-lookup"><span data-stu-id="8db1c-133">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="8db1c-134">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="8db1c-134">Uri</span></span> 

<span data-ttu-id="8db1c-135">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="8db1c-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="8db1c-136">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="8db1c-136">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="8db1c-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="8db1c-137">GetDeferral</span></span> 

<span data-ttu-id="8db1c-138">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="8db1c-138">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="8db1c-139">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="8db1c-139">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="8db1c-140">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="8db1c-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

