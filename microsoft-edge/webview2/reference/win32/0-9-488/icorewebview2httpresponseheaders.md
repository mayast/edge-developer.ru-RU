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
ms.openlocfilehash: fe03c3ab6d951ecd54bd76cd7abc89de637496ea
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654844"
---
# интерфейс ICoreWebView2HttpResponseHeaders 

```
interface ICoreWebView2HttpResponseHeaders
  : public IUnknown
```

Заголовки ответа HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[AppendHeader](#appendheader) | Добавляет строку заголовка с именем и значением.
[Contains](#contains) | Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.
["Голова"](#getheader) | Возвращает значение первого заголовка в коллекции, соответствующее имени.
["Голова"](#getheaders) | Возвращает значения заголовков, соответствующие имени.
[Реверсивный итератор](#getiterator) | Получает итератор на коллекцию всех заголовков ответа.

Используется для создания WebResourceResponse для события WebResourceRequested.

## Участников

#### AppendHeader 

Добавляет строку заголовка с именем и значением.

> общедоступные значения HRESULT [AppendHeader](#appendheader)(имя LPCWSTR, значение LPCWSTR)

#### Contains 

Проверяет, содержат ли заголовки записи, соответствующие имени заголовка.

> общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool * Contains)

#### "Голова" 

Возвращает значение первого заголовка в коллекции, соответствующее имени.

> общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR * Value)

#### "Голова" 

Возвращает значения заголовков, соответствующие имени.

> общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * итератор)

#### Реверсивный итератор 

Получает итератор на коллекцию всех заголовков ответа.

> общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * *)
