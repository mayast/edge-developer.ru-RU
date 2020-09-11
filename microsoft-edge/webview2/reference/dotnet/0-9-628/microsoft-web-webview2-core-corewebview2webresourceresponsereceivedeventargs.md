---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 2d0660616de0c234b1535b2af127843fea3a3a53
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012427"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponseReceivedEventArgs 

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

> общедоступный [запрос](#request) [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md)

Все изменения, внесенные в этот объект, будут игнорироваться.

#### Ответ 

Объект ответа на веб-ресурс.

> [ответ](#response) на общедоступные [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md)

Все изменения, внесенные в этот объект, будут игнорироваться.

#### PopulateResponseContentAsync 

Метод Async для запроса потока содержимого ответа.

> Public async Task [PopulateResponseContentAsync](#populateresponsecontentasync)()

