---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 1b80b42bc26316d1fcc8ac74656f24cb0db75bae
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012450"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationStartingEventArgs 

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

> общедоступная CoreWebView2HttpRequestHeaders [RequestHeaders](#requestheaders)

Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.

#### Универсальный код ресурса (URI) 

URI запрошенной навигации.

> [URI](#uri) общедоступной строки

