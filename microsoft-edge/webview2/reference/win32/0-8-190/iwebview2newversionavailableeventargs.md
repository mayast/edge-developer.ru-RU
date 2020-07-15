---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: e8965ebe2e0434d83b4d6e8eabe74466adb7cec6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878346"
---
# 0.8.355-Interface IWebView2NewVersionAvailableEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

Аргументы события для события NewVersionAvailable.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_NewVersion](#get_newversion) | Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md).

## Участников

#### get_NewVersion 

Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md).

> общедоступные значения HRESULT [get_NewVersion](#get_newversion)(LPWSTR * NewVersion)

