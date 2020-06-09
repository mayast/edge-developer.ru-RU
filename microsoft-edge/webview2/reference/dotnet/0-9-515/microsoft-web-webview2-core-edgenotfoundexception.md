---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 7f30bda4deb0811748c65880fcc49c21bc39a732
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697296"
---
# Класс Microsoft. Web. WebView2. Core. EdgeNotFoundException 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

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

