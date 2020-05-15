---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 201b9af4a5838c9537014864c31cd2121f9dfe76
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654649"
---
# интерфейс ICoreWebView2WebResourceRequest 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2WebResourceRequest
  : public IUnknown
```

HTTP-запрос, используемый для события WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | URI запроса.
[put_Uri](#put_uri) | Задайте свойство URI.
[get_Method](#get_method) | Метод HTTP-запроса.
[put_Method](#put_method) | Задайте свойство Method.
[get_Content](#get_content) | Текст сообщения HTTP-запроса в виде потока.
[put_Content](#put_content) | Задайте свойство Content (содержимое).
[get_Headers](#get_headers) | Изменяющиеся заголовки HTTP-запроса.

## Участников

#### get_Uri 

URI запроса.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### put_Uri 

Задайте свойство URI.

> общедоступные значения HRESULT [put_Uri](#put_uri)(URI LPCWSTR)

#### get_Method 

Метод HTTP-запроса.

> общедоступный [GET_METHOD](#get_method)HRESULT (метод LPWSTR *)

#### put_Method 

Задайте свойство Method.

> общедоступные значения HRESULT [put_Method](#put_method)(метод LPCWSTR)

#### get_Content 

Текст сообщения HTTP-запроса в виде потока.

> общедоступные значения HRESULT [get_Content](#get_content)(IStream * * содержимое)

Поместите здесь данные. Если задан поток, который переопределит тело сообщения, поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа. Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса. NULL означает, что данные содержимого отсутствуют. Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).

#### put_Content 

Задайте свойство Content (содержимое).

> общедоступные значения HRESULT [put_Content](#put_content)(IStream * Content)

#### get_Headers 

Изменяющиеся заголовки HTTP-запроса.

> общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) * * headers)

