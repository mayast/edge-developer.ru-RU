---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a67c5c267178ea873cd12d8a22dea7409b260d52
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880999"
---
# 0.9.430-Interface ICoreWebView2HttpRequestHeaders 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

Заголовки запросов HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
["Голова"](#getheader) | Возвращает значение заголовка, совпадающее с именем.
["Голова"](#getheaders) | Возвращает значение заголовка, совпадающее с именем через итератор.
[Contains](#contains) | Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.
[SetHeader](#setheader) | Добавляет или обновляет заголовок, соответствующий имени.
[RemoveHeader](#removeheader) | Удаляет заголовок, соответствующий имени.
[Реверсивный итератор](#getiterator) | Получает итератор на коллекцию заголовков запроса.

Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting. Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.

## Участников

#### "Голова" 

Возвращает значение заголовка, совпадающее с именем.

> общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR * Value)

#### "Голова" 

Возвращает значение заголовка, совпадающее с именем через итератор.

> общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR,[ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * * итератор)

#### Contains 

Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.

> общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool * Contains)

#### SetHeader 

Добавляет или обновляет заголовок, соответствующий имени.

> общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)

#### RemoveHeader 

Удаляет заголовок, соответствующий имени.

> общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)

#### Реверсивный итератор 

Получает итератор на коллекцию заголовков запроса.

> общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](ICoreWebView2HttpHeadersCollectionIterator.md) * *)

