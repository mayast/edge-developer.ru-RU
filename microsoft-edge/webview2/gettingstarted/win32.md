---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 460364b0c93e80c0e3868c3b69e20ea9dcf6c129
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697198"
---
# <span data-ttu-id="6cfd9-104">Начало работы с WebView2 (Предварительная версия для разработчиков)</span><span class="sxs-lookup"><span data-stu-id="6cfd9-104">Getting started with WebView2 (developer preview)</span></span>

<span data-ttu-id="6cfd9-105">В этом пошаговом руководстве рассматриваются часто используемые функции [WebView2 (Предварительная версия для разработчиков)](https://aka.ms/webview) и начинается создание первого приложения WebView2.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-105">This walkthrough goes over the commonly used functionalities of [WebView2 (developer preview)](https://aka.ms/webview) and gets you started on creating your first WebView2 app.</span></span> <span data-ttu-id="6cfd9-106">Дополнительные сведения об отдельных API можно найти в [справочнике по API](../reference/win32/0-9-538-reference-webview2.md) .</span><span class="sxs-lookup"><span data-stu-id="6cfd9-106">Visit [API reference](../reference/win32/0-9-538-reference-webview2.md) to learn more about individual APIs.</span></span>  

## <span data-ttu-id="6cfd9-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="6cfd9-107">Prerequisites</span></span>

* <span data-ttu-id="6cfd9-108">[Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download/) , установленный в поддерживаемой ОС (в настоящее время Windows 10, Windows 8,1 и Windows 7).</span><span class="sxs-lookup"><span data-stu-id="6cfd9-108">[Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download/) installed on supported OS (currently Windows 10, Windows 8.1, and Windows 7).</span></span> <span data-ttu-id="6cfd9-109">**Рекомендуем использовать канал Канарские и минимальную требуемую версию — 82.0.488.0**.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-109">**We recommend using the Canary channel and the minimum required version is 82.0.488.0**.</span></span>
* <span data-ttu-id="6cfd9-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 или более поздней версии с установленной поддержкой C++.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-110">[Visual Studio](https://visualstudio.microsoft.com/) 2015 or later with C++ support installed.</span></span>

## <span data-ttu-id="6cfd9-111">Шаг 1: создание одного окна приложение Win32</span><span class="sxs-lookup"><span data-stu-id="6cfd9-111">Step 1 - Create a single window win32 app</span></span>

<span data-ttu-id="6cfd9-112">Начнем с базового проекта для настольных компьютеров, который содержит одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-112">We will start with a basic desktop project containing a single main window.</span></span> <span data-ttu-id="6cfd9-113">Так как это не основное фокусирование на этом пошаговом руководстве, мы просто используем модифицированный образец кода из [пошагового руководства: создание традиционного классического приложения для Windows (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="6cfd9-113">As this is not the main focus of this walkthrough, we will simply use modified sample code from [Walkthrough: Create a traditional Windows Desktop application (C++)](/cpp/windows/walkthrough-creating-windows-desktop-applications-cpp?view=vs-2019).</span></span> <span data-ttu-id="6cfd9-114">[Загрузите](https://aka.ms/HelloWebView) модифицированный пример, чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-114">[Download](https://aka.ms/HelloWebView) the modified sample to get started.</span></span>

<span data-ttu-id="6cfd9-115">Откройте **WebView2GettingStarted. sln** в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-115">Open **WebView2GettingStarted.sln** in Visual Studio.</span></span> <span data-ttu-id="6cfd9-116">Если вы используете более старую версию Visual Studio, щелкните правой кнопкой мыши проект **WebView2GettingStarted** и выберите пункт **свойства**.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-116">If you are using an older version of Visual Studio, right click on the **WebView2GettingStarted** project and click **Properties**.</span></span> <span data-ttu-id="6cfd9-117">В разделе **Свойства конфигурации**  >  **Общие**измените **версию пакета SDK для Windows** и **набор инструментов платформы** , чтобы использовать набор инструментов Win10 SDK и VS.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-117">Under **Configuration Properties** > **General**, modify **Windows SDK Version** and **Platform Toolset** to use the Win10 SDK and VS toolset available to you.</span></span>

![версия средства](../media/tool-version.png)

<span data-ttu-id="6cfd9-119">Visual Studio может показывать некоторые ошибки из-за отсутствующего файла заголовка WebView2, который должен выйти после завершения действия 2.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-119">Visual Studio may show some errors due to missing WebView2 header file, which should go away once Step 2 is completed.</span></span>

## <span data-ttu-id="6cfd9-120">Шаг 2. Установка WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="6cfd9-120">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="6cfd9-121">Теперь добавим пакет SDK WebView2 в проект.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-121">Now let's add the WebView2 SDK into the project.</span></span> <span data-ttu-id="6cfd9-122">Для предварительного просмотра разработчик может установить пакет SDK Win32 с помощью NuGet.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-122">For the developer preview, you can install the Win32 SDK via Nuget.</span></span>

1. <span data-ttu-id="6cfd9-123">Щелкните проект правой кнопкой мыши и выберите пункт **Управление пакетами NuGet**.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-123">Right click the project and click **Manage Nuget Packages**.</span></span>

    ![Manage-NuGet-Packages](../media/manage-nuget-packages.png)

2. <span data-ttu-id="6cfd9-125">Введите **Microsoft. Windows. ImplementationLibrary** в строке поиска, выберите **Microsoft. Windows. ImplementationLibrary** из результатов и щелкните **установить** в правой части окна и установите последнюю версию SDK.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-125">Enter **Microsoft.Windows.ImplementationLibrary** in the search bar, click **Microsoft.Windows.ImplementationLibrary** from the results, and click **Install** inthe right hand side window and install the latest SDK.</span></span> <span data-ttu-id="6cfd9-126">NuGet загрузит пакет SDK на ваш компьютер.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-126">Nuget will download the SDK to your machine.</span></span> <span data-ttu-id="6cfd9-127">Несмотря на то, что мы используем [библиотеку реализации Windows](https://github.com/Microsoft/wil) и [библиотеку шаблонов среды выполнения Windows](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) для упрощения работы с COM в этом пошаговом руководстве, они являются полностью необязательными.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-127">While we use [Windows Implementation Library](https://github.com/Microsoft/wil) and [Windows Runtime C++ Template Library](/cpp/cppcx/wrl/windows-runtime-cpp-template-library-wrl?view=vs-2019) to make working with COM easier in this walkthrough, they are completely optional.</span></span>

    ![будет](../media/wil.png)

3. <span data-ttu-id="6cfd9-129">Введите **Microsoft. Web. WebView2** на панели поиска, выберите **Microsoft. Web. WebView2** из результатов и щелкните **установить** в правой части окна и установите последнюю версию SDK.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-129">Enter **Microsoft.Web.WebView2** in the search bar, click **Microsoft.Web.WebView2** from the results, and click **Install** in the right hand side window and install the latest SDK.</span></span> <span data-ttu-id="6cfd9-130">NuGet загрузит пакет SDK на ваш компьютер.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-130">Nuget will download the SDK to your machine.</span></span>

    ![NuGet](../media/nuget.png)

4. <span data-ttu-id="6cfd9-132">Включите заголовок WebView2.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-132">Include the WebView2 header.</span></span> <span data-ttu-id="6cfd9-133">В **HelloWebView. cpp**добавьте `#include "WebView2.h"` под строками `#include` s.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-133">In **HelloWebView.cpp**, add `#include "WebView2.h"` below the lines of `#include`s.</span></span>

    ```cpp
    ...
    #include <wrl.h>
    #include <wil/com.h>
    // include WebView2 header
    #include "WebView2.h"
    ```

<span data-ttu-id="6cfd9-134">Все готово для использования и сборки в API WebView2.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-134">You are all set to use and build against the WebView2 API.</span></span> <span data-ttu-id="6cfd9-135">Нажмите клавишу F5 для создания и запуска примера приложения.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-135">Press F5 to build and run the sample app.</span></span> <span data-ttu-id="6cfd9-136">Должно отобразиться приложение, в котором отображается пустое окно.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-136">You should see an app displaying an empty window.</span></span>

![Пустое приложение](../media/empty-app.png)

## <span data-ttu-id="6cfd9-138">Шаг 3: создание единого WebView в родительском окне</span><span class="sxs-lookup"><span data-stu-id="6cfd9-138">Step 3 - Create a single WebView within the parent window</span></span>

<span data-ttu-id="6cfd9-139">Теперь добавим WebView в главное окно.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-139">Now let's add a WebView to the main window.</span></span> <span data-ttu-id="6cfd9-140">Мы будем использовать `CreateCoreWebView2Environment` для настройки среды и поиска в браузере Microsoft EDGE (Chromium) элемента управления Powering.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-140">We'll use `CreateCoreWebView2Environment` to set up the environment and locate the Microsoft Edge (Chromium) browser powering the control.</span></span> <span data-ttu-id="6cfd9-141">Вы также можете использовать `CreateCoreWebView2EnvironmentWithOptions` этот параметр, если вы хотите указать расположение браузера, папку пользователя, флаги браузера и т. д., вместо использования параметра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-141">You can also use `CreateCoreWebView2EnvironmentWithOptions` if you want to specify browser location, user folder, browser flags, etc., instead of using the default setting.</span></span> <span data-ttu-id="6cfd9-142">После завершения вы сможете `CreateCoreWebView2Environment` позвонить `ICoreWebView2Environment::CreateCoreWebView2Controller` внутри `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` обратного вызова и вызов `ICoreWebView2Controller::get_CoreWebView2` для получения связанного WebView.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-142">Upon the completion of `CreateCoreWebView2Environment`, you'll be able to call `ICoreWebView2Environment::CreateCoreWebView2Controller` inside the `ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler` callback and call `ICoreWebView2Controller::get_CoreWebView2` to get the associated WebView.</span></span>

<span data-ttu-id="6cfd9-143">В обратном вызове также можно задать несколько параметров, изменить размер WebView, чтобы получить 100% родительского окна, и перейти к Bing.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-143">In the callback, let's also set a few settings, resize the WebView to take 100% of the parent window, and navigate to Bing.</span></span>

<span data-ttu-id="6cfd9-144">Скопируйте приведенный ниже код в **HelloWebView. cpp** между `// <-- WebView2 sample code starts here -->` and `// <-- WebView2 sample code ends here -->` .</span><span class="sxs-lookup"><span data-stu-id="6cfd9-144">Copy the following code to **HelloWebView.cpp** between `// <-- WebView2 sample code starts here -->` and `// <-- WebView2 sample code ends here -->`.</span></span>

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

<span data-ttu-id="6cfd9-145">Чтобы выполнить сборку и запустить приложение, нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-145">Press F5 to build and run the app.</span></span> <span data-ttu-id="6cfd9-146">Теперь у вас есть окно WebView, в котором отображается Bing.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-146">Now you have a WebView window displaying Bing.</span></span>

![Bing-окно](../media/bing-window.png)

## <span data-ttu-id="6cfd9-148">Шаг 4 — события навигации</span><span class="sxs-lookup"><span data-stu-id="6cfd9-148">Step 4 - Navigation events</span></span>

<span data-ttu-id="6cfd9-149">Мы уже посмотрели переход на URL-адрес с помощью `ICoreWebView2::Navigate` последнего шага.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-149">We already covered navigating to URL using `ICoreWebView2::Navigate` in the last step.</span></span> <span data-ttu-id="6cfd9-150">Во время навигации WebView запускает последовательность событий, которые узел может прослушать,,, `NavigationStarting` `SourceChanged` `ContentLoading` `HistoryChanged` а затем `NavigationCompleted` .</span><span class="sxs-lookup"><span data-stu-id="6cfd9-150">During navigation, WebView fires a sequence of events that the host can listen to - `NavigationStarting`, `SourceChanged`, `ContentLoading`, `HistoryChanged`, and then `NavigationCompleted`.</span></span> <span data-ttu-id="6cfd9-151">Щелкните [здесь](../reference/win32/0-9-538/ICoreWebView2.md#navigation-events) , чтобы получить дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-151">Click [here](../reference/win32/0-9-538/ICoreWebView2.md#navigation-events) to learn more.</span></span>

![события навигации](../media/navigation-events.png)

<span data-ttu-id="6cfd9-153">В случае ошибок может возникнуть или не быть `SourceChanged` , `ContentLoading` или `HistoryChanged` события (-ей), в зависимости от того, проявляется ли переход на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-153">In error cases there may or may not be `SourceChanged`, `ContentLoading`, or `HistoryChanged` event(s) depending on whether the navigation is continued to an error page.</span></span> <span data-ttu-id="6cfd9-154">В случае перенаправления HTTP `NavigationStarting` в строке будет несколько событий.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-154">In case of an HTTP redirect, there will be multiple `NavigationStarting` events in a row.</span></span>

<span data-ttu-id="6cfd9-155">В качестве примера использования этих событий можно зарегистрировать обработчик для `NavigationStarting` отмены любых запросов, не относящихся к HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-155">As an example of utilizing those events, let's register a handler for `NavigationStarting` to cancel any non-https requests.</span></span> <span data-ttu-id="6cfd9-156">Скопируйте приведенный ниже код в **HelloWebView. cpp** ниже `// Step 4 - Navigation events` .</span><span class="sxs-lookup"><span data-stu-id="6cfd9-156">Copy the following code to **HelloWebView.cpp** below `// Step 4 - Navigation events`.</span></span>

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

<span data-ttu-id="6cfd9-157">Теперь приложение не будет переходить на сайты, не поддерживающие HTTPS.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-157">Now the app will not navigate to any non-https sites.</span></span> <span data-ttu-id="6cfd9-158">Аналогичный механизм можно использовать для выполнения других задач, например для обеспечения возможности навигации в рамках собственного домена.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-158">You can use similar mechanism to accomplish other tasks, such as restricting navigation to within your own domain.</span></span>

## <span data-ttu-id="6cfd9-159">Шаг 5: создание сценариев</span><span class="sxs-lookup"><span data-stu-id="6cfd9-159">Step 5 - Scripting</span></span>

<span data-ttu-id="6cfd9-160">Ведущее приложение может также внедрить JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-160">The hosting app can also inject JavaScript into WebView.</span></span> <span data-ttu-id="6cfd9-161">Вы можете WebView задачу, чтобы выполнить произвольный сценарий JavaScript или добавить сценарии инициализации.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-161">You can task WebView to execute arbitrary JavaScript or add initialization scripts.</span></span> <span data-ttu-id="6cfd9-162">Добавленные сценарии инициализации применяются ко всем документам верхнего уровня и навигации дочернего фрейма до тех пор, пока они не будут удалены, а затем выполняются после создания глобального объекта и перед выполнением любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-162">Added initialization scripts apply to all future top level document and child frame navigation until removed, and run after the global object has been created and before any other script included by the HTML document is executed.</span></span>

<span data-ttu-id="6cfd9-163">Скопируйте приведенный ниже код `// Step 5 - Scripting` .</span><span class="sxs-lookup"><span data-stu-id="6cfd9-163">Copy the following code below `// Step 5 - Scripting`.</span></span>

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

<span data-ttu-id="6cfd9-164">Теперь WebView всегда закрепляет объект объекта и возвращает документ страницы один раз.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-164">Now WebView will always freeze the Object object and return the page document once.</span></span>

**<span data-ttu-id="6cfd9-165">Обратите внимание, что эти API внедрения сценария (и некоторые другие API WebView2) являются асинхронными, поэтому следует использовать обратные вызовы, если код должен выполняться в определенном порядке.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-165">Note that these script injection APIs (and some other WebView2 APIs) are asynchronous, you should use callbacks if code is to be executed in a particular order.</span></span>**

## <span data-ttu-id="6cfd9-166">Шаг 6 — взаимодействие между узлом и веб-контентом</span><span class="sxs-lookup"><span data-stu-id="6cfd9-166">Step 6 - Communication between host and web content</span></span>

<span data-ttu-id="6cfd9-167">Основное приложение и веб-контент также могут взаимодействовать друг с другом через `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="6cfd9-167">The host and the web content can also communicate with each other through `postMessage`.</span></span> <span data-ttu-id="6cfd9-168">Веб-содержимое, выполняемое в WebView, может публиковаться на узле `window.chrome.webview.postMessage` , и оно будет обрабатываться зарегистрированным `ICoreWebView2WebMessageReceivedEventHandler` на нем.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-168">The web content running within a WebView can post to the host through `window.chrome.webview.postMessage`, and the message would be handled by any registered `ICoreWebView2WebMessageReceivedEventHandler` on the host.</span></span> <span data-ttu-id="6cfd9-169">Аналогичным образом ведущее приложение может подавать сообщение в виде веб-содержимого с помощью `ICoreWebView2::PostWebMessageAsString` или `ICoreWebView2::PostWebMessageAsJSON` , которое может быть перехвачено обработчиками, добавленными из `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="6cfd9-169">Likewise, the host can message the web content through `ICoreWebView2::PostWebMessageAsString` or `ICoreWebView2::PostWebMessageAsJSON`, which would be caught by handlers added from `window.chrome.webview.addEventListener`.</span></span> <span data-ttu-id="6cfd9-170">Механизм связи позволяет веб-содержимому использовать собственные возможности путем передачи сообщений для запроса вызывающим узлом API-интерфейсов машинного кода.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-170">The communication mechanism allows the web content to utilize native capabilities by passing messages to ask the host to call native APIs.</span></span>

<span data-ttu-id="6cfd9-171">В качестве примера рассмотрим этот механизм, давайте попробуем распечатать URL-адрес документа в WebView с помощью небольшой демонстрации.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-171">As an example to understand the mechanism, let's try printing out the document URL in WebView with a little detour,</span></span>

1. <span data-ttu-id="6cfd9-172">Основное приложение регистрирует обработчик, чтобы вернуть полученное сообщение обратно в веб-содержимое.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-172">the host registers a handler to return received message back to the web content</span></span>
2. <span data-ttu-id="6cfd9-173">ведущее приложение вставляет сценарий в веб-содержимое, которое регистрирует обработчик для печати сообщения с узла.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-173">the host injects a script to the web content that registers a handler to print message from the host</span></span>
3. <span data-ttu-id="6cfd9-174">ведущее приложение вставляет сценарий в веб-содержимое, которое отправляет URL-адрес узлу.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-174">the host injects a script to the web content that posts the URL to the host</span></span>
4. <span data-ttu-id="6cfd9-175">вызывается обработчик узла и возвращает сообщение (URL-адрес) на веб-контент.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-175">the host's handler is triggered and returns the message (the URL) to the web content</span></span>
5. <span data-ttu-id="6cfd9-176">запустится обработчик веб-содержимого, и на нем будет распечатано сообщение узла (URL-адрес).</span><span class="sxs-lookup"><span data-stu-id="6cfd9-176">the web content's handler is triggered and prints the host's message (the URL)</span></span>

<span data-ttu-id="6cfd9-177">Скопируйте приведенный `// Step 6 - Communication between host and web content` ниже код.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-177">Copy the following code below `// Step 6 - Communication between host and web content`,</span></span>

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

<span data-ttu-id="6cfd9-178">Чтобы выполнить сборку и запустить приложение, нажмите клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-178">Press F5 to build and run the app.</span></span> <span data-ttu-id="6cfd9-179">Теперь перед переходом к страницам будут отображаться URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-179">It will now show URLs before navigating to pages.</span></span>

![Show-URL](../media/show-url.png)

<span data-ttu-id="6cfd9-181">Поздравляем! вы только что создали первое приложение WebView2!</span><span class="sxs-lookup"><span data-stu-id="6cfd9-181">Congratulations, you've just built your first WebView2 app!</span></span>

## <span data-ttu-id="6cfd9-182">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="6cfd9-182">Next Steps</span></span>

<span data-ttu-id="6cfd9-183">В этом пошаговом руководстве есть множество функциональных возможностей WebView2, не описанных в этом примере.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-183">There are plenty of WebView2 functionalities that are not covered in this walkthrough.</span></span>

<span data-ttu-id="6cfd9-184">Дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="6cfd9-184">To learn more:</span></span>

* <span data-ttu-id="6cfd9-185">[Пример извлечения WEBVIEW2 API](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) для подробного примера возможностей WebView2's.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-185">Checkout [WebView2 API Sample](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample) for a comprehensive example of WebView2's capabilities.</span></span>
* <span data-ttu-id="6cfd9-186">Извлечение [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) приложения, созданного с помощью WebView2.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-186">Checkout [WebView2Browser](https://github.com/MicrosoftEdge/WebView2Browser) an application built using WebView2.</span></span>
* <span data-ttu-id="6cfd9-187">Ознакомьтесь со [справочными](../reference/win32/0-9-538-reference-webview2.md) материалами по API для получения подробных сведений о нашем API.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-187">Please explore [API reference](../reference/win32/0-9-538-reference-webview2.md) for detailed information about our API.</span></span>  

## <span data-ttu-id="6cfd9-188">Связь с командой WebView2</span><span class="sxs-lookup"><span data-stu-id="6cfd9-188">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="6cfd9-189">Помогите нам создать более WebView2ную работу, поделитесь с нами.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-189">Help us build a richer WebView2 experience by sharing your feedback!</span></span> <span data-ttu-id="6cfd9-190">Посетите наш [репозиторий обратной связи](https://aka.ms/webviewfeedback) , чтобы отправить запросы функций или отчеты об ошибках или найти известные проблемы.</span><span class="sxs-lookup"><span data-stu-id="6cfd9-190">Visit our [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>
