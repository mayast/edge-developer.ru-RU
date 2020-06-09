---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 3d88d4ee0a89b4690b47f67ee90756ebecdd1c78
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698192"
---
# <span data-ttu-id="17cde-104">интерфейс ICoreWebView2PermissionRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="17cde-104">interface ICoreWebView2PermissionRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="17cde-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="17cde-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="17cde-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="17cde-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="17cde-107">Аргументы события для события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="17cde-107">Event args for the PermissionRequested event.</span></span>

## <span data-ttu-id="17cde-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="17cde-108">Summary</span></span>

 <span data-ttu-id="17cde-109">Участников</span><span class="sxs-lookup"><span data-stu-id="17cde-109">Members</span></span>                        | <span data-ttu-id="17cde-110">Описания</span><span class="sxs-lookup"><span data-stu-id="17cde-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="17cde-111">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="17cde-111">get_IsUserInitiated</span></span>](#get_isuserinitiated) | <span data-ttu-id="17cde-112">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="17cde-112">True when the permission request was initiated through a user gesture.</span></span>
[<span data-ttu-id="17cde-113">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="17cde-113">get_PermissionKind</span></span>](#get_permissionkind) | <span data-ttu-id="17cde-114">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="17cde-114">The type of the permission that is requested.</span></span>
[<span data-ttu-id="17cde-115">get_State</span><span class="sxs-lookup"><span data-stu-id="17cde-115">get_State</span></span>](#get_state) | <span data-ttu-id="17cde-116">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="17cde-116">The status of a permission request, i.e.</span></span>
[<span data-ttu-id="17cde-117">get_Uri</span><span class="sxs-lookup"><span data-stu-id="17cde-117">get_Uri</span></span>](#get_uri) | <span data-ttu-id="17cde-118">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="17cde-118">The origin of the web content that requests the permission.</span></span>
[<span data-ttu-id="17cde-119">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="17cde-119">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="17cde-120">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="17cde-120">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="17cde-121">put_State</span><span class="sxs-lookup"><span data-stu-id="17cde-121">put_State</span></span>](#put_state) | <span data-ttu-id="17cde-122">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="17cde-122">Set the State property.</span></span>

## <span data-ttu-id="17cde-123">Участников</span><span class="sxs-lookup"><span data-stu-id="17cde-123">Members</span></span>

#### <span data-ttu-id="17cde-124">get_IsUserInitiated</span><span class="sxs-lookup"><span data-stu-id="17cde-124">get_IsUserInitiated</span></span> 

<span data-ttu-id="17cde-125">Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.</span><span class="sxs-lookup"><span data-stu-id="17cde-125">True when the permission request was initiated through a user gesture.</span></span>

> <span data-ttu-id="17cde-126">общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool \* IsUserInitiated)</span><span class="sxs-lookup"><span data-stu-id="17cde-126">public HRESULT [get_IsUserInitiated](#get_isuserinitiated)(BOOL \* isUserInitiated)</span></span>

<span data-ttu-id="17cde-127">Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.</span><span class="sxs-lookup"><span data-stu-id="17cde-127">Note that being initiated through a user gesture doesn't mean that user intended to access the associated resource.</span></span>

#### <span data-ttu-id="17cde-128">get_PermissionKind</span><span class="sxs-lookup"><span data-stu-id="17cde-128">get_PermissionKind</span></span> 

<span data-ttu-id="17cde-129">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="17cde-129">The type of the permission that is requested.</span></span>

> <span data-ttu-id="17cde-130">общедоступное значение HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* значение)</span><span class="sxs-lookup"><span data-stu-id="17cde-130">public HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND \* value)</span></span>

#### <span data-ttu-id="17cde-131">get_State</span><span class="sxs-lookup"><span data-stu-id="17cde-131">get_State</span></span> 

<span data-ttu-id="17cde-132">Состояние запроса разрешения (например,</span><span class="sxs-lookup"><span data-stu-id="17cde-132">The status of a permission request, i.e.</span></span>

> <span data-ttu-id="17cde-133">общедоступное значение HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* значение)</span><span class="sxs-lookup"><span data-stu-id="17cde-133">public HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE \* value)</span></span>

<span data-ttu-id="17cde-134">предоставлен ли запрос.</span><span class="sxs-lookup"><span data-stu-id="17cde-134">whether the request is granted.</span></span> <span data-ttu-id="17cde-135">Значение по умолчанию — COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="17cde-135">Default value is COREWEBVIEW2_PERMISSION_STATE_DEFAULT.</span></span>

#### <span data-ttu-id="17cde-136">get_Uri</span><span class="sxs-lookup"><span data-stu-id="17cde-136">get_Uri</span></span> 

<span data-ttu-id="17cde-137">Источник содержимого веб-страницы, запрашивающего разрешение.</span><span class="sxs-lookup"><span data-stu-id="17cde-137">The origin of the web content that requests the permission.</span></span>

> <span data-ttu-id="17cde-138">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="17cde-138">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="17cde-139">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="17cde-139">GetDeferral</span></span> 

<span data-ttu-id="17cde-140">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="17cde-140">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="17cde-141">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="17cde-141">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="17cde-142">Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.</span><span class="sxs-lookup"><span data-stu-id="17cde-142">Developer can use the deferral object to make the permission decision at a later time.</span></span>

#### <span data-ttu-id="17cde-143">put_State</span><span class="sxs-lookup"><span data-stu-id="17cde-143">put_State</span></span> 

<span data-ttu-id="17cde-144">Задайте свойство State.</span><span class="sxs-lookup"><span data-stu-id="17cde-144">Set the State property.</span></span>

> <span data-ttu-id="17cde-145">общедоступные значения HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE значение)</span><span class="sxs-lookup"><span data-stu-id="17cde-145">public HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE value)</span></span>

