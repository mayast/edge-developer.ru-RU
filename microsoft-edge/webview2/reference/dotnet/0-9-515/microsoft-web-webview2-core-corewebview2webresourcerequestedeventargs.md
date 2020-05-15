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
ms.openlocfilehash: 9210a4b70d0e2edf30cbaad906f57b360688dfe8
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654703"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceRequestedEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Аргументы события для события WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Запрос](#request) | HTTP-запрос.
[ResourceContext](#resourcecontext) | Контексты запросов веб-ресурсов.
[Ответ](#response) | Ответ HTTP.
[GetDeferral](#getdeferral) | Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.

## Участников

#### Запрос 

HTTP-запрос.

> общедоступный [запрос](#request) HttpRequestMessage

#### ResourceContext 

Контексты запросов веб-ресурсов.

> общедоступная [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) [разделе ResourceContext](#resourcecontext)

#### Ответ 

Ответ HTTP.

> [ответ](#response) на общедоступные HttpResponseMessage

#### GetDeferral 

Получите объект CoreWebView2Deferral и помещайте событие в отложенное состояние.

> общедоступный [CoreWebView2Deferral](microsoft-web-webview2-core-corewebview2deferral.md) - [РБП](#getdeferral)()

Вы можете использовать объект CoreWebView2Deferral для выполнения сетевого запроса позже.

