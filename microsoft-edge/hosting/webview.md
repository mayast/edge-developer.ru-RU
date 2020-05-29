---
description: Размещение веб-содержимого в приложении для Windows 10 с помощью элемента управления WebView (EdgeHTML)
title: Microsoft Edge WebView для приложений для Windows 10
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: приложения x-MS-WebView, MSHTMLWebViewElement, WebView, Windows 10, UWP, EDGE
ms.openlocfilehash: 08efb1bb87877e0b11cbc3bee1061f9be6c9ab3f
ms.sourcegitcommit: 831fc41ea347e2d1160b1804fb5e5a427dc3070d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629551"
---
# <span data-ttu-id="ac198-104">WebView (EdgeHTML) для приложений для Windows 10</span><span class="sxs-lookup"><span data-stu-id="ac198-104">WebView (EdgeHTML) for Windows 10 apps</span></span>

<span data-ttu-id="ac198-105">Элемент управления WebView (EdgeHTML) позволяет размещать веб-содержимое в приложении для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ac198-105">The WebView (EdgeHTML) control enables you to host web content in your Windows 10 app.</span></span> 

<span data-ttu-id="ac198-106">Его можно использовать в качестве элемента XAML (для приложений [универсальной платформы Windows (UWP)](/uwp/api/Windows.UI.Xaml.Controls.WebView) , [Windows Forms и классических приложений WPF](/windows/communitytoolkit/controls/wpf-winforms/webview)) либо HTML-элемента (x-MS-WebView)/DOM (MSHTMLWebViewElement) для приложений на базе Windows 10 на основе JavaScript, как описано здесь.</span><span class="sxs-lookup"><span data-stu-id="ac198-106">You can use it as a XAML element (for [Universal Windows Platform (UWP) apps](/uwp/api/Windows.UI.Xaml.Controls.WebView) and [Windows Forms and WPF desktop applications](/windows/communitytoolkit/controls/wpf-winforms/webview)), or an HTML element (x-ms-webview)/DOM object (MSHTMLWebViewElement) for JavaScript-based Windows 10 apps, as described here.</span></span>

