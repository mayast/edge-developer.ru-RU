---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. EdgeNotFoundException
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 09a930231fd7f6886108904f25f07bde5c76db73
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879620"
---
# Класс Microsoft. Web. WebView2. Core. EdgeNotFoundException 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

```
class Microsoft.Web.WebView2.Core.EdgeNotFoundException
  : public Exception
```

Исключение, возникающее при отсутствии установки Edge.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[EdgeNotFoundException](#edgenotfoundexception) | Инициализирует новый экземпляр класса EdgeNotFoundException.
[EdgeNotFoundException](#edgenotfoundexception) | Инициализирует новый экземпляр класса EdgeNotFoundException ссылкой на внутреннее исключение, которое является причиной этого исключения.
[EdgeNotFoundException](#edgenotfoundexception) | Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке.
[EdgeNotFoundException](#edgenotfoundexception) | Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке и ссылкой на внутреннее исключение, которое является причиной этого исключения.

## Участников

#### EdgeNotFoundException 

Инициализирует новый экземпляр класса EdgeNotFoundException.

> общедоступная [EdgeNotFoundException](#edgenotfoundexception)()

#### EdgeNotFoundException 

Инициализирует новый экземпляр класса EdgeNotFoundException ссылкой на внутреннее исключение, которое является причиной этого исключения.

> общедоступный [EdgeNotFoundException](#edgenotfoundexception)(внутренние исключения)

##### Параметры
* `inner` Исключение, вызвавшее текущее исключение.

#### EdgeNotFoundException 

Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке.

> общедоступный [EdgeNotFoundException](#edgenotfoundexception)(строковое сообщение)

##### Параметры
* `message` Сообщение об ошибке, объясняющее причину исключения.

#### EdgeNotFoundException 

Инициализирует новый экземпляр класса EdgeNotFoundException с указанным сообщением об ошибке и ссылкой на внутреннее исключение, которое является причиной этого исключения.

> общедоступный [EdgeNotFoundException](#edgenotfoundexception)(строковое сообщение, исключение Inner)

##### Параметры
* `message` Сообщение об ошибке, объясняющее причину исключения. 

* `inner` Исключение, вызвавшее текущее исключение.

