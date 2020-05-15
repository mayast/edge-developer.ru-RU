---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654956"
---
# интерфейс IWebView2NewVersionAvailableEventArgs 

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

