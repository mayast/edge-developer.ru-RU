---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b44724f8e18e11374f88ed2cd22711f06f59f12d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654859"
---
# интерфейс ICoreWebView2NewBrowserVersionAvailableEventHandler 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления средству реализации аргументов события для соответствующего события.

Для получения нового номера версии используйте get_NewVersion метод [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) .

## Участников

#### Invoke 

Вызывается для предоставления средству реализации аргументов события для соответствующего события.

> Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) * webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) * args)

