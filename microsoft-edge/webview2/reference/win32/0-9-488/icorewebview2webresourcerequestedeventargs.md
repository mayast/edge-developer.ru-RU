---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 70a7d997dfd89b6d9bb8eb8af9a87ff0a130b69f
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880306"
---
# 0.9.515-Interface ICoreWebView2WebResourceRequestedEventArgs 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Аргументы события для события WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Request](#get_request) | HTTP-запрос.
[get_ResourceContext](#get_resourcecontext) | Контексты запросов веб-ресурсов.
[get_Response](#get_response) | Ответ HTTP.
[GetDeferral](#getdeferral) | Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.
[put_Response](#put_response) | Задайте свойство Response (ответ).

## Участников

#### get_Request 

HTTP-запрос.

> общедоступные значения HRESULT [get_Request](#get_request)(запрос[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) * *)

#### get_ResourceContext 

Контексты запросов веб-ресурсов.

> общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT * контекст)

#### get_Response 

Ответ HTTP.

> общедоступные значения HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * Response)

#### GetDeferral 

Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.

> общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * РБП)

Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) для выполнения сетевого запроса позже.

#### put_Response 

Задайте свойство Response (ответ).

> общедоступные значения HRESULT [put_Response](#put_response)(ответ[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) *)

