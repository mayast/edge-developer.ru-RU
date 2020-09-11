---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2PermissionRequestedEventArgs
ms.openlocfilehash: 4abb6fb058765a05ebb32fe97474348c4aebde12
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010035"
---
# <span data-ttu-id="0a11f-104">0.9.579-Interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0a11f-104">0.9.579 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="0a11f-105">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="0a11f-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="0a11f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0a11f-106">Summary</span></span>

 <span data-ttu-id="0a11f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="0a11f-107">Members</span></span>                        | <span data-ttu-id="0a11f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="0a11f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0a11f-109">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0a11f-109">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="0a11f-110">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a11f-110">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="0a11f-111">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="0a11f-111">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="0a11f-112">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="0a11f-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="0a11f-113">get_State</span><span class="sxs-lookup"><span data-stu-id="0a11f-113">get_State</span></span>](#get_state) | <span data-ttu-id="0a11f-114">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="0a11f-114">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="0a11f-115">get_Uri</span><span class="sxs-lookup"><span data-stu-id="0a11f-115">get_Uri</span></span>](#get_uri) | <span data-ttu-id="0a11f-116">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="0a11f-116">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="0a11f-117">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0a11f-117">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="0a11f-118">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="0a11f-118">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="0a11f-119">put_State</span><span class="sxs-lookup"><span data-stu-id="0a11f-119">put_State</span></span>](#put_state) | <span data-ttu-id="0a11f-120">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="0a11f-120">Set the State property.</span></span>

## <span data-ttu-id="0a11f-121">Участников</span><span class="sxs-lookup"><span data-stu-id="0a11f-121">Members</span></span>

#### <span data-ttu-id="0a11f-122">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="0a11f-122">get_IsUserInitiated</span></span> 

<span data-ttu-id="0a11f-123">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="0a11f-123">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="0a11f-124">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="0a11f-124">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="0a11f-125">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="0a11f-125">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="0a11f-126">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="0a11f-126">get_PermissionKind</span></span> 

<span data-ttu-id="0a11f-127">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="0a11f-127">The type of the permission that is requested.</span></span>

> <span data-ttu-id="0a11f-128">общедоступное значение HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* значение)</span><span class="sxs-lookup"><span data-stu-id="0a11f-128">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="0a11f-129">get_State</span><span class="sxs-lookup"><span data-stu-id="0a11f-129">get_State</span></span> 

<span data-ttu-id="0a11f-130">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="0a11f-130">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="0a11f-131">общедоступное значение HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* значение)</span><span class="sxs-lookup"><span data-stu-id="0a11f-131">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="0a11f-132">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="0a11f-132">whether the request is granted.</span></span> <span data-ttu-id="0a11f-133">Значение по умолчанию — COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="0a11f-133">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="0a11f-134">get_Uri</span><span class="sxs-lookup"><span data-stu-id="0a11f-134">get_Uri</span></span> 

<span data-ttu-id="0a11f-135">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="0a11f-135">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="0a11f-136">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="0a11f-136">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="0a11f-137">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="0a11f-137">GetDeferral</span></span> 

<span data-ttu-id="0a11f-138">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="0a11f-138">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="0a11f-139">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="0a11f-139">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="0a11f-140">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="0a11f-140">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="0a11f-141">put_State</span><span class="sxs-lookup"><span data-stu-id="0a11f-141">put_State</span></span> 

<span data-ttu-id="0a11f-142">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="0a11f-142">Set the State property.</span></span>

> <span data-ttu-id="0a11f-143">общедоступные значения HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE значение)</span><span class="sxs-lookup"><span data-stu-id="0a11f-143">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>

