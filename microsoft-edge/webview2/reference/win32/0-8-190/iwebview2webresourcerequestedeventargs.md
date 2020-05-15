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
ms.openlocfilehash: 899a6f50db1d77f3f24524c5ccec139dcbdbcaf9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654685"
---
# интерфейс IWebView2WebResourceRequestedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Аргументы события для события WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Request](#get_request) | HTTP-запрос.
[get_Response](#get_response) | Ответ HTTP.
[put_Response](#put_response) | Задайте свойство Response (ответ).
[GetDeferral](#getdeferral) | Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.

## Участников

#### get_Request 

HTTP-запрос.

> общедоступные значения HRESULT [get_Request](#get_request)(запрос[IWebView2WebResourceRequest](IWebView2WebResourceRequest.md) * *)

#### get_Response 

Ответ HTTP.

> общедоступные значения HRESULT [get_Response](#get_response)([IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) * * Response)

#### put_Response 

Задайте свойство Response (ответ).

> общедоступные значения HRESULT [put_Response](#put_response)(ответ[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) *)

#### GetDeferral 

Получите объект [IWebView2Deferral](IWebView2Deferral.md) и помещайте событие в отложенное состояние.

> общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) * * РБП)

Вы можете использовать объект [IWebView2Deferral](IWebView2Deferral.md) для выполнения сетевого запроса позже.

