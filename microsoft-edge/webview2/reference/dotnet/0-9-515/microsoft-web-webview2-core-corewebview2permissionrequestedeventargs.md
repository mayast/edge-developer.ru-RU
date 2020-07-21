---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2bfa4559824c9bb397648249ead8fa8cb60c281c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884633"
---
# класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Аргументы события для события PermissionRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[IsUserInitiated](#isuserinitiated) | Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.
[PermissionKind](#permissionkind) | Тип запрашиваемого разрешения.
[Состояние](#state) | Состояние запроса разрешения (например,
[Универсальный код ресурса (URI)](#uri) | Источник содержимого веб-страницы, запрашивающего разрешение.
[GetDeferral](#getdeferral) | Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.

## Участников

#### IsUserInitiated 

Значение true, если запрос на разрешение был инициирован с помощью жеста пользователя.

> Открытый логический [IsUserInitiated](#isuserinitiated)

Обратите внимание, что инициирование с помощью жеста пользователя не означает, что пользователь должен получить доступ к связанному ресурсу.

#### PermissionKind 

Тип запрашиваемого разрешения.

> общедоступная CoreWebView2PermissionKind [PermissionKind](#permissionkind)

#### Состояние 

Состояние запроса разрешения (например,

> [состояние](#state) общедоступной CoreWebView2PermissionState

предоставлен ли запрос.

По умолчанию используется значение CoreWebView2PermissionState. Default.

#### Универсальный код ресурса (URI) 

Источник содержимого веб-страницы, запрашивающего разрешение.

> [URI](#uri) общедоступной строки

#### GetDeferral 

Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.

> общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()

Разработчик может использовать объект РБП, чтобы принять решение о разрешении позже.

