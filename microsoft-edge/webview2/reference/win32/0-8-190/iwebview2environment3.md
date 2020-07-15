---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: d16a12aae823c48b7dd4b0b5e8225cdd40c1dafc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878528"
---
# 0.8.355-Interface IWebView2Environment3 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

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

