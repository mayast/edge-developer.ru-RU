---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 3af7c02f51a203e434c92bac5219dc4db58f406b
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699143"
---
# <span data-ttu-id="cd3b8-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="cd3b8-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="cd3b8-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="cd3b8-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="cd3b8-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="cd3b8-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="cd3b8-107">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="cd3b8-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="cd3b8-108">Summary</span></span>

 <span data-ttu-id="cd3b8-109">Участников</span><span class="sxs-lookup"><span data-stu-id="cd3b8-109">Members</span></span>                        | <span data-ttu-id="cd3b8-110">Описания</span><span class="sxs-lookup"><span data-stu-id="cd3b8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cd3b8-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="cd3b8-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="cd3b8-112">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="cd3b8-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cd3b8-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="cd3b8-114">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="cd3b8-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="cd3b8-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="cd3b8-116">Правильно Сравните версии браузеров, чтобы определить, какая версия более новая или более ранняя.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-116">Compare browser versions correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="cd3b8-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="cd3b8-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="cd3b8-118">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="cd3b8-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="cd3b8-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="cd3b8-120">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="cd3b8-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="cd3b8-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="cd3b8-122">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="cd3b8-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="cd3b8-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="cd3b8-124">Создание пустого CoreWebView2ExperimentalPointerInfo.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-124">Create an empty CoreWebView2ExperimentalPointerInfo.</span></span>
