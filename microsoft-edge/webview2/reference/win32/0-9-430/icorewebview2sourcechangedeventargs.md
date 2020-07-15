---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8a9f1b1e44353796c6d3b57d3f4c6f3d4997aad5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880201"
---
# 0.9.430-Interface ICoreWebView2SourceChangedEventArgs 

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

