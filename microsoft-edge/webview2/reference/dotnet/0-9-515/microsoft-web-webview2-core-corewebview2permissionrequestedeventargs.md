---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 22fc8ec74c8da0a0ff072cacf91a792b9246900f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879802"
---
# <span data-ttu-id="46dac-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="46dac-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PermissionRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="46dac-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="46dac-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="46dac-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="46dac-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="46dac-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="46dac-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="46dac-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="46dac-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="46dac-109">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="46dac-109">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="46dac-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="46dac-110">Summary</span></span>

 <span data-ttu-id="46dac-111">Участников</span><span class="sxs-lookup"><span data-stu-id="46dac-111">Members</span></span>                        | <span data-ttu-id="46dac-112">Описания</span><span class="sxs-lookup"><span data-stu-id="46dac-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="46dac-113">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="46dac-113">IsUserInitiated</span></span>](#isuserinitiated) | <span data-ttu-id="46dac-114">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="46dac-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="46dac-115">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="46dac-115">PermissionKind</span></span>](#permissionkind) | <span data-ttu-id="46dac-116">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="46dac-116">The type of the permission that is requested.</span></span>
[<span data-ttu-id="46dac-117">Состояние</span><span class="sxs-lookup"><span data-stu-id="46dac-117">State</span></span>](#state) | <span data-ttu-id="46dac-118">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="46dac-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="46dac-119">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="46dac-119">Uri</span></span>](#uri) | <span data-ttu-id="46dac-120">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="46dac-120">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="46dac-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="46dac-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="46dac-122">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="46dac-122">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="46dac-123">Участников</span><span class="sxs-lookup"><span data-stu-id="46dac-123">Members</span></span>

#### <span data-ttu-id="46dac-124">IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="46dac-124">IsUserInitiated</span></span> 

<span data-ttu-id="46dac-125">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="46dac-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="46dac-126">Открытый логический [IsUserInitiated](#isuserinitiated)</span><span class="sxs-lookup"><span data-stu-id="46dac-126">public bool [IsUserInitiated](#isuserinitiated)</span></span>

<span data-ttu-id="46dac-127">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="46dac-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="46dac-128">PermissionKind</span><span class="sxs-lookup"><span data-stu-id="46dac-128">PermissionKind</span></span> 

<span data-ttu-id="46dac-129">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="46dac-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="46dac-130">общедоступная CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span><span class="sxs-lookup"><span data-stu-id="46dac-130">public CoreWebView2PermissionKind [PermissionKind](#permissionkind)</span></span>

#### <span data-ttu-id="46dac-131">Состояние</span><span class="sxs-lookup"><span data-stu-id="46dac-131">State</span></span> 

<span data-ttu-id="46dac-132">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="46dac-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="46dac-133">[состояние](#state) общедоступной CoreWebView2PermissionState</span><span class="sxs-lookup"><span data-stu-id="46dac-133">public CoreWebView2PermissionState [State](#state)</span></span>

<span data-ttu-id="46dac-134">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="46dac-134">whether the request is granted.</span></span>

<span data-ttu-id="46dac-135">По умолчанию используется значение CoreWebView2PermissionState. Default.</span><span class="sxs-lookup"><span data-stu-id="46dac-135">Default value is CoreWebView2PermissionState.Default.</span></span>

#### <span data-ttu-id="46dac-136">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="46dac-136">Uri</span></span> 

<span data-ttu-id="46dac-137">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="46dac-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="46dac-138">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="46dac-138">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="46dac-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="46dac-139">GetDeferral</span></span> 

<span data-ttu-id="46dac-140">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="46dac-140">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="46dac-141">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="46dac-141">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="46dac-142">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="46dac-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

