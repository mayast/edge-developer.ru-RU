---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 986b1dc2870375243a0ee664262216105edd95a8
ms.sourcegitcommit: 3f8c8a5643e416b0851254833f9771192883ec45
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699502"
---
# <span data-ttu-id="f2cc5-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="f2cc5-104">Microsoft.Web.WebView2.Core.CoreWebView2Environment class</span></span> 

> [!NOTE]
> <span data-ttu-id="f2cc5-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="f2cc5-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="f2cc5-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f2cc5-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f2cc5-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="f2cc5-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f2cc5-109">Представляет среду WebView2.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-109">This represents the WebView2 Environment.</span></span>

## <span data-ttu-id="f2cc5-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f2cc5-110">Summary</span></span>

 <span data-ttu-id="f2cc5-111">Участников</span><span class="sxs-lookup"><span data-stu-id="f2cc5-111">Members</span></span>                        | <span data-ttu-id="f2cc5-112">Описания</span><span class="sxs-lookup"><span data-stu-id="f2cc5-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f2cc5-113">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="f2cc5-113">BrowserVersionString</span></span>](#browserversionstring) | <span data-ttu-id="f2cc5-114">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-114">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>
[<span data-ttu-id="f2cc5-115">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="f2cc5-115">NewBrowserVersionAvailable</span></span>](#newbrowserversionavailable) | <span data-ttu-id="f2cc5-116">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-116">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="f2cc5-117">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="f2cc5-117">CreateAsync</span></span>](#createasync) | <span data-ttu-id="f2cc5-118">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-118">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="f2cc5-119">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="f2cc5-119">CreateCoreWebView2ControllerAsync</span></span>](#createcorewebview2controllerasync) | <span data-ttu-id="f2cc5-120">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-120">Asynchronously create a new WebView.</span></span>
[<span data-ttu-id="f2cc5-121">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="f2cc5-121">CreateWebResourceResponse</span></span>](#createwebresourceresponse) | <span data-ttu-id="f2cc5-122">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-122">Create a new web resource response object.</span></span>

<span data-ttu-id="f2cc5-123">Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-123">WebViews created from an environment run on the Browser process specified with environment parameters and objects created from an environment should be used in the same environment.</span></span> <span data-ttu-id="f2cc5-124">Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-124">Using it in different environments are not guaranteed to be compatible and may fail.</span></span>

## <span data-ttu-id="f2cc5-125">Участников</span><span class="sxs-lookup"><span data-stu-id="f2cc5-125">Members</span></span>

#### <span data-ttu-id="f2cc5-126">BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="f2cc5-126">BrowserVersionString</span></span> 

<span data-ttu-id="f2cc5-127">Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-127">The browser version info of the current CoreWebView2Environment, including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="f2cc5-128">общедоступная строка [BrowserVersionString](#browserversionstring)</span><span class="sxs-lookup"><span data-stu-id="f2cc5-128">public string [BrowserVersionString](#browserversionstring)</span></span>

<span data-ttu-id="f2cc5-129">Это соответствует формату API GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-129">This matches the format of the GetAvailableCoreWebView2BrowserVersionString API.</span></span> <span data-ttu-id="f2cc5-130">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="f2cc5-130">Channel names are 'beta', 'dev', and 'canary'.</span></span>

#### <span data-ttu-id="f2cc5-131">NewBrowserVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="f2cc5-131">NewBrowserVersionAvailable</span></span> 

<span data-ttu-id="f2cc5-132">Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-132">The NewBrowserVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="f2cc5-133">событие EventHandler< объект > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span><span class="sxs-lookup"><span data-stu-id="f2cc5-133">public event EventHandler< object > [NewBrowserVersionAvailable](#newbrowserversionavailable)</span></span>

<span data-ttu-id="f2cc5-134">Для использования более новой версии браузера необходимо создать новую среду и WebView.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-134">To use the newer version of the browser you must create a new environment and WebView.</span></span> <span data-ttu-id="f2cc5-135">Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-135">This event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="f2cc5-136">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-136">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="f2cc5-137">Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-137">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the environment and WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="f2cc5-138">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-138">Or simply prompt the user to restart the app.</span></span>

#### <span data-ttu-id="f2cc5-139">CreateAsync</span><span class="sxs-lookup"><span data-stu-id="f2cc5-139">CreateAsync</span></span> 

<span data-ttu-id="f2cc5-140">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-140">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

> <span data-ttu-id="f2cc5-141">общедоступная статическая асинхронная задача< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(строка browserExecutableFolder, строка userDataFolder, CoreWebView2EnvironmentOptions параметры)</span><span class="sxs-lookup"><span data-stu-id="f2cc5-141">public static async Task< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md) > [CreateAsync](#createasync)(string browserExecutableFolder, string userDataFolder, CoreWebView2EnvironmentOptions options)</span></span>

##### <span data-ttu-id="f2cc5-142">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2cc5-142">Parameters</span></span>
* `browserExecutableFolder` <span data-ttu-id="f2cc5-143">Относительный путь к папке, содержащей внедренный край.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-143">The relative path to the folder that contains the embedded Edge.</span></span> 

* `userDataFolder` <span data-ttu-id="f2cc5-144">userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-144">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> 

* `options` <span data-ttu-id="f2cc5-145">Параметры, используемые для создания среды WebView2.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-145">Options used to create WebView2 Environment.</span></span>

#### <span data-ttu-id="f2cc5-146">CreateCoreWebView2ControllerAsync</span><span class="sxs-lookup"><span data-stu-id="f2cc5-146">CreateCoreWebView2ControllerAsync</span></span> 

<span data-ttu-id="f2cc5-147">Асинхронно создайте новый WebView.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-147">Asynchronously create a new WebView.</span></span>

> <span data-ttu-id="f2cc5-148">открытая асинхронная задача< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span><span class="sxs-lookup"><span data-stu-id="f2cc5-148">public async Task< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md) > [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)</span></span>

<span data-ttu-id="f2cc5-149">parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-149">parentWindow is the HWND in which the WebView should be displayed and from which receive input.</span></span> <span data-ttu-id="f2cc5-150">WebView добавит дочернее окно в заданное окно во время создания WebView.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-150">The WebView will add a child window to the provided window during WebView creation.</span></span> <span data-ttu-id="f2cc5-151">Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-151">Z-order and other things impacted by sibling window order will be affected accordingly.</span></span>

<span data-ttu-id="f2cc5-152">Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-152">It is recommended that the application set Application User Model ID for the process or the application window.</span></span> <span data-ttu-id="f2cc5-153">Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-153">If none is set, during WebView creation a generated Application User Model ID is set to root window of parentWindow.</span></span>

#### <span data-ttu-id="f2cc5-154">CreateWebResourceResponse</span><span class="sxs-lookup"><span data-stu-id="f2cc5-154">CreateWebResourceResponse</span></span> 

<span data-ttu-id="f2cc5-155">Создание нового объекта ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-155">Create a new web resource response object.</span></span>

> <span data-ttu-id="f2cc5-156">Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(потоковый контент, int StatusCode, String ReasonPhrase, заголовки строк)</span><span class="sxs-lookup"><span data-stu-id="f2cc5-156">public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(Stream Content, int StatusCode, string ReasonPhrase, string Headers)</span></span>

<span data-ttu-id="f2cc5-157">Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-157">The headers is the raw response header string delimited by newline.</span></span> <span data-ttu-id="f2cc5-158">Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать CoreWebView2HttpResponseHeaders для создания заголовков построчно.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-158">It's also possible to create this object with empty headers string and then use the CoreWebView2HttpResponseHeaders to construct the headers line by line.</span></span> <span data-ttu-id="f2cc5-159">Сведения о других параметрах смотрите в CoreWebView2WebResourceResponse.</span><span class="sxs-lookup"><span data-stu-id="f2cc5-159">For information on other parameters see CoreWebView2WebResourceResponse.</span></span>

