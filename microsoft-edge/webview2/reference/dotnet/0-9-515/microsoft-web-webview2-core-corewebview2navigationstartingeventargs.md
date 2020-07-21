---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2f129f36502ccc404da74904c73c4bdab1d9f472
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886376"
---
# класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Аргументы события для события NavigationStarting.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Отмена](#cancel) | Ведущее приложение может установить этот флаг, чтобы отменить навигацию.
[Redirect (перенаправление)](#isredirected) | Значение true, если перенаправлять навигацию.
[IsUserInitiated](#isuserinitiated) | Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.
[NavigationId](#navigationid) | Идентификатор навигации.
[RequestHeaders](#requestheaders) | Заголовки HTTP-запроса для навигации.
[Универсальный код ресурса (URI)](#uri) | URI запрошенной навигации.

## Участников

#### Отмена 

Ведущее приложение может установить этот флаг, чтобы отменить навигацию.

> [Отмена](#cancel) открытого bool

Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным. По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы. Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.

#### Redirect (перенаправление) 

Значение true, если перенаправлять навигацию.

> общедоступный bool [перенаправленный](#isredirected)

#### IsUserInitiated 

Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.

> Открытый логический [IsUserInitiated](#isuserinitiated)

#### NavigationId 

Идентификатор навигации.

> общедоступный ulong [NavigationId](#navigationid)

#### RequestHeaders 

Заголовки HTTP-запроса для навигации.

> общедоступная HttpRequestHeaders [RequestHeaders](#requestheaders)

Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.

#### Универсальный код ресурса (URI) 

URI запрошенной навигации.

> [URI](#uri) общедоступной строки

