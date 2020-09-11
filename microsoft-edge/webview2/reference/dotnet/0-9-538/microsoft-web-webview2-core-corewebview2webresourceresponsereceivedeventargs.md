---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: a8c988fdfee72ed22e74886b440819d7a9d6fe24
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010513"
---
# класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Аргументы события для события WebResourceResponseReceived.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Запрос](#request) | Объект запроса веб-ресурса.
[Ответ](#response) | Объект ответа на веб-ресурс.
[PopulateResponseContentAsync](#populateresponsecontentasync) | Метод Async для запроса потока содержимого ответа.

## Участников

#### Запрос 

Объект запроса веб-ресурса.

> общедоступный [запрос](#request) HttpRequestMessage

Все изменения, внесенные в этот объект, будут игнорироваться.

#### Ответ 

Объект ответа на веб-ресурс.

> [ответ](#response) на общедоступные HttpResponseMessage

Все изменения, внесенные в этот объект, будут игнорироваться.

#### PopulateResponseContentAsync 

Метод Async для запроса потока содержимого ответа.

> Public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()

