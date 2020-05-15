---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 3b348d64bb09fcdc693ffbdfa5481fe6d7520cae
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654689"
---
# интерфейс ICoreWebView2NavigationStartingEventArgs 

```
interface ICoreWebView2NavigationStartingEventArgs
  : public IUnknown
```

Аргументы события для события NavigationStarting.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Cancel](#get_cancel) | Ведущее приложение может установить этот флаг, чтобы отменить навигацию.
[get_IsRedirected](#get_isredirected) | Значение true, если перенаправлять навигацию.
[get_IsUserInitiated](#get_isuserinitiated) | Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.
[get_NavigationId](#get_navigationid) | Идентификатор навигации.
[get_RequestHeaders](#get_requestheaders) | Заголовки HTTP-запроса для навигации.
[get_Uri](#get_uri) | URI запрошенной навигации.
[put_Cancel](#put_cancel) | Задайте свойство Cancel.

## Участников

#### get_Cancel 

Ведущее приложение может установить этот флаг, чтобы отменить навигацию.

> общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool * Cancel)

Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным. По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы. Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.

#### get_IsRedirected 

Значение true, если перенаправлять навигацию.

> общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool * Redirect)

#### get_IsUserInitiated 

Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.

> общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

#### get_NavigationId 

Идентификатор навигации.

> общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 * navigation_id)

#### get_RequestHeaders 

Заголовки HTTP-запроса для навигации.

> общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) * * RequestHeaders)

Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.

#### get_Uri 

URI запрошенной навигации.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### put_Cancel 

Задайте свойство Cancel.

> общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)

