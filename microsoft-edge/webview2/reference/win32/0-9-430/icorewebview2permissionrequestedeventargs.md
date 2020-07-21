---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e29765a4b8a3e620b8c627c7b05b9f0b4ff63f95
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886418"
---
# <span data-ttu-id="2c532-104">0.9.430-Interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="2c532-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="2c532-105">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="2c532-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="2c532-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2c532-106">Summary</span></span>

 <span data-ttu-id="2c532-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2c532-107">Members</span></span>                        | <span data-ttu-id="2c532-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2c532-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2c532-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2c532-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="2c532-110">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="2c532-110">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="2c532-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="2c532-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="2c532-112">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="2c532-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="2c532-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2c532-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="2c532-114">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c532-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="2c532-115">get_State</span><span class="sxs-lookup"><span data-stu-id="2c532-115">get_State</span></span>](#get_state) | <span data-ttu-id="2c532-116">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="2c532-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="2c532-117">put_State</span><span class="sxs-lookup"><span data-stu-id="2c532-117">put_State</span></span>](#put_state) | <span data-ttu-id="2c532-118">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="2c532-118">Set the State property.</span></span>
[<span data-ttu-id="2c532-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2c532-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="2c532-120">Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="2c532-120">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="2c532-121">Участников</span><span class="sxs-lookup"><span data-stu-id="2c532-121">Members</span></span>

#### <span data-ttu-id="2c532-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="2c532-122">get_Uri</span></span> 

<span data-ttu-id="2c532-123">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="2c532-123">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="2c532-124">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="2c532-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="2c532-125">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="2c532-125">get_PermissionKind</span></span> 

<span data-ttu-id="2c532-126">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="2c532-126">The type of the permission that is requested.</span></span>

> <span data-ttu-id="2c532-127">общедоступное значение HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* значение)</span><span class="sxs-lookup"><span data-stu-id="2c532-127">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="2c532-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="2c532-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="2c532-129">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="2c532-129">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="2c532-130">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="2c532-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="2c532-131">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="2c532-131">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="2c532-132">get_State</span><span class="sxs-lookup"><span data-stu-id="2c532-132">get_State</span></span> 

<span data-ttu-id="2c532-133">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="2c532-133">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="2c532-134">общедоступное значение HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* значение)</span><span class="sxs-lookup"><span data-stu-id="2c532-134">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="2c532-135">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="2c532-135">whether the request is granted.</span></span> <span data-ttu-id="2c532-136">Значение по умолчанию — CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="2c532-136">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="2c532-137">put_State</span><span class="sxs-lookup"><span data-stu-id="2c532-137">put_State</span></span> 

<span data-ttu-id="2c532-138">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="2c532-138">Set the State property.</span></span>

> <span data-ttu-id="2c532-139">общедоступные значения HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE значение)</span><span class="sxs-lookup"><span data-stu-id="2c532-139">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="2c532-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="2c532-140">GetDeferral</span></span> 

<span data-ttu-id="2c532-141">Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="2c532-141">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="2c532-142">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="2c532-142">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="2c532-143">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="2c532-143">Developer can use the deferral object to make the permission decision at a later time.</span></span>

