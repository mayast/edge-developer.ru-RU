---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: dfa6aedb10e60a2af15c7b098c479f8537d6c747
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012406"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2NavigationCompletedEventArgs 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Аргументы события для события NavigationCompleted.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Удачи](#issuccess) | Значение true, если навигация выполнена успешно.
[NavigationId](#navigationid) | Идентификатор навигации.
[WebErrorStatus](#weberrorstatus) | Код ошибки, если навигация завершилась сбоем.

## Участников

#### Удачи 

Значение true, если навигация выполнена успешно.

> общедоступный bool ( [успешно](#issuccess) )

Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных сценариев, таких как Window. Stop (), вызываемых на странице навигации.

#### NavigationId 

Идентификатор навигации.

> общедоступный ulong [NavigationId](#navigationid)

#### WebErrorStatus 

Код ошибки, если навигация завершилась сбоем.

> общедоступная CoreWebView2WebErrorStatus [WebErrorStatus](#weberrorstatus)

