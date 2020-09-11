---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 501483894a2abca58c5a1856ab587b93be904c8b
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012432"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Аргументы события для события WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Запрос](#request) | Запрос на веб-ресурс.
[ResourceContext](#resourcecontext) | Контекст запроса веб-ресурса.
[Ответ](#response) | Заполнитель для объекта ответа на веб-ресурс.
[GetDeferral](#getdeferral) | Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.

## Участников

#### Запрос 

Запрос на веб-ресурс.

> общедоступный [запрос](#request) [CoreWebView2WebResourceRequest](microsoft-web-webview2-core-corewebview2webresourcerequest.md)

Возможно, в объекте Request отсутствует часть заголовков, добавленных в разделе "сетевой стек".

#### ResourceContext 

Контекст запроса веб-ресурса.

> общедоступная [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [разделе ResourceContext](#resourcecontext)

#### Ответ 

Заполнитель для объекта ответа на веб-ресурс.

> [ответ](#response) на общедоступные [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md)

Если этот объект задан, запрос на веб-ресурс будет выполнен с этим ответом. Пустой объект ответа на веб-ресурс можно создать с помощью CreateWebResourceResponse и затем изменить для создания ответа.

#### GetDeferral 

Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.

> общедоступный [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) - [РБП](#getdeferral)()

Вы можете использовать объект CoreWebView2Deferral, чтобы выполнить запрос позже.

