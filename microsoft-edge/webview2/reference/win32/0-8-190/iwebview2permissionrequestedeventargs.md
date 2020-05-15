---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 9d16f1c72a3921b220bd0046e78ed0c6b32a718a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654841"
---
# <span data-ttu-id="6c772-104">интерфейс IWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6c772-104">interface IWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="6c772-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="6c772-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="6c772-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="6c772-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="6c772-107">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="6c772-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="6c772-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6c772-108">Summary</span></span>

 <span data-ttu-id="6c772-109">Участников</span><span class="sxs-lookup"><span data-stu-id="6c772-109">Members</span></span>                        | <span data-ttu-id="6c772-110">Описания</span><span class="sxs-lookup"><span data-stu-id="6c772-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6c772-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6c772-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="6c772-112">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="6c772-112">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="6c772-113">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="6c772-113">get_PermissionType</span></span>](#get_permissiontype) | <span data-ttu-id="6c772-114">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="6c772-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="6c772-115">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6c772-115">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="6c772-116">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c772-116">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="6c772-117">get_State</span><span class="sxs-lookup"><span data-stu-id="6c772-117">get_State</span></span>](#get_state) | <span data-ttu-id="6c772-118">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="6c772-118">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="6c772-119">put_State</span><span class="sxs-lookup"><span data-stu-id="6c772-119">put_State</span></span>](#put_state) | <span data-ttu-id="6c772-120">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="6c772-120">Set the State property.</span></span>
[<span data-ttu-id="6c772-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6c772-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="6c772-122">Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="6c772-122">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="6c772-123">Участников</span><span class="sxs-lookup"><span data-stu-id="6c772-123">Members</span></span>

#### <span data-ttu-id="6c772-124">get_Uri</span><span class="sxs-lookup"><span data-stu-id="6c772-124">get_Uri</span></span> 

<span data-ttu-id="6c772-125">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="6c772-125">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="6c772-126">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="6c772-126">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="6c772-127">get_PermissionType</span><span class="sxs-lookup"><span data-stu-id="6c772-127">get_PermissionType</span></span> 

<span data-ttu-id="6c772-128">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="6c772-128">The type of the permission that is requested.</span></span>

> <span data-ttu-id="6c772-129">общедоступное значение HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* значение)</span><span class="sxs-lookup"><span data-stu-id="6c772-129">public HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE \* value)</span></span>

#### <span data-ttu-id="6c772-130">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="6c772-130">get_IsUserInitiated</span></span> 

<span data-ttu-id="6c772-131">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c772-131">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="6c772-132">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="6c772-132">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="6c772-133">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="6c772-133">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="6c772-134">get_State</span><span class="sxs-lookup"><span data-stu-id="6c772-134">get_State</span></span> 

<span data-ttu-id="6c772-135">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="6c772-135">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="6c772-136">общедоступное значение HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* значение)</span><span class="sxs-lookup"><span data-stu-id="6c772-136">public HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="6c772-137">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="6c772-137">whether the request is granted.</span></span> <span data-ttu-id="6c772-138">Значение по умолчанию — WEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="6c772-138">Default value is WEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="6c772-139">put_State</span><span class="sxs-lookup"><span data-stu-id="6c772-139">put_State</span></span> 

<span data-ttu-id="6c772-140">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="6c772-140">Set the State property.</span></span>

> <span data-ttu-id="6c772-141">общедоступные значения HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE значение)</span><span class="sxs-lookup"><span data-stu-id="6c772-141">public HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE value)</span></span>

#### <span data-ttu-id="6c772-142">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="6c772-142">GetDeferral</span></span> 

<span data-ttu-id="6c772-143">Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="6c772-143">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="6c772-144">общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="6c772-144">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="6c772-145">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="6c772-145">Developer can use the deferral object to make the permission decision at a later time.</span></span>

