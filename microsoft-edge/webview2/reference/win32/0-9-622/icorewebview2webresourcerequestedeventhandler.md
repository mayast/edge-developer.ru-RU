---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 6aa36c8b28a3e47a796324987687ab23179aae10
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012397"
---
# интерфейс ICoreWebView2WebResourceRequestedEventHandler 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

Активируется при выполнении запроса URL-адреса (с помощью сети, файла и т. д.) в WebView для фильтрации контекста ресурсов и URL-адреса, указанных в AddWebResourceRequestedFilter.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления средству реализации аргументов события для соответствующего события.

Основное приложение может просматривать и изменять запрос, а также предоставлять ответ в соответствии с похожим шаблоном на HTTP, в этом случае запрос немедленно завершен. Это не может содержать заголовки запросов, добавленные сетевым стеком, например заголовки авторизации.

## Участников

#### Invoke 

Вызывается для предоставления средству реализации аргументов события для соответствующего события.

> Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) * sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) * args)

