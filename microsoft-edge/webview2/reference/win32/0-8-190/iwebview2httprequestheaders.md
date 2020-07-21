---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpRequestHeaders
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 1e0148c0d1e27cb4f1c52fb6ad55cc2e7613a94b
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885970"
---
# 0.8.355-Interface IWebView2HttpRequestHeaders 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpRequestHeaders
  : public IUnknown
```

Заголовки запросов HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
["Голова"](#getheader) | Возвращает значение заголовка, совпадающее с именем.
[Contains](#contains) | Проверяет, содержат ли заголовки запись, совпадающую с именем заголовка.
[SetHeader](#setheader) | Добавляет или обновляет заголовок, соответствующий имени.
[RemoveHeader](#removeheader) | Удаляет заголовок, соответствующий имени.
[Реверсивный итератор](#getiterator) | Получает итератор на коллекцию заголовков запроса.

Используется для проверки HTTP-запроса на событие WebResourceRequested и событие NavigationStarting. Обратите внимание, что заголовки HTTP-запросов можно изменить из события WebResourceRequested, но не из события NavigationStarting.

## Участников

#### "Голова" 

Возвращает значение заголовка, совпадающее с именем.

> общедоступный [заголовок](#getheader)HRESULT (имя LPCWSTR, LPWSTR * Value)

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

> общедоступный HRESULT- [итератор](#getiterator)([IWebView2HttpHeadersCollectionIterator](IWebView2HttpHeadersCollectionIterator.md) * *)

