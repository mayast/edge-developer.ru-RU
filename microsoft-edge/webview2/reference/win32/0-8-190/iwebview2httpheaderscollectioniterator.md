---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: dbcc5b10ce1973df61554f3f27174f600fb25280
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885983"
---
# 0.8.355-Interface IWebView2HttpHeadersCollectionIterator 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Итератор для коллекции заголовков HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[GetCurrentHeader](#getcurrentheader) | Получите имя и значение текущего HTTP-заголовка итератора.
[MoveNext](#movenext) | Переместите итератор на следующий заголовок HTTP в коллекции.

Смотрите [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) и [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).

## Участников

#### GetCurrentHeader 

Получите имя и значение текущего HTTP-заголовка итератора.

> Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR * имя, LPWSTR * значение)

Этот метод завершается сбоем, если последний вызов MoveNext задает has_next значение FALSE.

#### MoveNext 

Переместите итератор на следующий заголовок HTTP в коллекции.

> общедоступный HRESULT [MoveNext](#movenext)(BOOL * has_next)

Для параметра has_next будет задано значение FALSE, если больше нет заголовков HTTP. После этого метод GetCurrentHeader завершается сбоем, если он вызывается.

