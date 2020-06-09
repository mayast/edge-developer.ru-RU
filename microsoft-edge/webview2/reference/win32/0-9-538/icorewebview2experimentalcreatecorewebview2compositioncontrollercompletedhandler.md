---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 92eab98dfbd5f4c9239a5263e524daa2e7346eb5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699172"
---
# интерфейс ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler 

> [!NOTE]
> Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.

```
interface ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс для получения CoreWebView2Controller, созданного с помощью CreateCoreWebView2CompositionController.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.

## Участников

#### Invoke 

Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.

> общедоступный [вызов](#invoke)HRESULT (результат HRESULT, [ICoreWebView2ExperimentalCompositionController](icorewebview2experimentalcompositioncontroller.md) * webView)

