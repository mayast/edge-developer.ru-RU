---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8acec97ec6060cd53adc3821f6a51db2048935fb
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699203"
---
# интерфейс ICoreWebView2ContentLoadingEventArgs 

```
interface ICoreWebView2ContentLoadingEventArgs
  : public IUnknown
```

Аргументы события для события ContentLoading.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_IsErrorPage](#get_iserrorpage) | Значение true, если загруженное содержимое является страницей ошибки.
[get_NavigationId](#get_navigationid) | Идентификатор навигации.

## Участников

#### get_IsErrorPage 

Значение true, если загруженное содержимое является страницей ошибки.

> общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool * IsErrorPage)

#### get_NavigationId 

Идентификатор навигации.

> общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 * navigation_id)

