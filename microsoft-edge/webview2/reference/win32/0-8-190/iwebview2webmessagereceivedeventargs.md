---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 053e186aec3871b47e2eb5c6684bc00c934c3a77
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654739"
---
# интерфейс IWebView2WebMessageReceivedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

Аргументы события для события WebMessageReceived.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Source](#get_source) | Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.
[get_WebMessageAsJson](#get_webmessageasjson) | Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.
[get_WebMessageAsString](#get_webmessageasstring) | Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.

## Участников

#### get_Source 

Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.

> общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR * Source)

#### get_WebMessageAsJson 

Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.

> общедоступные значения HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR * WebMessageAsJson)

Используйте этот способ для обмена данными с помощью объектов JavaScript.

Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### get_WebMessageAsString 

Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.

> общедоступные значения HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR * WebMessageAsString)

Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG. Используйте этот способ для обмена сообщениями через простые строки.

Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

