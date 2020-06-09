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
ms.openlocfilehash: bfc802d160f7516f5f65e5526fecfd9742504045
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699281"
---
# <span data-ttu-id="2aaeb-104">интерфейс ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2aaeb-104">interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="2aaeb-105">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="2aaeb-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2aaeb-106">Summary</span></span>

 <span data-ttu-id="2aaeb-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2aaeb-107">Members</span></span>                        | <span data-ttu-id="2aaeb-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2aaeb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2aaeb-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2aaeb-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="2aaeb-110">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="2aaeb-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="2aaeb-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="2aaeb-112">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="2aaeb-113">get_State</span><span class="sxs-lookup"><span data-stu-id="2aaeb-113">get_State</span></span>](#get_state) | <span data-ttu-id="2aaeb-114">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="2aaeb-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="2aaeb-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2aaeb-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2aaeb-116">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="2aaeb-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2aaeb-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2aaeb-118">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="2aaeb-119">put_State</span><span class="sxs-lookup"><span data-stu-id="2aaeb-119">put_State</span></span>](#put_state) | <span data-ttu-id="2aaeb-120">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-120">Set the State property.</span></span>

## <span data-ttu-id="2aaeb-121">Участников</span><span class="sxs-lookup"><span data-stu-id="2aaeb-121">Members</span></span>

#### <span data-ttu-id="2aaeb-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2aaeb-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="2aaeb-123">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="2aaeb-124">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="2aaeb-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="2aaeb-125">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="2aaeb-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="2aaeb-126">get_PermissionKind</span></span> 

<span data-ttu-id="2aaeb-127">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="2aaeb-128">общедоступное значение HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* значение)</span><span class="sxs-lookup"><span data-stu-id="2aaeb-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="2aaeb-129">get_State</span><span class="sxs-lookup"><span data-stu-id="2aaeb-129">get_State</span></span> 

<span data-ttu-id="2aaeb-130">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="2aaeb-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="2aaeb-131">общедоступное значение HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* значение)</span><span class="sxs-lookup"><span data-stu-id="2aaeb-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="2aaeb-132">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-132">whether the request is granted.</span></span> <span data-ttu-id="2aaeb-133">Значение по умолчанию — COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="2aaeb-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2aaeb-134">get_Uri</span></span> 

<span data-ttu-id="2aaeb-135">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="2aaeb-136">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2aaeb-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2aaeb-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2aaeb-137">GetDeferral</span></span> 

<span data-ttu-id="2aaeb-138">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="2aaeb-139">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="2aaeb-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2aaeb-140">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="2aaeb-141">put_State</span><span class="sxs-lookup"><span data-stu-id="2aaeb-141">put_State</span></span> 

<span data-ttu-id="2aaeb-142">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="2aaeb-142">Set the State property.</span></span>

> <span data-ttu-id="2aaeb-143">общедоступные значения HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE значение)</span><span class="sxs-lookup"><span data-stu-id="2aaeb-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>

