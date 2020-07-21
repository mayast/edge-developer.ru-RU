---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9f56ba33534c76cb1bd60c01a88eedfced45f1fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884864"
---
# 0.9.430-Interface ICoreWebView2NewBrowserVersionAvailableEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

Аргументы события для события NewBrowserVersionAvailable.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Сведения о версии браузера для текущего [ICoreWebView2Environment](ICoreWebView2Environment.md).

## Участников

#### get_NewVersion 

Сведения о версии браузера для текущего [ICoreWebView2Environment](ICoreWebView2Environment.md).

> общедоступные значения HRESULT [get_NewVersion](#get_newversion)(LPWSTR * NewVersion)

