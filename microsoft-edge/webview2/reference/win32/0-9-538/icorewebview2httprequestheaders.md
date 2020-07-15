---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 903355ff04463ad86f1e25771f5f321f7d0df479
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879165"
---
# интерфейс ICoreWebView2HttpRequestHeaders 

```
interface ICoreWebView2HttpRequestHeaders
  : public IUnknown
```

Заголовки запросов HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Contains](#contains) | Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.
["Голова"](#getheader) | Возвращает значение заголовка, совпадающее с именем.
["Голова"](#getheaders) | Возвращает значение заголовка, совпадающее с именем через итератор.
[Реверсивный итератор](#getiterator) | Получает итератор на коллекцию заголовков запроса.
[RemoveHeader](#removeheader) | Удаляет заголовок, соответствующий имени.
[SetHeader](#setheader) | Добавляет или обновляет заголовок, соответствующий имени.

Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting. Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.

## Участников

#### Contains 

Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.

> общедоступное значение HRESULT [Contains](#contains)(имя LPCWSTR, bool * Contains)

#### "Голова" 

Возвращает значение заголовка, совпадающее с именем.

> общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR * Value)

#### "Голова" 

Возвращает значение заголовка, совпадающее с именем через итератор.

> общедоступные [Выголовки](#getheaders)HRESULT (имя LPCWSTR, [ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * * итератор)

#### Реверсивный итератор 

Получает итератор на коллекцию заголовков запроса.

> общедоступный HRESULT- [итератор](#getiterator)([ICoreWebView2HttpHeadersCollectionIterator](icorewebview2httpheaderscollectioniterator.md) * *)

#### RemoveHeader 

Удаляет заголовок, соответствующий имени.

> общедоступное значение HRESULT [RemoveHeader](#removeheader)(имя LPCWSTR)

#### SetHeader 

Добавляет или обновляет заголовок, соответствующий имени.

> общедоступные значения HRESULT [SetHeader](#setheader)(имя LPCWSTR, значение LPCWSTR)

