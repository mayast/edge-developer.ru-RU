---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 44fc4f47aa10a7e409ac584cb75b750048056e47
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886529"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs 

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

