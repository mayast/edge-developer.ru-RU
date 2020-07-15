---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpResponseHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 44f7477eaa81198ef64d332faa0c3a22225d5ea4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880973"
---
# 0.9.430-Interface ICoreWebView2HttpResponseHeaders 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

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

> общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * итератор)

#### Реверсивный итератор 

Получает итератор на коллекцию всех заголовков ответа.

> общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * *)

