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
ms.openlocfilehash: 00b19d1174a5d5ac643a04038ecdd60c82211194
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654874"
---
# интерфейс IWebView2Environment2 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

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

