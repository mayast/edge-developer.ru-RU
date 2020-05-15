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
ms.openlocfilehash: cf321ff1091883827b7ce6cda7248a06f1128867
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654868"
---
# интерфейс IWebView2DevToolsProtocolEventReceivedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

Аргументы события для события DevToolsProtocolEventReceived.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_ParameterObjectAsJson](#get_parameterobjectasjson) | Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.

## Участников

#### get_ParameterObjectAsJson 

Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.

> общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR * ParameterObjectAsJson)

