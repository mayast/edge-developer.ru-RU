---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 327a182c5298ed6de6b9e55b407d138857dbe659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886096"
---
# 0.8.355-Interface IWebView2Environment3 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

Дополнительные функции, реализованные с помощью объекта Environment.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[add_NewVersionAvailable](#add_newversionavailable) | Событие NewVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.
[remove_NewVersionAvailable](#remove_newversionavailable) | Удалите обработчик событий, добавленный ранее add_NewVersionAvailable.

Дополнительные сведения вы видите в интерфейсе [IWebView2Environment](IWebView2Environment.md) . Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2Environment](IWebView2Environment.md).

## Участников

#### add_NewVersionAvailable 

Событие NewVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.

> общедоступные значения HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) * eventHandler, EventRegistrationToken * token)

Для использования более новой версии браузера необходимо создать новый [IWebView2Environment](IWebView2Environment.md) и [IWebView2WebView](IWebView2WebView.md). Событие будет инициировано только для новой версии из того же канала, из которого выполняется код. Если вы не используете установленный EDGE, событие не срабатывает.

Поскольку папка данных пользователя может использоваться только одним процессом браузера, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть [IWebView2Environment](IWebView2Environment.md) и IWebView2WebViews, которые используют более старую версию браузера. Или просто запросите пользователя перезапустить приложение.

```cpp
    // After the environment is successfully created,
    // register a handler for the NewVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewVersionAvailable(
        Callback<IWebView2NewVersionAvailableEventHandler>(
            [this](IWebView2Environment* sender, IWebView2NewVersionAvailableEventArgs* args)
                -> HRESULT {
                // Get the version value from args
                wil::unique_cotaskmem_string newVersion;
                CHECK_FAILURE(args->get_NewVersion(&newVersion));
                std::wstring message = L"We detected there is a new version for the browser.";
                message += L"\n\nVersion number: ";
                message += newVersion.get();
                message += L"\n\n";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewVersionAvailable 

Удалите обработчик событий, добавленный ранее add_NewVersionAvailable.

> общедоступные значения HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(маркер EventRegistrationToken)

