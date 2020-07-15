---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebResourceResponse
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c0c33bab95f8d2c7908864b1869bc9a186216ef9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877548"
---
# 0.9.430-Interface ICoreWebView2WebResourceResponse 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

HTTP-ответ, используемый с событием WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Содержимое ответа HTTP в виде потока.
[put_Content](#put_content) | Задайте свойство Content (содержимое).
[get_Headers](#get_headers) | Переопределенные заголовки HTTP-ответа.
[get_StatusCode](#get_statuscode) | Код состояния HTTP-ответа.
[put_StatusCode](#put_statuscode) | Задайте Свойство StatusCode.
[get_ReasonPhrase](#get_reasonphrase) | Фраза причина HTTP-ответа.
[put_ReasonPhrase](#put_reasonphrase) | Задайте свойство ReasonPhrase.

## Участников

#### get_Content 

Содержимое ответа HTTP в виде потока.

> общедоступные значения HRESULT [get_Content](#get_content)(IStream * * содержимое)

Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа. Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса. NULL означает, что данные содержимого отсутствуют. Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).

#### put_Content 

Задайте свойство Content (содержимое).

> общедоступные значения HRESULT [put_Content](#put_content)(IStream * Content)

#### get_Headers 

Переопределенные заголовки HTTP-ответа.

> общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) * * headers)

#### get_StatusCode 

Код состояния HTTP-ответа.

> общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int * StatusCode)

#### put_StatusCode 

Задайте Свойство StatusCode.

> общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)

#### get_ReasonPhrase 

Фраза причина HTTP-ответа.

> общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR * ReasonPhrase)

#### put_ReasonPhrase 

Задайте свойство ReasonPhrase.

> общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)

