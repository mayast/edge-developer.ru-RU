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
ms.openlocfilehash: 436e0e33180c65afcce0487fffeff5f168dceab7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654618"
---
# интерфейс IWebView2WebView3 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2WebView3
  : public IWebView2WebView
```

Дополнительные функции, реализованные основным объектом WebView.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Stop](#stop) | Остановите все переходы и ожидающие выборки ресурсов.
[add_NewWindowRequested](#add_newwindowrequested) | Добавьте обработчик событий для события NewWindowRequested.
[remove_NewWindowRequested](#remove_newwindowrequested) | Удалите обработчик событий, добавленный ранее add_NewWindowRequested.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Добавьте обработчик событий для события DocumentTitleChanged.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.
[get_DocumentTitle](#get_documenttitle) | Название текущего документа верхнего уровня.

Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md). Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .

## Участников

#### Stop 

Остановите все переходы и ожидающие выборки ресурсов.

> открытая [Остановка](#stop)HRESULT ()

#### add_NewWindowRequested 

Добавьте обработчик событий для события NewWindowRequested.

> общедоступные значения HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Вызывается, когда содержимое в WebView запросило открыть новое окно, например с помощью Window. Open. Приложение может передавать целевую WebView, которая будет считаться открытым окном.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<IWebView2NewWindowRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<IWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewWindowRequested 

Удалите обработчик событий, добавленный ранее add_NewWindowRequested.

> общедоступные значения HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(маркер EventRegistrationToken)

#### add_DocumentTitleChanged 

Добавьте обработчик событий для события DocumentTitleChanged.

> общедоступные значения HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Событие активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<IWebView2DocumentTitleChangedEventHandler>(
            [this](IWebView2WebView3* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### remove_DocumentTitleChanged 

Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.

> общедоступные значения HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(маркер EventRegistrationToken)

#### get_DocumentTitle 

Название текущего документа верхнего уровня.

> общедоступные значения HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR * Title)

Если документ не имеет явного заголовка или не является пустым, используется значение по умолчанию, которое может быть или не совпадать с URI документа.

