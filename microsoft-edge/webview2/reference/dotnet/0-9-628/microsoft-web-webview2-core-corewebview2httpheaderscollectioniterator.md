---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: e7aad408372acbbd19ecab9d04312f21e2396e88
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012479"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2HttpHeadersCollectionIterator 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Итератор для коллекции заголовков HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[HasCurrentHeader](#hascurrentheader) | Имеет значение true, если итератор не исходил из заголовков.
[MoveNext](#movenext) | Переместите итератор на следующий заголовок HTTP в коллекции.

Смотрите CoreWebView2HttpRequestHeaders и CoreWebView2HttpResponseHeaders.

## Участников

#### HasCurrentHeader 

Имеет значение true, если итератор не исходил из заголовков.

> Открытый логический [HasCurrentHeader](#hascurrentheader)

Если коллекция, в которой находится итератор, является пустой или, если итератор пропало за ее пределами, это ложный.

#### MoveNext 

Переместите итератор на следующий заголовок HTTP в коллекции.

> общедоступный bool [MoveNext](#movenext)()

При отсутствии заголовков HTTP для параметра hasNext будет задано значение FALSE. После этого метод GetCurrentHeader завершается сбоем, если он вызывается.

