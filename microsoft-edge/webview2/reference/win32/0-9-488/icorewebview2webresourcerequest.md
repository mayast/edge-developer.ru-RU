---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d91b7aeeebc8fd82587ac6c01fddd14e693c2559
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697065"
---
# интерфейс ICoreWebView2WebResourceRequest 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

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

