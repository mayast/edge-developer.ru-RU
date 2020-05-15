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
ms.openlocfilehash: ad3f4e5e95b0309628644f17e5d647ab6d4af658
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654674"
---
# интерфейс IWebView2WebResourceResponse 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2WebResourceResponse
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

> общедоступные значения HRESULT [get_Headers](#get_headers)([IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) * * headers)

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

