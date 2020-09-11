---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HttpRequestHeaders
ms.openlocfilehash: 8455db6adccf2d3d10e9934fee940d00bba7377c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012467"
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

