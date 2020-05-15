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
# интерфейс IWebView2PermissionRequestedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2PermissionRequestedEventArgs
  : public IUnknown
```

Аргументы события для события PermissionRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | Источник содержимого веб-страницы, запрашивающего разрешение.
[get_PermissionType](#get_permissiontype) | Тип запрашиваемого разрешения.
[get_IsUserInitiated](#get_isuserinitiated) | Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.
[get_State](#get_state) | Состояние запроса разрешения (например,
[put_State](#put_state) | Задайте свойство State.
[GetDeferral](#getdeferral) | Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.

## Участников

#### get_Uri 

Источник содержимого веб-страницы, запрашивающего разрешение.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### get_PermissionType 

Тип запрашиваемого разрешения.

> общедоступное значение HRESULT [get_PermissionType](#get_permissiontype)(WEBVIEW2_PERMISSION_TYPE * значение)

#### get_IsUserInitiated 

Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.

> общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.

#### get_State 

Состояние запроса разрешения (например,

> общедоступное значение HRESULT [get_State](#get_state)(WEBVIEW2_PERMISSION_STATE * значение)

предоставлен ли запрос. Значение по умолчанию — WEBVIEW2_PERMISSION_STATE_DEFAULT.

#### put_State 

Задайте свойство State.

> общедоступные значения HRESULT [put_State](#put_state)(WEBVIEW2_PERMISSION_STATE значение)

#### GetDeferral 

Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.

> общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * РБП)

Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.

