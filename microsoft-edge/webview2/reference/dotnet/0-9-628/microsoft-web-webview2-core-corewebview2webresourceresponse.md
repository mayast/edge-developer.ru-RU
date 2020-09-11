---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 5359634d83717ce844d2c1604a2645ceffc477cc
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012429"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2WebResourceResponse 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

HTTP-ответ, используемый с событием WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Содержимое](#content) | Содержимое ответа HTTP в виде потока.
[Заголовки](#headers) | Переопределенные заголовки HTTP-ответа.
[ReasonPhrase](#reasonphrase) | Фраза причина HTTP-ответа.
[StatusCode](#statuscode) | Код состояния HTTP-ответа.

## Участников

#### Содержимое 

Содержимое ответа HTTP в виде потока.

> Общее [содержимое](#content) потока

Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа. Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса. NULL означает, что данные содержимого отсутствуют. Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).

#### Заголовки 

Переопределенные заголовки HTTP-ответа.

> [заголовки](#headers) общедоступной [CoreWebView2HttpResponseHeaders](microsoft-web-webview2-core-corewebview2httpresponseheaders.md)

#### ReasonPhrase 

Фраза причина HTTP-ответа.

> общедоступная строка [ReasonPhrase](#reasonphrase)

#### StatusCode 

Код состояния HTTP-ответа.

> Открытый целочисленный [StatusCode](#statuscode)

