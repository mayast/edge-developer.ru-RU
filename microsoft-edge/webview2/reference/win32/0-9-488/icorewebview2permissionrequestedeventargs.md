---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 88f5008dbc9a4ebfccfe96299899a2474ecc6d95
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880411"
---
# <span data-ttu-id="49eee-104">0.9.515-Interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="49eee-104">0.9.515 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="49eee-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="49eee-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="49eee-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="49eee-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="49eee-107">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="49eee-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="49eee-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="49eee-108">Summary</span></span>

 <span data-ttu-id="49eee-109">Участников</span><span class="sxs-lookup"><span data-stu-id="49eee-109">Members</span></span>                        | <span data-ttu-id="49eee-110">Описания</span><span class="sxs-lookup"><span data-stu-id="49eee-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="49eee-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="49eee-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="49eee-112">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="49eee-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="49eee-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="49eee-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="49eee-114">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="49eee-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="49eee-115">get_State</span><span class="sxs-lookup"><span data-stu-id="49eee-115">get_State</span></span>](#get_state) | <span data-ttu-id="49eee-116">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="49eee-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="49eee-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="49eee-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="49eee-118">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="49eee-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="49eee-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="49eee-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="49eee-120">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="49eee-120">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="49eee-121">put_State</span><span class="sxs-lookup"><span data-stu-id="49eee-121">put_State</span></span>](#put_state) | <span data-ttu-id="49eee-122">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="49eee-122">Set the State property.</span></span>

## <span data-ttu-id="49eee-123">Участников</span><span class="sxs-lookup"><span data-stu-id="49eee-123">Members</span></span>

#### <span data-ttu-id="49eee-124">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="49eee-124">get_IsUserInitiated</span></span> 

<span data-ttu-id="49eee-125">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="49eee-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="49eee-126">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="49eee-126">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="49eee-127">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="49eee-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="49eee-128">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="49eee-128">get_PermissionKind</span></span> 

<span data-ttu-id="49eee-129">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="49eee-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="49eee-130">общедоступное значение HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* значение)</span><span class="sxs-lookup"><span data-stu-id="49eee-130">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="49eee-131">get_State</span><span class="sxs-lookup"><span data-stu-id="49eee-131">get_State</span></span> 

<span data-ttu-id="49eee-132">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="49eee-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="49eee-133">общедоступное значение HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* значение)</span><span class="sxs-lookup"><span data-stu-id="49eee-133">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="49eee-134">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="49eee-134">whether the request is granted.</span></span> <span data-ttu-id="49eee-135">Значение по умолчанию — COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="49eee-135">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="49eee-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="49eee-136">get_Uri</span></span> 

<span data-ttu-id="49eee-137">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="49eee-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="49eee-138">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="49eee-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="49eee-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="49eee-139">GetDeferral</span></span> 

<span data-ttu-id="49eee-140">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="49eee-140">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="49eee-141">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="49eee-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="49eee-142">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="49eee-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="49eee-143">put_State</span><span class="sxs-lookup"><span data-stu-id="49eee-143">put_State</span></span> 

<span data-ttu-id="49eee-144">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="49eee-144">Set the State property.</span></span>

> <span data-ttu-id="49eee-145">общедоступные значения HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE значение)</span><span class="sxs-lookup"><span data-stu-id="49eee-145">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>

