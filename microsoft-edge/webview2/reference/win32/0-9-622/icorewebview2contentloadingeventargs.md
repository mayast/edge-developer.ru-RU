---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ContentLoadingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ContentLoadingEventArgs
ms.openlocfilehash: 229389c6859363ef9a7c3fbf7719dbe30a061875
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012579"
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

> общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 * NavigationId)

