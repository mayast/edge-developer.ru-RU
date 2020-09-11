---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HttpResponseHeaders
ms.openlocfilehash: 1622d2c19159bca76e036408810e2ca145d30e85
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012466"
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

