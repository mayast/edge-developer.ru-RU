---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9a98e2afa5b15452d7521183abebc019d51e3a3c
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885459"
---
# 0.9.515-Interface ICoreWebView2SourceChangedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

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

