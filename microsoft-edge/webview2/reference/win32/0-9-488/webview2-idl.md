---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8a684d2a00aa1ae580a3b4391c9f6037dc8f9085
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697072"
---
# <span data-ttu-id="52da6-104">Глобальные настройки</span><span class="sxs-lookup"><span data-stu-id="52da6-104">Globals</span></span> 

> [!NOTE]
> <span data-ttu-id="52da6-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="52da6-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="52da6-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="52da6-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

## <span data-ttu-id="52da6-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="52da6-107">Summary</span></span>

 <span data-ttu-id="52da6-108">Участников</span><span class="sxs-lookup"><span data-stu-id="52da6-108">Members</span></span>                        | <span data-ttu-id="52da6-109">Описания</span><span class="sxs-lookup"><span data-stu-id="52da6-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="52da6-110">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="52da6-110">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="52da6-111">Этот метод предназначен для всех пользователей, которым нужно правильно сравнить версию, чтобы определить, какая версия более поздняя, устаревшая или та же.</span><span class="sxs-lookup"><span data-stu-id="52da6-111">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="52da6-112">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="52da6-112">CreateCoreWebView2Environment</span></span>](#createcorewebview2environment) | <span data-ttu-id="52da6-113">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="52da6-113">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="52da6-114">CreateCoreWebView2EnvironmentWithDetails</span><span class="sxs-lookup"><span data-stu-id="52da6-114">CreateCoreWebView2EnvironmentWithDetails</span></span>](#createcorewebview2environmentwithdetails) | <span data-ttu-id="52da6-115">Этот API-интерфейс будет удален в следующем выпуске SDK.</span><span class="sxs-lookup"><span data-stu-id="52da6-115">This API is going to be removed in next SDK release.</span></span>
