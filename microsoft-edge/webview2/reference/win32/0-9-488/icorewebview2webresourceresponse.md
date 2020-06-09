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
ms.openlocfilehash: 5b80691f0e42be4cdea7c99b165bfe9cebf632dd
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697933"
---
# интерфейс ICoreWebView2WebResourceResponse 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

```
interface ICoreWebView2WebResourceResponse
  : public IUnknown
```

HTTP-ответ, используемый с событием WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Content](#get_content) | Содержимое ответа HTTP в виде потока.
[get_Headers](#get_headers) | Переопределенные заголовки HTTP-ответа.
[get_ReasonPhrase](#get_reasonphrase) | Фраза причина HTTP-ответа.
[get_StatusCode](#get_statuscode) | Код состояния HTTP-ответа.
[put_Content](#put_content) | Задайте свойство Content (содержимое).
[put_ReasonPhrase](#put_reasonphrase) | Задайте свойство ReasonPhrase.
[put_StatusCode](#put_statuscode) | Задайте Свойство StatusCode.

## Участников

#### get_Content 

Содержимое ответа HTTP в виде потока.

> общедоступные значения HRESULT [get_Content](#get_content)(IStream * * содержимое)

Поток должен иметь все данные содержимого, доступные на момент завершения периода отсрочки события WebResourceRequested этого ответа. Поток должен быть гибким или создаваться из фонового потока, чтобы предотвратить снижение производительности потока пользовательского интерфейса. NULL означает, что данные содержимого отсутствуют. Семантики IStream применяются (возвращают S_OK для чтения звонков, пока все данные не будут исчерпаны).

#### get_Headers 

Переопределенные заголовки HTTP-ответа.

> общедоступные значения HRESULT [get_Headers](#get_headers)([ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md) * * headers)

#### get_ReasonPhrase 

Фраза причина HTTP-ответа.

> общедоступные значения HRESULT [get_ReasonPhrase](#get_reasonphrase)(LPWSTR * ReasonPhrase)

#### get_StatusCode 

Код состояния HTTP-ответа.

> общедоступные значения HRESULT [get_StatusCode](#get_statuscode)(int * StatusCode)

#### put_Content 

Задайте свойство Content (содержимое).

> общедоступные значения HRESULT [put_Content](#put_content)(IStream * Content)

#### put_ReasonPhrase 

Задайте свойство ReasonPhrase.

> общедоступные значения HRESULT [put_ReasonPhrase](#put_reasonphrase)(LPCWSTR ReasonPhrase)

#### put_StatusCode 

Задайте Свойство StatusCode.

> общедоступное значение HRESULT [put_StatusCode](#put_statuscode)(int StatusCode)

