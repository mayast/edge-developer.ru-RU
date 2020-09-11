---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: c6b1f1c62da5aa5ef64693575abb9cb46ac13851
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012480"
---
# <span data-ttu-id="7a9d0-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="7a9d0-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="7a9d0-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7a9d0-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7a9d0-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="7a9d0-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7a9d0-107">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="7a9d0-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7a9d0-108">Summary</span></span>

 <span data-ttu-id="7a9d0-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7a9d0-109">Members</span></span>                        | <span data-ttu-id="7a9d0-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7a9d0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a9d0-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="7a9d0-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="7a9d0-112">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="7a9d0-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="7a9d0-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="7a9d0-114">NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-114">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>
[<span data-ttu-id="7a9d0-115">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="7a9d0-115">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="7a9d0-116">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-116">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="7a9d0-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="7a9d0-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="7a9d0-118">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="7a9d0-119">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="7a9d0-119">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="7a9d0-120">Создание пустого CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-120">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="7a9d0-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="7a9d0-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="7a9d0-122">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-122">Create a new web resource response object.</span></span>
[<span data-ttu-id="7a9d0-123">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="7a9d0-123">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="7a9d0-124">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-124">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="7a9d0-125">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-125">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="7a9d0-126">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-126">Using it in different environments are not guaranteed to be compatible and may fail.</span></span> 

<span data-ttu-id="7a9d0-127">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-127">WebViews created from an environment run on the browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="7a9d0-128">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-128">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="7a9d0-129">Участников</span><span class="sxs-lookup"><span data-stu-id="7a9d0-129">Members</span></span>

#### <span data-ttu-id="7a9d0-130">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="7a9d0-130">BrowserVersionString</span></span> 

<span data-ttu-id="7a9d0-131">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-131">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="7a9d0-132">общедоступная строка [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="7a9d0-132">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="7a9d0-133">Это соответствует формату API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-133">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="7a9d0-134">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="7a9d0-134">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="7a9d0-135">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="7a9d0-135">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="7a9d0-136">NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-136">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>

> <span data-ttu-id="7a9d0-137">событие EventHandler< объект > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="7a9d0-137">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="7a9d0-138">Для использования более новой версии браузера необходимо создать новую среду и WebView.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-138">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="7a9d0-139">Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-139">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="7a9d0-140">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-140">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="7a9d0-141">Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-141">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="7a9d0-142">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-142">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="7a9d0-143">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="7a9d0-143">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="7a9d0-144">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-144">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="7a9d0-145">открытая асинхронная задача< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="7a9d0-145">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="7a9d0-146">parentWindow — это HWND, в котором приложение будет подключаться к визуальному дереву WebView.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-146">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="7a9d0-147">Это HWND того, что приложение получит ввод указателя или мыши, предназначенное для WebView (и для пересылки потребуется функция SendMouseInput/SendPointerInput).</span><span class="sxs-lookup"><span data-stu-id="7a9d0-147">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="7a9d0-148">Если приложение перемещает визуальное дерево WebView в другое окно, ему необходимо настроить CoreWebView2CompositionController. ParentWindow, чтобы обновить новый родительский дескриптор HWND визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-148">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="7a9d0-149">Задайте свойство RootVisualTarget в созданном CoreWebView2CompositionController, чтобы предоставить визуальное размещение визуального дерева браузера.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-149">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="7a9d0-150">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="7a9d0-151">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="7a9d0-152">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="7a9d0-152">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="7a9d0-153">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-153">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="7a9d0-154">открытая асинхронная задача< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="7a9d0-154">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="7a9d0-155">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-155">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="7a9d0-156">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-156">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="7a9d0-157">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-157">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="7a9d0-158">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-158">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="7a9d0-159">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-159">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="7a9d0-160">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="7a9d0-160">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="7a9d0-161">Создание пустого CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-161">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="7a9d0-162">общедоступная [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="7a9d0-162">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="7a9d0-163">Возвращенные CoreWebView2PointerInfo должны быть заполнены всеми соответствующими сведениями перед вызовом SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-163">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="7a9d0-164">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="7a9d0-164">CreateWebResourceResponse</span></span> 

<span data-ttu-id="7a9d0-165">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-165">Create a new web resource response object.</span></span>

> <span data-ttu-id="7a9d0-166">Public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(потоковый контент, int StatusCode, String ReasonPhrase, заголовки строк)</span><span class="sxs-lookup"><span data-stu-id="7a9d0-166">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="7a9d0-167">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-167">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="7a9d0-168">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать CoreWebView2HttpResponseHeaders для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-168">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="7a9d0-169">Сведения о других параметрах смотрите в CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-169">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="7a9d0-170">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="7a9d0-170">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="7a9d0-171">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="7a9d0-171">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="7a9d0-172">общедоступный объект [GetProviderForHwnd](#getproviderforhwnd)(IntPtr HWND)</span><span class="sxs-lookup"><span data-stu-id="7a9d0-172">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

