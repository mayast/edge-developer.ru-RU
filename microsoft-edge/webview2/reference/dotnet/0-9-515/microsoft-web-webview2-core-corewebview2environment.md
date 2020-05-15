---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: be8f475d4c1a886a92b46144f2bffde2d49dc9d4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654933"
---
# <span data-ttu-id="3d779-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="3d779-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

<span data-ttu-id="3d779-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3d779-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3d779-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="3d779-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3d779-107">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="3d779-107">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="3d779-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3d779-108">Summary</span></span>

 <span data-ttu-id="3d779-109">Участников</span><span class="sxs-lookup"><span data-stu-id="3d779-109">Members</span></span>                        | <span data-ttu-id="3d779-110">Описания</span><span class="sxs-lookup"><span data-stu-id="3d779-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d779-111">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="3d779-111">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="3d779-112">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="3d779-112">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="3d779-113">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="3d779-113">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="3d779-114">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="3d779-114">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="3d779-115">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="3d779-115">CreateAsync</span></span>](#createasync) | <span data-ttu-id="3d779-116">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="3d779-116">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="3d779-117">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="3d779-117">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="3d779-118">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="3d779-118">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="3d779-119">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="3d779-119">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="3d779-120">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="3d779-120">Create a new web resource response object.</span></span>

<span data-ttu-id="3d779-121">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="3d779-121">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="3d779-122">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="3d779-122">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="3d779-123">Участников</span><span class="sxs-lookup"><span data-stu-id="3d779-123">Members</span></span>

#### <span data-ttu-id="3d779-124">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="3d779-124">BrowserVersionString</span></span> 

<span data-ttu-id="3d779-125">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="3d779-125">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="3d779-126">общедоступная строка [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="3d779-126">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="3d779-127">Это соответствует формату API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="3d779-127">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="3d779-128">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="3d779-128">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="3d779-129">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="3d779-129">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="3d779-130">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="3d779-130">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="3d779-131">событие EventHandler< объект > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="3d779-131">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="3d779-132">Для использования более новой версии браузера необходимо создать новую среду и WebView.</span><span class="sxs-lookup"><span data-stu-id="3d779-132">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="3d779-133">Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="3d779-133">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="3d779-134">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="3d779-134">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="3d779-135">Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="3d779-135">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="3d779-136">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="3d779-136">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="3d779-137">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="3d779-137">CreateAsync</span></span> 

<span data-ttu-id="3d779-138">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="3d779-138">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="3d779-139">открытая асинхронная задача< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(строка browserExecutableFolder, строка userDataFolder, CoreWebView2EnvironmentOptions параметры)</span><span class="sxs-lookup"><span data-stu-id="3d779-139">public async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="3d779-140">Параметры</span><span class="sxs-lookup"><span data-stu-id="3d779-140">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="3d779-141">Относительный путь к папке, содержащей внедренный край.</span><span class="sxs-lookup"><span data-stu-id="3d779-141">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="3d779-142">userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2.</span><span class="sxs-lookup"><span data-stu-id="3d779-142">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="3d779-143">Параметры, используемые для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="3d779-143">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="3d779-144">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="3d779-144">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="3d779-145">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="3d779-145">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="3d779-146">открытая асинхронная задача< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="3d779-146">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="3d779-147">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="3d779-147">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="3d779-148">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="3d779-148">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="3d779-149">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="3d779-149">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="3d779-150">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="3d779-150">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="3d779-151">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="3d779-151">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="3d779-152">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="3d779-152">CreateWebResourceResponse</span></span> 

<span data-ttu-id="3d779-153">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="3d779-153">Create a new web resource response object.</span></span>

> <span data-ttu-id="3d779-154">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(потоковый контент, int StatusCode, String ReasonPhrase, заголовки строк)</span><span class="sxs-lookup"><span data-stu-id="3d779-154">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="3d779-155">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="3d779-155">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="3d779-156">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать CoreWebView2HttpResponseHeaders для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="3d779-156">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="3d779-157">Сведения о других параметрах смотрите в CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="3d779-157">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

