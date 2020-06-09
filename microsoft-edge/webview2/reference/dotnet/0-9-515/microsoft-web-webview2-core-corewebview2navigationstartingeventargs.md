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
ms.openlocfilehash: 98e242ace5eb0ae5958ddb1eb6cd380d194294be
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697632"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

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

