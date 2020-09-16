---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 05b8a10c723ae57b2c95551f4d5043f3336eba3b
ms.sourcegitcommit: 65db518273b3cd69f1b3c528809600719b9b70aa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2020
ms.locfileid: "11016328"
---
# <span data-ttu-id="a0a5e-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="a0a5e-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="a0a5e-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a0a5e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a0a5e-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a0a5e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a0a5e-107">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="a0a5e-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a0a5e-108">Summary</span></span>

 <span data-ttu-id="a0a5e-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a0a5e-109">Members</span></span>                        | <span data-ttu-id="a0a5e-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a0a5e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a0a5e-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a0a5e-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="a0a5e-112">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="a0a5e-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a0a5e-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="a0a5e-114">NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-114">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>
[<span data-ttu-id="a0a5e-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="a0a5e-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="a0a5e-116">Сравните версии браузеров, чтобы определить, совпадают ли они или различаются.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-116">Compare browser versions to determine if they match or are different.</span></span>
[<span data-ttu-id="a0a5e-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="a0a5e-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="a0a5e-118">Создает среду Evergreen WebView2 с помощью установленной версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-118">Creates an evergreen WebView2 Environment using the installed version of Microsoft Edge.</span></span>
[<span data-ttu-id="a0a5e-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a0a5e-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="a0a5e-120">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="a0a5e-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a0a5e-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="a0a5e-122">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="a0a5e-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="a0a5e-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="a0a5e-124">Создание пустого CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-124">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="a0a5e-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="a0a5e-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="a0a5e-126">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="a0a5e-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a0a5e-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="a0a5e-128">Получение сведений о версии браузера.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-128">Get the browser version information.</span></span>
[<span data-ttu-id="a0a5e-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="a0a5e-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="a0a5e-130">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="a0a5e-131">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="a0a5e-132">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span> 

## <span data-ttu-id="a0a5e-133">Участников</span><span class="sxs-lookup"><span data-stu-id="a0a5e-133">Members</span></span>

#### <span data-ttu-id="a0a5e-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a0a5e-134">BrowserVersionString</span></span> 

<span data-ttu-id="a0a5e-135">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="a0a5e-136">общедоступная строка [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="a0a5e-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="a0a5e-137">Это соответствует формату API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="a0a5e-138">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="a0a5e-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="a0a5e-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a0a5e-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="a0a5e-140">NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-140">NewBrowserVersionAvailable fires when a newer version of the Edge browser is installed and available for use via WebView2.</span></span>

> <span data-ttu-id="a0a5e-141">событие EventHandler< объект > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="a0a5e-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="a0a5e-142">Для использования более новой версии браузера необходимо создать новую среду и WebView.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="a0a5e-143">Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="a0a5e-144">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="a0a5e-145">Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="a0a5e-146">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="a0a5e-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="a0a5e-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="a0a5e-148">Сравните версии браузеров, чтобы определить, совпадают ли они или различаются.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-148">Compare browser versions to determine if they match or are different.</span></span>

> <span data-ttu-id="a0a5e-149">общедоступный статический целочисленный [CompareBrowserVersions](#comparebrowserversions)(строковый Version1, строка Version2)</span><span class="sxs-lookup"><span data-stu-id="a0a5e-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="a0a5e-150">Возвращает значение-1, 0 или 1 в зависимости от того, является ли первая версия меньше, равно или больше, чем Вторая сравниваемая версия.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-150">Returns -1, 0 or 1 depending on whether the first version is less than, equal to or greater than the second version being compared.</span></span>

<span data-ttu-id="a0a5e-151">Входные данные могут напрямую использовать versionInfo, полученный от GetAvailableCoreWebView2BrowserVersionString, сведения о канале будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-151">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

##### <span data-ttu-id="a0a5e-152">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0a5e-152">Parameters</span></span>
* `version1` <span data-ttu-id="a0a5e-153">Первая сравниваемая версия.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-153">The first version to compare.</span></span> 

* `version2` <span data-ttu-id="a0a5e-154">Вторая версия для сравнения.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-154">The second version to compare.</span></span>

#### <span data-ttu-id="a0a5e-155">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="a0a5e-155">CreateAsync</span></span> 

<span data-ttu-id="a0a5e-156">Создает среду Evergreen WebView2 с помощью установленной версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-156">Creates an evergreen WebView2 Environment using the installed version of Microsoft Edge.</span></span>

> <span data-ttu-id="a0a5e-157">общедоступная статическая асинхронная задача< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(строка browserExecutableFolder, строка userDataFolder, CoreWebView2EnvironmentOptions параметры)</span><span class="sxs-lookup"><span data-stu-id="a0a5e-157">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="a0a5e-158">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0a5e-158">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="a0a5e-159">Относительный путь к папке, содержащей фиксированную версию среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-159">The relative path to the folder that contains the fixed version of the WebView2 Runtime.</span></span> 

* `userDataFolder` <span data-ttu-id="a0a5e-160">userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-160">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="a0a5e-161">Параметры, используемые для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-161">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="a0a5e-162">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a0a5e-162">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="a0a5e-163">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-163">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="a0a5e-164">открытая асинхронная задача< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="a0a5e-164">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="a0a5e-165">parentWindow — это HWND, в котором приложение будет подключаться к визуальному дереву WebView.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-165">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="a0a5e-166">Это HWND того, что приложение получит ввод указателя или мыши, предназначенное для WebView (и для пересылки потребуется функция SendMouseInput/SendPointerInput).</span><span class="sxs-lookup"><span data-stu-id="a0a5e-166">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="a0a5e-167">Если приложение перемещает визуальное дерево WebView в другое окно, ему необходимо настроить CoreWebView2CompositionController. ParentWindow, чтобы обновить новый родительский дескриптор HWND визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-167">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="a0a5e-168">Задайте свойство RootVisualTarget в созданном CoreWebView2CompositionController, чтобы предоставить визуальное размещение визуального дерева браузера.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-168">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="a0a5e-169">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-169">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="a0a5e-170">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-170">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="a0a5e-171">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="a0a5e-171">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="a0a5e-172">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-172">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="a0a5e-173">открытая асинхронная задача< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="a0a5e-173">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="a0a5e-174">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-174">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="a0a5e-175">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-175">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="a0a5e-176">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-176">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="a0a5e-177">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-177">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="a0a5e-178">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-178">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="a0a5e-179">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="a0a5e-179">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="a0a5e-180">Создание пустого CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-180">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="a0a5e-181">общедоступная [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="a0a5e-181">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="a0a5e-182">Возвращенные CoreWebView2PointerInfo должны быть заполнены всеми соответствующими сведениями перед вызовом SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-182">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="a0a5e-183">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="a0a5e-183">CreateWebResourceResponse</span></span> 

<span data-ttu-id="a0a5e-184">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-184">Create a new web resource response object.</span></span>

> <span data-ttu-id="a0a5e-185">Public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(потоковый контент, int StatusCode, String ReasonPhrase, заголовки строк)</span><span class="sxs-lookup"><span data-stu-id="a0a5e-185">public [CoreWebView2WebResourceResponse](microsoft-web-webview2-core-corewebview2webresourceresponse.md) [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="a0a5e-186">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-186">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="a0a5e-187">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать CoreWebView2HttpResponseHeaders для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-187">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="a0a5e-188">Сведения о других параметрах смотрите в CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-188">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="a0a5e-189">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="a0a5e-189">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="a0a5e-190">Получение сведений о версии браузера.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-190">Get the browser version information.</span></span>

> <span data-ttu-id="a0a5e-191">общедоступная статическая строка [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(String browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="a0a5e-191">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

<span data-ttu-id="a0a5e-192">Кроме того, вы получаете имя канала, если канал не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-192">You also get the channel name if the channel is not a stable channel.</span></span> <span data-ttu-id="a0a5e-193">Если вы используете среду выполнения WebView2, имя канала возвращено не будет.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-193">If you use the WebView2 Runtime, no channel name is returned.</span></span>

##### <span data-ttu-id="a0a5e-194">Параметры</span><span class="sxs-lookup"><span data-stu-id="a0a5e-194">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="a0a5e-195">Относительный путь к папке, содержащей фиксированную версию среды выполнения WebView2.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-195">The relative path to the folder that contains the fixed version of the WebView2 Runtime.</span></span>

#### <span data-ttu-id="a0a5e-196">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="a0a5e-196">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="a0a5e-197">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="a0a5e-197">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="a0a5e-198">общедоступный объект [GetProviderForHwnd](#getproviderforhwnd)(IntPtr HWND)</span><span class="sxs-lookup"><span data-stu-id="a0a5e-198">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>
