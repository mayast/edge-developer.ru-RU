---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Globals
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2c6a84a0fec68c0026fad61faa1c5ed8ed27ddd8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010798"
---
# <span data-ttu-id="743e8-104">0.9.579-Globals</span><span class="sxs-lookup"><span data-stu-id="743e8-104">0.9.579 - Globals</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

## <span data-ttu-id="743e8-105">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="743e8-105">Summary</span></span>

 <span data-ttu-id="743e8-106">Участников</span><span class="sxs-lookup"><span data-stu-id="743e8-106">Members</span></span>                        | <span data-ttu-id="743e8-107">Описания</span><span class="sxs-lookup"><span data-stu-id="743e8-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="743e8-108">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="743e8-108">CompareBrowserVersions</span></span>](#comparebrowserversions) | <span data-ttu-id="743e8-109">Этот метод предназначен для всех пользователей, которым нужно правильно сравнить версию, чтобы определить, какая версия более поздняя, устаревшая или та же.</span><span class="sxs-lookup"><span data-stu-id="743e8-109">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>
[<span data-ttu-id="743e8-110">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="743e8-110">CreateCoreWebView2Environment</span></span>](#createcorewebview2environment) | <span data-ttu-id="743e8-111">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="743e8-111">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>
[<span data-ttu-id="743e8-112">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="743e8-112">CreateCoreWebView2EnvironmentWithOptions</span></span>](#createcorewebview2environmentwithoptions) | <span data-ttu-id="743e8-113">DLL Export для создания среды WebView2 с пользовательской версией EDGE, каталогом данных пользователя и (или) дополнительными параметрами.</span><span class="sxs-lookup"><span data-stu-id="743e8-113">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>
[<span data-ttu-id="743e8-114">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="743e8-114">GetAvailableCoreWebView2BrowserVersionString</span></span>](#getavailablecorewebview2browserversionstring) | <span data-ttu-id="743e8-115">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="743e8-115">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

## <span data-ttu-id="743e8-116">Участников</span><span class="sxs-lookup"><span data-stu-id="743e8-116">Members</span></span>

#### <span data-ttu-id="743e8-117">CompareBrowserVersions</span><span class="sxs-lookup"><span data-stu-id="743e8-117">CompareBrowserVersions</span></span> 

> <span data-ttu-id="743e8-118">общедоступные STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR Version1, PCWSTR Version2, int \* result)</span><span class="sxs-lookup"><span data-stu-id="743e8-118">public STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR version1, PCWSTR version2, int \* result)</span></span>

<span data-ttu-id="743e8-119">Этот метод предназначен для всех пользователей, которым нужно правильно сравнить версию, чтобы определить, какая версия более поздняя, устаревшая или та же.</span><span class="sxs-lookup"><span data-stu-id="743e8-119">This method is for anyone want to compare version correctly to determine which version is newer, older or same.</span></span>

<span data-ttu-id="743e8-120">Он может использоваться для определения того, следует ли использовать webview2 или определенную базу функций в версии.</span><span class="sxs-lookup"><span data-stu-id="743e8-120">It can be used to determine whether to use webview2 or certain feature base on version.</span></span> <span data-ttu-id="743e8-121">Задает для результата значение-1, 0 или 1, если Version1 меньше, равно или больше Version2 соответственно.</span><span class="sxs-lookup"><span data-stu-id="743e8-121">Sets the value of result to -1, 0 or 1 if version1 is less than, equal or greater than version2 respectively.</span></span> <span data-ttu-id="743e8-122">Возвращает E_INVALIDARG, если не удается проанализировать ни одну из строк версии, ни какой из входных параметров имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="743e8-122">Returns E_INVALIDARG if it fails to parse any of the version strings or any input parameter is null.</span></span> <span data-ttu-id="743e8-123">Входные данные могут напрямую использовать versionInfo, полученный от GetAvailableCoreWebView2BrowserVersionString, сведения о канале будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="743e8-123">Input can directly use the versionInfo obtained from GetAvailableCoreWebView2BrowserVersionString, channel info will be ignored.</span></span>

#### <span data-ttu-id="743e8-124">CreateCoreWebView2Environment</span><span class="sxs-lookup"><span data-stu-id="743e8-124">CreateCoreWebView2Environment</span></span> 

> <span data-ttu-id="743e8-125">общедоступная STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span><span class="sxs-lookup"><span data-stu-id="743e8-125">public STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="743e8-126">Создает среду Evergreen WebView2, используя установленную версию Edge.</span><span class="sxs-lookup"><span data-stu-id="743e8-126">Creates an evergreen WebView2 Environment using the installed Edge version.</span></span>

<span data-ttu-id="743e8-127">Это эквивалентно вызову CreateCoreWebView2EnvironmentWithOptions с помощью nullptr для browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span><span class="sxs-lookup"><span data-stu-id="743e8-127">This is equivalent to calling CreateCoreWebView2EnvironmentWithOptions with nullptr for browserExecutableFolder, userDataFolder, additionalBrowserArguments.</span></span> <span data-ttu-id="743e8-128">Более подробную информацию вы увидите в CreateCoreWebView2EnvironmentWithOptions.</span><span class="sxs-lookup"><span data-stu-id="743e8-128">See CreateCoreWebView2EnvironmentWithOptions for more details.</span></span>

#### <span data-ttu-id="743e8-129">CreateCoreWebView2EnvironmentWithOptions</span><span class="sxs-lookup"><span data-stu-id="743e8-129">CreateCoreWebView2EnvironmentWithOptions</span></span> 

> <span data-ttu-id="743e8-130">общедоступные STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* [environmentOptions, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler \* environment_created_handler](icorewebview2createcorewebview2environmentcompletedhandler.md) )</span><span class="sxs-lookup"><span data-stu-id="743e8-130">public STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR browserExecutableFolder, PCWSTR userDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) \* environmentOptions, [ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) \* environment_created_handler)</span></span>

