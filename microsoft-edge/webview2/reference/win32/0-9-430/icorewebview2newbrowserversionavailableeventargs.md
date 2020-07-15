---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f59b5acac510b66eae0e1ada51e28b6dd9363ca8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877856"
---
# 0.9.430-Interface ICoreWebView2NewBrowserVersionAvailableEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

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

