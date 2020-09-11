---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 1441d5a45caf4e8f561de2487438b66e067760f6
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012412"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2HttpRequestHeaders 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Заголовки запросов HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Contains](#contains) | Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.
["Голова"](#getheader) | Возвращает значение заголовка, совпадающее с именем.
["Голова"](#getheaders) | Возвращает значение заголовка, совпадающее с именем через итератор.
[Реверсивный итератор](#getiterator) | Получает итератор на коллекцию заголовков запроса.
[RemoveHeader](#removeheader) | Удаляет заголовок, соответствующий имени.
[SetHeader](#setheader) | Добавляет или обновляет заголовок, соответствующий имени.

Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting. Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.

## Участников

#### Contains 

Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.

> общедоступный bool [имеет](#contains)(строковое имя)

#### "Голова" 

Возвращает значение заголовка, совпадающее с именем.

> [заголовок](#getheader)общедоступной строки (имя строки)

#### "Голова" 

Возвращает значение заголовка, совпадающее с именем через итератор.

> общедоступные CoreWebView2HttpHeadersCollectionIterator- [заголовки](#getheaders)(строковое имя)

#### Реверсивный итератор 

Получает итератор на коллекцию заголовков запроса.

> Public CoreWebView2HttpHeadersCollectionIterator- [iterator](#getiterator)()

#### RemoveHeader 

Удаляет заголовок, соответствующий имени.

> общедоступная void [RemoveHeader](#removeheader)(строковое имя)

#### SetHeader 

Добавляет или обновляет заголовок, соответствующий имени.

> Public void [SetHeader](#setheader)(строковое имя, строковое значение)

