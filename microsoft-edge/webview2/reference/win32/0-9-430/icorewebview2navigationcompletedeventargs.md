---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NavigationCompletedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 099a022fef47beca0e0163e6e0e070aa37520a06
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883730"
---
# 0.9.430-Interface ICoreWebView2NavigationCompletedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NavigationCompletedEventArgs
  : public IUnknown
```

Аргументы события для события NavigationCompleted.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_IsSuccess](#get_issuccess) | Значение true, если навигация выполнена успешно.
[get_WebErrorStatus](#get_weberrorstatus) | Код ошибки, если навигация завершилась сбоем.
[get_NavigationId](#get_navigationid) | Идентификатор навигации.

## Участников

#### get_IsSuccess 

Значение true, если навигация выполнена успешно.

> общедоступные значения HRESULT [get_IsSuccess](#get_issuccess)(bool * "успешно")

Это значение является ложным для навигации, которая завершилась на странице ошибки (ошибки поиска DNS, HTTP-сервер отвечает на 4xx), но это также может быть ложным для дополнительных функций, таких как Window. Stop (), вызываемых на странице навигации.

#### get_WebErrorStatus 

Код ошибки, если навигация завершилась сбоем.

> общедоступные значения HRESULT [get_WebErrorStatus](#get_weberrorstatus)(CORE_WEBVIEW2_WEB_ERROR_STATUS * CORE_WEBVIEW2_WEB_ERROR_STATUS)

#### get_NavigationId 

Идентификатор навигации.

> общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 * navigation_id)

