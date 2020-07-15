---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 336a4204a69c596a8423c32f3ef49cf7d12f51d4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880950"
---
# 0.9.515-Interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

Вызывающий объект реализует этот интерфейс, чтобы получить результат метода AddScriptToExecuteOnDocumentCreated.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Invoke](#invoke) | Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.

## Участников

#### Invoke 

Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.

> общедоступный [вызов](#invoke)HRESULT (ErrorCode код_ошибки, ИД LPCWSTR)

