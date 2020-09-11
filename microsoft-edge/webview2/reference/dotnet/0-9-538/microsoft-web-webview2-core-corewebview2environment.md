---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: d1e30c17239eb1b609eb3f2c63e48a3a59616131
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011029"
---
# <span data-ttu-id="da9bb-104">класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="da9bb-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="da9bb-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="da9bb-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="da9bb-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="da9bb-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="da9bb-107">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="da9bb-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="da9bb-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="da9bb-108">Summary</span></span>

 <span data-ttu-id="da9bb-109">Участников</span><span class="sxs-lookup"><span data-stu-id="da9bb-109">Members</span></span>                        | <span data-ttu-id="da9bb-110">Описания</span><span class="sxs-lookup"><span data-stu-id="da9bb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="da9bb-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="da9bb-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="da9bb-112">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="da9bb-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="da9bb-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="da9bb-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="da9bb-114">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="da9bb-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="da9bb-115">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="da9bb-115">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="da9bb-116">Правильно Сравните версии браузеров, чтобы определить, какая версия более новая или более ранняя.</span><span class="sxs-lookup"><span data-stu-id="da9bb-116">Compare browser versions correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="da9bb-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="da9bb-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="da9bb-118">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="da9bb-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="da9bb-119">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="da9bb-119">CreateCoreWebView2CompositionControllerAsync</span></span>](#createcorewebview2compositioncontrollerasync) | <span data-ttu-id="da9bb-120">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="da9bb-120">Asynchronously create a new WebView for use with visual hosting.</span></span>
[<span data-ttu-id="da9bb-121">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="da9bb-121">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="da9bb-122">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="da9bb-122">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="da9bb-123">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="da9bb-123">CreateCoreWebView2PointerInfo</span></span>](#createcorewebview2pointerinfo) | <span data-ttu-id="da9bb-124">Создание пустого CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="da9bb-124">Create an empty CoreWebView2PointerInfo.</span></span>
[<span data-ttu-id="da9bb-125">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="da9bb-125">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="da9bb-126">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="da9bb-126">Create a new web resource response object.</span></span>
[<span data-ttu-id="da9bb-127">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="da9bb-127">GetAvailableBrowserVersionString</span></span>](#getavailablebrowserversionstring) | <span data-ttu-id="da9bb-128">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="da9bb-128">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>
[<span data-ttu-id="da9bb-129">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="da9bb-129">GetProviderForHwnd</span></span>](#getproviderforhwnd) | <span data-ttu-id="da9bb-130">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="da9bb-130">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

<span data-ttu-id="da9bb-131">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="da9bb-131">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="da9bb-132">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="da9bb-132">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="da9bb-133">Участников</span><span class="sxs-lookup"><span data-stu-id="da9bb-133">Members</span></span>

#### <span data-ttu-id="da9bb-134">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="da9bb-134">BrowserVersionString</span></span> 

<span data-ttu-id="da9bb-135">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="da9bb-135">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="da9bb-136">общедоступная строка [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="da9bb-136">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="da9bb-137">Это соответствует формату API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="da9bb-137">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="da9bb-138">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="da9bb-138">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="da9bb-139">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="da9bb-139">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="da9bb-140">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="da9bb-140">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="da9bb-141">событие EventHandler< объект > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="da9bb-141">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="da9bb-142">Для использования более новой версии браузера необходимо создать новую среду и WebView.</span><span class="sxs-lookup"><span data-stu-id="da9bb-142">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="da9bb-143">Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="da9bb-143">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="da9bb-144">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="da9bb-144">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="da9bb-145">Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="da9bb-145">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="da9bb-146">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="da9bb-146">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="da9bb-147">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="da9bb-147">CompareBrowserVersions</span></span> 

<span data-ttu-id="da9bb-148">Правильно Сравните версии браузеров, чтобы определить, какая версия более новая или более ранняя.</span><span class="sxs-lookup"><span data-stu-id="da9bb-148">Compare browser versions correctly to determine which version is newer, older or same.</span></span>

> <span data-ttu-id="da9bb-149">общедоступный статический целочисленный [CompareBrowserVersions](#comparebrowserversions)(строковый Version1, строка Version2)</span><span class="sxs-lookup"><span data-stu-id="da9bb-149">public static int [CompareBrowserVersions](#comparebrowserversions)(string version1, string version2)</span></span>

<span data-ttu-id="da9bb-150">Возвращает значение-1, 0 или 1 в зависимости от того, является ли Version1 меньше, равно или больше Version2, соответственно.</span><span class="sxs-lookup"><span data-stu-id="da9bb-150">Returns -1, 0 or 1 depending on whether version1 is less than, equal to or greater than version2, respectively.</span></span>

##### <span data-ttu-id="da9bb-151">Параметры</span><span class="sxs-lookup"><span data-stu-id="da9bb-151">Parameters</span></span>
* `version1` <span data-ttu-id="da9bb-152">Одна из строк версии для сравнения.</span><span class="sxs-lookup"><span data-stu-id="da9bb-152">One of the version strings to compare.</span></span> 

* `version2` <span data-ttu-id="da9bb-153">Другая сравниваемая строка версии.</span><span class="sxs-lookup"><span data-stu-id="da9bb-153">The other version string to compare.</span></span>

#### <span data-ttu-id="da9bb-154">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="da9bb-154">CreateAsync</span></span> 

<span data-ttu-id="da9bb-155">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="da9bb-155">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="da9bb-156">общедоступная статическая асинхронная задача< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(строка browserExecutableFolder, строка userDataFolder, CoreWebView2EnvironmentOptions параметры)</span><span class="sxs-lookup"><span data-stu-id="da9bb-156">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="da9bb-157">Параметры</span><span class="sxs-lookup"><span data-stu-id="da9bb-157">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="da9bb-158">Относительный путь к папке, содержащей внедренный край.</span><span class="sxs-lookup"><span data-stu-id="da9bb-158">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="da9bb-159">userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2.</span><span class="sxs-lookup"><span data-stu-id="da9bb-159">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="da9bb-160">Параметры, используемые для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="da9bb-160">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="da9bb-161">CreateCoreWebView2CompositionControllerAsync</span><span class="sxs-lookup"><span data-stu-id="da9bb-161">CreateCoreWebView2CompositionControllerAsync</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="da9bb-162">Асинхронно создайте новый WebView для использования с визуальным размещением.</span><span class="sxs-lookup"><span data-stu-id="da9bb-162">Asynchronously create a new WebView for use with visual hosting.</span></span>

> <span data-ttu-id="da9bb-163">открытая асинхронная задача< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="da9bb-163">public async Task< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md) > [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="da9bb-164">parentWindow — это HWND, в котором приложение будет подключаться к визуальному дереву WebView.</span><span class="sxs-lookup"><span data-stu-id="da9bb-164">parentWindow is the HWND in which the app will connect the visual tree of the WebView.</span></span> <span data-ttu-id="da9bb-165">Это HWND того, что приложение получит ввод указателя или мыши, предназначенное для WebView (и для пересылки потребуется функция SendMouseInput/SendPointerInput).</span><span class="sxs-lookup"><span data-stu-id="da9bb-165">This will be the HWND that the app will receive pointer/ mouse input meant for the WebView (and will need to use SendMouseInput/ SendPointerInput to forward).</span></span> <span data-ttu-id="da9bb-166">Если приложение перемещает визуальное дерево WebView в другое окно, ему необходимо настроить CoreWebView2CompositionController. ParentWindow, чтобы обновить новый родительский дескриптор HWND визуального дерева.</span><span class="sxs-lookup"><span data-stu-id="da9bb-166">If the app moves the WebView visual tree to underneath a different window, then it needs to set CoreWebView2CompositionController.ParentWindow to update the new parent HWND of the visual tree.</span></span>

<span data-ttu-id="da9bb-167">Задайте свойство RootVisualTarget в созданном CoreWebView2CompositionController, чтобы предоставить визуальное размещение визуального дерева браузера.</span><span class="sxs-lookup"><span data-stu-id="da9bb-167">Set RootVisualTarget property on the created CoreWebView2CompositionController to provide a visual to host the browser's visual tree.</span></span>

<span data-ttu-id="da9bb-168">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="da9bb-168">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="da9bb-169">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="da9bb-169">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="da9bb-170">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="da9bb-170">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="da9bb-171">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="da9bb-171">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="da9bb-172">открытая асинхронная задача< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="da9bb-172">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="da9bb-173">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="da9bb-173">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="da9bb-174">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="da9bb-174">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="da9bb-175">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="da9bb-175">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="da9bb-176">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="da9bb-176">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="da9bb-177">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="da9bb-177">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="da9bb-178">CreateCoreWebView2PointerInfo</span><span class="sxs-lookup"><span data-stu-id="da9bb-178">CreateCoreWebView2PointerInfo</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="da9bb-179">Создание пустого CoreWebView2PointerInfo.</span><span class="sxs-lookup"><span data-stu-id="da9bb-179">Create an empty CoreWebView2PointerInfo.</span></span>

> <span data-ttu-id="da9bb-180">общедоступная [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span><span class="sxs-lookup"><span data-stu-id="da9bb-180">public [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()</span></span>

<span data-ttu-id="da9bb-181">Возвращенные CoreWebView2PointerInfo должны быть заполнены всеми соответствующими сведениями перед вызовом SendPointerInput.</span><span class="sxs-lookup"><span data-stu-id="da9bb-181">The returned CoreWebView2PointerInfo needs to be populated with all of the relevant info before calling SendPointerInput.</span></span>

#### <span data-ttu-id="da9bb-182">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="da9bb-182">CreateWebResourceResponse</span></span> 

<span data-ttu-id="da9bb-183">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="da9bb-183">Create a new web resource response object.</span></span>

> <span data-ttu-id="da9bb-184">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(потоковый контент, int StatusCode, String ReasonPhrase, заголовки строк)</span><span class="sxs-lookup"><span data-stu-id="da9bb-184">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="da9bb-185">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="da9bb-185">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="da9bb-186">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать CoreWebView2HttpResponseHeaders для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="da9bb-186">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="da9bb-187">Сведения о других параметрах смотрите в CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="da9bb-187">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

#### <span data-ttu-id="da9bb-188">GetAvailableBrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="da9bb-188">GetAvailableBrowserVersionString</span></span> 

<span data-ttu-id="da9bb-189">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="da9bb-189">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

> <span data-ttu-id="da9bb-190">общедоступная статическая строка [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(String browserExecutableFolder)</span><span class="sxs-lookup"><span data-stu-id="da9bb-190">public static string [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(string browserExecutableFolder)</span></span>

##### <span data-ttu-id="da9bb-191">Параметры</span><span class="sxs-lookup"><span data-stu-id="da9bb-191">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="da9bb-192">Относительный путь к папке, содержащей внедренный край.</span><span class="sxs-lookup"><span data-stu-id="da9bb-192">The relative path to the folder that contains the embedded Edge.</span></span>

#### <span data-ttu-id="da9bb-193">GetProviderForHwnd</span><span class="sxs-lookup"><span data-stu-id="da9bb-193">GetProviderForHwnd</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

<span data-ttu-id="da9bb-194">Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.</span><span class="sxs-lookup"><span data-stu-id="da9bb-194">Returns the UI Automation Provider for the CoreWebView2CompositionController that corresponds with the given HWND.</span></span>

> <span data-ttu-id="da9bb-195">общедоступный объект [GetProviderForHwnd](#getproviderforhwnd)(IntPtr HWND)</span><span class="sxs-lookup"><span data-stu-id="da9bb-195">public object [GetProviderForHwnd](#getproviderforhwnd)(IntPtr hwnd)</span></span>

