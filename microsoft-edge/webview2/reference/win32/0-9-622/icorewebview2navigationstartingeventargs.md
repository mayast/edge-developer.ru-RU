---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2NavigationStartingEventArgs
ms.openlocfilehash: ebfb4aaf3f0c2b5531aaab3783572cf550bebf83
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012537"
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

Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным. По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы. Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации. Отмена для навигации: пустая или переход по рамкам в srcdoc не поддерживается. Такие попытки будут игнорироваться.

#### get_IsRedirected 

Значение true, если перенаправлять навигацию.

> общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool * Redirect)

#### get_IsUserInitiated 

Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.

> общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

#### get_NavigationId 

Идентификатор навигации.

> общедоступные значения HRESULT [get_NavigationId](#get_navigationid)(UINT64 * NavigationId)

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

