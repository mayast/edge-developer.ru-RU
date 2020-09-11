---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebResourceRequestedEventArgs
ms.openlocfilehash: 14b88f83e9635c94e205df05f6764e059f0def78
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012417"
---
# интерфейс ICoreWebView2WebResourceRequestedEventArgs 

```
interface ICoreWebView2WebResourceRequestedEventArgs
  : public IUnknown
```

Аргументы события для события WebResourceRequested.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Запрос на веб-ресурс.
[get_ResourceContext](#get_resourcecontext) | Контекст запроса веб-ресурса.
[get_Response](#get_response) | Заполнитель для объекта ответа на веб-ресурс.
[GetDeferral](#getdeferral) | Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.
[put_Response](#put_response) | Задайте свойство Response (ответ).

## Участников

#### get_Request 

Запрос на веб-ресурс.

> общедоступные значения HRESULT [get_Request](#get_request)(запрос[ICoreWebView2WebResourceRequest](icorewebview2webresourcerequest.md) * *)

Возможно, в объекте Request отсутствует часть заголовков, добавленных в разделе "сетевой стек".

#### get_ResourceContext 

Контекст запроса веб-ресурса.

> общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(COREWEBVIEW2_WEB_RESOURCE_CONTEXT * контекст)

#### get_Response 

Заполнитель для объекта ответа на веб-ресурс.

> общедоступные значения HRESULT [get_Response](#get_response)([ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) * * Response)

Если этот объект задан, запрос на веб-ресурс будет выполнен с этим ответом.

#### GetDeferral 

Получите объект [ICoreWebView2Deferral](icorewebview2deferral.md) и помещайте событие в отложенное состояние.

> общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) * * РБП)

Вы можете использовать объект [ICoreWebView2Deferral](icorewebview2deferral.md) , чтобы выполнить запрос позже.

#### put_Response 

Задайте свойство Response (ответ).

> общедоступные значения HRESULT [put_Response](#put_response)(ответ[ICoreWebView2WebResourceResponse](icorewebview2webresourceresponse.md) *)

Пустой объект ответа на веб-ресурс можно создать с помощью CreateWebResourceResponse и затем изменить для создания ответа.

