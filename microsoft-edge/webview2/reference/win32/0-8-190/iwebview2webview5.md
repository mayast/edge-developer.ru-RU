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
ms.openlocfilehash: 3c32cd59e75eb81bf69661d01f6044a0628ba35d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654613"
---
# интерфейс IWebView2WebView5 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

Дополнительные функции, реализованные основным объектом WebView.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Уведомляет об изменении свойства ContainsFullScreenElement.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Указывает, содержит ли WebView элемент HTML на весь экран.
[add_WebResourceRequested](#add_webresourcerequested) | Добавьте обработчик событий для события WebResourceRequested.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.

Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md). Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .

## Участников

#### add_ContainsFullScreenElementChanged 

Уведомляет об изменении свойства ContainsFullScreenElement.

> общедоступные значения HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Это означает, что HTML-элемент, находящиеся внутри WebView, помещается на размер WebView или выходит за экран. Это событие полезно, если, например, элемент видео запрашивается на весь экран. Прослушиватель ContainsFullScreenElementChanged может затем изменить размер WebView в ответе.

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<IWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](IWebView2WebView5* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_ContainsFullScreenElementChanged 

Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.

> общедоступные значения HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(маркер EventRegistrationToken)

#### get_ContainsFullScreenElement 

Указывает, содержит ли WebView элемент HTML на весь экран.

> общедоступные значения HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool * ContainsFullScreenElement)

#### add_WebResourceRequested 

Добавьте обработчик событий для события WebResourceRequested.

> общедоступные значения HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Активируется, когда WebView выполняет запрос HTTP к соответствующему URL-адресу и фильтру контекста ресурсов, добавленному с помощью AddWebResourceRequestedFilter. Для срабатывания события необходимо добавить хотя бы один фильтр.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### AddWebResourceRequestedFilter 

Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.

> общедоступный HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const разделе ResourceContext)

Параметр URI может быть строкой с подстановочными знаками ("": ноль или больше; "?": только один). nullptr эквивалентен L "". Описание фильтров контекста ресурсов приведено в разделе WEBVIEW2_WEB_RESOURCE_CONTEXT перечисление.

#### RemoveWebResourceRequestedFilter 

Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.

> общедоступный HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const разделе ResourceContext)

Если один и тот же фильтр был добавлен несколько значений, его необходимо будет удалить столько, сколько вхождений было добавлено для эффективного. Возвращает E_INVALIDARG для фильтра, который еще не был добавлен.

