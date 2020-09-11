---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Experimental
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2Experimental
ms.openlocfilehash: 44795ab425e814054dd3d58cba585f1badfbf431
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012510"
---
# интерфейс ICoreWebView2Experimental 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2Experimental
  : public IUnknown
```

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[add_WebResourceResponseReceived](#add_webresourceresponsereceived) | Добавьте обработчик событий для события WebResourceResponseReceived.
[remove_WebResourceResponseReceived](#remove_webresourceresponsereceived) | Удаляет обработчик событий WebResourceResponseReceived, добавленный ранее add_WebResourceResponseReceived.

## Участников

#### add_WebResourceResponseReceived 

Добавьте обработчик событий для события WebResourceResponseReceived.

> общедоступные значения HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) * eventHandler, EventRegistrationToken * token)

Событие WebResourceResponseReceived срабатывает после того, как WebView получил и обработал ответ для запроса на веб-ресурс. Аргументы события включают в себя WebResourceRequest, отправленный по каналу и WebResourceResponse, включая все дополнительные заголовки, добавленные сетевым стеком, которые не были включены как часть связанного события WebResourceRequested, например заголовки проверки подлинности. 
```cpp
    wil::com_ptr<ICoreWebView2Experimental> webviewExperimental;
    CHECK_FAILURE(m_appWindow->GetWebView()->QueryInterface(IID_PPV_ARGS(&webviewExperimental)));
    CHECK_FAILURE(webviewExperimental->add_WebResourceResponseReceived(
        Callback<ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler>(
            [this](
                ICoreWebView2Experimental* sender,
                ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs* args) {           
                wil::com_ptr<ICoreWebView2WebResourceRequest> request;
                CHECK_FAILURE(args->get_Request(&request));
                wil::unique_cotaskmem_string uri;
                CHECK_FAILURE(request->get_Uri(&uri));
                if (wcscmp(uri.get(), L"https://authenticationtest.com/HTTPAuth/") == 0)
                {
                    wil::com_ptr<ICoreWebView2HttpRequestHeaders> requestHeaders;
                    CHECK_FAILURE(request->get_Headers(&requestHeaders));

                    wil::unique_cotaskmem_string authHeaderValue;
                    if (requestHeaders->GetHeader(L"Authorization", &authHeaderValue) == S_OK)
                    {
                        std::wstring message(L"Authorization: ");
                        message += authHeaderValue.get();
                        MessageBox(nullptr, message.c_str(), nullptr, MB_OK);
                        m_appWindow->DeleteComponent(this);
                    }
                }
                
                return S_OK;
            })
            .Get(),
        &m_webResourceResponseReceivedToken));
```

#### remove_WebResourceResponseReceived 

Удаляет обработчик событий WebResourceResponseReceived, добавленный ранее add_WebResourceResponseReceived.

> общедоступные значения HRESULT [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)(маркер EventRegistrationToken)

