---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 529f4a444b3ad6d0d5831da6015831b077102354
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654652"
---
# интерфейс ICoreWebView2PermissionRequestedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Аргументы события для события PermissionRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Источник содержимого веб-страницы, запрашивающего разрешение.
[get_PermissionKind](#get_permissionkind) | Тип запрашиваемого разрешения.
[get_IsUserInitiated](#get_isuserinitiated) | Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.
[get_State](#get_state) | Состояние запроса разрешения (например,
[put_State](#put_state) | Задайте свойство State.
[GetDeferral](#getdeferral) | Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.

## Участников

#### get_Uri 

Источник содержимого веб-страницы, запрашивающего разрешение.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### get_PermissionKind 

Тип запрашиваемого разрешения.

> общедоступное значение HRESULT [get_PermissionKind](#get_permissionkind)(CORE_WEBVIEW2_PERMISSION_KIND * значение)

#### get_IsUserInitiated 

Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.

> общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.

#### get_State 

Состояние запроса разрешения (например,

> общедоступное значение HRESULT [get_State](#get_state)(CORE_WEBVIEW2_PERMISSION_STATE * значение)

предоставлен ли запрос. Значение по умолчанию — CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT.

#### put_State 

Задайте свойство State.

> общедоступные значения HRESULT [put_State](#put_state)(CORE_WEBVIEW2_PERMISSION_STATE значение)

#### GetDeferral 

Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.

> общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * РБП)

Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.

