---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Глобальные настройки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d291a4973656d106f803382ee985f0006bf5d68d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877625"
---
# Глобальные настройки 

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[CompareBrowserVersions](#comparebrowserversions) | Этот метод предназначен для всех пользователей, которым нужно правильно сравнить версию, чтобы определить, какая версия более поздняя, устаревшая или та же.
[CreateCoreWebView2Environment](#createcorewebview2environment) | Создает среду Evergreen WebView2, используя установленную версию Edge.
[CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions) | DLL Export для создания среды WebView2 с пользовательской версией EDGE, каталогом данных пользователя и (или) дополнительными параметрами.
[GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring) | Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.

## Участников

#### CompareBrowserVersions 

> общедоступные STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR Version1, PCWSTR Version2, int * result)

Этот метод предназначен для всех пользователей, которым нужно правильно сравнить версию, чтобы определить, какая версия более поздняя, устаревшая или та же.

Он может использоваться для определения того, следует ли использовать webview2 или определенную базу функций в версии. Задает для результата значение-1, 0 или 1, если Version1 меньше, равно или больше Version2 соответственно. Возвращает E_INVALIDARG, если не удается проанализировать ни одну из строк версии, ни какой из входных параметров имеет значение null. Входные данные могут напрямую использовать versionInfo, полученный от GetAvailableCoreWebView2BrowserVersionString, сведения о канале будут игнорироваться.

#### CreateCoreWebView2Environment 

> общедоступная STDAPI [CreateCoreWebView2Environment](#createcorewebview2environment)([ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler](icorewebview2createcorewebview2environmentcompletedhandler.md) * environment_created_handler)

Создает среду Evergreen WebView2, используя установленную версию Edge.

Это эквивалентно вызову CreateCoreWebView2EnvironmentWithOptions с помощью nullptr для browserExecutableFolder, userDataFolder, additionalBrowserArguments. Более подробную информацию вы увидите в CreateCoreWebView2EnvironmentWithOptions.

#### CreateCoreWebView2EnvironmentWithOptions 

> общедоступные STDAPI [CreateCoreWebView2EnvironmentWithOptions](#createcorewebview2environmentwithoptions)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR UserDataFolder, [ICoreWebView2EnvironmentOptions](icorewebview2environmentoptions.md) * [environmentOptions, ICoreWebView2CreateCoreWebView2EnvironmentCompletedHandler * environment_created_handler](icorewebview2createcorewebview2environmentcompletedhandler.md) )

DLL Export для создания среды WebView2 с пользовательской версией EDGE, каталогом данных пользователя и (или) дополнительными параметрами.

Используется `browserExecutableFolder` , чтобы указать, используют ли элементы управления WebView2 внедренную версию EDGE или установленную версию EDGE, которая уже есть на клиентском компьютере. Чтобы использовать внедренную версию EDGE, передайте относительный путь к папке, содержащей внедренную версию Edge `browserExecutableFolder` . Чтобы получить внедренную версию EDGE, скопируйте ее имя из установленной версии Edge на клиентский компьютер. Например, скопируйте `73.0.52.0` папку из папки, в которой была установлена версия Edge 73.0.52.0. Убедитесь в том, что в папке есть файлы **msedgewebview2.exe** и **msedge.dll** . Для создания элементов управления WebView2, использующих установленную версию EDGE, которая существует на клиентских компьютерах, передайте ей значение null или пустую строку `browserExecutableFolder` . В этом сценарии API пытается найти совместимую версию EDGE, установленную на клиентском компьютере (первый на уровне компьютера, а затем на пользователя), используя выбранный параметр канала. 

Порядок поиска по каналам по умолчанию — стабильный, бета-, для разработчиков и Канарские. Если переопределение WEBVIEW2_RELEASE_CHANNEL_PREFERENCE переменной среды или применимого значения реестра releaseChannelPreference со значением 1, порядок поиска каналов будет реверсирован.

userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2. Путь может представлять собой абсолютный путь к файлу или относительный путь, который интерпретируется относительно исполняемого файла текущего процесса. В противном случае для приложений UWP папка данных пользователя по умолчанию будет папкой "данные приложения" для пакета; для приложений, не являющихся UWP, папка данных пользователя по умолчанию `{Executable File Name}.WebView2` будет создана в той же папке, что и исполняемый объект приложения. Создание WebView2 может завершиться сбоем, если исполняемый объект запущен в каталоге, у процесса которого нет разрешения на создание новой папки в. Приложение несет ответственность за очистку папки данных пользователя после ее завершения.

Обратите внимание, что так как процесс браузера может быть общим для разных представлений, создание WebView завершится сбоем с HRESULT_FROM_WIN32 (ERROR_INVALID_STATE), если указанные параметры не соответствуют параметрам веб-представлений, которые в данный момент выполняются в процессе общего браузера.

environment_created_handler является результатом обработчика асинхронной операции, которая будет содержать созданный WebView2Environment.

BrowserExecutableFolder, userDataFolder и additionalBrowserArguments environmentOptions могут быть переопределены значениями, заданными в переменных среды или в реестре.

При создании WebView2Environment проверяются следующие переменные среды:

```
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

Если обнаружена переменная среды override, мы используем значения browserExecutableFolder, userDataFolder и additionalBrowserArguments в качестве замены соответствующих значений в CreateCoreWebView2EnvironmentWithOptions параметрах.

Несмотря на то, что не строго переопределяется, существуют дополнительные переменные среды, которые можно установить.

```
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

Если обнаружено непустое значение, это указывает на то, что WebView запускается в отладчике сценариев. В этом случае WebView будет выдать `Page.waitForDebugger` команду CDP, которая приведет к выполнению сценария в WebView для приостановки при запуске, пока отладчик не выдаст соответствующую `Runtime.runIfWaitingForDebugger` команду CDP для возобновления выполнения. Примечание. Этот параметр реестра не эквивалентен данной переменной среды.

```
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

Если обнаружено непустое значение, это указывает на то, что WebView запускается в отладчике сценария, который также поддерживает хост-приложения, использующие несколько веб-представлений. Это значение используется в качестве идентификатора для именованного канала, который будет открываться и записываться при создании нового WebView в ведущем приложении. Полезные данные будут соответствовать целевому объекту JSON порта удаленной отладки и могут использоваться внешним отладчиком для присоединения к определенному экземпляру WebView. Ниже представлен формат канала, созданного отладчиком `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` :

* `{app_name}` имя файла exe приложения, например WebView2Example.exe

* `{pipe_name}` значение, заданное для WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.

Чтобы включить отладку целевых объектов, идентифицированных с помощью JSON, вам также потребуется задать переменную среды WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS для отправки `--remote-debugging-port={port_num}` .

* `{port_num}` порт, на который будет привязан сервер CDP.

Имейте в виду, что настройка переменных среды WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER и WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS приведет к тому, что веб-представления, размещенные в вашем приложении, и их содержимое будут доступны сторонним приложениям, например отладчикам.

Примечание. Этот параметр реестра не эквивалентен данной переменной среды.

Если ни одна из этих переменных среды не существует, далее будет проверяться реестр. Проверяются следующие разделы реестра:

```
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

В маловероятном случае, когда некоторые экземпляры WebView открыты во время обновления браузера, мы сможем блокировать удаление старых браузеров Edge. Чтобы не запустить свободное место на диске, новое создание WebView завершится сбоем при следующей ошибке, если обнаружится, что на вашем компьютере установлено множество старых версий.

```
ERROR_DISK_FULL
```

По умолчанию максимально допустимое число версий Edge равно 20.

Максимально допустимое число старых версий Edge может быть переписано значением следующей переменной среды.

```
WEBVIEW2_MAX_INSTANCES
```

Если WebView зависит от установленного края и удалено все последующее создание завершается сбоем при следующей ошибке

```
ERROR_PRODUCT_UNINSTALLED
```

Сначала мы рассмотрим корневой раздел реестра HKLM, а затем HKCU. AppId сначала присваивается идентификатор пользовательской модели приложения для процесса вызывающего объекта, а если соответствующий раздел реестра отсутствует, для AppId задано имя исполняемого процесса вызывающего объекта или если этот раздел не является ключом реестра "*". Если найден раздел реестра override, мы используем значения реестра browserExecutableFolder, userDataFolder и additionalBrowserArguments как замены соответствующих значений в CreateCoreWebView2EnvironmentWithOptions параметрах.

#### GetAvailableCoreWebView2BrowserVersionString 

> общедоступные STDAPI [GetAvailableCoreWebView2BrowserVersionString](#getavailablecorewebview2browserversionstring)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWSTR * versionInfo)

Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.

Названия каналов — это бета-версия, разработка и Канарские. Если для browserExecutableFolder или настройки канала существует переопределение, будет использоваться переопределение. Если переопределение не задано, используется параметр, переданный в GetAvailableCoreWebView2BrowserVersionString.
