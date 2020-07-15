---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 149a37dd2781b27522ec01b46a10efce943c71c8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881111"
---
# 0.9.430-Interface ICoreWebView2Environment 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface ICoreWebView2Environment
  : public IUnknown
```

Представляет среду WebView2.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[CreateCoreWebView2Host](#createcorewebview2host) | Асинхронно создайте новый WebView.
[CreateWebResourceResponse](#createwebresourceresponse) | Создание нового объекта ответа на веб-ресурс.
[get_BrowserVersionInfo](#get_browserversioninfo) | Сведения о версии браузера для текущего [ICoreWebView2Environment](), включая имя канала, если он не является стабильным каналом.
[add_NewBrowserVersionAvailable](#add_newbrowserversionavailable) | Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.
[remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable) | Удалите обработчик событий, добавленный ранее add_NewBrowserVersionAvailable.

Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде. Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.

## Участников

#### CreateCoreWebView2Host 

Асинхронно создайте новый WebView.

> общедоступные значения HRESULT [CreateCoreWebView2Host](#createcorewebview2host)(HWND ParentWindow,[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) * обработчик)

parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные. WebView добавит дочернее окно в заданное окно во время создания WebView. Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.

Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен. Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow. 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateCoreWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
        Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
            this, &AppWindow::OnCreateEnvironmentCompleted)
            .Get());
    if (!SUCCEEDED(hr))
    {
        if (hr == HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND))
        {
            MessageBox(
                m_mainWindow,
                L"Couldn't find Edge installation. "
                "Do you have a version installed that's compatible with this "
                "WebView2 SDK version?",
                nullptr, MB_OK);
        }
        else
        {
            ShowFailure(hr, L"Failed to create webview environment");
        }
    }
}

// This is the callback passed to CreateWebViewEnvironmnetWithDetails.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Host(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2HostCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2HostCompleted)
                              .Get()));
    return S_OK;
}
```

 Рекомендуется, чтобы приложение обрабатывало сообщения диспетчера перезапуска, чтобы его можно было перезапустить надлежащим образом в случае, когда приложение использует Edge для WebView с определенной установкой и удаляется установка. Например, если пользователь устанавливает ребро с канала разработки и использует ребро с этого канала для тестирования приложения, а затем удаляет Edge из него, не закрывая приложение, приложение будет перезапущена, чтобы разрешить удаление канала разработки для успешного выполнения. 

```cpp
    case WM_QUERYENDSESSION:
    {
        // yes, we can shut down
        // Register how we might be restarted
        RegisterApplicationRestart(L"--restore", RESTART_NO_CRASH | RESTART_NO_HANG);
        *result = TRUE;
        return true;
    }
    break;
    case WM_ENDSESSION:
    {
        if (wParam == TRUE)
        {
            // save app state and exit.
            PostQuitMessage(0);
            return true;
        }
    }
    break;
```

#### CreateWebResourceResponse 

Создание нового объекта ответа на веб-ресурс.

> общедоступные значения HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream * Content, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR Headers,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) * * Response)

Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки. Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) для создания заголовков построчно. Сведения о других параметрах смотрите в [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
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

#### get_BrowserVersionInfo 

Сведения о версии браузера для текущего [ICoreWebView2Environment](), включая имя канала, если он не является стабильным каналом.

> общедоступные значения HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR * versionInfo)

Это соответствует формату API GetCoreWebView2BrowserVersionInfo. Названия каналов: "бета-версия", "Dev" и "Канарские".

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### add_NewBrowserVersionAvailable 

Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.

> общедоступные значения HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](ICoreWebView2NewBrowserVersionAvailableEventHandler.md) * eventHandler, EventRegistrationToken * token)

Для использования более новой версии браузера необходимо создать новую среду и WebView. Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код. Если вы не используете установленный EDGE, событие не срабатывает.

Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера. Или просто запросите пользователя перезапустить приложение.

```cpp
    // After the environment is successfully created,
    // register a handler for the NewBrowserVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewBrowserVersionAvailable(
        Callback<ICoreWebView2NewBrowserVersionAvailableEventHandler>(
            [this](
                ICoreWebView2Environment* sender,
                ICoreWebView2NewBrowserVersionAvailableEventArgs* args) -> HRESULT {
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

#### remove_NewBrowserVersionAvailable 

Удалите обработчик событий, добавленный ранее add_NewBrowserVersionAvailable.

> общедоступные значения HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(маркер EventRegistrationToken)

