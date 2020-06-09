---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 56f2e59b8f7c19f130bba1e579fac28e4536dd90
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699295"
---
# интерфейс ICoreWebView2ExperimentalEnvironment 

> [!NOTE]
> Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.

```
interface ICoreWebView2ExperimentalEnvironment
  : public IUnknown
```

Этот интерфейс является расширением [ICoreWebView2Environment](icorewebview2environment.md).

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller) | Асинхронно создайте новый WebView для использования с визуальным размещением.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Создание пустого [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).
[GetProviderForHwnd](#getproviderforhwnd) | Возвращает поставщик модели автоматизации пользовательского интерфейса для ICoreWebView2CompositionController, соответствующего данному дескриптору HWND.

Объект, реализующий интерфейс [ICoreWebView2ExperimentalEnvironment]() , также будет реализовывать [ICoreWebView2Environment](icorewebview2environment.md).

## Участников

#### CreateCoreWebView2CompositionController 

Асинхронно создайте новый WebView для использования с визуальным размещением.

> общедоступные значения HRESULT [CreateCoreWebView2CompositionController](#createcorewebview2compositioncontroller)(HWND ParentWindow, [ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler](icorewebview2experimentalcreatecorewebview2compositioncontrollercompletedhandler.md) * обработчик)

parentWindow — это HWND, в котором приложение будет подключаться к визуальному дереву WebView. Это HWND того, что приложение получит ввод указателя или мыши, предназначенное для WebView (и для пересылки потребуется функция SendMouseInput/SendPointerInput). Если приложение перемещает визуальное дерево WebView в другое окно, ему нужно вызвать put_ParentWindow, чтобы обновить новый родительский дескриптор HWND визуального дерева.

Используйте put_RootVisualTarget в созданном CoreWebView2CompositionController, чтобы предоставить визуальное приложение для размещения визуального дерева браузера.

Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен. Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow. 
```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView()
{
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();
    m_dcompDevice = nullptr;
    m_wincompHelper = nullptr;
    LPCWSTR subFolder = nullptr;

    if (m_creationModeId == IDM_CREATION_MODE_VISUAL_DCOMP)
    {
        HRESULT hr = DCompositionCreateDevice2(nullptr, IID_PPV_ARGS(&m_dcompDevice));
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using DComp Visual is not supported.\r\n"
                "DComp device creation failed.\r\n"
                "Current OS may not support DComp.",
                L"Create with Windowless DComp Visual Failed", MB_OK);
            return;
        }
    }
    else if (m_creationModeId == IDM_CREATION_MODE_VISUAL_WINCOMP)
    {
        HRESULT hr = CreateWinCompCompositor();
        if (!SUCCEEDED(hr))
        {
            MessageBox(
                m_mainWindow,
                L"Attempting to create WebView using WinComp Visual is not supported.\r\n"
                "WinComp compositor creation failed.\r\n"
                "Current OS may not support WinComp.",
                L"Create with Windowless WinComp Visual Failed", MB_OK);
            return;
        }
    }
    auto options = Microsoft::WRL::Make<CoreWebView2EnvironmentOptions>();
    if(!m_language.empty())
        CHECK_FAILURE(options->put_Language(m_language.c_str()));
    HRESULT hr = CreateCoreWebView2EnvironmentWithOptions(
        subFolder, nullptr, options.Get(),
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
// This is the callback passed to CreateWebViewEnvironmentWithOptions.
// Here we simply create the WebView.
HRESULT AppWindow::OnCreateEnvironmentCompleted(
    HRESULT result, ICoreWebView2Environment* environment)
{
    CHECK_FAILURE(result);
    m_webViewEnvironment = environment;

    auto webViewExperimentalEnvironment =
        m_webViewEnvironment.try_query<ICoreWebView2ExperimentalEnvironment>();
    if (webViewExperimentalEnvironment && (m_dcompDevice || m_wincompHelper))
    {
        CHECK_FAILURE(webViewExperimentalEnvironment->CreateCoreWebView2CompositionController(
            m_mainWindow,
            Callback<
                ICoreWebView2ExperimentalCreateCoreWebView2CompositionControllerCompletedHandler>(
                [this](
                    HRESULT result,
                    ICoreWebView2ExperimentalCompositionController* compositionController) -> HRESULT {
                    auto controller =
                        wil::com_ptr<ICoreWebView2ExperimentalCompositionController>(compositionController)
                            .query<ICoreWebView2Controller>();
                    return OnCreateCoreWebView2ControllerCompleted(result, controller.get());
                })
                .Get()));
    }
    else
    {
        CHECK_FAILURE(m_webViewEnvironment->CreateCoreWebView2Controller(
            m_mainWindow, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                              this, &AppWindow::OnCreateCoreWebView2ControllerCompleted)
                              .Get()));
    }

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

#### CreateCoreWebView2PointerInfo 

Создание пустого [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).

> общедоступные значения HRESULT [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)([ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * * pointerInfo)

Возвращенные [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) должны быть заполнены всеми соответствующими сведениями перед вызовом SendPointerInput.

#### GetProviderForHwnd 

Возвращает поставщик модели автоматизации пользовательского интерфейса для ICoreWebView2CompositionController, соответствующего данному дескриптору HWND.

> общедоступные значения HRESULT [GetProviderForHwnd](#getproviderforhwnd)(HWND HWND * Provider)