[<span data-ttu-id="cd3b8-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="cd3b8-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="cd3b8-126">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="cd3b8-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="cd3b8-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="cd3b8-128">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-128">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>
[<span data-ttu-id="cd3b8-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="cd3b8-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="cd3b8-130">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="cd3b8-131">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="cd3b8-132">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="cd3b8-133">Участников</span><span class="sxs-lookup"><span data-stu-id="cd3b8-133">Members</span></span>

#### <span data-ttu-id="cd3b8-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="cd3b8-134">BrowserVersionString</span></span> 

<span data-ttu-id="cd3b8-135">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="cd3b8-136">общедоступная строка [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="cd3b8-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="cd3b8-137">Это соответствует формату API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="cd3b8-138">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="cd3b8-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="cd3b8-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="cd3b8-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="cd3b8-140">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-140">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="cd3b8-141">событие EventHandler< объект > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="cd3b8-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="cd3b8-142">Для использования более новой версии браузера необходимо создать новую среду и WebView.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="cd3b8-143">Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="cd3b8-144">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="cd3b8-145">Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="cd3b8-146">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="cd3b8-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="cd3b8-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="cd3b8-148">Правильно Сравните версии браузеров, чтобы определить, какая версия более новая или более ранняя.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-148">Compare browser versions correctly to determine which version is newer, older or same.</span></span>

> <span data-ttu-id="cd3b8-149">общедоступный статический целочисленный [CompareBrowserVersions](#comparebrowserversions)(строковый Version1, строка Version2)</span><span class="sxs-lookup"><span data-stu-id="cd3b8-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="cd3b8-150">Возвращает значение-1, 0 или 1 в зависимости от того, является ли Version1 меньше, равно или больше Version2, соответственно.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-150">Returns -1, 0 or 1 depending on whether version1 is less than, equal to or greater than version2, respectively.</span></span>

##### <span data-ttu-id="cd3b8-151">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd3b8-151">Parameters</span></span>
* `version1` <span data-ttu-id="cd3b8-152">Одна из строк версии для сравнения.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-152">One of the version strings to compare.</span></span> 

* `version2` <span data-ttu-id="cd3b8-153">Другая сравниваемая строка версии.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-153">The other version string to compare.</span></span>

#### <span data-ttu-id="cd3b8-154">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="cd3b8-154">CreateAsync</span></span> 

<span data-ttu-id="cd3b8-155">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-155">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="cd3b8-156">общедоступная статическая асинхронная задача< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(строка browserExecutableFolder, строка userDataFolder, CoreWebView2EnvironmentOptions параметры)</span><span class="sxs-lookup"><span data-stu-id="cd3b8-156">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="cd3b8-157">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd3b8-157">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="cd3b8-158">Относительный путь к папке, содержащей внедренный край.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-158">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="cd3b8-159">userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-159">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="cd3b8-160">Параметры, используемые для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-160">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="cd3b8-161">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="cd3b8-161">CreateCoreWebView2CompositionControllerAsync</span></span> 

> [!NOTE]
> <span data-ttu-id="cd3b8-162">Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="cd3b8-162">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="cd3b8-163">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-163">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="cd3b8-164">открытая асинхронная задача< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="cd3b8-164">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="cd3b8-165">parentWindow — это HWND, в котором приложение будет подключаться к визуальному дереву WebView.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-165">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="cd3b8-166">Это HWND того, что приложение получит ввод указателя или мыши, предназначенное для WebView (и для пересылки потребуется функция SendMouseInput/SendPointerInput).</span><span class="sxs-lookup"><span data-stu-id="cd3b8-166">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="cd3b8-167">Если приложение перемещает визуальное дерево WebView в другое окно, ему необходимо настроить CoreWebView2CompositionController. ParentWindow, чтобы обновить новый родительский дескриптор HWND визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-167">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="cd3b8-168">Задайте свойство RootVisualTarget в созданном CoreWebView2CompositionController, чтобы предоставить визуальное размещение визуального дерева браузера.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-168">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="cd3b8-169">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-169">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="cd3b8-170">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-170">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="cd3b8-171">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="cd3b8-171">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="cd3b8-172">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-172">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="cd3b8-173">открытая асинхронная задача< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="cd3b8-173">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="cd3b8-174">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-174">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="cd3b8-175">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-175">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="cd3b8-176">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-176">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="cd3b8-177">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-177">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="cd3b8-178">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-178">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="cd3b8-179">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="cd3b8-179">CreateCoreWebView2PointerInfo</span></span> 

> [!NOTE]
> <span data-ttu-id="cd3b8-180">Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="cd3b8-180">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="cd3b8-181">Создание пустого CoreWebView2ExperimentalPointerInfo.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-181">Create an empty CoreWebView2ExperimentalPointerInfo.</span></span>

> <span data-ttu-id="cd3b8-182">общедоступная [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="cd3b8-182">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="cd3b8-183">Возвращенные CoreWebView2ExperimentalPointerInfo должны быть заполнены всеми соответствующими сведениями перед вызовом SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-183">The returned CoreWebView2ExperimentalPointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="cd3b8-184">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="cd3b8-184">CreateWebResourceResponse</span></span> 

<span data-ttu-id="cd3b8-185">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-185">Create a new web resource response object.</span></span>

> <span data-ttu-id="cd3b8-186">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(потоковый контент, int StatusCode, String ReasonPhrase, заголовки строк)</span><span class="sxs-lookup"><span data-stu-id="cd3b8-186">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="cd3b8-187">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-187">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="cd3b8-188">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать CoreWebView2HttpResponseHeaders для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-188">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="cd3b8-189">Сведения о других параметрах смотрите в CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-189">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="cd3b8-190">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="cd3b8-190">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="cd3b8-191">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-191">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

> <span data-ttu-id="cd3b8-192">общедоступная статическая строка [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(String browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="cd3b8-192">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

##### <span data-ttu-id="cd3b8-193">Параметры</span><span class="sxs-lookup"><span data-stu-id="cd3b8-193">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="cd3b8-194">Относительный путь к папке, содержащей внедренный край.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-194">The relative path to the folder that contains the embedded Edge.</span></span>

#### <span data-ttu-id="cd3b8-195">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="cd3b8-195">GetProviderForHwnd</span></span> 

> [!NOTE]
> <span data-ttu-id="cd3b8-196">Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).</span><span class="sxs-lookup"><span data-stu-id="cd3b8-196">This is an [experimental API](../../../concepts/versioning.md#experimental-apis) that shipped with our SDK version [0.9.538-prerelease](../../../releasenotes.md#09538).</span></span>

<span data-ttu-id="cd3b8-197">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="cd3b8-197">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="cd3b8-198">общедоступный объект [GetProviderForHwnd](#getproviderforhwnd)(IntPtr HWND)</span><span class="sxs-lookup"><span data-stu-id="cd3b8-198">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

