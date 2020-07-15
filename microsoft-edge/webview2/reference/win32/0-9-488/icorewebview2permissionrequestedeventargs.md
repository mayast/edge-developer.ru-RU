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
# 0.9.515-Interface ICoreWebView2PermissionRequestedEventArgs 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Аргументы события для события PermissionRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_IsUserInitiated](#get_isuserinitiated) | Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.
[get_PermissionKind](#get_permissionkind) | Тип запрашиваемого разрешения.
[get_State](#get_state) | Состояние запроса разрешения (например,
[get_Uri](#get_uri) | Источник содержимого веб-страницы, запрашивающего разрешение.
[GetDeferral](#getdeferral) | Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.
[put_State](#put_state) | Задайте свойство State.

## Участников

#### get_IsUserInitiated 

Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.

> общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.

#### get_PermissionKind 

Тип запрашиваемого разрешения.

> общедоступное значение HRESULT [get_PermissionKind](#get_permissionkind)(COREWEBVIEW2_PERMISSION_KIND * значение)

#### get_State 

Состояние запроса разрешения (например,

> общедоступное значение HRESULT [get_State](#get_state)(COREWEBVIEW2_PERMISSION_STATE * значение)

предоставлен ли запрос. Значение по умолчанию — COREWEBVIEW2_PERMISSION_STATE_DEFAULT.

#### get_Uri 

Источник содержимого веб-страницы, запрашивающего разрешение.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### GetDeferral 

Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.

> общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * РБП)

Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.

#### put_State 

Задайте свойство State.

> общедоступные значения HRESULT [put_State](#put_state)(COREWEBVIEW2_PERMISSION_STATE значение)

