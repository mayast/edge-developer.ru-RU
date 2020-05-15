---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 59557ca86e8b044fb937fe93b3060c0879abb6f1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654949"
---
# интерфейс ICoreWebView2WebResourceRequestedEventArgs 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Аргументы события для события WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Request](#get_request) | HTTP-запрос.
[get_Response](#get_response) | Ответ HTTP.
[put_Response](#put_response) | Задайте свойство Response (ответ).
[GetDeferral](#getdeferral) | Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.
[get_ResourceContext](#get_resourcecontext) | Контексты запросов веб-ресурсов.

## Участников

#### get_Request 

HTTP-запрос.

> общедоступные значения HRESULT [get_Request](#get_request)(запрос[ICoreWebView2WebResourceRequest](ICoreWebView2WebResourceRequest.md) * *)

#### get_Response 

Ответ HTTP.

> общедоступные значения HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) * * Response)

#### put_Response 

Задайте свойство Response (ответ).

> общедоступные значения HRESULT [put_Response](#put_response)(ответ[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) *)

#### GetDeferral 

Получите объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) и помещайте событие в отложенное состояние.

> общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) * * РБП)

Вы можете использовать объект [ICoreWebView2Deferral](ICoreWebView2Deferral.md) для выполнения сетевого запроса позже.

#### get_ResourceContext 

Контексты запросов веб-ресурсов.

> общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT * контекст)

