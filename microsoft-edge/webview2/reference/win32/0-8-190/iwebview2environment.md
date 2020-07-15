---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 759c4a57e5ab099310c5f6d38f6777abcfc9fefa
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878535"
---
# <span data-ttu-id="ee4c4-104">0.8.355-Interface IWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="ee4c4-104">0.8.355 - interface IWebView2Environment</span></span> 

> [!NOTE]
> <span data-ttu-id="ee4c4-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="ee4c4-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment
  : public IUnknown
```

<span data-ttu-id="ee4c4-107">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="ee4c4-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ee4c4-108">Summary</span></span>

 <span data-ttu-id="ee4c4-109">Участников</span><span class="sxs-lookup"><span data-stu-id="ee4c4-109">Members</span></span>                        | <span data-ttu-id="ee4c4-110">Описания</span><span class="sxs-lookup"><span data-stu-id="ee4c4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ee4c4-111">CreateWebView</span><span class="sxs-lookup"><span data-stu-id="ee4c4-111">CreateWebView</span></span>](#createwebview) | <span data-ttu-id="ee4c4-112">Асинхронно создайте новый [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="ee4c4-112">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>
[<span data-ttu-id="ee4c4-113">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="ee4c4-113">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="ee4c4-114">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-114">Create a new web resource response object.</span></span>

<span data-ttu-id="ee4c4-115">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-115">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="ee4c4-116">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-116">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="ee4c4-117">Участников</span><span class="sxs-lookup"><span data-stu-id="ee4c4-117">Members</span></span>

#### <span data-ttu-id="ee4c4-118">CreateWebView</span><span class="sxs-lookup"><span data-stu-id="ee4c4-118">CreateWebView</span></span> 

<span data-ttu-id="ee4c4-119">Асинхронно создайте новый [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="ee4c4-119">Asynchronously create a new [IWebView2WebView](IWebView2WebView.md).</span></span>

> <span data-ttu-id="ee4c4-120">общедоступные значения HRESULT [CreateWebView](#createwebview)(HWND ParentWindow,[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \* обработчик)</span><span class="sxs-lookup"><span data-stu-id="ee4c4-120">public HRESULT [CreateWebView](#createwebview)(HWND parentWindow,[IWebView2CreateWebViewCompletedHandler](IWebView2CreateWebViewCompletedHandler.md) \* handler)</span></span>

<span data-ttu-id="ee4c4-121">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-121">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="ee4c4-122">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-122">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="ee4c4-123">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-123">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="ee4c4-124">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-124">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="ee4c4-125">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-125">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span> 

```cpp
// Create or recreate the WebView and its environment.
void AppWindow::InitializeWebView(InitializeWebViewFlags webviewInitFlags)
{
    m_lastUsedInitFlags = webviewInitFlags;
    // To ensure browser switches get applied correctly, we need to close
    // the existing WebView. This will result in a new browser process
    // getting created which will apply the browser switches.
    CloseWebView();

    LPCWSTR subFolder = nullptr;
    LPCWSTR additionalBrowserSwitches = nullptr;
    HRESULT hr = CreateWebView2EnvironmentWithDetails(
        subFolder, nullptr, additionalBrowserSwitches,
        Callback<IWebView2CreateWebView2EnvironmentCompletedHandler>(
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
    HRESULT result, IWebView2Environment* environment)
{
    CHECK_FAILURE(result);

    CHECK_FAILURE(environment->QueryInterface(IID_PPV_ARGS(&m_webViewEnvironment)));
        CHECK_FAILURE(m_webViewEnvironment->CreateWebView(
            m_mainWindow, Callback<IWebView2CreateWebViewCompletedHandler>(
                              this, &AppWindow::OnCreateWebViewCompleted)
                              .Get()));
    return S_OK;
}
```

 <span data-ttu-id="ee4c4-126">Рекомендуется, чтобы приложение обрабатывало сообщения диспетчера перезапуска, чтобы его можно было перезапустить надлежащим образом в случае, когда приложение использует Edge для WebView с определенной установкой и удаляется установка.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-126">It is recommended that the application handles restart manager messages so that it can be restarted gracefully in the case when the app is using Edge for webview from a certain installation and that installation is being uninstalled.</span></span> <span data-ttu-id="ee4c4-127">Например, если пользователь устанавливает ребро с канала разработки и использует ребро с этого канала для тестирования приложения, а затем удаляет Edge из него, не закрывая приложение, приложение будет перезапущена, чтобы разрешить удаление канала разработки для успешного выполнения.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-127">For example, if a user installs Edge from Dev channel and opts to use Edge from that channel for testing the app, and then uninstalls Edge from that channel without closing the app, the app will be restarted to allow uninstallation of the dev channel to succeed.</span></span> 

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

#### <span data-ttu-id="ee4c4-128">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="ee4c4-128">CreateWebResourceResponse</span></span> 

<span data-ttu-id="ee4c4-129">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-129">Create a new web resource response object.</span></span>

> <span data-ttu-id="ee4c4-130">общедоступные значения HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* Content, int STATUSCODE, LPCWSTR REASONPHRASE, LPCWSTR Headers,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="ee4c4-130">public HRESULT [CreateWebResourceResponse](#createwebresourceresponse)(IStream \* content,int statusCode,LPCWSTR reasonPhrase,LPCWSTR headers,[IWebView2WebResourceResponse](IWebView2WebResourceResponse.md) \*\* response)</span></span>

<span data-ttu-id="ee4c4-131">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-131">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="ee4c4-132">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="ee4c4-132">It's also possible to create this object with empty headers string and then use the [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md) to construct the headers line by line.</span></span> <span data-ttu-id="ee4c4-133">Сведения о других параметрах смотрите в [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span><span class="sxs-lookup"><span data-stu-id="ee4c4-133">For information on other parameters see [IWebView2WebResourceResponse](IWebView2WebResourceResponse.md).</span></span>

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

