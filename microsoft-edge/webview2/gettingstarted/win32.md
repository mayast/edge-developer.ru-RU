---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f62fa25dab7ee1e89f268e4b77a9c0612cac665f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655035"
---
# Начало работы с WebView2 (Предварительная версия для разработчиков)

В этом пошаговом руководстве рассматриваются часто используемые функции [WebView2 (Предварительная версия для разработчиков)](https://aka.ms/webview) и начинается создание первого приложения WebView2. Дополнительные сведения об отдельных API можно найти в [справочнике по API](../reference/win32/0-9-488-reference-webview2.md) .  

## Предварительные условия

* [Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download/) , установленный в поддерживаемой ОС (в настоящее время Windows 10, Windows 8,1 и Windows 7). **Рекомендуем использовать канал Канарские и минимальную требуемую версию — 82.0.488.0**.
* [Visual Studio](https://visualstudio.microsoft.com/) 2015 или более поздней версии с установленной поддержкой C++.

## Шаг 1: создание одного окна приложение Win32

Начнем с базового проекта для настольных компьютеров, который содержит одно главное окно. Так как это не основное фокусирование на этом пошаговом руководстве, мы просто используем модифицированный образец кода из [пошагового руководства: создание традиционного классического приложения для Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019). [Загрузите](https://aka.ms/HelloWebView) модифицированный пример, чтобы приступить к работе.

Откройте **WebView2GettingStarted. sln** в Visual Studio. Если вы используете более старую версию Visual Studio, щелкните правой кнопкой мыши проект **WebView2GettingStarted** и выберите пункт **свойства**. В разделе **Свойства конфигурации**  >  **Общие**измените **версию пакета SDK для Windows** и **набор инструментов платформы** , чтобы использовать набор инструментов Win10 SDK и VS.

![версия средства](../media/tool-version.png)

Visual Studio может показывать некоторые ошибки из-за отсутствующего файла заголовка WebView2, который должен выйти после завершения действия 2.

## Шаг 2. Установка WebView2 SDK

Теперь добавим пакет SDK WebView2 в проект. Для предварительного просмотра разработчик может установить пакет SDK Win32 с помощью NuGet.

1. Щелкните проект правой кнопкой мыши и выберите пункт **Управление пакетами NuGet**.

    ![Manage-NuGet-Packages](../media/manage-nuget-packages.png)

2. Введите **Microsoft. Windows. ImplementationLibrary** в строке поиска, выберите **Microsoft. Windows. ImplementationLibrary** из результатов и щелкните **установить** в правой части окна и установите последнюю версию SDK. NuGet загрузит пакет SDK на ваш компьютер. Несмотря на то, что мы используем [библиотеку реализации Windows](https://github.com/Microsoft/wil) и [библиотеку шаблонов среды выполнения Windows](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) для упрощения работы с COM в этом пошаговом руководстве, они являются полностью необязательными.

    ![будет](../media/wil.png)

3. Введите **Microsoft. Web. WebView2** на панели поиска, выберите **Microsoft. Web. WebView2** из результатов и щелкните **установить** в правой части окна и установите последнюю версию SDK. NuGet загрузит пакет SDK на ваш компьютер.

    ![NuGet](../media/nuget.png)

4. Включите заголовок WebView2. В **HelloWebView. cpp**добавьте `#include "WebView2.h"` под строками `#include` s.

    ```cpp
    ...
    #include <wrl.h>
    #include <wil/com.h>
    // include WebView2 header
    #include "WebView2.h"
    ```

Все готово для использования и сборки в API WebView2. Нажмите клавишу F5 для создания и запуска примера приложения. Должно отобразиться приложение, в котором отображается пустое окно.

![Пустое приложение](../media/empty-app.png)

## Шаг 3: создание единого WebView в родительском окне

Теперь добавим WebView в главное окно. Мы будем использовать `CreateCoreWebView2Environment` для настройки среды и поиска в браузере Microsoft EDGE (Chromium) элемента управления Powering. Вы также можете использовать `CreateCoreWebView2EnvironmentWithOptions` этот параметр, если вы хотите указать расположение браузера, папку пользователя, флаги браузера и т. д., вместо использования параметра по умолчанию. После завершения вы сможете `CreateCoreWebView2Environment` позвонить `ICoreWebView2Environment::CreateCoreWebView2Controller` внутри `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` обратного вызова и вызов `ICoreWebView2Controller::get_CoreWebView2` для получения связанного WebView.

В обратном вызове также можно задать несколько параметров, изменить размер WebView, чтобы получить 100% родительского окна, и перейти к Bing.

Скопируйте приведенный ниже код в **HelloWebView. cpp** между `// <-- WebView2 sample code starts here -->` and `// <-- WebView2 sample code ends here -->` .

```cpp
// Step 3 - Create a single WebView within the parent window
// Locate the browser and set up the environment for WebView
CreateCoreWebView2EnvironmentWithOptions(nullptr, nullptr, nullptr,
    Callback<ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler>(
        [hWnd](HRESULT result, ICoreWebView2Environment* env) -> HRESULT {

            // Create a CoreWebView2Controller and get the associated CoreWebView2 whose parent is the main window hWnd
            env->CreateCoreWebView2Controller(hWnd, Callback<ICoreWebView2CreateCoreWebView2ControllerCompletedHandler>(
                [hWnd](HRESULT result, ICoreWebView2Controller* controller) -> HRESULT {
                if (controller != nullptr) {
                    webviewController = controller;
                    webviewController->get_CoreWebView2(&webviewWindow);
                }

                // Add a few settings for the webview
                // this is a redundant demo step as they are the default settings values
                ICoreWebView2Settings* Settings;
                webviewWindow->get_Settings(&Settings);
                Settings->put_IsScriptEnabled(TRUE);
                Settings->put_AreDefaultScriptDialogsEnabled(TRUE);
                Settings->put_IsWebMessageEnabled(TRUE);

                // Resize WebView to fit the bounds of the parent window
                RECT bounds;
                GetClientRect(hWnd, &bounds);
                webviewController->put_Bounds(bounds);

                // Schedule an async task to navigate to Bing
                webviewWindow->Navigate(L"https://www.bing.com/");

                // Step 4 - Navigation events


                // Step 5 - Scripting


                // Step 6 - Communication between host and web content


                return S_OK;
            }).Get());
        return S_OK;
    }).Get());
```

Чтобы выполнить сборку и запустить приложение, нажмите клавишу F5. Теперь у вас есть окно WebView, в котором отображается Bing.

![Bing-окно](../media/bing-window.png)

## Шаг 4 — события навигации

Мы уже посмотрели переход на URL-адрес с помощью `ICoreWebView2::Navigate` последнего шага. Во время навигации WebView запускает последовательность событий, которые узел может прослушать,,, `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` а затем `NavigationCompleted` . Щелкните [здесь](../reference/win32/0-9-488/ICoreWebView2.md#navigation-events) , чтобы получить дополнительные сведения.

![события навигации](../media/navigation-events.png)

В случае ошибок может возникнуть или не быть `SourceChanged` , `ContentLoading` или `HistoryChanged` события (-ей), в зависимости от того, проявляется ли переход на страницу ошибки. В случае перенаправления HTTP `NavigationStarting` в строке будет несколько событий.

В качестве примера использования этих событий можно зарегистрировать обработчик для `NavigationStarting` отмены любых запросов, не относящихся к HTTPS. Скопируйте приведенный ниже код в **HelloWebView. cpp** ниже `// Step 4 - Navigation events` .

```cpp
// register an ICoreWebView2NavigationStartingEventHandler to cancel any non-https navigation
EventRegistrationToken token;
webviewWindow->add_NavigationStarting(Callback<ICoreWebView2NavigationStartingEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2NavigationStartingEventArgs * args) -> HRESULT {
        PWSTR uri;
        args->get_Uri(&uri);
        std::wstring source(uri);
        if (source.substr(0, 5) != L"https") {
            args->put_Cancel(true);
        }
        CoTaskMemFree(uri);
        return S_OK;
    }).Get(), &token);
```

Теперь приложение не будет переходить на сайты, не поддерживающие HTTPS. Аналогичный механизм можно использовать для выполнения других задач, например для обеспечения возможности навигации в рамках собственного домена.

## Шаг 5: создание сценариев

Ведущее приложение может также внедрить JavaScript в WebView. Вы можете WebView задачу, чтобы выполнить произвольный сценарий JavaScript или добавить сценарии инициализации. Добавленные сценарии инициализации применяются ко всем документам верхнего уровня и навигации дочернего фрейма до тех пор, пока они не будут удалены, а затем выполняются после создания глобального объекта и перед выполнением любого другого сценария, включенного в документ HTML.

Скопируйте приведенный ниже код `// Step 5 - Scripting` .

```cpp
// Schedule an async task to add initialization script that freezes the Object object
webviewWindow->AddScriptToExecuteOnDocumentCreated(L"Object.freeze(Object);", nullptr);
// Schedule an async task to get the document URL
webviewWindow->ExecuteScript(L"window.document.URL;", Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
    [](HRESULT errorCode, LPCWSTR resultObjectAsJson) -> HRESULT {
        LPCWSTR URL = resultObjectAsJson;
        //doSomethingWithURL(URL);
        return S_OK;
    }).Get());
```

Теперь WebView всегда закрепляет объект объекта и возвращает документ страницы один раз.

**Обратите внимание, что эти API внедрения сценария (и некоторые другие API WebView2) являются асинхронными, поэтому следует использовать обратные вызовы, если код должен выполняться в определенном порядке.**

## Шаг 6 — взаимодействие между узлом и веб-контентом

Основное приложение и веб-контент также могут взаимодействовать друг с другом через `postMessage` . Веб-содержимое, выполняемое в WebView, может публиковаться на узле `window.chrome.webview.postMessage` , и оно будет обрабатываться зарегистрированным `ICoreWebView2WebMessageReceivedEventHandler` на нем. Аналогичным образом ведущее приложение может подавать сообщение в виде веб-содержимого с помощью `ICoreWebView2::PostWebMessageAsString` или `ICoreWebView2::PostWebMessageAsJSON` , которое может быть перехвачено обработчиками, добавленными из `window.chrome.webview.addEventListener` . Механизм связи позволяет веб-содержимому использовать собственные возможности путем передачи сообщений для запроса вызывающим узлом API-интерфейсов машинного кода.

В качестве примера рассмотрим этот механизм, давайте попробуем распечатать URL-адрес документа в WebView с помощью небольшой демонстрации.

1. Основное приложение регистрирует обработчик, чтобы вернуть полученное сообщение обратно в веб-содержимое.
2. ведущее приложение вставляет сценарий в веб-содержимое, которое регистрирует обработчик для печати сообщения с узла.
3. ведущее приложение вставляет сценарий в веб-содержимое, которое отправляет URL-адрес узлу.
4. вызывается обработчик узла и возвращает сообщение (URL-адрес) на веб-контент.
5. запустится обработчик веб-содержимого, и на нем будет распечатано сообщение узла (URL-адрес).

Скопируйте приведенный `// Step 6 - Communication between host and web content` ниже код.

```cpp
// Set an event handler for the host to return received message back to the web content
webviewWindow->add_WebMessageReceived(Callback<ICoreWebView2WebMessageReceivedEventHandler>(
    [](ICoreWebView2* webview, ICoreWebView2WebMessageReceivedEventArgs * args) -> HRESULT {
        PWSTR message;
        args->TryGetWebMessageAsString(&message);
        // processMessage(&message);
        webview->PostWebMessageAsString(message);
        CoTaskMemFree(message);
        return S_OK;
    }).Get(), &token);

// Schedule an async task to add initialization script that
// 1) Add an listener to print message from the host
// 2) Post document URL to the host
webviewWindow->AddScriptToExecuteOnDocumentCreated(
    L"window.chrome.webview.addEventListener(\'message\', event => alert(event.data));" \
    L"window.chrome.webview.postMessage(window.document.URL);",
nullptr);
```

Чтобы выполнить сборку и запустить приложение, нажмите клавишу F5. Теперь перед переходом к страницам будут отображаться URL-адреса.

![Show-URL](../media/show-url.png)

Поздравляем! вы только что создали первое приложение WebView2!

## Дальнейшие действия

В этом пошаговом руководстве есть множество функциональных возможностей WebView2, не описанных в этом примере.

Дополнительные сведения:

* [Пример извлечения API WebView2](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) для подробного примера наших возможностей SDK.
* Извлечение [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) приложения, созданного с помощью WebView2.
* Ознакомьтесь со статьей [справочник API](../reference/win32/0-9-488-reference-webview2.md) для получения подробных сведений об API out.  

## Связь с командой WebView2  

Помогите нам создать более WebView2ную работу, поделитесь с нами. Посетите наш [репозиторий обратной связи](https://aka.ms/webviewfeedback) , чтобы отправить запросы функций или отчеты об ошибках или найти известные проблемы.
