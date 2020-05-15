---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c6bb99078b5574ba89c0d66b49e2c63cd6888d28
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654900"
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

