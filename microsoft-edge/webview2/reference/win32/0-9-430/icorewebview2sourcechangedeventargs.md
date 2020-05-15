---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 69c569be7e712d0f5cfddbaa180419be8d475ad0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655005"
---
# интерфейс ICoreWebView2SourceChangedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

Аргументы события для события SourceChanged.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | Значение true, если страница, на которую осуществляется переход, является новым документом.

## Участников

#### get_IsNewDocument 

Значение true, если страница, на которую осуществляется переход, является новым документом.

> общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool * IsNewDocument)

