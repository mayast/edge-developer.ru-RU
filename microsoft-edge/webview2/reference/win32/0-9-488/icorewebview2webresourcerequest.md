---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b60df5b7493ab095c6e71f7d28dbb6ec78d39052
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883772"
---
# 0.9.515-Interface ICoreWebView2WebResourceRequest 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

HTTP-запрос, используемый для события WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Текст сообщения HTTP-запроса в виде потока.
[get_Headers](#get_headers) | Изменяющиеся заголовки HTTP-запроса.
[get_Method](#get_method) | Метод HTTP-запроса.
[get_Uri](#get_uri) | URI запроса.
[put_Content](#put_content) | Задайте свойство Content (содержимое).
[put_Method](#put_method) | Задайте свойство Method.
[put_Uri](#put_uri) | Задайте свойство URI.

## Участников

#### get_Content 

Текст сообщения HTTP-запроса в виде потока.

> общедоступные значения HRESULT [get_Content](#get_content)(IStream * * содержимое)

Поместите здесь данные. Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа. Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса. NULL означает, что данные содержимого отсутствуют. Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).

#### get_Headers 

Изменяющиеся заголовки HTTP-запроса.

> общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) * * headers)

#### get_Method 

Метод HTTP-запроса.

> общедоступный [GET_METHOD](#get_method)HRESULT (метод LPWSTR *)

#### get_Uri 

URI запроса.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### put_Content 

Задайте свойство Content (содержимое).

> общедоступные значения HRESULT [put_Content](#put_content)(IStream * Content)

#### put_Method 

Задайте свойство Method.

> общедоступные значения HRESULT [put_Method](#put_method)(метод LPCWSTR)

#### put_Uri 

Задайте свойство URI.

> общедоступные значения HRESULT [put_Uri](#put_uri)(URI LPCWSTR)

