---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 75f88a08f5a94df85a471658704fcd77a5926417
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877793"
---
# <span data-ttu-id="38263-104">0.9.430-Interface ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="38263-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="38263-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="38263-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="38263-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="38263-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="38263-107">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="38263-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="38263-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="38263-108">Summary</span></span>

 <span data-ttu-id="38263-109">Участников</span><span class="sxs-lookup"><span data-stu-id="38263-109">Members</span></span>                        | <span data-ttu-id="38263-110">Описания</span><span class="sxs-lookup"><span data-stu-id="38263-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="38263-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="38263-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="38263-112">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="38263-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="38263-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="38263-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="38263-114">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="38263-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="38263-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="38263-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="38263-116">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="38263-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="38263-117">get_State</span><span class="sxs-lookup"><span data-stu-id="38263-117">get_State</span></span>](#get_state) | <span data-ttu-id="38263-118">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="38263-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="38263-119">put_State</span><span class="sxs-lookup"><span data-stu-id="38263-119">put_State</span></span>](#put_state) | <span data-ttu-id="38263-120">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="38263-120">Set the State property.</span></span>
[<span data-ttu-id="38263-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="38263-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="38263-122">Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="38263-122">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="38263-123">Участников</span><span class="sxs-lookup"><span data-stu-id="38263-123">Members</span></span>

#### <span data-ttu-id="38263-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="38263-124">get_Uri</span></span> 

<span data-ttu-id="38263-125">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="38263-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="38263-126">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="38263-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="38263-127">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="38263-127">get_PermissionKind</span></span> 

<span data-ttu-id="38263-128">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="38263-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="38263-129">общедоступное значение HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* значение)</span><span class="sxs-lookup"><span data-stu-id="38263-129">public HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="38263-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="38263-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="38263-131">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="38263-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="38263-132">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="38263-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="38263-133">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="38263-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="38263-134">get_State</span><span class="sxs-lookup"><span data-stu-id="38263-134">get_State</span></span> 

<span data-ttu-id="38263-135">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="38263-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="38263-136">общедоступное значение HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* значение)</span><span class="sxs-lookup"><span data-stu-id="38263-136">public HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="38263-137">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="38263-137">whether the request is granted.</span></span> <span data-ttu-id="38263-138">Значение по умолчанию — CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="38263-138">Default value is CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="38263-139">put_State</span><span class="sxs-lookup"><span data-stu-id="38263-139">put_State</span></span> 

<span data-ttu-id="38263-140">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="38263-140">Set the State property.</span></span>

> <span data-ttu-id="38263-141">общедоступные значения HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE значение)</span><span class="sxs-lookup"><span data-stu-id="38263-141">public HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="38263-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="38263-142">GetDeferral</span></span> 

<span data-ttu-id="38263-143">Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="38263-143">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="38263-144">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="38263-144">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="38263-145">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="38263-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>

