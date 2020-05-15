---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8baa7b1f571d62fad21a30441f47835bff3da96a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654918"
---
# 0.9.430-Reference (WebView2)  

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../webview2-api-reference.md) информацией по последней ссылке на API.

Элемент управления Microsoft Edge WebView2 позволяет размещать веб-содержимое в приложении с помощью [Microsoft Edge \ (Chromium \)](https://www.microsoftedgeinsider.com) в качестве обработчика визуализации.  Дополнительные сведения можно найти в [статье Обзор Microsoft Edge WebView2](../../index.md)) и [Приступая к работе с WebView2](../../gettingstarted/win32.md).  [ICoreWebView2](0-9-430/ICoreWebView2.md) — это удобное место для изучения данных API.  

## Глобальные  

*   [Глобальные](0-9-430/webview2-idl.md)  

## Приклад  
*   [ICoreWebView2](0-9-430/ICoreWebView2.md)
*   [ICoreWebView2Deferral](0-9-430/ICoreWebView2Deferral.md)
*   [ICoreWebView2DevToolsProtocolEventReceiver](0-9-430/ICoreWebView2DevToolsProtocolEventReceiver.md)
*   [ICoreWebView2Environment](0-9-430/ICoreWebView2Environment.md)
*   [ICoreWebView2Host](0-9-430/ICoreWebView2Host.md)
*   [ICoreWebView2HttpHeadersCollectionIterator](0-9-430/ICoreWebView2HttpHeadersCollectionIterator.md)
*   [ICoreWebView2HttpRequestHeaders](0-9-430/ICoreWebView2HttpRequestHeaders.md)
*   [ICoreWebView2HttpResponseHeaders](0-9-430/ICoreWebView2HttpResponseHeaders.md)
*   [ICoreWebView2Settings](0-9-430/ICoreWebView2Settings.md)
*   [ICoreWebView2WebResourceRequest](0-9-430/ICoreWebView2WebResourceRequest.md)
*   [ICoreWebView2WebResourceResponse](0-9-430/ICoreWebView2WebResourceResponse.md)

### Интерфейсы аргументов событий

*   [ICoreWebView2AcceleratorKeyPressedEventArgs](0-9-430/ICoreWebView2AcceleratorKeyPressedEventArgs.md)
*   [ICoreWebView2ContentLoadingEventArgs](0-9-430/ICoreWebView2ContentLoadingEventArgs.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventArgs](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventArgs.md)
*   [ICoreWebView2MoveFocusRequestedEventArgs](0-9-430/ICoreWebView2MoveFocusRequestedEventArgs.md)
*   [ICoreWebView2NavigationCompletedEventArgs](0-9-430/ICoreWebView2NavigationCompletedEventArgs.md)
*   [ICoreWebView2NavigationStartingEventArgs](0-9-430/ICoreWebView2NavigationStartingEventArgs.md)
*   [ICoreWebView2NewBrowserVersionAvailableEventArgs](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventArgs.md)
*   [ICoreWebView2NewWindowRequestedEventArgs](0-9-430/ICoreWebView2NewWindowRequestedEventArgs.md)
*   [ICoreWebView2PermissionRequestedEventArgs](0-9-430/ICoreWebView2PermissionRequestedEventArgs.md)
*   [ICoreWebView2ProcessFailedEventArgs](0-9-430/ICoreWebView2ProcessFailedEventArgs.md)
*   [ICoreWebView2ScriptDialogOpeningEventArgs](0-9-430/ICoreWebView2ScriptDialogOpeningEventArgs.md)
*   [ICoreWebView2SourceChangedEventArgs](0-9-430/ICoreWebView2SourceChangedEventArgs.md)
*   [ICoreWebView2WebMessageReceivedEventArgs](0-9-430/ICoreWebView2WebMessageReceivedEventArgs.md)
*   [ICoreWebView2WebResourceRequestedEventArgs](0-9-430/ICoreWebView2WebResourceRequestedEventArgs.md)

### Интерфейсы делегатов

*   [ICoreWebView2AcceleratorKeyPressedEventHandler](0-9-430/ICoreWebView2AcceleratorKeyPressedEventHandler.md)
*   [ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](0-9-430/ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md)
*   [ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](0-9-430/ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md)
*   [ICoreWebView2CapturePreviewCompletedHandler](0-9-430/ICoreWebView2CapturePreviewCompletedHandler.md)
*   [ICoreWebView2ContainsFullScreenElementChangedEventHandler](0-9-430/ICoreWebView2ContainsFullScreenElementChangedEventHandler.md)
*   [ICoreWebView2ContentLoadingEventHandler](0-9-430/ICoreWebView2ContentLoadingEventHandler.md)
*   [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](0-9-430/ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler.md)
*   [ICoreWebView2CreateCoreWebView2HostCompletedHandler](0-9-430/ICoreWebView2CreateCoreWebView2HostCompletedHandler.md)
*   [ICoreWebView2DevToolsProtocolEventReceivedEventHandler](0-9-430/ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md)
*   [ICoreWebView2DocumentTitleChangedEventHandler](0-9-430/ICoreWebView2DocumentTitleChangedEventHandler.md)
*   [ICoreWebView2ExecuteScriptCompletedHandler](0-9-430/ICoreWebView2ExecuteScriptCompletedHandler.md)
*   [ICoreWebView2FocusChangedEventHandler](0-9-430/ICoreWebView2FocusChangedEventHandler.md)
*   [ICoreWebView2HistoryChangedEventHandler](0-9-430/ICoreWebView2HistoryChangedEventHandler.md)
*   [ICoreWebView2MoveFocusRequestedEventHandler](0-9-430/ICoreWebView2MoveFocusRequestedEventHandler.md)
*   [ICoreWebView2NavigationCompletedEventHandler](0-9-430/ICoreWebView2NavigationCompletedEventHandler.md)
*   [ICoreWebView2NavigationStartingEventHandler](0-9-430/ICoreWebView2NavigationStartingEventHandler.md)
*   [ICoreWebView2NewBrowserVersionAvailableEventHandler](0-9-430/ICoreWebView2NewBrowserVersionAvailableEventHandler.md)
*   [ICoreWebView2NewWindowRequestedEventHandler](0-9-430/ICoreWebView2NewWindowRequestedEventHandler.md)
*   [ICoreWebView2PermissionRequestedEventHandler](0-9-430/ICoreWebView2PermissionRequestedEventHandler.md)
*   [ICoreWebView2ProcessFailedEventHandler](0-9-430/ICoreWebView2ProcessFailedEventHandler.md)
*   [ICoreWebView2ScriptDialogOpeningEventHandler](0-9-430/ICoreWebView2ScriptDialogOpeningEventHandler.md)
*   [ICoreWebView2SourceChangedEventHandler](0-9-430/ICoreWebView2SourceChangedEventHandler.md)
*   [ICoreWebView2WebMessageReceivedEventHandler](0-9-430/ICoreWebView2WebMessageReceivedEventHandler.md)
*   [ICoreWebView2WebResourceRequestedEventHandler](0-9-430/ICoreWebView2WebResourceRequestedEventHandler.md)
*   [ICoreWebView2WindowCloseRequestedEventHandler](0-9-430/ICoreWebView2WindowCloseRequestedEventHandler.md)
*   [ICoreWebView2ZoomFactorChangedEventHandler](0-9-430/ICoreWebView2ZoomFactorChangedEventHandler.md)
