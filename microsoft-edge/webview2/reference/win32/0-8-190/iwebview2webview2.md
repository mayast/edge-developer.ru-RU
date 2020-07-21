---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 64dac6c56576b618cbdc84da2c8fcbcd0e41028f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884738"
---
# 0.8.355-Interface IWebView2WebView2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView2
  : public IUnknown
```

Дополнительные функции, реализованные основным объектом WebView.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Stop](#stop) | Остановите все переходы и ожидающие выборки ресурсов.

Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md). Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .

## Участников

#### Stop 

Остановите все переходы и ожидающие выборки ресурсов.

> открытая [Остановка](#stop)HRESULT ()

