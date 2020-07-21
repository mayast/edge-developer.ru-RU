---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 75741c1ba1d835d1c26c7d1db0845071216e0705
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886124"
---
# 0.8.355-Interface IWebView2DocumentStateChangedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

Аргументы события для события DocumentStateChanged.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_IsNewDocument](#get_isnewdocument) | Значение true, если страница, на которую осуществляется переход, является новым документом.
[get_IsErrorPage](#get_iserrorpage) | Значение true, если загруженное содержимое является страницей ошибки.

## Участников

#### get_IsNewDocument 

Значение true, если страница, на которую осуществляется переход, является новым документом.

> общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool * IsNewDocument)

#### get_IsErrorPage 

Значение true, если загруженное содержимое является страницей ошибки.

> общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool * IsErrorPage)

