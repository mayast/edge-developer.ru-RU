---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 51218283460975421859c65da8a43553767ad216
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012476"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2HttpResponseHeaders 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Заголовки ответа HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Добавляет строку заголовка с именем и значением.
[Contains](#contains) | Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.
["Голова"](#getheader) | Возвращает значение первого заголовка в коллекции, соответствующее имени.
["Голова"](#getheaders) | Возвращает значения заголовков, соответствующие имени.
[Реверсивный итератор](#getiterator) | Получает итератор на коллекцию всех заголовков ответа.

Используется для создания WebResourceResponse для события WebResourceRequested.

## Участников

#### AppendHeader 

Добавляет строку заголовка с именем и значением.

> Public void [AppendHeader](#appendheader)(строковое имя, строковое значение)

#### Contains 

Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.

> общедоступный bool [имеет](#contains)(строковое имя)

#### "Голова" 

Возвращает значение первого заголовка в коллекции, соответствующее имени.

> [заголовок](#getheader)общедоступной строки (имя строки)

#### "Голова" 

Возвращает значения заголовков, соответствующие имени.

> общедоступные CoreWebView2HttpHeadersCollectionIterator- [заголовки](#getheaders)(строковое имя)

#### Реверсивный итератор 

Получает итератор на коллекцию всех заголовков ответа.

> Public CoreWebView2HttpHeadersCollectionIterator- [iterator](#getiterator)()

