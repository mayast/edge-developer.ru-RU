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
ms.openlocfilehash: 4b9ad48d9b09343bad04d4acbe7c49750e76427d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654979"
---
# интерфейс IWebView2HttpHeadersCollectionIterator 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

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

