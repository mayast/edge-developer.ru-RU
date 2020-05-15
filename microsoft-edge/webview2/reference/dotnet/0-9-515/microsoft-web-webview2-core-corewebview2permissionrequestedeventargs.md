---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 5aeeebfc3d8434c096e6946e5161437809f207d3
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654641"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

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