| | |
|-|-|
| [**<span data-ttu-id="ac198-107">События</span><span class="sxs-lookup"><span data-stu-id="ac198-107">Events</span></span>**](#events) | <span data-ttu-id="ac198-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting)и [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted,](#mswebviewnavigationcompleted) [,](#mswebviewpermissionrequested) [, MSWebViewNavigationStarting](#mswebviewnavigationstarting) [, MSWebViewNewWindowRequested](#mswebviewnewwindowrequested)и [MSWebViewPermissionRequested](#mswebviewwebresourcerequested) [MSWebViewProcessExited](#mswebviewprocessexited) [MSWebViewScriptNotify](#mswebviewscriptnotify) [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying) [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified) [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified)</span><span class="sxs-lookup"><span data-stu-id="ac198-108">[departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting), [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted), [MSWebViewNavigationStarting](#mswebviewnavigationstarting), [MSWebViewNewWindowRequested](#mswebviewnewwindowrequested), [MSWebViewPermissionRequested](#mswebviewpermissionrequested), [MSWebViewProcessExited](#mswebviewprocessexited), [MSWebViewWebResourceRequested](#mswebviewwebresourcerequested), [MSWebViewScriptNotify](#mswebviewscriptnotify), [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying), [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified), [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified)</span></span>
| [**<span data-ttu-id="ac198-109">Методы</span><span class="sxs-lookup"><span data-stu-id="ac198-109">Methods</span></span>**](#methods) | <span data-ttu-id="ac198-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [goBack](#goback), [goForward,](#goforward), [navigateFocus](#navigatefocus) [navigateFocus](#navigatewithhttprequestmessage), [navigateTolocalStreamUri,](#navigatetolocalstreamuri) [Обновить](#refresh), [остановить](#stop) [navigate](#navigate) [navigateToString](#navigatetostring)</span><span class="sxs-lookup"><span data-stu-id="ac198-110">[addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [goBack](#goback), [goForward](#goforward), [navigate](#navigate), [navigateFocus](#navigatefocus), [navigateTolocalStreamUri](#navigatetolocalstreamuri), [navigateToString](#navigatetostring), [navigateWithHttpRequestMessage](#navigatewithhttprequestmessage), [refresh](#refresh), [stop](#stop)</span></span> |
| [**<span data-ttu-id="ac198-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-111">Properties</span></span>**](#properties) | <span data-ttu-id="ac198-112">[canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [DocumentTitle](#documenttitle), [Высота](#height), [процесс](#process), [Параметры](#settings), [src](#src), [Ширина](#width)</span><span class="sxs-lookup"><span data-stu-id="ac198-112">[canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [documentTitle](#documenttitle), [height](#height), [process](#process), [settings](#settings), [src](#src), [width](#width)</span></span> |

## <span data-ttu-id="ac198-113">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ac198-113">Syntax</span></span>

```js
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```

## <span data-ttu-id="ac198-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac198-114">Remarks</span></span>

### <span data-ttu-id="ac198-115">WebView и IFRAME</span><span class="sxs-lookup"><span data-stu-id="ac198-115">WebView versus iframe</span></span>

<span data-ttu-id="ac198-116">Как и стандартный HTML-элемент [IFRAME](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) , вы можете использовать WebView для загрузки удаленных страниц по протоколу HTTP и локальным страницам (*MS-appx-web:///*) из пакета приложения.</span><span class="sxs-lookup"><span data-stu-id="ac198-116">Like a standard HTML [iframe](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) element,  you can use WebView to load remote pages over HTTP and local pages (*ms-appx-web:///*) from your app package.</span></span> <span data-ttu-id="ac198-117">Однако WebView также может:</span><span class="sxs-lookup"><span data-stu-id="ac198-117">However, the WebView can also:</span></span>

 - <span data-ttu-id="ac198-118">Загрузка страниц и ресурсов из [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (локальных, перемещаемых, временных папок) (*MS-appdata:///*) и [потоков в памяти](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-Memory-Stream:///*)</span><span class="sxs-lookup"><span data-stu-id="ac198-118">Load pages and resources from your [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (local, roaming, temp) folders (*ms-appdata:///*) and [in-memory streams](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*ms-local-stream:///*)</span></span>

 - <span data-ttu-id="ac198-119">Предоставьте элементы управления, подобные браузеру: для [возврата](#goback) и [пересылки](#goforward) по журналу навигации, а также для [остановки](#stop) или [обновления](#refresh) текущей страницы.</span><span class="sxs-lookup"><span data-stu-id="ac198-119">Provide browser-like controls: for going [back](#goback) and [forward](#goforward) in navigation history, and [stopping](#stop) or [refreshing](#refresh) the current page.</span></span> 

 - <span data-ttu-id="ac198-120">Создавайте [снимки экрана веб-содержимого](#capturepreviewtoblobasync) , чтобы упростить реализацию контракта на [использование общего доступа к](/windows/uwp/app-to-app/share-data) приложениям для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="ac198-120">[Capture screenshots of web content](#capturepreviewtoblobasync) making it easy to implement the Windows 10 app [Share](/windows/uwp/app-to-app/share-data) contract.</span></span>

 - <span data-ttu-id="ac198-121">Разрешите JavaScript-код, выполняющийся в WebView, вызвать пользовательские события ([MSWebViewScriptNotify](#mswebviewscriptnotify)) для вашего приложения и разрешить приложению запускать JavaScript в WebView ([invokeScriptAsync](#invokescriptasync)).</span><span class="sxs-lookup"><span data-stu-id="ac198-121">Allow JavaScript code running within a webview to raise custom events ([MSWebViewScriptNotify](#mswebviewscriptnotify)) to your app, and allow your app to run JavaScript within the webview ([invokeScriptAsync](#invokescriptasync)).</span></span>

 - <span data-ttu-id="ac198-122">Предоставьте вам детально настроенные события WebView содержимого:</span><span class="sxs-lookup"><span data-stu-id="ac198-122">Provide you with fine-tuned webview content events:</span></span>
    
    <span data-ttu-id="ac198-123">Событие WebView DOM</span><span class="sxs-lookup"><span data-stu-id="ac198-123">WebView DOM event</span></span> | <span data-ttu-id="ac198-124">Описание</span><span class="sxs-lookup"><span data-stu-id="ac198-124">Description</span></span>
    --------- | ------
    [<span data-ttu-id="ac198-125">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="ac198-125">MSWebViewNavigationStarting</span></span>](#mswebviewnavigationstarting) | <span data-ttu-id="ac198-126">Указывает, что WebView начинает навигацию</span><span class="sxs-lookup"><span data-stu-id="ac198-126">Indicates the WebView is starting to navigate</span></span>
    [<span data-ttu-id="ac198-127">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="ac198-127">MSWebViewContentLoading</span></span>](#mswebviewcontentloading) | <span data-ttu-id="ac198-128">HTML-содержимое загружается и загружается в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ac198-128">The HTML content is downloaded and is being loaded into the control</span></span>
    [<span data-ttu-id="ac198-129">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="ac198-129">MSWebViewDOMContentLoaded</span></span>](#mswebviewdomcontentloaded) | <span data-ttu-id="ac198-130">Указывает на то, что основные элементы DOM завершили загрузку</span><span class="sxs-lookup"><span data-stu-id="ac198-130">Indicates that the main DOM elements have finished loading</span></span>
    [<span data-ttu-id="ac198-131">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="ac198-131">MSWebViewNavigationCompleted</span></span>](#mswebviewnavigationcompleted) | <span data-ttu-id="ac198-132">Указывает, что Навигация завершена и все элементы мультимедиа отображаются</span><span class="sxs-lookup"><span data-stu-id="ac198-132">Indicates the navigation is complete, and all media elements are rendered</span></span>
    [<span data-ttu-id="ac198-133">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="ac198-133">MSWebViewUnviewableContentIdentified</span></span>](#mswebviewunviewablecontentidentified) | <span data-ttu-id="ac198-134">WebView обнаружил, что содержимое не является HTML-кодом</span><span class="sxs-lookup"><span data-stu-id="ac198-134">The WebView found the content was not HTML</span></span>
    [<span data-ttu-id="ac198-135">UnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="ac198-135">UnsafeContentWarningDisplaying</span></span>](#mswebviewunsafecontentwarningdisplaying) | <span data-ttu-id="ac198-136">В WebView показана страница с предупреждением о том, что *Фильтр SmartScreen*Windows сообщил о небезопасном содержимом.</span><span class="sxs-lookup"><span data-stu-id="ac198-136">The WebView shows a warning page for content that was reported as unsafe by Windows *SmartScreen Filter*.</span></span>

    <span data-ttu-id="ac198-137">... включая соответствующие [события](#events) для содержимого IFRAME, загруженного в WebView (например, [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ac198-137">...including corresponding [events](#events) for iframe content loaded within a WebView (such as [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) and so on.)</span></span>

### <span data-ttu-id="ac198-138">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="ac198-138">Printing</span></span>

<span data-ttu-id="ac198-139">При печати приложения для Windows с использованием JavaScript теги преобразуются `<x-ms-webview>` в `<iframe>` теги перед печатью.</span><span class="sxs-lookup"><span data-stu-id="ac198-139">When a Windows app using JavaScript is printed, the `<x-ms-webview>` tags are transformed into `<iframe>` tags before printing.</span></span> <span data-ttu-id="ac198-140">Помимо обычной разницы между отображением на экране и отрисовкой для печати, стили CSS, примененные к `<iframe>` элементам, затем применяются к `<iframe>` преобразованным `<x-ms-webview>` .</span><span class="sxs-lookup"><span data-stu-id="ac198-140">Besides the normal difference between displaying on screen and rendered for print, CSS styles applied to `<iframe>` elements are then applicable to the `<iframe>` transformed from `<x-ms-webview>`.</span></span>

### <span data-ttu-id="ac198-141">Обслуживание сотрудников</span><span class="sxs-lookup"><span data-stu-id="ac198-141">Service workers</span></span>

<span data-ttu-id="ac198-142">Начиная с [обновления Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [сотрудники служб поддерживаются в элементе управления WebView](/microsoft-edge/dev-guide#service-workers) (в дополнение к обозревателю Microsoft EDGE и приложениям для Windows 10 с поддержкой JavaScript).</span><span class="sxs-lookup"><span data-stu-id="ac198-142">Starting with the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [service workers are supported in the WebView control](/microsoft-edge/dev-guide#service-workers) (in addition to the Microsoft Edge browser and Windows 10 apps with JavaScript).</span></span>

<span data-ttu-id="ac198-143">архитектуры приложений для архитектуры x64 требуются нейтральные (любые ЦП) или 64-разрядные пакеты, так как работники служб не поддерживаются в процессах WoW64.</span><span class="sxs-lookup"><span data-stu-id="ac198-143">x64 app architectures require Neutral (Any CPU) or x64 packages, as service workers are not supported in WoW64 processes.</span></span> <span data-ttu-id="ac198-144">(Для экономии места на диске версия WoW необходимых DLL не включена в Windows.)</span><span class="sxs-lookup"><span data-stu-id="ac198-144">(To conserve disk space, the WoW version of the required DLLs are not natively included in Windows.)</span></span>

### <span data-ttu-id="ac198-145">Модель потоков и надежность</span><span class="sxs-lookup"><span data-stu-id="ac198-145">Threading model and reliability</span></span>

<span data-ttu-id="ac198-146">Создание WebView посредством `document.createElement("x-ms-webview")` `<x-ms-webview>` разметки создает WebView в новом уникальном потоке в процессе приложения.</span><span class="sxs-lookup"><span data-stu-id="ac198-146">Creating a WebView via `document.createElement("x-ms-webview")` or via `<x-ms-webview>` markup creates a WebView on a new unique thread in the app's process.</span></span> <span data-ttu-id="ac198-147">Выполнение в новом уникальном потоке означает, что долго выполняемый сценарий из одного WebView не может зависнуть приложение или другие веб-представления.</span><span class="sxs-lookup"><span data-stu-id="ac198-147">Running on a new unique thread means that long running script from one WebView is unable to hang the app or other WebViews.</span></span> <span data-ttu-id="ac198-148">Создание WebView через `new MSWebView()` конструктор создает WebView в отдельном WebView процессе.</span><span class="sxs-lookup"><span data-stu-id="ac198-148">Creating a WebView via the `new MSWebView()` constructor creates a WebView in a separate WebView process.</span></span> <span data-ttu-id="ac198-149">Выполнение в уникальных процессах означает, что в дополнение к защите от длительно выполняемого сценария приложение также защищено от веб-содержимого, которое не зависает в процессе WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-149">Running in a unique process means that in addition to protection from long running script, the app is also protected from web content that crashes the WebView process.</span></span> <span data-ttu-id="ac198-150">Создание WebView с помощью [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) метода также создает WebView в отдельном процессе, но позволяет вызывающему объекту больше управлять параметрами процесса и группового просмотра в WebView процессах.</span><span class="sxs-lookup"><span data-stu-id="ac198-150">Creating a WebView via the [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) method also creates a WebView in a separate process but allows the caller more control over process settings and grouping WebViews in WebView processes.</span></span> <span data-ttu-id="ac198-151">Дополнительные сведения см. в статье `MSWebViewProcess`.</span><span class="sxs-lookup"><span data-stu-id="ac198-151">See `MSWebViewProcess` for more information.</span></span> 

### <span data-ttu-id="ac198-152">Доступ к API WinRT</span><span class="sxs-lookup"><span data-stu-id="ac198-152">WinRT API access</span></span>

<span data-ttu-id="ac198-153">Приложение UWP может допускает доступ документов HTML в веб-представлениях к API-интерфейсам WinRT.</span><span class="sxs-lookup"><span data-stu-id="ac198-153">A UWP app may allow HTML documents inside WebViews to have access to WinRT APIs.</span></span> <span data-ttu-id="ac198-154">Это осуществляется с помощью атрибута WindowsRuntimeAccess дочерних элементов правила для элемента ApplicationContentUriRules в AppxManifest. XML приложения UWP.</span><span class="sxs-lookup"><span data-stu-id="ac198-154">This is via the WindowsRuntimeAccess attribute of the Rule child elements of the ApplicationContentUriRules element of the AppxManifest.xml of the UWP app.</span></span> <span data-ttu-id="ac198-155">Установить для WindowsRuntimeAccess значение "все", а документы HTML с соответствующими URI будут разрешены использовать WinRT.</span><span class="sxs-lookup"><span data-stu-id="ac198-155">Set WindowsRuntimeAccess to 'all' and HTML documents with matching URIs will be allowed to use WinRT.</span></span> <span data-ttu-id="ac198-156">Это то же, что и предоставление доступа к контенту HTML в приложениях UWP в JavaScript, поэтому для получения дополнительных сведений ознакомьтесь [с API вызова WinRT из PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) .</span><span class="sxs-lookup"><span data-stu-id="ac198-156">This is the same as providing WinRT access to HTML content in JavaScript UWP apps so see [Call WinRT APIs from your PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) for more information.</span></span>

<span data-ttu-id="ac198-157">API-интерфейсы WinRT, связанные с пользовательским интерфейсом, могут не работать при вызове из WebView, запущенного на своем собственном потоке, но может работать при вызове из WebView, выполняющегося в отдельном WebView процессе.</span><span class="sxs-lookup"><span data-stu-id="ac198-157">UI related WinRT APIs may not work when called from a WebView running on its own thread but may work when called from a WebView running in a separate WebView process.</span></span> <span data-ttu-id="ac198-158">При использовании WebView для собственного уникального потока этот поток не является потоком представления приложения.</span><span class="sxs-lookup"><span data-stu-id="ac198-158">When using a WebView on its own unique thread, that thread is not the app's view thread.</span></span> <span data-ttu-id="ac198-159">Некоторые API-интерфейсы WinRT, связанные с пользовательским интерфейсом, должны вызываться из потока представления приложения.</span><span class="sxs-lookup"><span data-stu-id="ac198-159">Some UI related WinRT APIs require to be called from the app's view thread.</span></span> <span data-ttu-id="ac198-160">Представления веб-приложения, созданные в отдельном WebView процессе, выполняются для потока представления и не должны иметь те же ограничения, что и WebView, запущенные для собственного уникального потока.</span><span class="sxs-lookup"><span data-stu-id="ac198-160">WebViews created in a separate WebView process do run on a view thread and so should not face the same restrictions as WebView's running on their own unique thread.</span></span> <span data-ttu-id="ac198-161">Если у вас возникли проблемы с API-интерфейсами, относящимися к пользовательскому интерфейсу, в WebView убедитесь в том, что вы используете WebView в своем собственном процессе WebView, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="ac198-161">If you have trouble with UI related WinRT APIs in a WebView ensure that you're using a WebView in its own WebView process as described above.</span></span>

### <span data-ttu-id="ac198-162">Ограничения хранилища AppCache</span><span class="sxs-lookup"><span data-stu-id="ac198-162">AppCache storage limitations</span></span>

<span data-ttu-id="ac198-163">В приложениях, использующих поддержку JavaScript API кэша приложения (или AppCache), как определено в [спецификации HTML5](https://go.microsoft.com/fwlink/p/?LinkId=228542), для создания автономных веб-приложений необходимо учитывать ограничения на доступ к хранилищу.</span><span class="sxs-lookup"><span data-stu-id="ac198-163">Applications using JavaScript support of the Application Cache API (or AppCache), as defined in the [HTML5 specification](https://go.microsoft.com/fwlink/p/?LinkId=228542), to create offline web applications must observe available storage limitations.</span></span> <span data-ttu-id="ac198-164">Особенно это относится к устройствам с ограниченным объемом памяти.</span><span class="sxs-lookup"><span data-stu-id="ac198-164">This is especially true in devices with limited memory space.</span></span> <span data-ttu-id="ac198-165">Практические ограничения на размер AppCache всегда являются функцией доступного места для дискового хранилища.</span><span class="sxs-lookup"><span data-stu-id="ac198-165">The practical limits on the size of the AppCache are always a function of available disk storage space.</span></span> <span data-ttu-id="ac198-166">Общие рекомендации указаны ниже.</span><span class="sxs-lookup"><span data-stu-id="ac198-166">The general guidelines are shown below.</span></span>

| <span data-ttu-id="ac198-167">Размер тома</span><span class="sxs-lookup"><span data-stu-id="ac198-167">Volume size</span></span>         |<span data-ttu-id="ac198-168">AppCache на домен</span><span class="sxs-lookup"><span data-stu-id="ac198-168">AppCache per domain</span></span> | <span data-ttu-id="ac198-169">AppCache для каждого пользователя</span><span class="sxs-lookup"><span data-stu-id="ac198-169">AppCache per user</span></span>   | 
|---------------|---------------|-------------------------|
<span data-ttu-id="ac198-170">До 4 Гбайт</span><span class="sxs-lookup"><span data-stu-id="ac198-170">Up to 4GB</span></span> | <span data-ttu-id="ac198-171">СВЯЗЬ</span><span class="sxs-lookup"><span data-stu-id="ac198-171">10MB</span></span> | <span data-ttu-id="ac198-172">50 МБ</span><span class="sxs-lookup"><span data-stu-id="ac198-172">50MB</span></span> |
<span data-ttu-id="ac198-173">4 ГБ – 16 ГБ</span><span class="sxs-lookup"><span data-stu-id="ac198-173">4GB to 16GB</span></span> | <span data-ttu-id="ac198-174">50 МБ</span><span class="sxs-lookup"><span data-stu-id="ac198-174">50MB</span></span> | <span data-ttu-id="ac198-175">500MB</span><span class="sxs-lookup"><span data-stu-id="ac198-175">500MB</span></span> | 
<span data-ttu-id="ac198-176">от 16 до 32 ГБ</span><span class="sxs-lookup"><span data-stu-id="ac198-176">16GB to 32 GB</span></span> | <span data-ttu-id="ac198-177">50 МБ</span><span class="sxs-lookup"><span data-stu-id="ac198-177">50MB</span></span> | <span data-ttu-id="ac198-178">Гбайт</span><span class="sxs-lookup"><span data-stu-id="ac198-178">1GB</span></span> |

<span data-ttu-id="ac198-179">Все приложения Windows10 должны использовать одну и ту же модель квоты AppCache, поэтому доступное ограничение дискового пространства распространяется на приложения для настольных компьютеров и для телефонов.</span><span class="sxs-lookup"><span data-stu-id="ac198-179">All Windows10 apps are intended to use the same AppCache quota model, so the available disk storage limitation applies to both desktop and phone apps.</span></span> <span data-ttu-id="ac198-180">Кроме того, при использовании страниц, загруженных внутри **WebView** , на жестком диске занимают 1 ГБ *AppCache* места. запросы на дополнительное хранилище *AppCache* выше этого ограничения будут отвергнуты.</span><span class="sxs-lookup"><span data-stu-id="ac198-180">The is also a hard limit after pages loaded inside **WebView** together have consumed 1 GB of *AppCache* space; requests for additional *AppCache* storage above this limit will be denied.</span></span> 

<span data-ttu-id="ac198-181">Дополнительные сведения можно найти в разделе [Пример элемента управления WebView HTML](https://go.microsoft.com/fwlink/p/?linkid=309825) и JSBrowser с документацией по [элементу управления WebView](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) .</span><span class="sxs-lookup"><span data-stu-id="ac198-181">For more information, see the [HTML WebView control sample](https://go.microsoft.com/fwlink/p/?linkid=309825) and the JSBrowser's [Harnessing the WebView control](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) documentation.</span></span>

## <span data-ttu-id="ac198-182">События</span><span class="sxs-lookup"><span data-stu-id="ac198-182">Events</span></span>

### <span data-ttu-id="ac198-183">departingFocus</span><span class="sxs-lookup"><span data-stu-id="ac198-183">departingFocus</span></span>

<span data-ttu-id="ac198-184">Указывает на то, что фокус не входит в **WebView** в приложение.</span><span class="sxs-lookup"><span data-stu-id="ac198-184">Indicates focus departing from the **webview** into the app.</span></span> <span data-ttu-id="ac198-185">Активируется, когда документ верхнего уровня WebView вызывает Window. departFocus.</span><span class="sxs-lookup"><span data-stu-id="ac198-185">Fires when the webview's top level document calls window.departFocus.</span></span> <span data-ttu-id="ac198-186">Аргументы FocusNavigationEvent в событии departingFocus совпадают с параметрами, предоставленными departFocus, за исключением того, что параметры начала переводятся из document's координатного пространства WebView в пространство координат в документе хоста WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-186">The FocusNavigationEvent args in the departingFocus event match the parameters provided to departFocus except the origin parameters are translated from the webview's document's coordinate space to the coordinate space of the webview host document.</span></span> <span data-ttu-id="ac198-187">Просмотрите метод WebView. navigateFocus и соответствующее событие окна navigatingFocus для перемещения фокуса с узла на WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-187">See the webview.navigateFocus method and corresponding window navigatingFocus event for transferring focus from host to webview.</span></span> <span data-ttu-id="ac198-188">В этой статье приведены примеры реализации навигации по фокусу с помощью клавиатуры или игрового планшета, обрабатывающего данное событие, в [библиотеке навигации направления TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .</span><span class="sxs-lookup"><span data-stu-id="ac198-188">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that handles this event.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```

#### <span data-ttu-id="ac198-189">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-189">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-190">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-190">Interface</span></span>** | [<span data-ttu-id="ac198-191">FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-191">FocusNavigationEvent</span></span>](./webview/FocusNavigationEvent.md) |
|**<span data-ttu-id="ac198-192">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-192">Synchronous</span></span>** |<span data-ttu-id="ac198-193">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-193">Yes</span></span> |    
|**<span data-ttu-id="ac198-194">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-194">Bubbles</span></span>**     |<span data-ttu-id="ac198-195">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-195">Yes</span></span> |   
|**<span data-ttu-id="ac198-196">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-196">Cancelable</span></span>**  |<span data-ttu-id="ac198-197">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-197">No</span></span> |            

### <span data-ttu-id="ac198-198">MSWebViewContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="ac198-198">MSWebViewContainsFullScreenElementChanged</span></span>

<span data-ttu-id="ac198-199">Возникает при изменении состояния, если **WebView** в настоящее время включает элемент на весь экран.</span><span class="sxs-lookup"><span data-stu-id="ac198-199">Occurs when the status changes of whether or not the **webview** currently contains a full screen element.</span></span> <span data-ttu-id="ac198-200">Используйте свойство containsFullScreenElement для текущего значения.</span><span class="sxs-lookup"><span data-stu-id="ac198-200">Use the containsFullScreenElement property to the current value.</span></span> <span data-ttu-id="ac198-201">Элемент "полный экран" — это представление полного элемента [API DOM](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) с помощью функций DOM Elements. requestFullScreen и Document. exitFullScreen.</span><span class="sxs-lookup"><span data-stu-id="ac198-201">Full screen element here refers to the [Fullscreen DOM APIs](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) notion of a full screen element via the element.requestFullScreen and document.exitFullScreen DOM functions.</span></span>

```js
function containsFullScreenElementChangedHandler(eventInfo) {
    const applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
    if (webview.containsFullScreenElement) {
        webview.classList.add("fullscreen"); // Have the webview fill the app view
        applicationView.tryEnterFullScreenMode(); // Have the app view fill the screen
    }
    else {
        webview.classList.remove("fullscreen"); // Return webview to normal
        applicationView.exitFullScreenMode(); // Return app view to normal
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
webview.removeEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
```

#### <span data-ttu-id="ac198-202">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-202">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-203">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-203">Interface</span></span>** | **<span data-ttu-id="ac198-204">Событие</span><span class="sxs-lookup"><span data-stu-id="ac198-204">Event</span></span>** |
|**<span data-ttu-id="ac198-205">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-205">Synchronous</span></span>** |<span data-ttu-id="ac198-206">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-206">Yes</span></span> |    
|**<span data-ttu-id="ac198-207">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-207">Bubbles</span></span>**     |<span data-ttu-id="ac198-208">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-208">No</span></span> |   
|**<span data-ttu-id="ac198-209">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-209">Cancelable</span></span>**  |<span data-ttu-id="ac198-210">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-210">No</span></span> |  

### <span data-ttu-id="ac198-211">MSWebViewContentLoading</span><span class="sxs-lookup"><span data-stu-id="ac198-211">MSWebViewContentLoading</span></span>

<span data-ttu-id="ac198-212">Указывает на то, что содержимое HTML загружается и загружается в элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ac198-212">Indicates that the HTML content is downloaded and is being loaded into the control.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```

#### <span data-ttu-id="ac198-213">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-213">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-214">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-214">Interface</span></span>** | [<span data-ttu-id="ac198-215">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-215">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="ac198-216">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-216">Synchronous</span></span>** |<span data-ttu-id="ac198-217">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-217">Yes</span></span>  |    
|**<span data-ttu-id="ac198-218">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-218">Bubbles</span></span>**     |<span data-ttu-id="ac198-219">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-219">No</span></span> |   
|**<span data-ttu-id="ac198-220">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-220">Cancelable</span></span>**  |<span data-ttu-id="ac198-221">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-221">No</span></span> |    

### <span data-ttu-id="ac198-222">MSWebViewDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="ac198-222">MSWebViewDOMContentLoaded</span></span>

<span data-ttu-id="ac198-223">Указывает на то, что основные элементы DOM завершили загрузку.</span><span class="sxs-lookup"><span data-stu-id="ac198-223">Indicates that the main DOM elements have finished loading.</span></span>


```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```

#### <span data-ttu-id="ac198-224">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-224">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-225">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-225">Interface</span></span>** | [<span data-ttu-id="ac198-226">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-226">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="ac198-227">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-227">Synchronous</span></span>** |<span data-ttu-id="ac198-228">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-228">Yes</span></span>  |    
|**<span data-ttu-id="ac198-229">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-229">Bubbles</span></span>**     |<span data-ttu-id="ac198-230">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-230">No</span></span> |   
|**<span data-ttu-id="ac198-231">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-231">Cancelable</span></span>**  |<span data-ttu-id="ac198-232">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-232">No</span></span> |                 

### <span data-ttu-id="ac198-233">MSWebViewFrameContentLoading</span><span class="sxs-lookup"><span data-stu-id="ac198-233">MSWebViewFrameContentLoading</span></span>

<span data-ttu-id="ac198-234">Указывает на то, что содержимое HTML загружено и загружено в `<iframe>` элемент управления.</span><span class="sxs-lookup"><span data-stu-id="ac198-234">Indicates that the HTML content downloaded and is being loaded into the `<iframe>` control.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```

#### <span data-ttu-id="ac198-235">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-235">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-236">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-236">Interface</span></span>** | [<span data-ttu-id="ac198-237">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-237">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="ac198-238">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-238">Synchronous</span></span>** |<span data-ttu-id="ac198-239">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-239">Yes</span></span>  |    
|**<span data-ttu-id="ac198-240">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-240">Bubbles</span></span>**     |<span data-ttu-id="ac198-241">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-241">No</span></span> |   
|**<span data-ttu-id="ac198-242">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-242">Cancelable</span></span>**  |<span data-ttu-id="ac198-243">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-243">No</span></span> |                 

### <span data-ttu-id="ac198-244">MSWebViewFrameDOMContentLoaded</span><span class="sxs-lookup"><span data-stu-id="ac198-244">MSWebViewFrameDOMContentLoaded</span></span>

<span data-ttu-id="ac198-245">Указывает на то, что основные элементы DOM завершили загрузку в `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="ac198-245">Indicates that the main DOM elements have finished loading in the `<iframe>`.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```

#### <span data-ttu-id="ac198-246">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-246">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-247">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-247">Interface</span></span>** | [<span data-ttu-id="ac198-248">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-248">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="ac198-249">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-249">Synchronous</span></span>** |<span data-ttu-id="ac198-250">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-250">Yes</span></span>  |    
|**<span data-ttu-id="ac198-251">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-251">Bubbles</span></span>**     |<span data-ttu-id="ac198-252">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-252">No</span></span> |   
|**<span data-ttu-id="ac198-253">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-253">Cancelable</span></span>**  |<span data-ttu-id="ac198-254">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-254">No</span></span> |    


### <span data-ttu-id="ac198-255">MSWebViewFrameNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="ac198-255">MSWebViewFrameNavigationCompleted</span></span>

<span data-ttu-id="ac198-256">Указывает на то, что Навигация завершена, и все элементы мультимедиа отображаются в файле `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="ac198-256">Indicates the navigation is complete, and all media elements are rendered in the `<iframe>`.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```

#### <span data-ttu-id="ac198-257">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-257">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-258">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-258">Interface</span></span>** | [<span data-ttu-id="ac198-259">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-259">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |
|**<span data-ttu-id="ac198-260">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-260">Synchronous</span></span>** |<span data-ttu-id="ac198-261">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-261">Yes</span></span> |    
|**<span data-ttu-id="ac198-262">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-262">Bubbles</span></span>**     |<span data-ttu-id="ac198-263">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-263">No</span></span> |   
|**<span data-ttu-id="ac198-264">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-264">Cancelable</span></span>**  |<span data-ttu-id="ac198-265">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-265">No</span></span> |       

### <span data-ttu-id="ac198-266">MSWebViewFrameNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="ac198-266">MSWebViewFrameNavigationStarting</span></span>

<span data-ttu-id="ac198-267">Указывает, что `<iframe>` начинается Навигация в **WebView** .</span><span class="sxs-lookup"><span data-stu-id="ac198-267">Indicates a `<iframe>` within a **webview** is starting to navigate.</span></span> <span data-ttu-id="ac198-268">Это происходит перед получением каких – либо ресурсов из сети для навигации.</span><span class="sxs-lookup"><span data-stu-id="ac198-268">This is fired before obtaining any resources from the network for the navigation.</span></span> <span data-ttu-id="ac198-269">Навигация не будет запущена, пока все обработчики событий MSWebViewFrameNavigationStarting не будут завершены.</span><span class="sxs-lookup"><span data-stu-id="ac198-269">The navigation is not started until all MSWebViewFrameNavigationStarting event handlers complete.</span></span> <span data-ttu-id="ac198-270">Это событие можно отменить через вызов `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="ac198-270">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span> <span data-ttu-id="ac198-271">Если вы отменили, WebView не будет выполнять навигацию.</span><span class="sxs-lookup"><span data-stu-id="ac198-271">If cancelled, the WebView will not perform the navigation.</span></span>


```js
function frameNavigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
webview.removeEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
```

#### <span data-ttu-id="ac198-272">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-272">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-273">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-273">Interface</span></span>** | [<span data-ttu-id="ac198-274">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-274">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="ac198-275">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-275">Synchronous</span></span>** |<span data-ttu-id="ac198-276">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-276">Yes</span></span>  |    
|**<span data-ttu-id="ac198-277">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-277">Bubbles</span></span>**     |<span data-ttu-id="ac198-278">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-278">No</span></span> |   
|**<span data-ttu-id="ac198-279">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-279">Cancelable</span></span>**  |<span data-ttu-id="ac198-280">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-280">Yes</span></span> |                 
          
### <span data-ttu-id="ac198-281">MSWebViewLongRunningScriptDetected</span><span class="sxs-lookup"><span data-stu-id="ac198-281">MSWebViewLongRunningScriptDetected</span></span>

<span data-ttu-id="ac198-282">Периодически возникает в **WebView**, что позволяет прервать выполнение сценария.</span><span class="sxs-lookup"><span data-stu-id="ac198-282">Occurs periodically during uninterrupted script execution in the **webview**, letting you halt the script.</span></span>

```js
function handler(eventInfo) {
    const stopPageScriptThreshold = 5 * 1000;
    if (eventInfo.executionTime > stopPageScriptThreshold) {
        eventInfo.stopPageScriptExecution = true; // Stop the long running script if it goes over our threshold
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewLongRunningScriptDetected", handler);
webview.removeEventListener("MSWebViewLongRunningScriptDetected", handler);
```

#### <span data-ttu-id="ac198-283">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-283">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-284">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-284">Interface</span></span>** | [<span data-ttu-id="ac198-285">LongRunningScriptDetectedEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-285">LongRunningScriptDetectedEvent</span></span>](./webview/LongRunningScriptDetectedEvent.md) |
|**<span data-ttu-id="ac198-286">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-286">Synchronous</span></span>** |<span data-ttu-id="ac198-287">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-287">Yes</span></span> |    
|**<span data-ttu-id="ac198-288">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-288">Bubbles</span></span>**     |<span data-ttu-id="ac198-289">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-289">No</span></span> |   
|**<span data-ttu-id="ac198-290">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-290">Cancelable</span></span>**  |<span data-ttu-id="ac198-291">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-291">No</span></span> |            

### <span data-ttu-id="ac198-292">MSWebViewNavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="ac198-292">MSWebViewNavigationCompleted</span></span>

<span data-ttu-id="ac198-293">Указывает на то, что Навигация завершена, и все элементы мультимедиа отображаются либо произошла ошибка навигации.</span><span class="sxs-lookup"><span data-stu-id="ac198-293">Indicates the navigation is complete, and all media elements are rendered or there was a navigation error.</span></span> <span data-ttu-id="ac198-294">Убедитесь в том, что навигация была выполнена успешно, а свойство webErrorStatus для сведений об ошибке навигации — в свойстве "событие".</span><span class="sxs-lookup"><span data-stu-id="ac198-294">Check the event args isSuccess property to tell if the navigation was successful and the webErrorStatus property for details on the navigation error.</span></span> <span data-ttu-id="ac198-295">Ошибки навигации могут возникать перед получением содержимого из сети для экземпляра, если имя узла URI не разрешается, в этом случае событие MSWebViewNavigationStarted будет срабатывать после события MSWebViewNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="ac198-295">Navigation errors can occur before obtaining any content from the network for instance if the hostname of a URI does not resolve in which case the MSWebViewNavigationStarted event will fire followed by the MSWebViewNavigationCompleted event.</span></span> <span data-ttu-id="ac198-296">Ошибки навигации также могут возникать после получения страницы ошибки на веб-сервере (например, страница 404 на HTTP-сервере, в этом случае все события навигации будут срабатывать, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded, а затем MSWebViewNavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="ac198-296">Navigation errors may also occur after receiving an error page from a web server, for instance a 404 page from an HTTP server in which case all navigation events will fire, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded, and then MSWebViewNavigationCompleted.</span></span> <span data-ttu-id="ac198-297">Чтобы предоставить страницу ошибки навигации приложения для случаев, когда веб-сервер не предоставил страницу ошибки, необходимо проверить, не была ли MSWebViewContentLoading выполнена для неудачной навигации, указывающей на то, что сервер не предоставил страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="ac198-297">To provide an app navigation error page for cases where the web server hasn't provided an error page, you'll need to check if MSWebViewContentLoading hasn't fired for a failed navigation which indicates there is no server provided error page.</span></span>

```js
let hasContent = false;
webview.addEventListener("MSWebViewNavigationStarting", () => { hasContent = false; });
webview.addEventListener("MSWebViewContentLoading", () => { hasContent = true; });

webview.addEventListener("MSWebViewNavigationCompleted", navigationCompletedEventArgs => {
    // Navigation failures may or may not come after getting an error page from the web server.
    // We keep track of the ContentLoading event with hasContent to tell if we have an error page from the server.
    // So we only navigate to our app error page when there's no server provided error page.
    if (!navigationCompletedEventArgs.isSuccess && !hasContent) {
        // Pass our failed URI and error details in the query and the error page script can read it as appropriate.
        webview.navigate("ms-appx-web:///appErrorPage.html?" + 
            "uri=" + encodeURIComponent(navigationCompletedEventArgs.uri) + "&" +
            "webErrorStatus=" + encodeURIComponent(navigationCompletedEventArgs.webErrorStatus));
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationCompleted", handler);
webview.removeEventListener("MSWebViewNavigationCompleted", handler);
```

#### <span data-ttu-id="ac198-298">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-298">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-299">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-299">Interface</span></span>** | [<span data-ttu-id="ac198-300">NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-300">NavigationCompletedEvent</span></span>](./webview/NavigationCompletedEvent.md) |
|**<span data-ttu-id="ac198-301">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-301">Synchronous</span></span>** |<span data-ttu-id="ac198-302">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-302">Yes</span></span>  |    
|**<span data-ttu-id="ac198-303">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-303">Bubbles</span></span>**     |<span data-ttu-id="ac198-304">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-304">No</span></span> |   
|**<span data-ttu-id="ac198-305">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-305">Cancelable</span></span>**  |<span data-ttu-id="ac198-306">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-306">No</span></span> |                 
         

### <span data-ttu-id="ac198-307">MSWebViewNavigationStarting</span><span class="sxs-lookup"><span data-stu-id="ac198-307">MSWebViewNavigationStarting</span></span>

<span data-ttu-id="ac198-308">Указывает, что **WebView** начинает навигацию.</span><span class="sxs-lookup"><span data-stu-id="ac198-308">Indicates the **webview** is starting to navigate.</span></span> <span data-ttu-id="ac198-309">Это происходит перед получением каких – либо ресурсов из сети для навигации.</span><span class="sxs-lookup"><span data-stu-id="ac198-309">This is fired before obtaining any resources from the network for the navigation.</span></span> <span data-ttu-id="ac198-310">Навигация не будет запущена, пока все обработчики событий MSWebViewNavigationStarting не будут завершены.</span><span class="sxs-lookup"><span data-stu-id="ac198-310">The navigation is not started until all MSWebViewNavigationStarting event handlers complete.</span></span> <span data-ttu-id="ac198-311">Это событие можно отменить через вызов `eventArgs.preventDefault()` .</span><span class="sxs-lookup"><span data-stu-id="ac198-311">This event is cancellable via calling `eventArgs.preventDefault()`.</span></span> <span data-ttu-id="ac198-312">Если вы отменили, WebView не будет выполнять навигацию.</span><span class="sxs-lookup"><span data-stu-id="ac198-312">If cancelled, the WebView will not perform the navigation.</span></span>


```js
function navigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
webview.removeEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
```

#### <span data-ttu-id="ac198-313">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-313">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-314">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-314">Interface</span></span>** | [<span data-ttu-id="ac198-315">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-315">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="ac198-316">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-316">Synchronous</span></span>** |<span data-ttu-id="ac198-317">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-317">No</span></span>  |    
|**<span data-ttu-id="ac198-318">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-318">Bubbles</span></span>**     |<span data-ttu-id="ac198-319">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-319">Yes</span></span> |   
|**<span data-ttu-id="ac198-320">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-320">Cancelable</span></span>**  |<span data-ttu-id="ac198-321">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-321">Yes</span></span> |      

### <span data-ttu-id="ac198-322">MSWebViewNewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="ac198-322">MSWebViewNewWindowRequested</span></span>

<span data-ttu-id="ac198-323">Вызывается, когда содержимое в **WebView** пытается открыть новое окно.</span><span class="sxs-lookup"><span data-stu-id="ac198-323">Raised when content in **webview** is trying to open a new window.</span></span> <span data-ttu-id="ac198-324">Если событие не отменено, WebView запустит URI нового запроса окна в браузере пользователя по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ac198-324">If the event isn't cancelled the webview will launch the URI of the new window request in the user's default browser.</span></span>

```js
function handler(eventInfo) {
    // Prevent the webview from opening URIs in the default browser.
    eventInfo.preventDefault();
    
    // Only allow https://example.com/ to open new windows.
    if (eventInfo.referer === "https://example.com/") {
        // Perform some custom handling of the URI.
        openUri(eventInfo.uri);
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNewWindowRequested", handler);
webview.removeEventListener("MSWebViewNewWindowRequested", handler);
```

#### <span data-ttu-id="ac198-325">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-325">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-326">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-326">Interface</span></span>** | [<span data-ttu-id="ac198-327">NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="ac198-327">NavigationEventWithReferrer</span></span>](./webview/NavigationEventWithReferrer.md) |
|**<span data-ttu-id="ac198-328">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-328">Synchronous</span></span>** |<span data-ttu-id="ac198-329">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-329">Yes</span></span>  |    
|**<span data-ttu-id="ac198-330">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-330">Bubbles</span></span>**     |<span data-ttu-id="ac198-331">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-331">No</span></span> |   
|**<span data-ttu-id="ac198-332">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-332">Cancelable</span></span>**  |<span data-ttu-id="ac198-333">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-333">Yes</span></span> |                 
           

### <span data-ttu-id="ac198-334">MSWebViewPermissionRequested</span><span class="sxs-lookup"><span data-stu-id="ac198-334">MSWebViewPermissionRequested</span></span>

<span data-ttu-id="ac198-335">Указывает на то, что содержимое в **WebView** пытается получить доступ к функциональным возможностям (например, географическое расположение или доступ к блокировкам указателей), для которых обычно требуются разрешения конечных пользователей.</span><span class="sxs-lookup"><span data-stu-id="ac198-335">Indicates that content in the **webview**  is trying to access functionality (such as geolocation, or pointer lock access) that normally requires end-user permissions.</span></span> <span data-ttu-id="ac198-336">Если обработчик событий не зарегистрирован или обработчик событий не вызывает eventArgs. permissionRequest. Allow (), отсрочка () или Deny (), по умолчанию запрос разрешения будет отвергнут.</span><span class="sxs-lookup"><span data-stu-id="ac198-336">If no event handler is registered or if the event handler doesn't call eventArgs.permissionRequest.allow(), defer(), or deny(), then by default the permission request will be denied.</span></span> <span data-ttu-id="ac198-337">Если вам нужно решить, разрешено или запрещено ли разрешение асинхронно для экземпляра, если вам нужно запрашивать пользователя, используйте eventArgs. permissionRequest. Отсрочка ().</span><span class="sxs-lookup"><span data-stu-id="ac198-337">If you need to decide if permission is allowed or denied asynchronously for instance if you need to prompt the user, use eventArgs.permissionRequest.defer().</span></span> <span data-ttu-id="ac198-338">Запрос на разрешение будет отложен до тех пор, пока не будет использоваться WebView. getDeferredPermissionRequestById или WebView. getDeferredPermissionRequests и метод Allow () или Deny () в DeferredPermissionRequest с соответствующим значением идентификатора.</span><span class="sxs-lookup"><span data-stu-id="ac198-338">The permission request will be deferred until you use webview.getDeferredPermissionRequestById or webview.getDeferredPermissionRequests and call allow() or deny() on the DeferredPermissionRequest with the corresponding id value.</span></span>

```js
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});

// addEventListener syntax
webview.addEventListener("MSWebViewPermissionRequested", handler);
webview.removeEventListener("MSWebViewPermissionRequested", handler);
```

#### <span data-ttu-id="ac198-339">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-339">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-340">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-340">Interface</span></span>** | [<span data-ttu-id="ac198-341">PermissionRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-341">PermissionRequestedEvent</span></span>](./webview/PermissionRequestedEvent.md) |
|**<span data-ttu-id="ac198-342">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-342">Synchronous</span></span>** |<span data-ttu-id="ac198-343">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-343">Yes</span></span>  |    
|**<span data-ttu-id="ac198-344">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-344">Bubbles</span></span>**     |<span data-ttu-id="ac198-345">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-345">No</span></span> |   
|**<span data-ttu-id="ac198-346">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-346">Cancelable</span></span>**  |<span data-ttu-id="ac198-347">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-347">No</span></span> |    


### <span data-ttu-id="ac198-348">MSWebViewProcessExited</span><span class="sxs-lookup"><span data-stu-id="ac198-348">MSWebViewProcessExited</span></span>

<span data-ttu-id="ac198-349">Указывает на то, что компонент **WebView** Process crashsed.</span><span class="sxs-lookup"><span data-stu-id="ac198-349">Indicates that the **webview** component process crashsed.</span></span> <span data-ttu-id="ac198-350">Это относится только к незавершенному WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-350">This is only relevant for an out-of-process WebView.</span></span> <span data-ttu-id="ac198-351">Ознакомьтесь с разделом "Примечания", чтобы создать WebView, не являющиеся процессами, а не попроцессными WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-351">See the Remarks section for how to create an out-of-process WebView as opposed to an in-process WebView.</span></span> <span data-ttu-id="ac198-352">После того как это событие срабатывает, соответствующая WebView будет переведена в состояние сбоя.</span><span class="sxs-lookup"><span data-stu-id="ac198-352">After this event fires, the corresponding WebView is put into a crashed state.</span></span> <span data-ttu-id="ac198-353">Вызов большинства специальных методов WebView или доступ к большинству WebView определенных свойств в случае сбоя WebView приведет к созданию исключения.</span><span class="sxs-lookup"><span data-stu-id="ac198-353">Calling most WebView specific methods or accessing most WebView specific properties on a crashed WebView will throw an exception.</span></span> <span data-ttu-id="ac198-354">Чтобы восстановить состояние после этого события, удалите сбойный WebView из DOM и замените его новым WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-354">To recover from this event, remove the crashed WebView from the DOM and replace it with a new WebView.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```

#### <span data-ttu-id="ac198-355">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-355">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-356">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-356">Interface</span></span>** | **<span data-ttu-id="ac198-357">Событие</span><span class="sxs-lookup"><span data-stu-id="ac198-357">Event</span></span>** |
|**<span data-ttu-id="ac198-358">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-358">Synchronous</span></span>** |<span data-ttu-id="ac198-359">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-359">Yes</span></span> |    
|**<span data-ttu-id="ac198-360">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-360">Bubbles</span></span>**     |<span data-ttu-id="ac198-361">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-361">No</span></span> |   
|**<span data-ttu-id="ac198-362">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-362">Cancelable</span></span>**  |<span data-ttu-id="ac198-363">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-363">No</span></span> |      


### <span data-ttu-id="ac198-364">MSWebViewWebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="ac198-364">MSWebViewWebResourceRequested</span></span>

<span data-ttu-id="ac198-365">Вызывается, когда страница внутри элемента **WebView** запрашивает ресурс.</span><span class="sxs-lookup"><span data-stu-id="ac198-365">Raised when a page inside the **webview** element requests a resource.</span></span>

```js
// A handler that completes synchronously with a custom HTTP response built from a string.
function handlerWithSyncString(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        const Http = Windows.Web.Http;
        // Create the custom response using a string
        webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(Http.HttpStatusCode.ok);
        webResourceRequestedEventArgs.args.response.content = new Http.HttpStringContent("<H1>Example</H1>");
    }
});

// A more complicated handler that completes asynchronously with a custom HTTP response built from a stream.
function handlerWithAsyncStream(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        // Take a deferral on the WebResourceRequested event so that we can create the custom HTTP response asynchronously.
        const deferral = webResourceRequestedEventArgs.args.getDeferral();

        // Use fetch to get a Blob of the content of the URI
        fetch("ms-appx:///replacement.html").then(fetchResponse => {
            return fetchResponse.blob();
        }).then(fetchResponseBlob => {
            const Http = Windows.Web.Http;
            webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(
                Http.HttpStatusCode.ok);

            // Use Blob.msDetachStream to convert the Blob to a Windows.Storage.Streams.IInputStream
            webResourceRequestedEventArgs.args.response.content = new Http.HttpStreamContent(
                fetchResponseBlob.msDetachStream());

        }).finally(() => {
            // Use a finally call to complete the deferral so even if there is an error we will unblock the event.
            deferral.complete();
        });
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewWebResourceRequested", handler);
webview.removeEventListener("MSWebViewWebResourceRequested", handler);
```

#### <span data-ttu-id="ac198-366">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-366">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-367">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-367">Interface</span></span>** | [<span data-ttu-id="ac198-368">WebResourceRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-368">WebResourceRequestedEvent</span></span>](./webview/WebResourceRequestedEvent.md) |
|**<span data-ttu-id="ac198-369">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-369">Synchronous</span></span>** |<span data-ttu-id="ac198-370">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-370">Yes</span></span> |    
|**<span data-ttu-id="ac198-371">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-371">Bubbles</span></span>**     |<span data-ttu-id="ac198-372">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-372">No</span></span> |   
|**<span data-ttu-id="ac198-373">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-373">Cancelable</span></span>**  |<span data-ttu-id="ac198-374">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-374">No</span></span> |      


### <span data-ttu-id="ac198-375">MSWebViewScriptNotify</span><span class="sxs-lookup"><span data-stu-id="ac198-375">MSWebViewScriptNotify</span></span>

<span data-ttu-id="ac198-376">Вызывается, когда страница внутри элемента **WebView** вызывает метод **Window. external. notify** .</span><span class="sxs-lookup"><span data-stu-id="ac198-376">Raised when a page inside the **webview** element calls the **window.external.notify** method.</span></span> <span data-ttu-id="ac198-377">Метод Window. external. notify доступен только для документов с URI-идентификаторами, которые соответствуют правилам в manifest's ApplicationContentUriRules или программно разрешены с помощью задания WebView. Settings. isScriptNotifyAllowed в true.</span><span class="sxs-lookup"><span data-stu-id="ac198-377">The window.external.notify method is only available to documents with URIs that match rules in the app's manifest's ApplicationContentUriRules or that has been programatically allowed via setting webview.settings.isScriptNotifyAllowed to true.</span></span> <span data-ttu-id="ac198-378">Кроме того, Window. external. notify доступен только для документов верхнего уровня WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-378">Additionally window.external.notify is only available to the webview's top level document.</span></span>

```js
webview.addEventListener("MSWebViewScriptNotify", eventInfo => {
    console.log("The URI " + eventInfo.callingUri + 
        " has sent notification " + eventInfo.value);
});

// Allow the next URI to which we navigate access to window.external.notify
webview.settings.isScriptNotifyAllowed = true;
webview.navigate("https://example.com/");

webview.addEventListener("MSWebViewNavigationCompleted", () => {
    // Inject script to the webview that will send a notification back.
    const asyncOp = webview.invokeScriptAsync("eval", "window.external.notify('example notification')");
    asyncOp.start();
});
```

#### <span data-ttu-id="ac198-379">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-379">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-380">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-380">Interface</span></span>** | [<span data-ttu-id="ac198-381">ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-381">ScriptNotifyEvent</span></span>](./webview/ScriptNotifyEvent.md) |
|**<span data-ttu-id="ac198-382">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-382">Synchronous</span></span>** |<span data-ttu-id="ac198-383">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-383">Yes</span></span>  |    
|**<span data-ttu-id="ac198-384">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-384">Bubbles</span></span>**     |<span data-ttu-id="ac198-385">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-385">No</span></span> |   
|**<span data-ttu-id="ac198-386">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-386">Cancelable</span></span>**  |<span data-ttu-id="ac198-387">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-387">No</span></span> |      

### <span data-ttu-id="ac198-388">MSWebViewUnsafeContentWarningDisplaying</span><span class="sxs-lookup"><span data-stu-id="ac198-388">MSWebViewUnsafeContentWarningDisplaying</span></span>

<span data-ttu-id="ac198-389">Возникает, когда в **WebView** показана страница предупреждения для содержимого, обнаруженного как небезопасное фильтром SmartScreen.</span><span class="sxs-lookup"><span data-stu-id="ac198-389">Occurs when the **webview** shows a warning page for content that was reported as unsafe by SmartScreen Filter.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```

#### <span data-ttu-id="ac198-390">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-390">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-391">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-391">Interface</span></span>** | **<span data-ttu-id="ac198-392">Событие</span><span class="sxs-lookup"><span data-stu-id="ac198-392">Event</span></span>** |
|**<span data-ttu-id="ac198-393">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-393">Synchronous</span></span>** |<span data-ttu-id="ac198-394">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-394">Yes</span></span> |    
|**<span data-ttu-id="ac198-395">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-395">Bubbles</span></span>**     |<span data-ttu-id="ac198-396">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-396">No</span></span> |   
|**<span data-ttu-id="ac198-397">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-397">Cancelable</span></span>**  |<span data-ttu-id="ac198-398">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-398">No</span></span> |    

### <span data-ttu-id="ac198-399">MSWebViewUnsupportedUriSchemeIdentified</span><span class="sxs-lookup"><span data-stu-id="ac198-399">MSWebViewUnsupportedUriSchemeIdentified</span></span>

<span data-ttu-id="ac198-400">Вызывается при переходе на универсальный код ресурса (URI), который не поддерживает **WebView** .</span><span class="sxs-lookup"><span data-stu-id="ac198-400">Raised when there is navigation to an Uniform Resource Identifier (URI) that the **webview** does not support.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```

#### <span data-ttu-id="ac198-401">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-401">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-402">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-402">Interface</span></span>** | [<span data-ttu-id="ac198-403">NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-403">NavigationEvent</span></span>](./webview/NavigationEvent.md) |
|**<span data-ttu-id="ac198-404">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-404">Synchronous</span></span>** |<span data-ttu-id="ac198-405">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-405">Yes</span></span>  |    
|**<span data-ttu-id="ac198-406">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-406">Bubbles</span></span>**     |<span data-ttu-id="ac198-407">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-407">No</span></span> |   
|**<span data-ttu-id="ac198-408">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-408">Cancelable</span></span>**  |<span data-ttu-id="ac198-409">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-409">Yes</span></span> |     

### <span data-ttu-id="ac198-410">MSWebViewUnviewableContentIdentified</span><span class="sxs-lookup"><span data-stu-id="ac198-410">MSWebViewUnviewableContentIdentified</span></span>

<span data-ttu-id="ac198-411">Вызывается, когда **WebView** пытается перейти к веб-контенту с неподдерживаемым типом контента.</span><span class="sxs-lookup"><span data-stu-id="ac198-411">Raised when the **webview** attempts to navigate to web content with an unsupported content type.</span></span> <span data-ttu-id="ac198-412">Например, в настоящее время PDF-файлы не поддерживаются WebView и для навигации по документам PDF они не будут перемещаться, а затем вызывать это событие.</span><span class="sxs-lookup"><span data-stu-id="ac198-412">For example, PDFs are currently not supported by webview and navigations to PDF documents will not navigate and instead raise this event.</span></span>

```js
function handler(args) {
    if (args.mediaType === "application/pdf") {
        Windows.System.Launcher.launchUriAsync(new Windows.Foundation.Uri(args.uri));
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewUnviewableContentIdentified", handler);
webview.removeEventListener("MSWebViewUnviewableContentIdentified", handler);
```

#### <span data-ttu-id="ac198-413">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="ac198-413">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-414">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="ac198-414">Interface</span></span>** | [<span data-ttu-id="ac198-415">UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="ac198-415">UnviewableContentIdentifiedEvent</span></span>](./webview/UnviewableContentIdentifiedEvent.md) |
|**<span data-ttu-id="ac198-416">Синхронный</span><span class="sxs-lookup"><span data-stu-id="ac198-416">Synchronous</span></span>** |<span data-ttu-id="ac198-417">Да</span><span class="sxs-lookup"><span data-stu-id="ac198-417">Yes</span></span>  |    
|**<span data-ttu-id="ac198-418">Давать</span><span class="sxs-lookup"><span data-stu-id="ac198-418">Bubbles</span></span>**     |<span data-ttu-id="ac198-419">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-419">No</span></span> |   
|**<span data-ttu-id="ac198-420">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="ac198-420">Cancelable</span></span>**  |<span data-ttu-id="ac198-421">Нет</span><span class="sxs-lookup"><span data-stu-id="ac198-421">No</span></span> |                 
         

## <span data-ttu-id="ac198-422">Методы</span><span class="sxs-lookup"><span data-stu-id="ac198-422">Methods</span></span>

### <span data-ttu-id="ac198-423">addWebAllowedObject</span><span class="sxs-lookup"><span data-stu-id="ac198-423">addWebAllowedObject</span></span>

<span data-ttu-id="ac198-424">Добавляет собственный объект среды выполнения Windows в качестве глобального параметра в документ верхнего уровня в **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-424">Adds a native Windows Runtime object as a global parameter to the top-level document inside of a **webview**.</span></span>

<span data-ttu-id="ac198-425">Объект не был добавлен в текущий документ, а в следующий документ верхнего уровня, в который WebView переходит.</span><span class="sxs-lookup"><span data-stu-id="ac198-425">The object is not injected into the current document, but rather the next top-level document to which the webview navigates.</span></span> <span data-ttu-id="ac198-426">Объект будет вставлен перед выполнением любого сценария HTML-документа, чтобы можно было полагаться на объект в глобальном сценарии документа.</span><span class="sxs-lookup"><span data-stu-id="ac198-426">The object is injected before any script from the HTML document runs so you can rely on the object in your document's global script.</span></span>

<span data-ttu-id="ac198-427">AddWebAllowedObject следует использовать либо во время события MSWebViewNavigationStarting, либо перед явным вызовом метода Navigate.</span><span class="sxs-lookup"><span data-stu-id="ac198-427">You should use addWebAllowedObject either during an MSWebViewNavigationStarting event or before explicitly calling a navigate method.</span></span> <span data-ttu-id="ac198-428">В этих случаях объект вставляется в документ соответствующей навигации.</span><span class="sxs-lookup"><span data-stu-id="ac198-428">In these cases the object is injected into the document of the corresponding navigation.</span></span> <span data-ttu-id="ac198-429">Звонить в какой-либо другой контекст, вы не можете быть уверены в том, какой документ вы хотите вставить в объект.</span><span class="sxs-lookup"><span data-stu-id="ac198-429">Calling it in some other context, you don't have a way to be certain into what document you'll inject your object.</span></span>

<span data-ttu-id="ac198-430">Многократное вызов addWebAllowedObject в строке приводит к вставке нескольких объектов в документ.</span><span class="sxs-lookup"><span data-stu-id="ac198-430">Calling addWebAllowedObject multiple times in a row will inject multiple objects into the document.</span></span> <span data-ttu-id="ac198-431">Если вы вызываете метод перед явным вызовом навигации, а затем снова во время соответствующего события MSWebViewNavigationStarting, оба звонка будут успешными, и вы увидите несколько объектов, которые добавлены.</span><span class="sxs-lookup"><span data-stu-id="ac198-431">If you call it both before an explicit navigate call and then again during the corresponding MSWebViewNavigationStarting event, both calls will succeed and you'll have multiple objects injected.</span></span> <span data-ttu-id="ac198-432">Если вы звоните несколько раз с одним и тем же параметром name, последний вызов WINS и предыдущие вызовы с этим именем игнорируются.</span><span class="sxs-lookup"><span data-stu-id="ac198-432">If you call multiple times with the same name parameter, the last call wins and the previous calls with that name are ignored.</span></span>

<span data-ttu-id="ac198-433">Если навигация завершается ошибкой или перенаправлена, вызовы addWebAllowedObject для этой навигации игнорируются.</span><span class="sxs-lookup"><span data-stu-id="ac198-433">If a navigate fails or is redirected, the addWebAllowedObject calls for that navigation are ignored.</span></span> <span data-ttu-id="ac198-434">Если вы хотите обрабатывать переадресацию, вы можете подписаться на событие MSWebViewNavigationStarting, чтобы перенаправлять и повторно вызвать addWebAllowedObject, в зависимости от того, какие условия подходит для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="ac198-434">If you want to handle redirects you can subscribe to the MSWebViewNavigationStarting event watch for redirects and call addWebAllowedObject again according to whatever criteria is appropriate for your application.</span></span> <span data-ttu-id="ac198-435">Аналогичным образом, после того как документ перейдет к следующему документу, вы перейдете на него, и вам потребуется явно вызвать addWebAllowedObject, если вы хотите, чтобы они переходили их.</span><span class="sxs-lookup"><span data-stu-id="ac198-435">Similarly, once a document navigates away any objects injected via addWebAllowedObject for that document will not carry over to the next document and you'll need to explicitly call addWebAllowedObject if you want them to carry over.</span></span>

<span data-ttu-id="ac198-436">Если вы вызываете addWebAllowedObject для документа, у которого нет доступа WinRT, или у него есть [AllowForWebOnly доступ через ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) , этот объект будет добавлен только в том случае, если объект имеет атрибут метаданных Windows. Foundation. Metadata. AllowForWeb.</span><span class="sxs-lookup"><span data-stu-id="ac198-436">If you call addWebAllowedObject for a document that has no WinRT access otherwise, or if it has [AllowForWebOnly access via ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) then the object will only be injected if the object has the Windows.Foundation.Metadata.AllowForWeb metadata attribute.</span></span> <span data-ttu-id="ac198-437">В противном случае введение завершится ошибкой, и в консоль разработчика JavaScript появится сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="ac198-437">Otherwise injection will fail and an error will be reported to the JavaScript developer console.</span></span> <span data-ttu-id="ac198-438">При вызове для документа, имеющего полный доступ к WinRT, этот объект будет вставлен независимо от атрибута AllowForWeb.</span><span class="sxs-lookup"><span data-stu-id="ac198-438">If called on a document that has full WinRT access, then the object will be injected regardless of the AllowForWeb attribute.</span></span> 

<span data-ttu-id="ac198-439">Кроме того, объект должен реализовывать интерфейс IAgileObject.</span><span class="sxs-lookup"><span data-stu-id="ac198-439">Additionally, the object must implement the IAgileObject interface.</span></span> <span data-ttu-id="ac198-440">Это обусловлено тем, что элементы XAML и WebView выполняются на потоках представлений ASTA приложения, а поток JavaScript WebView — это другой ASTA поток, и мы хотели бы посоветовать разработчикам приложения, чтобы убедиться, что их объект может выполняться в потоке JavaScript, не блокируя поток представления приложения, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="ac198-440">This is because the XAML and HTML webview elements run on their app's ASTA view threads and the WebView's JavaScript thread is a different ASTA thread and we want to encourage app developers to ensure their object can run on the JavaScript thread without blocking the app view thread if possible.</span></span>

<span data-ttu-id="ac198-441">Параметр Name должен быть допустимым именем свойства JavaScript, в противном случае звонок не будет выполнен автоматически.</span><span class="sxs-lookup"><span data-stu-id="ac198-441">The name parameter must be a valid JavaScript property name otherwise the call will fail silently.</span></span> <span data-ttu-id="ac198-442">Если имя имеет свойство, которое уже есть в глобальном объекте, то это свойство перезаписывается, если свойство может быть настроено.</span><span class="sxs-lookup"><span data-stu-id="ac198-442">If the name is of a property that already exists on the global object then that property is overwritten if the property is configurable.</span></span> <span data-ttu-id="ac198-443">Ненастраиваемые свойства глобального объекта не перезаписываются, а вызов addWebAllowedObject завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="ac198-443">Non-configurable properties on the global object are not overwritten and the addWebAllowedObject call fails silently.</span></span> <span data-ttu-id="ac198-444">Свойства JavaScript, созданные с помощью addWebAllowedObject, доступны для записи, настраиваемые и перечислимые.</span><span class="sxs-lookup"><span data-stu-id="ac198-444">JavaScript properties created via addWebAllowedObject are writable, configurable, and enumerable.</span></span>

```js
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```

#### <span data-ttu-id="ac198-445">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-445">Parameters</span></span>
*<span data-ttu-id="ac198-446">name</span><span class="sxs-lookup"><span data-stu-id="ac198-446">name</span></span>*
* <span data-ttu-id="ac198-447">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-447">Type: **String**</span></span>
* <span data-ttu-id="ac198-448">Имя объекта, доступного для документа в **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-448">The name of the object to expose to the document in the **webview**.</span></span>

*<span data-ttu-id="ac198-449">applicationObject</span><span class="sxs-lookup"><span data-stu-id="ac198-449">applicationObject</span></span>*
* <span data-ttu-id="ac198-450">Тип: **объект**</span><span class="sxs-lookup"><span data-stu-id="ac198-450">Type: **Object**</span></span>
* <span data-ttu-id="ac198-451">Объект, который необходимо предоставить документу в **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-451">The object to expose to the document in the **webview**.</span></span>

#### <span data-ttu-id="ac198-452">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-452">Return value</span></span>
<span data-ttu-id="ac198-453">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-453">This method does not return a value.</span></span>

#### <span data-ttu-id="ac198-454">Дополнительные функции и требования</span><span class="sxs-lookup"><span data-stu-id="ac198-454">Additional features and requirements</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-455">Минимальный поддерживаемый клиент</span><span class="sxs-lookup"><span data-stu-id="ac198-455">Minimum supported client</span></span>** |<span data-ttu-id="ac198-456">Windows10 [только для приложений Магазина Windows]</span><span class="sxs-lookup"><span data-stu-id="ac198-456">Windows10 [Windows Store apps only]</span></span> |    
|**<span data-ttu-id="ac198-457">Минимальный поддерживаемый сервер</span><span class="sxs-lookup"><span data-stu-id="ac198-457">Minimum supported server</span></span>** |<span data-ttu-id="ac198-458">Ничего не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac198-458">None supported</span></span> |   
|**<span data-ttu-id="ac198-459">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="ac198-459">Minimum supported phone</span></span>**  |<span data-ttu-id="ac198-460">Ничего не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac198-460">None supported</span></span> |  

### <span data-ttu-id="ac198-461">buildLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="ac198-461">buildLocalStreamUri</span></span>

<span data-ttu-id="ac198-462">Создает универсальный код ресурса (URI), который можно передать в [navigateToLocalStreamUri](#methods).</span><span class="sxs-lookup"><span data-stu-id="ac198-462">Creates a URI that you can pass to [navigateToLocalStreamUri](#methods).</span></span>

```js
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```

#### <span data-ttu-id="ac198-463">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-463">Parameters</span></span>
*<span data-ttu-id="ac198-464">contentIdentifier</span><span class="sxs-lookup"><span data-stu-id="ac198-464">contentIdentifier</span></span>*
* <span data-ttu-id="ac198-465">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-465">Type: **String**</span></span>
* <span data-ttu-id="ac198-466">Уникальный идентификатор содержимого, на который ссылается URI.</span><span class="sxs-lookup"><span data-stu-id="ac198-466">A unique identifier for the content the URI is referencing.</span></span> <span data-ttu-id="ac198-467">Этот элемент определяет корневой элемент универсального кода ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="ac198-467">This defines the root of the URI.</span></span>

*<span data-ttu-id="ac198-468">relativePath</span><span class="sxs-lookup"><span data-stu-id="ac198-468">relativePath</span></span>*
* <span data-ttu-id="ac198-469">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-469">Type: **String**</span></span>
* <span data-ttu-id="ac198-470">Путь к ресурсу относительно корня.</span><span class="sxs-lookup"><span data-stu-id="ac198-470">The path to the resource, relative to the root.</span></span>

#### <span data-ttu-id="ac198-471">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-471">Return value</span></span>
<span data-ttu-id="ac198-472">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-472">Type: **String**</span></span>

<span data-ttu-id="ac198-473">Универсальный код ресурса (URI), созданный путем объединения и нормализации *contentIdentifier* и *relativePath*.</span><span class="sxs-lookup"><span data-stu-id="ac198-473">The URI created by combining and normalizing the *contentIdentifier* and *relativePath*.</span></span>

#### <span data-ttu-id="ac198-474">Пример.</span><span class="sxs-lookup"><span data-stu-id="ac198-474">Example</span></span>

<span data-ttu-id="ac198-475">В следующем примере показан типичный вариант использования.</span><span class="sxs-lookup"><span data-stu-id="ac198-475">The following example illustrates a typical use case.</span></span> 

```js
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### <span data-ttu-id="ac198-476">capturePreviewToBlobAsync</span><span class="sxs-lookup"><span data-stu-id="ac198-476">capturePreviewToBlobAsync</span></span>

<span data-ttu-id="ac198-477">Создает изображение текущего [элемента WebView](./webview.md) и записывает его в указанный элемент изображения.</span><span class="sxs-lookup"><span data-stu-id="ac198-477">Creates an image of the current [webview element](./webview.md) and write it to the specified image element.</span></span>

```js
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```

#### <span data-ttu-id="ac198-478">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-478">Parameters</span></span>
<span data-ttu-id="ac198-479">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ac198-479">This method has no parameters.</span></span>

#### <span data-ttu-id="ac198-480">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-480">Return value</span></span>
<span data-ttu-id="ac198-481">Type (тип): **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="ac198-481">Type: **MSWebViewAsyncOperation**</span></span>

<span data-ttu-id="ac198-482">Объект **MSWebViewAsyncOperation** , который после его завершения предоставляет объект **BLOB** , содержащий изображение.</span><span class="sxs-lookup"><span data-stu-id="ac198-482">An **MSWebViewAsyncOperation** object that, when it completes, provides a **Blob** object that contains the image.</span></span> <span data-ttu-id="ac198-483">При использовании **capturePreviewToBlobAsync**необходимо определить обработчики успехов и ошибок после определения операции.</span><span class="sxs-lookup"><span data-stu-id="ac198-483">When using **capturePreviewToBlobAsync**, you need to define success and error handlers after defining the operation.</span></span> <span data-ttu-id="ac198-484">После применения обработчиков событий вызовите метод Start объекта [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) , чтобы выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="ac198-484">After applying the event handlers, call the start method on the [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) object to execute the operation.</span></span>

### <span data-ttu-id="ac198-485">captureSelectedContentToDataPackageAsync</span><span class="sxs-lookup"><span data-stu-id="ac198-485">captureSelectedContentToDataPackageAsync</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ac198-486">Этот метод устарел и имеет известную ошибку.</span><span class="sxs-lookup"><span data-stu-id="ac198-486">This method has been deprecated and has a known issue.</span></span> <span data-ttu-id="ac198-487">Старайтесь не использовать этот метод в рабочем коде.</span><span class="sxs-lookup"><span data-stu-id="ac198-487">Avoid using this method in your production code.</span></span> 

<span data-ttu-id="ac198-488">Асинхронно возвращает [пакет](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) данных, содержащий выбранное содержимое в **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-488">Asynchronously gets a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) that contains the selected content within the **webview**.</span></span>

```js
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```

#### <span data-ttu-id="ac198-489">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-489">Parameters</span></span>
<span data-ttu-id="ac198-490">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ac198-490">This method has no parameters.</span></span>

#### <span data-ttu-id="ac198-491">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-491">Return value</span></span>
<span data-ttu-id="ac198-492">Type (тип): **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="ac198-492">Type: **MSWebViewAsyncOperation**</span></span>

<span data-ttu-id="ac198-493">Объект **MSWebViewAsyncOperation** , который после его завершения предоставляет объект [Package](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) , содержащий изображение.</span><span class="sxs-lookup"><span data-stu-id="ac198-493">An **MSWebViewAsyncOperation** object that, when it completes, provides a [DataPackage](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) object that contains the image.</span></span> <span data-ttu-id="ac198-494">При использовании **captureSelectedContentToDataPackageAsync**необходимо определить обработчики успехов и ошибок после определения операции.</span><span class="sxs-lookup"><span data-stu-id="ac198-494">When using **captureSelectedContentToDataPackageAsync**, you need to define success and error handlers after defining the operation.</span></span> <span data-ttu-id="ac198-495">После применения обработчиков событий вызовите метод Start объекта MSWebViewAsyncOperation, чтобы выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="ac198-495">After applying the event handlers, call the start method on the MSWebViewAsyncOperation object to execute the operation.</span></span>

```js
 var operation = webview.captureSelectedContentToDataPackageAsync();
    operation.oncomplete = function () {
        // operation.result is a package object that contains the selected data.
        var url = URL.createObjectURL(operation.result, { oneTimeOnly: true });
        // After converting the package to a URI, put it in an image element.
        document.getElementById('webviewPreview').src = url;
    };
    operation.start();  

```

### <span data-ttu-id="ac198-496">invokeScriptAsync</span><span class="sxs-lookup"><span data-stu-id="ac198-496">invokeScriptAsync</span></span>

<span data-ttu-id="ac198-497">Как асинхронное действие выполняет указанную функцию сценария из загруженного HTML-кода с определенными аргументами.</span><span class="sxs-lookup"><span data-stu-id="ac198-497">As an asynchronous action, executes the specified script function from the currently loaded HTML, with specific arguments.</span></span>

```js
webview.invokeScriptAsync(functionName, ...args)
```

#### <span data-ttu-id="ac198-498">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-498">Parameters</span></span>

**<span data-ttu-id="ac198-499">functionName</span><span class="sxs-lookup"><span data-stu-id="ac198-499">functionName</span></span>**
* <span data-ttu-id="ac198-500">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-500">Type: **String**</span></span>
* <span data-ttu-id="ac198-501">Имя вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="ac198-501">The name of the function to invoke.</span></span> <span data-ttu-id="ac198-502">Это имя свойства в объекте глобального окна документа верхнего уровня WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-502">This is a property name on the global window object of the WebView's top level document.</span></span> <span data-ttu-id="ac198-503">Это может быть Встроенная глобальная функция, например eval или Open, а также функция, определенная сценарием, для объекта глобального окна.</span><span class="sxs-lookup"><span data-stu-id="ac198-503">This can be a built-in global function like eval or open, or it can be a script defined function on the global window object.</span></span> <span data-ttu-id="ac198-504">Только функции в документе верхнего уровня WebView могут быть вызваны.</span><span class="sxs-lookup"><span data-stu-id="ac198-504">Only functions in the top level document of the WebView may be invoked.</span></span>

**<span data-ttu-id="ac198-505">аргументы</span><span class="sxs-lookup"><span data-stu-id="ac198-505">args</span></span>**
* <span data-ttu-id="ac198-506">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-506">Type: **String**</span></span>
* <span data-ttu-id="ac198-507">Необязательные строковые параметры для передачи в вызываемую функцию.</span><span class="sxs-lookup"><span data-stu-id="ac198-507">Optional string parameters to pass to the invoked function.</span></span> <span data-ttu-id="ac198-508">После аргумента functionName любые дополнительные параметры invokeScriptAsync являются строками, передаваемыми вызываемой функции.</span><span class="sxs-lookup"><span data-stu-id="ac198-508">After functionName, any additional parameters to invokeScriptAsync are strings passed to the invoked function.</span></span>

#### <span data-ttu-id="ac198-509">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-509">Return value</span></span>
<span data-ttu-id="ac198-510">Type (тип): **MSWebViewAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="ac198-510">Type: **MSWebViewAsyncOperation**</span></span>

<span data-ttu-id="ac198-511">При использовании **invokeScriptAsync**необходимо определить обработчики успехов и ошибок после определения операции.</span><span class="sxs-lookup"><span data-stu-id="ac198-511">When using **invokeScriptAsync**, you need to define success and error handlers after defining the operation.</span></span> <span data-ttu-id="ac198-512">После применения обработчиков событий вызовите метод **MSWebViewAsyncOperation. Start** , чтобы выполнить операцию.</span><span class="sxs-lookup"><span data-stu-id="ac198-512">After applying the event handlers, call **MSWebViewAsyncOperation.start** to execute the operation.</span></span> <span data-ttu-id="ac198-513">При возникновении события Complete MSWebViewAsyncOperation свойство Result MSWebViewAsyncOperation является строковым возвращаемым значением из вызова функции.</span><span class="sxs-lookup"><span data-stu-id="ac198-513">If the MSWebViewAsyncOperation's complete event fires then the MSWebViewAsyncOperation's result property is the string return value from invoking the function.</span></span> <span data-ttu-id="ac198-514">Использование возвращаемого значения вызываемой функции обеспечивает синхронное взаимодействие содержимого WebView с узлом WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-514">Using the invoked function's return value allows for the WebView content to communication synchronously back to the WebView host.</span></span> <span data-ttu-id="ac198-515">Чтобы получить содержимое WebView асинхронно обратно на узел WebView, просмотрите событие MSWebViewScriptNotify.</span><span class="sxs-lookup"><span data-stu-id="ac198-515">To instead have the WebView content communicate asynchronously back to the WebView host see the MSWebViewScriptNotify event.</span></span> <span data-ttu-id="ac198-516">Если функция вызывается из-за неуправляемого исключения, возникает событие ошибки MSWebViewAsyncOperation.</span><span class="sxs-lookup"><span data-stu-id="ac198-516">If the function invoked throws an unhandled exception then the MSWebViewAsyncOperation's error event will fire.</span></span> 

```js
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```

### <span data-ttu-id="ac198-517">getDeferredPermissionRequests</span><span class="sxs-lookup"><span data-stu-id="ac198-517">getDeferredPermissionRequests</span></span>

<span data-ttu-id="ac198-518">Возвращает список отложенных запросов разрешений, выданных содержимым в элементе управления **WebView** .</span><span class="sxs-lookup"><span data-stu-id="ac198-518">Returns a list of deferred permission requests issued by content in the **webview** control.</span></span>

```js
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```

#### <span data-ttu-id="ac198-519">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-519">Parameters</span></span>
<span data-ttu-id="ac198-520">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ac198-520">This method has no parameters.</span></span>

#### <span data-ttu-id="ac198-521">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-521">Return value</span></span>
<span data-ttu-id="ac198-522">Type (тип): [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="ac198-522">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>

<span data-ttu-id="ac198-523">Указанный запрос на отложенный доступ.</span><span class="sxs-lookup"><span data-stu-id="ac198-523">The specified deferred permission request.</span></span>

#### <span data-ttu-id="ac198-524">Дополнительные функции и требования</span><span class="sxs-lookup"><span data-stu-id="ac198-524">Additional features and requirements</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-525">Минимальный поддерживаемый клиент</span><span class="sxs-lookup"><span data-stu-id="ac198-525">Minimum supported client</span></span>** |<span data-ttu-id="ac198-526">Windows10 [только для приложений Магазина Windows]</span><span class="sxs-lookup"><span data-stu-id="ac198-526">Windows10 [Windows Store apps only]</span></span> |    
|**<span data-ttu-id="ac198-527">Минимальный поддерживаемый сервер</span><span class="sxs-lookup"><span data-stu-id="ac198-527">Minimum supported server</span></span>** |<span data-ttu-id="ac198-528">Ничего не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac198-528">None supported</span></span>|   
|**<span data-ttu-id="ac198-529">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="ac198-529">Minimum supported phone</span></span>**  |<span data-ttu-id="ac198-530">Ничего не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac198-530">None supported</span></span> |    


### <span data-ttu-id="ac198-531">getDeferredPermissionRequestById</span><span class="sxs-lookup"><span data-stu-id="ac198-531">getDeferredPermissionRequestById</span></span>

<span data-ttu-id="ac198-532">Возвращает указанный запрос на отложенный доступ.</span><span class="sxs-lookup"><span data-stu-id="ac198-532">Returns the specified deferred permission request.</span></span> 

```js
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```

#### <span data-ttu-id="ac198-533">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-533">Parameters</span></span>
*<span data-ttu-id="ac198-534">id</span><span class="sxs-lookup"><span data-stu-id="ac198-534">id</span></span>*
* <span data-ttu-id="ac198-535">Тип: **Long без знака**</span><span class="sxs-lookup"><span data-stu-id="ac198-535">Type: **unsigned long**</span></span>
* <span data-ttu-id="ac198-536">Идентификатор запроса отложенного разрешения, который вы хотите получить.</span><span class="sxs-lookup"><span data-stu-id="ac198-536">The ID of the deferred permission request you wish to get.</span></span>

#### <span data-ttu-id="ac198-537">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-537">Return value</span></span>
<span data-ttu-id="ac198-538">Type (тип): [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span><span class="sxs-lookup"><span data-stu-id="ac198-538">Type: [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)</span></span>

<span data-ttu-id="ac198-539">Указанный запрос на отложенный доступ.</span><span class="sxs-lookup"><span data-stu-id="ac198-539">The specified deferred permission request.</span></span>

#### <span data-ttu-id="ac198-540">Дополнительные функции и требования</span><span class="sxs-lookup"><span data-stu-id="ac198-540">Additional features and requirements</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="ac198-541">Минимальный поддерживаемый клиент</span><span class="sxs-lookup"><span data-stu-id="ac198-541">Minimum supported client</span></span>** |<span data-ttu-id="ac198-542">Windows10 [только для приложений Магазина Windows]</span><span class="sxs-lookup"><span data-stu-id="ac198-542">Windows10 [Windows Store apps only]</span></span> |    
|**<span data-ttu-id="ac198-543">Минимальный поддерживаемый сервер</span><span class="sxs-lookup"><span data-stu-id="ac198-543">Minimum supported server</span></span>** |<span data-ttu-id="ac198-544">Ничего не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac198-544">None supported</span></span>|   
|**<span data-ttu-id="ac198-545">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="ac198-545">Minimum supported phone</span></span>**  |<span data-ttu-id="ac198-546">Ничего не поддерживается</span><span class="sxs-lookup"><span data-stu-id="ac198-546">None supported</span></span> | 

### <span data-ttu-id="ac198-547">goBack</span><span class="sxs-lookup"><span data-stu-id="ac198-547">goBack</span></span>

<span data-ttu-id="ac198-548">Переход по **WebView** на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="ac198-548">Navigates the **webview** to the previous page in the navigation history.</span></span> 

```js
webview.goBack();
```

#### <span data-ttu-id="ac198-549">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-549">Parameters</span></span>
<span data-ttu-id="ac198-550">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ac198-550">This method has no parameters.</span></span>

#### <span data-ttu-id="ac198-551">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-551">Return value</span></span>
<span data-ttu-id="ac198-552">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-552">This method does not return a value.</span></span>

### <span data-ttu-id="ac198-553">goForward</span><span class="sxs-lookup"><span data-stu-id="ac198-553">goForward</span></span>

<span data-ttu-id="ac198-554">Переход по **WebView** к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="ac198-554">Navigates the **webview** to the next page in the navigation history.</span></span> 

```js
webview.goForward();
```

#### <span data-ttu-id="ac198-555">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-555">Parameters</span></span>
<span data-ttu-id="ac198-556">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ac198-556">This method has no parameters.</span></span>

#### <span data-ttu-id="ac198-557">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-557">Return value</span></span>
<span data-ttu-id="ac198-558">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-558">This method does not return a value.</span></span>

### <span data-ttu-id="ac198-559">переход</span><span class="sxs-lookup"><span data-stu-id="ac198-559">navigate</span></span>

<span data-ttu-id="ac198-560">Загружает HTML-содержимое по указанному универсальному идентификатору ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="ac198-560">Loads the HTML content at the specified Uniform Resource Identifier (URI).</span></span> 

```js
webview.navigate(uri);
```

#### <span data-ttu-id="ac198-561">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-561">Parameters</span></span>

**<span data-ttu-id="ac198-562">uri</span><span class="sxs-lookup"><span data-stu-id="ac198-562">uri</span></span>**
* <span data-ttu-id="ac198-563">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-563">Type: **String**</span></span>
* <span data-ttu-id="ac198-564">URI для загрузки.</span><span class="sxs-lookup"><span data-stu-id="ac198-564">The URI to load.</span></span>

#### <span data-ttu-id="ac198-565">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-565">Return value</span></span>
<span data-ttu-id="ac198-566">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-566">This  method does not return a value.</span></span>

### <span data-ttu-id="ac198-567">navigateFocus</span><span class="sxs-lookup"><span data-stu-id="ac198-567">navigateFocus</span></span>

<span data-ttu-id="ac198-568">Перемещение фокуса на **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-568">Navigates focus onto the **webview**.</span></span> <span data-ttu-id="ac198-569">Вызывает событие WebView window's navigatingfocus документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="ac198-569">Fires the webview's top level document's window's navigatingfocus event.</span></span> <span data-ttu-id="ac198-570">Аргументы FocusNavigationEvent, используемые в событии navigatingfocus, совпадают с параметрами, предоставленными navigateFocus, за исключением параметров происхождения, которые преобразуются из пространства координат основного документа в пространство координат документа верхнего уровня WebView.</span><span class="sxs-lookup"><span data-stu-id="ac198-570">The FocusNavigationEvent args used in the navigatingfocus event match the parameters provided to navigateFocus except the origin parameters are translated from the host document's coordinate space to the coordinate space of the webview's top level document.</span></span> <span data-ttu-id="ac198-571">Просмотрите событие WebView departingFocus и соответствующий метод Window. departFocus для перемещения фокуса с WebView на узел.</span><span class="sxs-lookup"><span data-stu-id="ac198-571">See the webview departingFocus event and corresponding window.departFocus method for transferring focus from the webview to the host.</span></span> <span data-ttu-id="ac198-572">Пример реализации навигации по фокусу с помощью клавиатуры или игрового приложения, использующего этот метод, можно найти в [библиотеке навигации направления TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .</span><span class="sxs-lookup"><span data-stu-id="ac198-572">See the [TVJS's Direction Navigation library](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) for an example of an implementation of focus navigation via keyboard or gamepad that uses this method.</span></span>

```js
const activeElementBounds = document.activeElement.getBoundingClientRect();
const origin = { 
    originLeft: activeElementBounds.left,
    originTop: activeElementBounds.top,
    originWidth: activeElementBounds.width,
    originHeight: activeElementBounds.height
};
webview.navigateFocus(navigationReason, origin);
```

#### <span data-ttu-id="ac198-573">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-573">Parameters</span></span>
*<span data-ttu-id="ac198-574">navigationReason</span><span class="sxs-lookup"><span data-stu-id="ac198-574">navigationReason</span></span>*
* <span data-ttu-id="ac198-575">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-575">Type: **String**</span></span>
* <span data-ttu-id="ac198-576">Причина для навигации.</span><span class="sxs-lookup"><span data-stu-id="ac198-576">The reason for the navigation.</span></span> <span data-ttu-id="ac198-577">Это значение должно быть "Left", "стрелка вверх", "вправо" или "вниз".</span><span class="sxs-lookup"><span data-stu-id="ac198-577">The value should be either "left", "up", "right", or "down".</span></span> <span data-ttu-id="ac198-578">Это направление, в котором фокус перемещается от элемента, на который Вы ориентированы в данный момент.</span><span class="sxs-lookup"><span data-stu-id="ac198-578">It is the direction in which focus is moving away from the currently focused element.</span></span>

*<span data-ttu-id="ac198-579">исходных</span><span class="sxs-lookup"><span data-stu-id="ac198-579">origin</span></span>*
* <span data-ttu-id="ac198-580">Тип: **объект**</span><span class="sxs-lookup"><span data-stu-id="ac198-580">Type: **Object**</span></span>
* <span data-ttu-id="ac198-581">Источник навигации.</span><span class="sxs-lookup"><span data-stu-id="ac198-581">The origin of the navigation.</span></span> <span data-ttu-id="ac198-582">Это объект JavaScript со свойствами "originLeft", "originTop", "originWidth" и "originHeight".</span><span class="sxs-lookup"><span data-stu-id="ac198-582">This is a JavaScript object with properties "originLeft", "originTop", "originWidth", and "originHeight".</span></span> <span data-ttu-id="ac198-583">Эти значения должны описывать расположение и размер элемента, в котором находится фокус, вне которой перемещается фокус.</span><span class="sxs-lookup"><span data-stu-id="ac198-583">These values should describe the position and size of the currently focused element away from which focus is moving.</span></span>

#### <span data-ttu-id="ac198-584">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-584">Return value</span></span>
<span data-ttu-id="ac198-585">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-585">This method does not return a value.</span></span>

### <span data-ttu-id="ac198-586">navigateToLocalStreamUri</span><span class="sxs-lookup"><span data-stu-id="ac198-586">navigateToLocalStreamUri</span></span>

<span data-ttu-id="ac198-587">Загружает локальное веб-содержимое по указанному URI с помощью [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span><span class="sxs-lookup"><span data-stu-id="ac198-587">Loads local web content at the specified URI using a [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).</span></span>

```js
webview.navigateToLocalStreamUri(source, streamResolver); 
```

#### <span data-ttu-id="ac198-588">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-588">Parameters</span></span>

*<span data-ttu-id="ac198-589">исходный</span><span class="sxs-lookup"><span data-stu-id="ac198-589">source</span></span>*
* <span data-ttu-id="ac198-590">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-590">Type: **String**</span></span>
* <span data-ttu-id="ac198-591">Универсальный код ресурса (URI) MS-Stream, который определяет локальное HTML-содержимое для загрузки.</span><span class="sxs-lookup"><span data-stu-id="ac198-591">An ms-local-stream URI identifying the local HTML content to load.</span></span> <span data-ttu-id="ac198-592">Создайте эту строку с помощью [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span><span class="sxs-lookup"><span data-stu-id="ac198-592">Create this string using [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).</span></span>

*<span data-ttu-id="ac198-593">streamResolver</span><span class="sxs-lookup"><span data-stu-id="ac198-593">streamResolver</span></span>*
* <span data-ttu-id="ac198-594">Type (тип): Any</span><span class="sxs-lookup"><span data-stu-id="ac198-594">Type: any</span></span>
* <span data-ttu-id="ac198-595">Сопоставитель, преобразующий URI в поток для загрузки.</span><span class="sxs-lookup"><span data-stu-id="ac198-595">A resolver that converts the URI into a stream to load.</span></span>

#### <span data-ttu-id="ac198-596">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-596">Return value</span></span>
<span data-ttu-id="ac198-597">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-597">This method does not return a value.</span></span>

### <span data-ttu-id="ac198-598">navigateToString</span><span class="sxs-lookup"><span data-stu-id="ac198-598">navigateToString</span></span>

<span data-ttu-id="ac198-599">Загружает указанное HTML-содержимое в новый документ.</span><span class="sxs-lookup"><span data-stu-id="ac198-599">Loads the specified HTML content as a new document.</span></span> 

```js
webview.navigateToString(contents);
```

#### <span data-ttu-id="ac198-600">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-600">Parameters</span></span>

*<span data-ttu-id="ac198-601">содержимое</span><span class="sxs-lookup"><span data-stu-id="ac198-601">contents</span></span>*
* <span data-ttu-id="ac198-602">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-602">Type: **String**</span></span>
* <span data-ttu-id="ac198-603">Отображаемое содержимое HTML.</span><span class="sxs-lookup"><span data-stu-id="ac198-603">The HTML content to display.</span></span>

#### <span data-ttu-id="ac198-604">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-604">Return value</span></span>
<span data-ttu-id="ac198-605">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-605">This method does not return a value.</span></span>

### <span data-ttu-id="ac198-606">navigateWithHttpRequestMessage</span><span class="sxs-lookup"><span data-stu-id="ac198-606">navigateWithHttpRequestMessage</span></span>

<span data-ttu-id="ac198-607">Переход по WebView на универсальный код ресурса (URI) с запросом POST и заголовками HTTP.</span><span class="sxs-lookup"><span data-stu-id="ac198-607">Navigates the webview to a Uniform Resource Identifier (URI) with a POST request and HTTP headers.</span></span> 

```js
webview.navigateWithHttpRequestMessage(requestMessage);
```

#### <span data-ttu-id="ac198-608">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-608">Parameters</span></span>

*<span data-ttu-id="ac198-609">requestMessage</span><span class="sxs-lookup"><span data-stu-id="ac198-609">requestMessage</span></span>*
* <span data-ttu-id="ac198-610">Type (тип): **HttpRequestMessage**</span><span class="sxs-lookup"><span data-stu-id="ac198-610">Type: **HttpRequestMessage**</span></span>
* <span data-ttu-id="ac198-611">Сведения о запросе HTTP.</span><span class="sxs-lookup"><span data-stu-id="ac198-611">The details of the HTTP request.</span></span> 

#### <span data-ttu-id="ac198-612">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-612">Return value</span></span>
<span data-ttu-id="ac198-613">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-613">This method does not return a value.</span></span>

#### <span data-ttu-id="ac198-614">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ac198-614">Remarks</span></span>

> [!WARNING]
> <span data-ttu-id="ac198-615">Если вы добавите в этот запрос дополнительные заголовки, например учетные данные для проверки подлинности, помните, что эти заголовки также будут включены в любые последующие дочерние запросы.</span><span class="sxs-lookup"><span data-stu-id="ac198-615">If you add additional headers to this request, such as authentication credentials, remember that those headers will also be included with any subsequent child requests.</span></span> <span data-ttu-id="ac198-616">Будьте внимательны, чтобы предотвратить случайное раскрытие конфиденциальных и персональных данных.</span><span class="sxs-lookup"><span data-stu-id="ac198-616">Use caution to prevent accidental disclosure of confidential or personal information.</span></span> 


### <span data-ttu-id="ac198-617">Обновлен</span><span class="sxs-lookup"><span data-stu-id="ac198-617">refresh</span></span> 

<span data-ttu-id="ac198-618">Перезагружает текущее содержимое в **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-618">Reloads the current content in the **webview**.</span></span> 

```js
webview.refresh();
```

#### <span data-ttu-id="ac198-619">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-619">Parameters</span></span>
<span data-ttu-id="ac198-620">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ac198-620">This method has no parameters.</span></span>

#### <span data-ttu-id="ac198-621">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-621">Return value</span></span>
<span data-ttu-id="ac198-622">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-622">This method does not return a value.</span></span>


### <span data-ttu-id="ac198-623">stop</span><span class="sxs-lookup"><span data-stu-id="ac198-623">stop</span></span>

<span data-ttu-id="ac198-624">Останавливает текущую навигацию по **WebView** или загрузку.</span><span class="sxs-lookup"><span data-stu-id="ac198-624">Halts the current **webview** navigation or download.</span></span> 

```js
webview.stop();
```

#### <span data-ttu-id="ac198-625">Параметры</span><span class="sxs-lookup"><span data-stu-id="ac198-625">Parameters</span></span>
<span data-ttu-id="ac198-626">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="ac198-626">This method has no parameters.</span></span>

#### <span data-ttu-id="ac198-627">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ac198-627">Return value</span></span>
<span data-ttu-id="ac198-628">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="ac198-628">This method does not return a value.</span></span>


## <span data-ttu-id="ac198-629">Свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-629">Properties</span></span>

### <span data-ttu-id="ac198-630">canGoBack</span><span class="sxs-lookup"><span data-stu-id="ac198-630">canGoBack</span></span>

<span data-ttu-id="ac198-631">Возвращает значение, указывающее, может ли **WebView** переход назад.</span><span class="sxs-lookup"><span data-stu-id="ac198-631">Gets a value that indicates whether the **webview** can navigate backward.</span></span>

<span data-ttu-id="ac198-632">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ac198-632">This property is read-only.</span></span>

```js
var canGoBack = webview.canGoBack;
```

#### <span data-ttu-id="ac198-633">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-633">Property value</span></span>
<span data-ttu-id="ac198-634">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="ac198-634">Type: **Boolean**</span></span>

<span data-ttu-id="ac198-635">**Значение true** , если **WebView** может перейти назад; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ac198-635">**True** if the **webview** can navigate backward; otherwise, **false**.</span></span>

### <span data-ttu-id="ac198-636">canGoForward</span><span class="sxs-lookup"><span data-stu-id="ac198-636">canGoForward</span></span>

<span data-ttu-id="ac198-637">Возвращает значение, указывающее, может ли **WebView** переход вперед.</span><span class="sxs-lookup"><span data-stu-id="ac198-637">Gets a value that indicates whether the **webview** can navigate forward.</span></span>

<span data-ttu-id="ac198-638">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ac198-638">This property is read-only.</span></span>

```js
var canGoForward = webview.canGoForward;
```

#### <span data-ttu-id="ac198-639">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-639">Property value</span></span>
<span data-ttu-id="ac198-640">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="ac198-640">Type: **Boolean**</span></span>

<span data-ttu-id="ac198-641">**Значение true** , если **WebView** может перейти вперед; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ac198-641">**True** if the **webview** can navigate forward; otherwise, **false**.</span></span>

### <span data-ttu-id="ac198-642">containsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="ac198-642">containsFullScreenElement</span></span>

<span data-ttu-id="ac198-643">Возвращает значение, указывающее, содержит ли **WebView** элемент, поддерживающий полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="ac198-643">Gets a value that indicates whether the **webview** contains an element that supports full screen.</span></span> <span data-ttu-id="ac198-644">Дополнительные сведения вы видите в событии MSWebViewContainsFullScreenElementChanged.</span><span class="sxs-lookup"><span data-stu-id="ac198-644">See the MSWebViewContainsFullScreenElementChanged event for more info.</span></span>

<span data-ttu-id="ac198-645">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ac198-645">This property is read-only.</span></span>

```js
var containsFullScreenElement = webview.containsFullScreenElement;
```

#### <span data-ttu-id="ac198-646">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-646">Property value</span></span>
<span data-ttu-id="ac198-647">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="ac198-647">Type: **Boolean**</span></span>

<span data-ttu-id="ac198-648">**Значение true** , если **WebView** включает элемент, поддерживающий полный экран; в противном случае — **значение false**.</span><span class="sxs-lookup"><span data-stu-id="ac198-648">**True** if the **webview** contains an element that supports full screen; otherwise, **false**.</span></span>


### <span data-ttu-id="ac198-649">documentTitle</span><span class="sxs-lookup"><span data-stu-id="ac198-649">documentTitle</span></span>

<span data-ttu-id="ac198-650">Получает заголовок страницы, отображаемой в данный момент в **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-650">Gets the title of the page currently displayed in the **webview**.</span></span> 

<span data-ttu-id="ac198-651">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ac198-651">This property is read-only.</span></span>

```js
var documentTitle = webview.documentTitle;
```

#### <span data-ttu-id="ac198-652">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-652">Property value</span></span>
<span data-ttu-id="ac198-653">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-653">Type: **String**</span></span>

<span data-ttu-id="ac198-654">Заголовок страницы.</span><span class="sxs-lookup"><span data-stu-id="ac198-654">The page title.</span></span>

### <span data-ttu-id="ac198-655">height</span><span class="sxs-lookup"><span data-stu-id="ac198-655">height</span></span>

<span data-ttu-id="ac198-656">Возвращает или задает высоту **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-656">Gets or sets the height of the **webview**.</span></span> 

```js
var height = webview.height;
webview.height = height;

```

#### <span data-ttu-id="ac198-657">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-657">Property value</span></span>
<span data-ttu-id="ac198-658">Тип: **номер**</span><span class="sxs-lookup"><span data-stu-id="ac198-658">Type: **Number**</span></span>

<span data-ttu-id="ac198-659">Высота **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-659">The height of the **webview**.</span></span> 


### <span data-ttu-id="ac198-660">работу другого</span><span class="sxs-lookup"><span data-stu-id="ac198-660">process</span></span>

<span data-ttu-id="ac198-661">Возвращает процесс **WebView** .</span><span class="sxs-lookup"><span data-stu-id="ac198-661">Gets the **webview** process.</span></span>

<span data-ttu-id="ac198-662">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ac198-662">This property is read-only.</span></span>

```js
var process = webview.process;
webview.process = process;
```

#### <span data-ttu-id="ac198-663">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-663">Property value</span></span>
<span data-ttu-id="ac198-664">Type (тип): [MSWebViewProcess](./webview/MSWebViewProcess.md)</span><span class="sxs-lookup"><span data-stu-id="ac198-664">Type: [MSWebViewProcess](./webview/MSWebViewProcess.md)</span></span>


### <span data-ttu-id="ac198-665">settings</span><span class="sxs-lookup"><span data-stu-id="ac198-665">settings</span></span>

<span data-ttu-id="ac198-666">Возвращает объект [MSWebViewSettings](./webview/MSWebViewSettings.md) , содержащий свойства для включения или отключения функций **WebView** .</span><span class="sxs-lookup"><span data-stu-id="ac198-666">Gets a [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>

<span data-ttu-id="ac198-667">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ac198-667">This property is read-only.</span></span>

```js
var settings = webview.settings;
webview.settings = settings;
```

#### <span data-ttu-id="ac198-668">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-668">Property value</span></span>
<span data-ttu-id="ac198-669">Type (тип): [MSWebViewSettings](./webview/MSWebViewSettings.md)</span><span class="sxs-lookup"><span data-stu-id="ac198-669">Type: [MSWebViewSettings](./webview/MSWebViewSettings.md)</span></span>

<span data-ttu-id="ac198-670">Объект [MSWebViewSettings](./webview/MSWebViewSettings.md) , содержащий свойства для включения или отключения функций **WebView** .</span><span class="sxs-lookup"><span data-stu-id="ac198-670">A [MSWebViewSettings](./webview/MSWebViewSettings.md) object that contains properties to enable or disable **webview** features.</span></span>

### <span data-ttu-id="ac198-671">src</span><span class="sxs-lookup"><span data-stu-id="ac198-671">src</span></span>

<span data-ttu-id="ac198-672">Возвращает или задает универсальный код ресурса (URI) для содержимого HTML, которое будет отображаться в элементе управления **WebView** .</span><span class="sxs-lookup"><span data-stu-id="ac198-672">Gets or sets the Uniform Resource Identifier (URI) source of the HTML content to display in the **webview** control.</span></span> 

```js
var src = webview.src;
webview.src = src;
```

#### <span data-ttu-id="ac198-673">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-673">Property value</span></span>
<span data-ttu-id="ac198-674">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="ac198-674">Type: **String**</span></span>

<span data-ttu-id="ac198-675">Источник универсального кода ресурса (URI) для содержимого HTML, которое будет отображаться в элементе управления **WebView** .</span><span class="sxs-lookup"><span data-stu-id="ac198-675">The URI source of the HTML content to display in the **webview** control.</span></span> 


### <span data-ttu-id="ac198-676">width</span><span class="sxs-lookup"><span data-stu-id="ac198-676">width</span></span>

<span data-ttu-id="ac198-677">Возвращает или задает ширину **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-677">Gets or sets the width of the **webview**.</span></span>

```js
var width = webview.width;
webview.width = width;
```

#### <span data-ttu-id="ac198-678">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ac198-678">Property value</span></span>
<span data-ttu-id="ac198-679">Тип: **номер**</span><span class="sxs-lookup"><span data-stu-id="ac198-679">Type: **Number**</span></span>

<span data-ttu-id="ac198-680">Ширина **WebView**.</span><span class="sxs-lookup"><span data-stu-id="ac198-680">The width of the **webview**.</span></span>