<span data-ttu-id="743e8-131">DLL Export для создания среды WebView2 с пользовательской версией EDGE, каталогом данных пользователя и (или) дополнительными параметрами.</span><span class="sxs-lookup"><span data-stu-id="743e8-131">DLL export to create a WebView2 environment with a custom version of Edge, user data directory and/or additional options.</span></span>

<span data-ttu-id="743e8-132">Используется `browserExecutableFolder` , чтобы указать, используют ли элементы управления WebView2 внедренную версию EDGE или установленную версию EDGE, которая уже есть на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="743e8-132">Use `browserExecutableFolder` to specify whether WebView2 controls use an embedded version of Edge, or the installed version of Edge that exists on a client machine.</span></span> <span data-ttu-id="743e8-133">Чтобы использовать внедренную версию EDGE, передайте относительный путь к папке, содержащей внедренную версию Edge `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="743e8-133">To use an embedded version of Edge, pass the relative path of the folder that contains the embedded version of Edge to `browserExecutableFolder`.</span></span> <span data-ttu-id="743e8-134">Чтобы получить внедренную версию EDGE, скопируйте ее имя из установленной версии Edge на клиентский компьютер.</span><span class="sxs-lookup"><span data-stu-id="743e8-134">To obtain the embedded version of Edge, copy the versioned folder name from your installed version of Edge on a client machine.</span></span> <span data-ttu-id="743e8-135">Например, скопируйте `73.0.52.0` папку из папки, в которой была установлена версия Edge 73.0.52.0.</span><span class="sxs-lookup"><span data-stu-id="743e8-135">For example, copy the `73.0.52.0` folder from the folder where Edge version 73.0.52.0 was installed.</span></span> <span data-ttu-id="743e8-136">Убедитесь в том, что в папке есть файлы **msedgewebview2.exe** и **msedge.dll** .</span><span class="sxs-lookup"><span data-stu-id="743e8-136">Ensure that the folder has both the **msedgewebview2.exe** and **msedge.dll** files.</span></span> <span data-ttu-id="743e8-137">Для создания элементов управления WebView2, использующих установленную версию EDGE, которая существует на клиентских компьютерах, передайте ей значение null или пустую строку `browserExecutableFolder` .</span><span class="sxs-lookup"><span data-stu-id="743e8-137">To create WebView2 controls that use the installed version of Edge that exists on client machines, pass a null or empty string to `browserExecutableFolder`.</span></span> <span data-ttu-id="743e8-138">В этом сценарии API пытается найти совместимую версию EDGE, установленную на клиентском компьютере (первый на уровне компьютера, а затем на пользователя), используя выбранный параметр канала.</span><span class="sxs-lookup"><span data-stu-id="743e8-138">In this scenario, the API tries to find a compatible version of Edge that is installed on the client machine (first at the machine level, and then per user) using the selected channel preference.</span></span>

<span data-ttu-id="743e8-139">Порядок поиска по каналам по умолчанию — стабильный, бета-, для разработчиков и Канарские.</span><span class="sxs-lookup"><span data-stu-id="743e8-139">The default channel search order is stable, beta, dev, and canary.</span></span> <span data-ttu-id="743e8-140">Если переопределение WEBVIEW2_RELEASE_CHANNEL_PREFERENCE переменной среды или применимого значения реестра releaseChannelPreference со значением 1, порядок поиска каналов будет реверсирован.</span><span class="sxs-lookup"><span data-stu-id="743e8-140">When there is an override WEBVIEW2_RELEASE_CHANNEL_PREFERENCE environment variable or applicable releaseChannelPreference registry value with the value of 1, the channel search order is reversed.</span></span>

<span data-ttu-id="743e8-141">userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2.</span><span class="sxs-lookup"><span data-stu-id="743e8-141">userDataFolder can be specified to change the default user data folder location for WebView2.</span></span> <span data-ttu-id="743e8-142">Путь может представлять собой абсолютный путь к файлу или относительный путь, который интерпретируется относительно исполняемого файла текущего процесса.</span><span class="sxs-lookup"><span data-stu-id="743e8-142">The path can be an absolute file path or a relative file path that is interpreted as relative to the current process's executable.</span></span> <span data-ttu-id="743e8-143">В противном случае для приложений UWP папка данных пользователя по умолчанию будет папкой "данные приложения" для пакета; для приложений, не являющихся UWP, папка данных пользователя по умолчанию `{Executable File Name}.WebView2` будет создана в той же папке, что и исполняемый объект приложения.</span><span class="sxs-lookup"><span data-stu-id="743e8-143">Otherwise, for UWP apps, the default user data folder will be the app data folder for the package; for non-UWP apps, the default user data folder `{Executable File Name}.WebView2` will be created in the same directory next to the app executable.</span></span> <span data-ttu-id="743e8-144">Создание WebView2 может завершиться сбоем, если исполняемый объект запущен в каталоге, у процесса которого нет разрешения на создание новой папки в.</span><span class="sxs-lookup"><span data-stu-id="743e8-144">WebView2 creation can fail if the executable is running in a directory that the process doesn't have permission to create a new folder in.</span></span> <span data-ttu-id="743e8-145">Приложение несет ответственность за очистку папки данных пользователя после ее завершения.</span><span class="sxs-lookup"><span data-stu-id="743e8-145">The app is responsible to clean up its user data folder when it is done.</span></span>

<span data-ttu-id="743e8-146">Обратите внимание, что так как процесс браузера может быть общим для разных представлений, создание WebView завершится сбоем с HRESULT_FROM_WIN32 (ERROR_INVALID_STATE), если указанные параметры не соответствуют параметрам веб-представлений, которые в данный момент выполняются в процессе общего браузера.</span><span class="sxs-lookup"><span data-stu-id="743e8-146">Note that as a browser process might be shared among WebViews, WebView creation will fail with HRESULT_FROM_WIN32(ERROR_INVALID_STATE) if the specified options does not match the options of the WebViews that are currently running in the shared browser process.</span></span>

<span data-ttu-id="743e8-147">environment_created_handler является результатом обработчика асинхронной операции, которая будет содержать созданный WebView2Environment.</span><span class="sxs-lookup"><span data-stu-id="743e8-147">environment_created_handler is the handler result to the async operation which will contain the WebView2Environment that got created.</span></span>

<span data-ttu-id="743e8-148">BrowserExecutableFolder, userDataFolder и additionalBrowserArguments environmentOptions могут быть переопределены значениями, заданными в переменных среды или в реестре.</span><span class="sxs-lookup"><span data-stu-id="743e8-148">The browserExecutableFolder, userDataFolder and additionalBrowserArguments of the environmentOptions may be overridden by values either specified in environment variables or in the registry.</span></span>

<span data-ttu-id="743e8-149">При создании WebView2Environment проверяются следующие переменные среды:</span><span class="sxs-lookup"><span data-stu-id="743e8-149">When creating a WebView2Environment the following environment variables are checked:</span></span>

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

<span data-ttu-id="743e8-150">Если обнаружена переменная среды override, мы используем значения browserExecutableFolder, userDataFolder и additionalBrowserArguments в качестве замены соответствующих значений в CreateCoreWebView2EnvironmentWithOptions параметрах.</span><span class="sxs-lookup"><span data-stu-id="743e8-150">If an override environment variable is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

<span data-ttu-id="743e8-151">Несмотря на то, что не строго переопределяется, существуют дополнительные переменные среды, которые можно установить.</span><span class="sxs-lookup"><span data-stu-id="743e8-151">While not strictly overrides, there exists additional environment variables that can be set:</span></span>

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="743e8-152">Если обнаружено непустое значение, это указывает на то, что WebView запускается в отладчике сценариев.</span><span class="sxs-lookup"><span data-stu-id="743e8-152">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger.</span></span> <span data-ttu-id="743e8-153">В этом случае WebView будет выдать `Page.waitForDebugger` команду CDP, которая приведет к выполнению сценария в WebView для приостановки при запуске, пока отладчик не выдаст соответствующую `Runtime.runIfWaitingForDebugger` команду CDP для возобновления выполнения.</span><span class="sxs-lookup"><span data-stu-id="743e8-153">In this case, the WebView will issue a `Page.waitForDebugger` CDP command that will cause script execution inside the WebView to pause on launch, until a debugger issues a corresponding `Runtime.runIfWaitingForDebugger` CDP command to resume execution.</span></span> <span data-ttu-id="743e8-154">Примечание. Этот параметр реестра не эквивалентен данной переменной среды.</span><span class="sxs-lookup"><span data-stu-id="743e8-154">Note: There is no registry key equivalent of this environment variable.</span></span>

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

<span data-ttu-id="743e8-155">Если обнаружено непустое значение, это указывает на то, что WebView запускается в отладчике сценария, который также поддерживает хост-приложения, использующие несколько веб-представлений.</span><span class="sxs-lookup"><span data-stu-id="743e8-155">When found with a non-empty value, this indicates that the WebView is being launched under a script debugger that also supports host applications that use multiple WebViews.</span></span> <span data-ttu-id="743e8-156">Это значение используется в качестве идентификатора для именованного канала, который будет открываться и записываться при создании нового WebView в ведущем приложении.</span><span class="sxs-lookup"><span data-stu-id="743e8-156">The value is used as the identifier for a named pipe that will be opened and written to when a new WebView is created by the host application.</span></span> <span data-ttu-id="743e8-157">Полезные данные будут соответствовать целевому объекту JSON порта удаленной отладки и могут использоваться внешним отладчиком для присоединения к определенному экземпляру WebView.</span><span class="sxs-lookup"><span data-stu-id="743e8-157">The payload will match that of the remote-debugging-port JSON target and can be used by the external debugger to attach to a specific WebView instance.</span></span> <span data-ttu-id="743e8-158">Ниже представлен формат канала, созданного отладчиком `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` :</span><span class="sxs-lookup"><span data-stu-id="743e8-158">The format of the pipe created by the debugger should be: `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` where:</span></span>

* `{app_name}` <span data-ttu-id="743e8-159">имя файла exe приложения, например WebView2Example.exe</span><span class="sxs-lookup"><span data-stu-id="743e8-159">is the host application exe filename, e.g. WebView2Example.exe</span></span>

* `{pipe_name}` <span data-ttu-id="743e8-160">значение, заданное для WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span><span class="sxs-lookup"><span data-stu-id="743e8-160">is the value set for WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.</span></span>

<span data-ttu-id="743e8-161">Чтобы включить отладку целевых объектов, идентифицированных с помощью JSON, вам также потребуется задать переменную среды WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS для отправки `--remote-debugging-port={port_num}` .</span><span class="sxs-lookup"><span data-stu-id="743e8-161">To enable debugging of the targets identified by the JSON you will also need to set the WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variable to send `--remote-debugging-port={port_num}` where:</span></span>

* `{port_num}` <span data-ttu-id="743e8-162">порт, на который будет привязан сервер CDP.</span><span class="sxs-lookup"><span data-stu-id="743e8-162">is the port on which the CDP server will bind.</span></span>

<span data-ttu-id="743e8-163">Имейте в виду, что настройка переменных среды WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER и WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS приведет к тому, что веб-представления, размещенные в вашем приложении, и их содержимое будут доступны сторонним приложениям, например отладчикам.</span><span class="sxs-lookup"><span data-stu-id="743e8-163">Be aware that setting both the WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER and WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS environment variables will cause the WebViews hosted in your application and their contents to be exposed to 3rd party applications such as debuggers.</span></span>

<span data-ttu-id="743e8-164">Примечание. Этот параметр реестра не эквивалентен данной переменной среды.</span><span class="sxs-lookup"><span data-stu-id="743e8-164">Note: There is no registry key equivalent of this environment variable.</span></span>

<span data-ttu-id="743e8-165">Если ни одна из этих переменных среды не существует, далее будет проверяться реестр.</span><span class="sxs-lookup"><span data-stu-id="743e8-165">If none of those environment variables exist, then the registry is examined next.</span></span> <span data-ttu-id="743e8-166">Проверяются следующие разделы реестра:</span><span class="sxs-lookup"><span data-stu-id="743e8-166">The following registry keys are checked:</span></span>

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

<span data-ttu-id="743e8-167">В маловероятном случае, когда некоторые экземпляры WebView открыты во время обновления браузера, мы сможем блокировать удаление старых браузеров Edge.</span><span class="sxs-lookup"><span data-stu-id="743e8-167">In the unlikely scenario where some instances of WebView are open during a browser update we could end up blocking the deletion of old Edge browsers.</span></span> <span data-ttu-id="743e8-168">Чтобы не запустить свободное место на диске, новое создание WebView завершится сбоем при следующей ошибке, если обнаружится, что на вашем компьютере установлено множество старых версий.</span><span class="sxs-lookup"><span data-stu-id="743e8-168">To avoid running out of disk space a new WebView creation will fail with the next error if it detects that there are many old versions present.</span></span>

```
ERROR_DISK_FULL
```

<span data-ttu-id="743e8-169">По умолчанию максимально допустимое число версий Edge равно 20.</span><span class="sxs-lookup"><span data-stu-id="743e8-169">The default maximum number of Edge versions allowed is 20.</span></span>

<span data-ttu-id="743e8-170">Максимально допустимое число старых версий Edge может быть переписано значением следующей переменной среды.</span><span class="sxs-lookup"><span data-stu-id="743e8-170">The maximum number of old Edge versions allowed can be overwritten with the value of the following environment variable.</span></span>

```
WEBVIEW2_MAX_INSTANCES
```

<span data-ttu-id="743e8-171">Если WebView зависит от установленного края и удалено все последующее создание завершается сбоем при следующей ошибке</span><span class="sxs-lookup"><span data-stu-id="743e8-171">If the Webview depends on an installed Edge and it is uninstalled any subsequent creation will fail with the next error</span></span>

```
ERROR_PRODUCT_UNINSTALLED
```

<span data-ttu-id="743e8-172">Сначала мы рассмотрим корневой раздел реестра HKLM, а затем HKCU.</span><span class="sxs-lookup"><span data-stu-id="743e8-172">First we check with Root as HKLM and then HKCU.</span></span> <span data-ttu-id="743e8-173">AppId сначала присваивается идентификатор пользовательской модели приложения для процесса вызывающего объекта, а если соответствующий раздел реестра отсутствует, для AppId задано имя исполняемого процесса вызывающего объекта или если этот раздел не является ключом реестра "\*".</span><span class="sxs-lookup"><span data-stu-id="743e8-173">AppId is first set to the Application User Model ID of the caller's process, then if there's no corresponding registry key the AppId is set to the executable name of the caller's process, or if that isn't a registry key then '\*'.</span></span> <span data-ttu-id="743e8-174">Если найден раздел реестра override, мы используем значения реестра browserExecutableFolder, userDataFolder и additionalBrowserArguments как замены соответствующих значений в CreateCoreWebView2EnvironmentWithOptions параметрах.</span><span class="sxs-lookup"><span data-stu-id="743e8-174">If an override registry key is found then we use the browserExecutableFolder, userDataFolder and additionalBrowserArguments registry values as replacements for the corresponding values in CreateCoreWebView2EnvironmentWithOptions parameters.</span></span>

#### <span data-ttu-id="743e8-175">GetAvailableCoreWebView2BrowserVersionString</span><span class="sxs-lookup"><span data-stu-id="743e8-175">GetAvailableCoreWebView2BrowserVersionString</span></span> 

> <span data-ttu-id="743e8-176">общедоступные STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="743e8-176">public STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR browserExecutableFolder, LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="743e8-177">Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.</span><span class="sxs-lookup"><span data-stu-id="743e8-177">Get the browser version info including channel name if it is not the stable channel or the Embedded Edge.</span></span>

<span data-ttu-id="743e8-178">Названия каналов — это бета-версия, разработка и Канарские.</span><span class="sxs-lookup"><span data-stu-id="743e8-178">Channel names are beta, dev, and canary.</span></span> <span data-ttu-id="743e8-179">Если для browserExecutableFolder или настройки канала существует переопределение, будет использоваться переопределение.</span><span class="sxs-lookup"><span data-stu-id="743e8-179">If an override exists for the browserExecutableFolder or the channel preference, the override will be used.</span></span> <span data-ttu-id="743e8-180">Если переопределение не задано, используется параметр, переданный в GetAvailableCoreWebView2BrowserVersionString.</span><span class="sxs-lookup"><span data-stu-id="743e8-180">If there isn't an override, then the parameter passed to GetAvailableCoreWebView2BrowserVersionString is used.</span></span>

