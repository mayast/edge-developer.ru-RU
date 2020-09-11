---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 87993559d4d70daef84cbd86a2305f09cc017aa9
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012447"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2PermissionRequestedEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Аргументы события для события PermissionRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[IsUserInitiated](#isuserinitiated) | Значение true, если новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.
[PermissionKind](#permissionkind) | Тип запрашиваемого разрешения.
[Состояние](#state) | Состояние запроса разрешения (например,
[Универсальный код ресурса (URI)](#uri) | Источник содержимого веб-страницы, запрашивающего разрешение.
[GetDeferral](#getdeferral) | Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.

## Участников

#### IsUserInitiated 

Значение true, если новый запрос окна был инициирован с помощью жеста пользователя, например щелчка тега привязки с целевым объектом.

> Открытый логический [IsUserInitiated](#isuserinitiated)

Заблокированный блочный блок "Edge" отключен для WebView, поэтому приложение может использовать этот флаг, чтобы заблокировать всплывающие окна, не инициированные пользователем.

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

