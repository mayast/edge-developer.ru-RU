---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 547e9a451283de55658a95a8134ecb8a838f9e50
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011407"
---
# 0.9.579-Interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

Аргументы события для события WebResourceResponseReceived.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Request](#get_request) | Объект запроса веб-ресурса. Все изменения, внесенные в этот объект, будут игнорироваться.
[get_Response](#get_response) | Объект ответа на веб-ресурс.
[PopulateResponseContent](#populateresponsecontent) | Метод Async для запроса потока содержимого ответа.

Будет содержать запрос, отправленный по мере его отправки, и ответ, полученный от него. Примечание. чтобы получить поток содержимого ответа, сначала вызовите PopulateResponseContent и дождитесь завершения асинхронного вызова, в противном случае возвращаемый объект потока содержимого будет иметь значение null.

## Участников

#### get_Request 

Объект запроса веб-ресурса. Все изменения, внесенные в этот объект, будут игнорироваться.

> общедоступные значения HRESULT [get_Request](#get_request)(запрос ICoreWebView2WebResourceRequest * *)

#### get_Response 

Объект ответа на веб-ресурс.

> общедоступные значения HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse * * Response)

Все изменения, внесенные в этот объект, будут игнорироваться.

#### PopulateResponseContent 

Метод Async для запроса потока содержимого ответа.

> общедоступные значения HRESULT [PopulateResponseContent](#populateresponsecontent)(обработчик[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) *)

```cpp
                    args->PopulateResponseContent(
                        Callback<
                            ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler>(
                            [this, webResourceRequest, webResourceResponse](HRESULT result) {
                                std::wstring message =
                                    L"{ \"kind\": \"event\", \"name\": "
                                    L"\"WebResourceResponseReceived\", \"args\": {"
                                    L"\"request\": " +
                                    RequestToJsonString(webResourceRequest.get()) +
                                    L", "
                                    L"\"response\": " +
                                    ResponseToJsonString(webResourceResponse.get()) + L"}";

                                message +=
                                    WebViewPropertiesToJsonString(m_webviewEventSource.get());
                                message += L"}";
                                PostEventMessage(message);
                                return S_OK;
                            })
                            .Get());
```

