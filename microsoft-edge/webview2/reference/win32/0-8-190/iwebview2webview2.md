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
ms.openlocfilehash: 62daeaab702b431f787bc800ab79664fc183c4ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654614"
---
# интерфейс IWebView2WebView2 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

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

