---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 5c8d164b24995cc31070232dd9b1a2d88fc16cec
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012433"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequest 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

HTTP-запрос, используемый для события WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Содержимое](#content) | Текст сообщения HTTP-запроса в виде потока.
[Заголовки](#headers) | Изменяющиеся заголовки HTTP-запроса.
[Метод](#method) | Метод HTTP-запроса.
[Универсальный код ресурса (URI)](#uri) | URI запроса.

## Участников

#### Содержимое 

Текст сообщения HTTP-запроса в виде потока.

> Общее [содержимое](#content) потока

Поместите здесь данные. Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа. Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса. NULL означает, что данные содержимого отсутствуют. Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).

#### Заголовки 

Изменяющиеся заголовки HTTP-запроса.

> [заголовки](#headers) общедоступной [CoreWebView2HttpRequestHeaders](microsoft-web-webview2-core-corewebview2httprequestheaders.md)

#### Метод 

Метод HTTP-запроса.

> [метод](#method) общедоступной строки

#### Универсальный код ресурса (URI) 

URI запроса.

> [URI](#uri) общедоступной строки

