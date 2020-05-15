---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2f376cdd7098c512a8c7a0a3a463f5302f0bfbd7
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655052"
---
# <span data-ttu-id="cad56-104">интерфейс ICoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="cad56-104">interface ICoreWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="cad56-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="cad56-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="cad56-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="cad56-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Environment
  : public IUnknown
```

<span data-ttu-id="cad56-107">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="cad56-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="cad56-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="cad56-108">Summary</span></span>

 <span data-ttu-id="cad56-109">Участников</span><span class="sxs-lookup"><span data-stu-id="cad56-109">Members</span></span>                        | <span data-ttu-id="cad56-110">Описания</span><span class="sxs-lookup"><span data-stu-id="cad56-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cad56-111">CreateCoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="cad56-111">CreateCoreWebView2Host</span></span>](#createcorewebview2host) | <span data-ttu-id="cad56-112">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="cad56-112">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="cad56-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="cad56-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="cad56-114">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="cad56-114">Create a new web resource response object.</span></span>
[<span data-ttu-id="cad56-115">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cad56-115">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="cad56-116">Сведения о версии браузера для текущего [ICoreWebView2Environment](), включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="cad56-116">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="cad56-117">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cad56-117">add_NewBrowserVersionAvailable</span></span>](#add_newbrowserversionavailable) | <span data-ttu-id="cad56-118">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="cad56-118">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="cad56-119">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cad56-119">remove_NewBrowserVersionAvailable</span></span>](#remove_newbrowserversionavailable) | <span data-ttu-id="cad56-120">Удалите обработчик событий, добавленный ранее add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="cad56-120">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

<span data-ttu-id="cad56-121">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="cad56-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="cad56-122">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="cad56-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="cad56-123">Участников</span><span class="sxs-lookup"><span data-stu-id="cad56-123">Members</span></span>

#### <span data-ttu-id="cad56-124">CreateCoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="cad56-124">CreateCoreWebView2Host</span></span> 

<span data-ttu-id="cad56-125">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="cad56-125">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="cad56-126">общедоступные значения HRESULT [CreateCoreWebView2Host](#createcorewebview2host)(HWND ParentWindow,[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="cad56-126">public HRESULT [CreateCoreWebView2Host](#createcorewebview2host)(HWND parentWindow,[ICoreWebView2CreateCoreWebView2HostCompletedHandler](ICoreWebView2CreateCoreWebView2HostCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="cad56-127">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="cad56-127">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="cad56-128">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="cad56-128">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="cad56-129">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="cad56-129">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="cad56-130">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="cad56-130">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="cad56-131">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="cad56-131">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

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

 <span data-ttu-id="cad56-132">Рекомендуется, чтобы приложение обрабатывало сообщения диспетчера перезапуска, чтобы его можно было перезапустить надлежащим образом в случае, когда приложение использует Edge для WebView с определенной установкой и удаляется установка.</span><span class="sxs-lookup"><span data-stu-id="cad56-132">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="cad56-133">Например, если пользователь устанавливает ребро с канала разработки и использует ребро с этого канала для тестирования приложения, а затем удаляет Edge из него, не закрывая приложение, приложение будет перезапущена, чтобы разрешить удаление канала разработки для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="cad56-133">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

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

#### <span data-ttu-id="cad56-134">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="cad56-134">CreateWebResourceResponse</span></span> 

<span data-ttu-id="cad56-135">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="cad56-135">Create a new web resource response object.</span></span>

> <span data-ttu-id="cad56-136">общедоступные значения HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* Content, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR Headers,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="cad56-136">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="cad56-137">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="cad56-137">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="cad56-138">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="cad56-138">It's also possible to create this object with empty headers string and then use the [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="cad56-139">Сведения о других параметрах смотрите в [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="cad56-139">For information on other parameters see [ICoreWebView2WebResourceResponse](ICoreWebView2WebResourceResponse.md).</span></span>

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

#### <span data-ttu-id="cad56-140">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cad56-140">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="cad56-141">Сведения о версии браузера для текущего [ICoreWebView2Environment](), включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="cad56-141">The browser version info of the current [ICoreWebView2Environment](), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="cad56-142">общедоступные значения HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="cad56-142">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="cad56-143">Это соответствует формату API GetCoreWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="cad56-143">This matches the format of the GetCoreWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="cad56-144">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="cad56-144">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

#### <span data-ttu-id="cad56-145">add_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cad56-145">add_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="cad56-146">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="cad56-146">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="cad56-147">общедоступные значения HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](ICoreWebView2NewBrowserVersionAvailableEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="cad56-147">public HRESULT [add_NewBrowserVersionAvailable](#add_newbrowserversionavailable)([ICoreWebView2NewBrowserVersionAvailableEventHandler](ICoreWebView2NewBrowserVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="cad56-148">Для использования более новой версии браузера необходимо создать новую среду и WebView.</span><span class="sxs-lookup"><span data-stu-id="cad56-148">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="cad56-149">Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="cad56-149">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="cad56-150">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="cad56-150">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="cad56-151">Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="cad56-151">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="cad56-152">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="cad56-152">Or simply prompt the user to restart the app.</span></span>

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

#### <span data-ttu-id="cad56-153">remove_NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cad56-153">remove_NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="cad56-154">Удалите обработчик событий, добавленный ранее add_NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="cad56-154">Remove an event handler previously added with add_NewBrowserVersionAvailable.</span></span>

> <span data-ttu-id="cad56-155">общедоступные значения HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="cad56-155">public HRESULT [remove_NewBrowserVersionAvailable](#remove_newbrowserversionavailable)(EventRegistrationToken token)</span></span>

