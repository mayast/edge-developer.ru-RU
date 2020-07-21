---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 6b03997c8bd76137b20bb71edfd0d57b3686914a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885291"
---
# <span data-ttu-id="1161d-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="1161d-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="1161d-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="1161d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="1161d-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="1161d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="1161d-107">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="1161d-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="1161d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1161d-108">Summary</span></span>

 <span data-ttu-id="1161d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="1161d-109">Members</span></span>                        | <span data-ttu-id="1161d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="1161d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1161d-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1161d-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="1161d-112">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="1161d-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="1161d-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="1161d-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="1161d-114">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="1161d-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="1161d-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="1161d-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="1161d-116">Правильно Сравните версии браузеров, чтобы определить, какая версия более новая или более ранняя.</span><span class="sxs-lookup"><span data-stu-id="1161d-116">Compare browser versions correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="1161d-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="1161d-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="1161d-118">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="1161d-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="1161d-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1161d-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="1161d-120">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="1161d-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="1161d-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1161d-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="1161d-122">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="1161d-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="1161d-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="1161d-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="1161d-124">Создание пустого CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="1161d-124">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="1161d-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="1161d-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="1161d-126">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="1161d-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="1161d-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1161d-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="1161d-128">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="1161d-128">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>
[<span data-ttu-id="1161d-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="1161d-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="1161d-130">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="1161d-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="1161d-131">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="1161d-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="1161d-132">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="1161d-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="1161d-133">Участников</span><span class="sxs-lookup"><span data-stu-id="1161d-133">Members</span></span>

#### <span data-ttu-id="1161d-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1161d-134">BrowserVersionString</span></span> 

<span data-ttu-id="1161d-135">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="1161d-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="1161d-136">общедоступная строка [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="1161d-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="1161d-137">Это соответствует формату API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="1161d-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="1161d-138">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="1161d-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="1161d-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="1161d-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="1161d-140">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="1161d-140">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="1161d-141">событие EventHandler< объект > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="1161d-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="1161d-142">Для использования более новой версии браузера необходимо создать новую среду и WebView.</span><span class="sxs-lookup"><span data-stu-id="1161d-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="1161d-143">Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="1161d-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="1161d-144">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="1161d-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="1161d-145">Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="1161d-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="1161d-146">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="1161d-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="1161d-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="1161d-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="1161d-148">Правильно Сравните версии браузеров, чтобы определить, какая версия более новая или более ранняя.</span><span class="sxs-lookup"><span data-stu-id="1161d-148">Compare browser versions correctly to determine which version is newer, older or same.</span></span>

> <span data-ttu-id="1161d-149">общедоступный статический целочисленный [CompareBrowserVersions](#comparebrowserversions)(строковый Version1, строка Version2)</span><span class="sxs-lookup"><span data-stu-id="1161d-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="1161d-150">Возвращает значение-1, 0 или 1 в зависимости от того, является ли Version1 меньше, равно или больше Version2, соответственно.</span><span class="sxs-lookup"><span data-stu-id="1161d-150">Returns -1, 0 or 1 depending on whether version1 is less than, equal to or greater than version2, respectively.</span></span>

##### <span data-ttu-id="1161d-151">Параметры</span><span class="sxs-lookup"><span data-stu-id="1161d-151">Parameters</span></span>
* `version1` <span data-ttu-id="1161d-152">Одна из строк версии для сравнения.</span><span class="sxs-lookup"><span data-stu-id="1161d-152">One of the version strings to compare.</span></span> 

* `version2` <span data-ttu-id="1161d-153">Другая сравниваемая строка версии.</span><span class="sxs-lookup"><span data-stu-id="1161d-153">The other version string to compare.</span></span>

#### <span data-ttu-id="1161d-154">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="1161d-154">CreateAsync</span></span> 

<span data-ttu-id="1161d-155">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="1161d-155">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="1161d-156">общедоступная статическая асинхронная задача< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(строка browserExecutableFolder, строка userDataFolder, CoreWebView2EnvironmentOptions параметры)</span><span class="sxs-lookup"><span data-stu-id="1161d-156">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="1161d-157">Параметры</span><span class="sxs-lookup"><span data-stu-id="1161d-157">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="1161d-158">Относительный путь к папке, содержащей внедренный край.</span><span class="sxs-lookup"><span data-stu-id="1161d-158">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="1161d-159">userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2.</span><span class="sxs-lookup"><span data-stu-id="1161d-159">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="1161d-160">Параметры, используемые для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="1161d-160">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="1161d-161">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1161d-161">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="1161d-162">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="1161d-162">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="1161d-163">открытая асинхронная задача< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="1161d-163">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="1161d-164">parentWindow — это HWND, в котором приложение будет подключаться к визуальному дереву WebView.</span><span class="sxs-lookup"><span data-stu-id="1161d-164">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="1161d-165">Это HWND того, что приложение получит ввод указателя или мыши, предназначенное для WebView (и для пересылки потребуется функция SendMouseInput/SendPointerInput).</span><span class="sxs-lookup"><span data-stu-id="1161d-165">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="1161d-166">Если приложение перемещает визуальное дерево WebView в другое окно, ему необходимо настроить CoreWebView2CompositionController. ParentWindow, чтобы обновить новый родительский дескриптор HWND визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="1161d-166">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="1161d-167">Задайте свойство RootVisualTarget в созданном CoreWebView2CompositionController, чтобы предоставить визуальное размещение визуального дерева браузера.</span><span class="sxs-lookup"><span data-stu-id="1161d-167">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="1161d-168">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="1161d-168">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="1161d-169">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="1161d-169">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="1161d-170">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="1161d-170">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="1161d-171">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="1161d-171">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="1161d-172">открытая асинхронная задача< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="1161d-172">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="1161d-173">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="1161d-173">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="1161d-174">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="1161d-174">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="1161d-175">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1161d-175">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="1161d-176">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="1161d-176">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="1161d-177">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="1161d-177">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="1161d-178">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="1161d-178">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="1161d-179">Создание пустого CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="1161d-179">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="1161d-180">общедоступная [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="1161d-180">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="1161d-181">Возвращенные CoreWebView2PointerInfo должны быть заполнены всеми соответствующими сведениями перед вызовом SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="1161d-181">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="1161d-182">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="1161d-182">CreateWebResourceResponse</span></span> 

<span data-ttu-id="1161d-183">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="1161d-183">Create a new web resource response object.</span></span>

> <span data-ttu-id="1161d-184">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(потоковый контент, int StatusCode, String ReasonPhrase, заголовки строк)</span><span class="sxs-lookup"><span data-stu-id="1161d-184">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="1161d-185">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="1161d-185">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="1161d-186">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать CoreWebView2HttpResponseHeaders для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="1161d-186">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="1161d-187">Сведения о других параметрах смотрите в CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="1161d-187">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="1161d-188">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="1161d-188">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="1161d-189">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="1161d-189">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

> <span data-ttu-id="1161d-190">общедоступная статическая строка [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(String browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="1161d-190">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

##### <span data-ttu-id="1161d-191">Параметры</span><span class="sxs-lookup"><span data-stu-id="1161d-191">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="1161d-192">Относительный путь к папке, содержащей внедренный край.</span><span class="sxs-lookup"><span data-stu-id="1161d-192">The relative path to the folder that contains the embedded Edge.</span></span>

#### <span data-ttu-id="1161d-193">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="1161d-193">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="1161d-194">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="1161d-194">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="1161d-195">общедоступный объект [GetProviderForHwnd](#getproviderforhwnd)(IntPtr HWND)</span><span class="sxs-lookup"><span data-stu-id="1161d-195">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

