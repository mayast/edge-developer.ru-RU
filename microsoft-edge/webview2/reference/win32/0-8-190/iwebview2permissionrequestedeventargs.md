---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: e2a9486011d5ef3ef480271ed32a7c8b586cf9bd
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885830"
---
# <span data-ttu-id="e9839-104">0.8.355-Interface IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e9839-104">0.8.355 - interface IWebView2PermissionRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="e9839-105">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="e9839-105">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="e9839-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e9839-106">Summary</span></span>

 <span data-ttu-id="e9839-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e9839-107">Members</span></span>                        | <span data-ttu-id="e9839-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e9839-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e9839-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e9839-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="e9839-110">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="e9839-110">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="e9839-111">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="e9839-111">get_PermissionType</span></span>](#get_permissiontype) | <span data-ttu-id="e9839-112">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="e9839-112">The type of the permission that is requested.</span></span>
[<span data-ttu-id="e9839-113">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e9839-113">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="e9839-114">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="e9839-114">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="e9839-115">get_State</span><span class="sxs-lookup"><span data-stu-id="e9839-115">get_State</span></span>](#get_state) | <span data-ttu-id="e9839-116">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="e9839-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="e9839-117">put_State</span><span class="sxs-lookup"><span data-stu-id="e9839-117">put_State</span></span>](#put_state) | <span data-ttu-id="e9839-118">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="e9839-118">Set the State property.</span></span>
[<span data-ttu-id="e9839-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e9839-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="e9839-120">Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="e9839-120">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="e9839-121">Участников</span><span class="sxs-lookup"><span data-stu-id="e9839-121">Members</span></span>

#### <span data-ttu-id="e9839-122">get_Uri</span><span class="sxs-lookup"><span data-stu-id="e9839-122">get_Uri</span></span> 

<span data-ttu-id="e9839-123">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="e9839-123">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="e9839-124">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="e9839-124">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="e9839-125">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="e9839-125">get_PermissionType</span></span> 

<span data-ttu-id="e9839-126">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="e9839-126">The type of the permission that is requested.</span></span>

> <span data-ttu-id="e9839-127">общедоступное значение HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* значение)</span><span class="sxs-lookup"><span data-stu-id="e9839-127">public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span></span>

#### <span data-ttu-id="e9839-128">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="e9839-128">get_IsUserInitiated</span></span> 

<span data-ttu-id="e9839-129">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="e9839-129">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="e9839-130">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="e9839-130">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="e9839-131">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="e9839-131">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="e9839-132">get_State</span><span class="sxs-lookup"><span data-stu-id="e9839-132">get_State</span></span> 

<span data-ttu-id="e9839-133">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="e9839-133">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="e9839-134">общедоступное значение HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* значение)</span><span class="sxs-lookup"><span data-stu-id="e9839-134">public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="e9839-135">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="e9839-135">whether the request is granted.</span></span> <span data-ttu-id="e9839-136">Значение по умолчанию — WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="e9839-136">Default value is WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="e9839-137">put_State</span><span class="sxs-lookup"><span data-stu-id="e9839-137">put_State</span></span> 

<span data-ttu-id="e9839-138">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="e9839-138">Set the State property.</span></span>

> <span data-ttu-id="e9839-139">общедоступные значения HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE значение)</span><span class="sxs-lookup"><span data-stu-id="e9839-139">public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="e9839-140">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="e9839-140">GetDeferral</span></span> 

<span data-ttu-id="e9839-141">Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="e9839-141">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="e9839-142">общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="e9839-142">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="e9839-143">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="e9839-143">Developer can use the deferral object to make the permission decision at a later time.</span></span>

