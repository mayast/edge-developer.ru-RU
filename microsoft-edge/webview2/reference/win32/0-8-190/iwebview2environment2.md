---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: e3177f159ff397ee9d4781936aa32f2715d4af02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886089"
---
# 0.8.355-Interface IWebView2Environment2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment2
  : public IWebView2Environment
```

Дополнительные функции, реализованные с помощью объекта Environment.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_BrowserVersionInfo](#get_browserversioninfo) | Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md), включая имя канала, если он не является стабильным каналом.

Дополнительные сведения вы видите в интерфейсе [IWebView2Environment](IWebView2Environment.md) . Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2Environment](IWebView2Environment.md).

## Участников

#### get_BrowserVersionInfo 

Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md), включая имя канала, если он не является стабильным каналом.

> общедоступные значения HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR * versionInfo)

Это соответствует формату API GetWebView2BrowserVersionInfo. Названия каналов: "бета-версия", "Dev" и "Канарские".

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

