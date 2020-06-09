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
ms.openlocfilehash: b917f309194316b26ee94aa94dc8289ef4430007
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697541"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Аргументы события для события WebMessageReceived.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Источник](#source) | Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.
[WebMessageAsJson](#webmessageasjson) | Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.
[TryGetWebMessageAsString](#trygetwebmessageasstring) | Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.

## Участников

#### Источник 

Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.

> [источник](#source) общедоступной строки

#### WebMessageAsJson 

Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.

> общедоступная строка [WebMessageAsJson](#webmessageasjson)

Используйте этот способ для обмена данными с помощью объектов JavaScript.

Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### TryGetWebMessageAsString 

Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.

> public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()

Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG. Используйте этот способ для обмена сообщениями через простые строки.

Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

