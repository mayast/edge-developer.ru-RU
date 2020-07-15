---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NavigationStartingEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 8bc625d12cc3b3ebe06970fd282dd8f60bcabd22
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878402"
---
# 0.8.355-Interface IWebView2NavigationStartingEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2NavigationStartingEventArgs
  : public IUnknown
```

Аргументы события для события NavigationStarting.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Uri](#get_uri) | URI запрошенной навигации.
[get_IsUserInitiated](#get_isuserinitiated) | Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.
[get_IsRedirected](#get_isredirected) | Значение true, если перенаправлять навигацию.
[get_RequestHeaders](#get_requestheaders) | Заголовки HTTP-запроса для навигации.
[get_Cancel](#get_cancel) | Ведущее приложение может установить этот флаг, чтобы отменить навигацию.
[put_Cancel](#put_cancel) | Задайте свойство Cancel.

## Участников

#### get_Uri 

URI запрошенной навигации.

> общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR * URI)

#### get_IsUserInitiated 

Значение true, если навигация была инициирована с помощью жеста пользователя, а не программной навигации.

> общедоступные значения HRESULT [get_IsUserInitiated](#get_isuserinitiated)(bool * IsUserInitiated)

#### get_IsRedirected 

Значение true, если перенаправлять навигацию.

> общедоступные значения HRESULT [get_IsRedirected](#get_isredirected)(bool * Redirect)

#### get_RequestHeaders 

Заголовки HTTP-запроса для навигации.

> общедоступные значения HRESULT [get_RequestHeaders](#get_requestheaders)([IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) * * RequestHeaders)

Обратите внимание, что вы не можете изменять заголовки HTTP-запросов в событии NavigationStarting.

#### get_Cancel 

Ведущее приложение может установить этот флаг, чтобы отменить навигацию.

> общедоступные значения HRESULT [get_Cancel](#get_cancel)(bool * Cancel)

Если этот параметр установлен, это может быть так, как если бы Навигация не выполнялась, но содержимое текущей страницы будет неизменным. По соображениям быстродействия получение HTTP-запросов может происходить, когда хост отвечает на запросы. Это означает, что cookie-файлы могут быть настроены и использованы частью запроса навигации.

#### put_Cancel 

Задайте свойство Cancel.

> общедоступные значения HRESULT [put_Cancel](#put_cancel)(bool Cancel)

