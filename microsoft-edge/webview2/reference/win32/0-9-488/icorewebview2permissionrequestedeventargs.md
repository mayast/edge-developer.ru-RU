---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 85cba958c5c918bb99f14cb7202c7645b0ae6c52
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885207"
---
# <span data-ttu-id="65218-104">0.9.515-Interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="65218-104">0.9.515 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="65218-105">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="65218-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="65218-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="65218-106">Summary</span></span>

 <span data-ttu-id="65218-107">Участников</span><span class="sxs-lookup"><span data-stu-id="65218-107">Members</span></span>                        | <span data-ttu-id="65218-108">Описания</span><span class="sxs-lookup"><span data-stu-id="65218-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="65218-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="65218-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="65218-110">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="65218-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="65218-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="65218-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="65218-112">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="65218-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="65218-113">get_State</span><span class="sxs-lookup"><span data-stu-id="65218-113">get_State</span></span>](#get_state) | <span data-ttu-id="65218-114">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="65218-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="65218-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="65218-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="65218-116">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="65218-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="65218-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="65218-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="65218-118">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="65218-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="65218-119">put_State</span><span class="sxs-lookup"><span data-stu-id="65218-119">put_State</span></span>](#put_state) | <span data-ttu-id="65218-120">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="65218-120">Set the State property.</span></span>

## <span data-ttu-id="65218-121">Участников</span><span class="sxs-lookup"><span data-stu-id="65218-121">Members</span></span>

#### <span data-ttu-id="65218-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="65218-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="65218-123">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="65218-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="65218-124">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="65218-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="65218-125">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="65218-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="65218-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="65218-126">get_PermissionKind</span></span> 

<span data-ttu-id="65218-127">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="65218-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="65218-128">общедоступное значение HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* значение)</span><span class="sxs-lookup"><span data-stu-id="65218-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="65218-129">get_State</span><span class="sxs-lookup"><span data-stu-id="65218-129">get_State</span></span> 

<span data-ttu-id="65218-130">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="65218-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="65218-131">общедоступное значение HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* значение)</span><span class="sxs-lookup"><span data-stu-id="65218-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="65218-132">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="65218-132">whether the request is granted.</span></span> <span data-ttu-id="65218-133">Значение по умолчанию — COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="65218-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="65218-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="65218-134">get_Uri</span></span> 

<span data-ttu-id="65218-135">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="65218-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="65218-136">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="65218-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="65218-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="65218-137">GetDeferral</span></span> 

<span data-ttu-id="65218-138">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="65218-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="65218-139">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="65218-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="65218-140">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="65218-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="65218-141">put_State</span><span class="sxs-lookup"><span data-stu-id="65218-141">put_State</span></span> 

<span data-ttu-id="65218-142">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="65218-142">Set the State property.</span></span>

> <span data-ttu-id="65218-143">общедоступные значения HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE значение)</span><span class="sxs-lookup"><span data-stu-id="65218-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>

