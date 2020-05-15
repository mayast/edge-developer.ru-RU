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
ms.openlocfilehash: 7a4e074d445b4bab11e8e79dc6cfe5346effbb3f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654978"
---
# интерфейс IWebView2CreateWebView2EnvironmentCompletedHandler 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2CreateWebView2EnvironmentCompletedHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс для получения WebView2Environment, созданного с помощью CreateWebView2Environment.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.

## Участников

#### Invoke 

Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.

> общедоступный [вызов](#invoke)HRESULT (результат HRESULT,[IWebView2Environment](IWebView2Environment.md) * webViewEnvironment)

