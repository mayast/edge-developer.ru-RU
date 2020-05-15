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
ms.openlocfilehash: 55ada31485ef061bb3649fb5e2a2811358913dd7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654702"
---
# Класс Microsoft. Web. WebView2. Core. EdgeNotFoundException 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

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