[<span data-ttu-id="52da6-116">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="52da6-116">CreateCoreWebView2EnvironmentWithOptions</span></span>](#createcorewebview2environmentwithoptions) | <span data-ttu-id="52da6-117">DLL Export для создания среды WebView2 с пользовательской версией EDGE, каталогом данных пользователя и (или) дополнительными параметрами.</span><span class="sxs-lookup"><span data-stu-id="52da6-117">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>
[<span data-ttu-id="52da6-118">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="52da6-118">GetAvailableCoreWebView2BrowserVersionString</span></span>](#getavailablecorewebview2browserversionstring) | <span data-ttu-id="52da6-119">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="52da6-119">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

## <span data-ttu-id="52da6-120">Участников</span><span class="sxs-lookup"><span data-stu-id="52da6-120">Members</span></span>

#### <span data-ttu-id="52da6-121">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="52da6-121">CompareBrowserVersions</span></span> 

> <span data-ttu-id="52da6-122">общедоступные STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR Version1, PCWSTR Version2, int \* result)</span><span class="sxs-lookup"><span data-stu-id="52da6-122">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span></span>

<span data-ttu-id="52da6-123">Этот метод предназначен для всех пользователей, которым нужно правильно сравнить версию, чтобы определить, какая версия более поздняя, устаревшая или та же.</span><span class="sxs-lookup"><span data-stu-id="52da6-123">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>

<span data-ttu-id="52da6-124">Он может использоваться для определения того, следует ли использовать webview2 или определенную базу функций в версии.</span><span class="sxs-lookup"><span data-stu-id="52da6-124">It can be used to determine whether to use webview2 or certain feature base on version.</span></span> <span data-ttu-id="52da6-125">Задает для результата значение-1, 0 или 1, если Version1 меньше, равно или больше Version2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="52da6-125">Sets the value of result to -1, 0 or 1 if version1 is less than, equal or greater than version2 respectively.</span></span> <span data-ttu-id="52da6-126">Возвращает E_INVALIDARG, если не удается проанализировать ни одну из строк версии, ни какой из входных параметров имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="52da6-126">Returns E_INVALIDARG if it fails to parse any of the version strings or any input parameter is null.</span></span> <span data-ttu-id="52da6-127">Входные данные могут напрямую использовать versionInfo, полученный от GetAvailableCoreWebView2BrowserVersionString, сведения о канале будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="52da6-127">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

#### <span data-ttu-id="52da6-128">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="52da6-128">CreateCoreWebView2Environment</span></span> 

> <span data-ttu-id="52da6-129">общедоступная STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="52da6-129">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="52da6-130">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="52da6-130">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

<span data-ttu-id="52da6-131">Это эквивалентно вызову CreateCoreWebView2EnvironmentWithOptions с помощью nullptr для browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="52da6-131">This is equivalent to calling CreateCoreWebView2EnvironmentWithOptions with nullptr for browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span></span> <span data-ttu-id="52da6-132">Более подробную информацию вы увидите в CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="52da6-132">See CreateCoreWebView2EnvironmentWithOptions for more details.</span></span>

#### <span data-ttu-id="52da6-133">CreateCoreWebView2EnvironmentWithDetails</span><span class="sxs-lookup"><span data-stu-id="52da6-133">CreateCoreWebView2EnvironmentWithDetails</span></span> 

> <span data-ttu-id="52da6-134">общедоступные STDAPI [CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR USERDATAFOLDER, PCWSTR AdditionalBrowserArguments, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="52da6-134">public STDAPI [CreateCoreWebView2EnvironmentWithDetails](#createcorewebview2environmentwithdetails)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, PCWSTR additionalBrowserArguments, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="52da6-135">Этот API-интерфейс будет удален в следующем выпуске SDK.</span><span class="sxs-lookup"><span data-stu-id="52da6-135">This API is going to be removed in next SDK release.</span></span>

<span data-ttu-id="52da6-136">Пожалуйста, используйте CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="52da6-136">Please use CreateCoreWebView2EnvironmentWithOptions.</span></span>

#### <span data-ttu-id="52da6-137">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="52da6-137">CreateCoreWebView2EnvironmentWithOptions</span></span> 

> <span data-ttu-id="52da6-138">общедоступные STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* [environmentOptions, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environment_created_handler](icorewebview2createcorewebview2environmentcompletedhandler.md) )</span><span class="sxs-lookup"><span data-stu-id="52da6-138">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="52da6-139">DLL Export для создания среды WebView2 с пользовательской версией EDGE, каталогом данных пользователя и (или) дополнительными параметрами.</span><span class="sxs-lookup"><span data-stu-id="52da6-139">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>

<span data-ttu-id="52da6-140">browserExecutableFolder — это относительный путь к папке, содержащей внедренный край.</span><span class="sxs-lookup"><span data-stu-id="52da6-140">browserExecutableFolder is the relative path to the folder that contains the embedded Edge.</span></span> <span data-ttu-id="52da6-141">Внедренный край можно получить, скопировав именованную папку установленного края, например подпапку 73.0.52.0 для установленного 73.0.52.0ного края.</span><span class="sxs-lookup"><span data-stu-id="52da6-141">The embedded Edge can be obtained by copying the version named folder of an installed Edge, like 73.0.52.0 sub folder of an installed 73.0.52.0 Edge.</span></span> <span data-ttu-id="52da6-142">Папка должна иметь msedge. exe, msedge. dll и т. д.</span><span class="sxs-lookup"><span data-stu-id="52da6-142">The folder should have msedge.exe, msedge.dll, and so on.</span></span> <span data-ttu-id="52da6-143">Используйте null или пустую строку для browserExecutableFolder, чтобы создать WebView на компьютере, в этом случае API попытается найти совместимую версию EDGE, установленной на компьютере, в соответствии с предпочтениями канала, в котором была предпринята попытка найти первую установку для пользователя, а затем установить на компьютер.</span><span class="sxs-lookup"><span data-stu-id="52da6-143">Use null or empty string for browserExecutableFolder to create WebView using Edge installed on the machine, in which case the API will try to find a compatible version of Edge installed on the machine according to the channel preference trying to find first per user install and then per machine install.</span></span>

<span data-ttu-id="52da6-144">Порядок поиска по каналам по умолчанию — стабильный, бета-, для разработчиков и Канарские.</span><span class="sxs-lookup"><span data-stu-id="52da6-144">The default channel search order is stable, beta, dev, and canary.</span></span> <span data-ttu-id="52da6-145">Если переопределение WEBVIEW2_RELEASE_CHANNEL_PREFERENCE переменной среды или применимого значения реестра releaseChannelPreference со значением 1, порядок поиска каналов будет реверсирован.</span><span class="sxs-lookup"><span data-stu-id="52da6-145">When there is an override WEBVIEW2_RELEASE_CHANNEL_PREFERENCE environment variable or applicable releaseChannelPreference registry value with the value of 1, the channel search order is reversed.</span></span>

<span data-ttu-id="52da6-146">userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2.</span><span class="sxs-lookup"><span data-stu-id="52da6-146">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> <span data-ttu-id="52da6-147">Путь может представлять собой абсолютный путь к файлу или относительный путь, который интерпретируется относительно исполняемого файла текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="52da6-147">The path can be an absolute file path or a relative file path that is interpreted as relative to the current process's executable.</span></span> <span data-ttu-id="52da6-148">В противном случае для приложений UWP папка данных пользователя по умолчанию будет папкой "данные приложения" для пакета; для приложений, не являющихся UWP, папка данных пользователя по умолчанию `{Executable File Name}.WebView2` будет создана в той же папке, что и исполняемый объект приложения.</span><span class="sxs-lookup"><span data-stu-id="52da6-148">Otherwise, for UWP apps, the default user data folder will be the app data folder for the package; for non-UWP apps, the default user data folder `{Executable File Name}.WebView2` will be created in the same directory next to the app executable.</span></span> <span data-ttu-id="52da6-149">Создание WebView2 может завершиться сбоем, если исполняемый объект запущен в каталоге, у процесса которого нет разрешения на создание новой папки в.</span><span class="sxs-lookup"><span data-stu-id="52da6-149">WebView2 creation can fail if the executable is running in a directory that the process doesn't have permission to create a new folder in.</span></span> <span data-ttu-id="52da6-150">Приложение несет ответственность за очистку папки данных пользователя после ее завершения.</span><span class="sxs-lookup"><span data-stu-id="52da6-150">The app is responsible to clean up its user data folder when it is done.</span></span>

<span data-ttu-id="52da6-151">Обратите внимание, что так как процесс браузера может быть общим для разных представлений, создание WebView завершится сбоем с HRESULT_FROM_WIN32 (ERROR_INVALID_STATE), если указанные параметры не соответствуют параметрам веб-представлений, которые в данный момент выполняются в процессе общего браузера.</span><span class="sxs-lookup"><span data-stu-id="52da6-151">Note that as a browser process might be shared among WebViews, WebView creation will fail with HRESULT_FROM_WIN32(ERROR_INVALID_STATE) if the specified options does not match the options of the WebViews that are currently running in the shared browser process.</span></span>

<span data-ttu-id="52da6-152">environment_created_handler является результатом обработчика асинхронной операции, которая будет содержать созданный WebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="52da6-152">environment_created_handler is the handler result to the async operation which will contain the WebView2Environment that got created.</span></span>

<span data-ttu-id="52da6-153">BrowserExecutableFolder, userDataFolder и additionalBrowserArguments environmentOptions могут быть переопределены значениями, заданными в переменных среды или в реестре.</span><span class="sxs-lookup"><span data-stu-id="52da6-153">The browserExecutableFolder, userDataFolder and additionalBrowserArguments of the environmentOptions may be overridden by values either specified in environment variables or in the registry.</span></span>

<span data-ttu-id="52da6-154">При создании WebView2Environment проверяются следующие переменные среды:</span><span class="sxs-lookup"><span data-stu-id="52da6-154">When creating a WebView2Environment the following environment variables are checked:</span></span>

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

<span data-ttu-id="52da6-155">Если обнаружена переменная среды override, мы используем значения browserExecutableFolder, userDataFolder и additionalBrowserArguments в качестве замены соответствующих значений в CreateCoreWebView2EnvironmentWithOptions параметрах.</span><span class="sxs-lookup"><span data-stu-id="52da6-155">If an override environment variable is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

<span data-ttu-id="52da6-156">Несмотря на то, что не строго переопределяется, существуют дополнительные переменные среды, которые можно установить.</span><span class="sxs-lookup"><span data-stu-id="52da6-156">While not strictly overrides, there exists additional environment variables that can be set:</span></span>

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="52da6-157">Если обнаружено непустое значение, это указывает на то, что WebView запускается в отладчике сценариев.</span><span class="sxs-lookup"><span data-stu-id="52da6-157">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger.</span></span> <span data-ttu-id="52da6-158">В этом случае WebView будет выдать `Page.waitForDebugger` команду CDP, которая приведет к выполнению сценария в WebView для приостановки при запуске, пока отладчик не выдаст соответствующую `Runtime.runIfWaitingForDebugger` команду CDP для возобновления выполнения.</span><span class="sxs-lookup"><span data-stu-id="52da6-158">In this case, the WebView will issue a `Page.waitForDebugger` CDP command that will cause script execution inside the WebView to pause on launch, until a debugger issues a corresponding `Runtime.runIfWaitingForDebugger` CDP command to resume execution.</span></span> <span data-ttu-id="52da6-159">Примечание. Этот параметр реестра не эквивалентен данной переменной среды.</span><span class="sxs-lookup"><span data-stu-id="52da6-159">Note: There is no registry key equivalent of this environment variable.</span></span>

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="52da6-160">Если обнаружено непустое значение, это указывает на то, что WebView запускается в отладчике сценария, который также поддерживает хост-приложения, использующие несколько веб-представлений.</span><span class="sxs-lookup"><span data-stu-id="52da6-160">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger that also supports host applications that use multiple WebViews.</span></span> <span data-ttu-id="52da6-161">Это значение используется в качестве идентификатора для именованного канала, который будет открываться и записываться при создании нового WebView в ведущем приложении.</span><span class="sxs-lookup"><span data-stu-id="52da6-161">The value is used as the identifier for a named pipe that will be opened and written to when a new WebView is created by the host application.</span></span> <span data-ttu-id="52da6-162">Полезные данные будут соответствовать целевому объекту JSON порта удаленной отладки и могут использоваться внешним отладчиком для присоединения к определенному экземпляру WebView.</span><span class="sxs-lookup"><span data-stu-id="52da6-162">The payload will match that of the remote-debugging-port JSON target and can be used by the external debugger to attach to a specific WebView instance.</span></span> <span data-ttu-id="52da6-163">Ниже представлен формат канала, созданного отладчиком `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` :</span><span class="sxs-lookup"><span data-stu-id="52da6-163">The format of the pipe created by the debugger should be: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` where:</span></span>

* `{app_name}` <span data-ttu-id="52da6-164">имя файла exe приложения, например WebView2Example. exe</span><span class="sxs-lookup"><span data-stu-id="52da6-164">is the host application exe filename, e.g. WebView2Example.exe</span></span>

* `{pipe_name}` <span data-ttu-id="52da6-165">значение, заданное для WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span><span class="sxs-lookup"><span data-stu-id="52da6-165">is the value set for WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span></span>

<span data-ttu-id="52da6-166">Чтобы включить отладку целевых объектов, идентифицированных с помощью JSON, вам также потребуется задать переменную среды WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS для отправки `--remote-debugging-port={port_num}` .</span><span class="sxs-lookup"><span data-stu-id="52da6-166">To enable debugging of the targets identified by the JSON you will also need to set the WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variable to send `--remote-debugging-port={port_num}` where:</span></span>

* `{port_num}` <span data-ttu-id="52da6-167">порт, на который будет привязан сервер CDP.</span><span class="sxs-lookup"><span data-stu-id="52da6-167">is the port on which the CDP server will bind.</span></span>

<span data-ttu-id="52da6-168">Имейте в виду, что настройка переменных среды WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER и WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS приведет к тому, что веб-представления, размещенные в вашем приложении, и их содержимое будут доступны сторонним приложениям, например отладчикам.</span><span class="sxs-lookup"><span data-stu-id="52da6-168">Be aware that setting both the WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER and WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variables will cause the WebViews hosted in your application and their contents to be exposed to 3rd party applications such as debuggers.</span></span>

<span data-ttu-id="52da6-169">Примечание. Этот параметр реестра не эквивалентен данной переменной среды.</span><span class="sxs-lookup"><span data-stu-id="52da6-169">Note: There is no registry key equivalent of this environment variable.</span></span>

<span data-ttu-id="52da6-170">Если ни одна из этих переменных среды не существует, далее будет проверяться реестр.</span><span class="sxs-lookup"><span data-stu-id="52da6-170">If none of those environment variables exist, then the registry is examined next.</span></span> <span data-ttu-id="52da6-171">Проверяются следующие разделы реестра:</span><span class="sxs-lookup"><span data-stu-id="52da6-171">The following registry keys are checked:</span></span>

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

<span data-ttu-id="52da6-172">В маловероятном случае, когда некоторые экземпляры WebView открыты во время обновления браузера, мы сможем блокировать удаление старых браузеров Edge.</span><span class="sxs-lookup"><span data-stu-id="52da6-172">In the unlikely scenario where some instances of WebView are open during a browser update we could end up blocking the deletion of old Edge browsers.</span></span> <span data-ttu-id="52da6-173">Чтобы не запустить свободное место на диске, новое создание WebView завершится сбоем при следующей ошибке, если обнаружится, что на вашем компьютере установлено множество старых версий.</span><span class="sxs-lookup"><span data-stu-id="52da6-173">To avoid running out of disk space a new WebView creation will fail with the next error if it detects that there are many old versions present.</span></span>

```
ERROR_DISK_FULL
```

<span data-ttu-id="52da6-174">По умолчанию максимально допустимое число версий Edge равно 20.</span><span class="sxs-lookup"><span data-stu-id="52da6-174">The default maximum number of Edge versions allowed is 20.</span></span>

<span data-ttu-id="52da6-175">Максимально допустимое число старых версий Edge может быть переписано значением следующей переменной среды.</span><span class="sxs-lookup"><span data-stu-id="52da6-175">The maximum number of old Edge versions allowed can be overwritten with the value of the following environment variable.</span></span>

```
WEBVIEW2_MAX_INSTANCES
```

<span data-ttu-id="52da6-176">Если WebView зависит от установленного края и удалено все последующее создание завершается сбоем при следующей ошибке</span><span class="sxs-lookup"><span data-stu-id="52da6-176">If the Webview depends on an installed Edge and it is uninstalled any subsequent creation will fail with the next error</span></span>

```
ERROR_PRODUCT_UNINSTALLED
```

<span data-ttu-id="52da6-177">Сначала мы рассмотрим корневой раздел реестра HKLM, а затем HKCU.</span><span class="sxs-lookup"><span data-stu-id="52da6-177">First we check with Root as HKLM and then HKCU.</span></span> <span data-ttu-id="52da6-178">AppId сначала присваивается идентификатор пользовательской модели приложения для процесса вызывающего объекта, а если соответствующий раздел реестра отсутствует, для AppId задано имя исполняемого процесса вызывающего объекта или если этот раздел не является ключом реестра "\*".</span><span class="sxs-lookup"><span data-stu-id="52da6-178">AppId is first set to the Application User Model ID of the caller's process, then if there's no corresponding registry key the AppId is set to the executable name of the caller's process, or if that isn't a registry key then '\*'.</span></span> <span data-ttu-id="52da6-179">Если найден раздел реестра override, мы используем значения реестра browserExecutableFolder, userDataFolder и additionalBrowserArguments как замены соответствующих значений в CreateCoreWebView2EnvironmentWithOptions параметрах.</span><span class="sxs-lookup"><span data-stu-id="52da6-179">If an override registry key is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments registry values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

#### <span data-ttu-id="52da6-180">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="52da6-180">GetAvailableCoreWebView2BrowserVersionString</span></span> 

> <span data-ttu-id="52da6-181">общедоступные STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="52da6-181">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="52da6-182">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="52da6-182">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

<span data-ttu-id="52da6-183">Названия каналов — это бета-версия, разработка и Канарские.</span><span class="sxs-lookup"><span data-stu-id="52da6-183">Channel names are beta, dev, and canary.</span></span> <span data-ttu-id="52da6-184">Если для browserExecutableFolder или настройки канала существует переопределение, будет использоваться переопределение.</span><span class="sxs-lookup"><span data-stu-id="52da6-184">If an override exists for the browserExecutableFolder or the channel preference, the override will be used.</span></span> <span data-ttu-id="52da6-185">Если переопределение не задано, используется параметр, переданный в GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="52da6-185">If there isn't an override, then the parameter passed to GetAvailableCoreWebView2BrowserVersionString is used.</span></span>

