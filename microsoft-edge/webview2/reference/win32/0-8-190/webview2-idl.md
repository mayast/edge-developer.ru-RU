---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 58b32c1fe46183e55b8ac0bb4f4264b1f38e6eeb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654619"
---
# Глобальные 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[CreateWebView2EnvironmentWithDetails](#createwebview2environmentwithdetails) | DLL Export для создания среды WebView2 с пользовательской версией EDGE, каталогом данных пользователя и/или дополнительными переключателями браузера.
[CreateWebView2Environment](#createwebview2environment) | Создает среду Evergreen WebView2, используя установленную версию Edge.
[GetWebView2BrowserVersionInfo](#getwebview2browserversioninfo) | Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.
[CompareBrowserVersions](#comparebrowserversions) | Этот метод предназначен для всех пользователей, которым нужно правильно сравнить версию, чтобы определить, какая версия более поздняя, устаревшая или та же.

## Участников

#### CreateWebView2EnvironmentWithDetails 

> общедоступные STDAPI [CreateWebView2EnvironmentWithDetails](#createwebview2environmentwithdetails)(PCWSTR BROWSEREXECUTABLEFOLDER, PCWSTR USERDATAFOLDER, PCWSTR AdditionalBrowserArguments,[IWebView2CreateWebView2EnvironmentCompletedHandler](IWebView2CreateWebView2EnvironmentCompletedHandler.md) * environment_created_handler)

DLL Export для создания среды WebView2 с пользовательской версией EDGE, каталогом данных пользователя и/или дополнительными переключателями браузера.

browserExecutableFolder — это относительный путь к папке, содержащей внедренный край. Внедренный край можно получить, скопировав именованную папку установленного края, например подпапку 73.0.52.0 для установленного 73.0.52.0ного края. Папка должна иметь msedge. exe, msedge. dll и т. д. Используйте null или пустую строку для browserExecutableFolder, чтобы создать WebView на компьютере, в этом случае API попытается найти совместимую версию EDGE, установленной на компьютере, в соответствии с предпочтениями канала, в котором была предпринята попытка найти первую установку для пользователя, а затем установить на компьютер.

Порядок поиска по каналам по умолчанию — стабильный, бета-, для разработчиков и Канарские. Если переопределение WEBVIEW2_RELEASE_CHANNEL_PREFERENCE переменной среды или применимого значения реестра releaseChannelPreference со значением 1, порядок поиска каналов будет реверсирован.

userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2. Путь может представлять собой абсолютный путь к файлу или относительный путь, который интерпретируется относительно исполняемого файла текущего процесса. В противном случае для приложений UWP папка данных пользователя по умолчанию будет папкой "данные приложения" для пакета; для приложений, не являющихся UWP, папка данных пользователя по умолчанию `{Executable File Name}.WebView2` будет создана в той же папке, что и исполняемый объект приложения. Создание WebView2 может завершиться сбоем, если исполняемый объект запущен в каталоге, у процесса которого нет разрешения на создание новой папки в. Приложение несет ответственность за очистку папки данных пользователя после ее завершения.

additionalBrowserArguments можно указать, чтобы изменить поведение WebView. Они будут переданы в процесс браузера как часть командной строки. Дополнительные сведения о параметрах командной строки для процесса браузера можно найти [в разделе Run Chromium with flags](https://aka.ms/RunChromiumWithFlags) . Если приложение запускается с переключателем командной строки, `--edge-webview-switches=xxx` значение этого переключателя (XXX в приведенном выше примере) также будет добавлено в командную строку процесса браузера. Некоторые переключатели `--user-data-dir` , такие как внутренние и важные для WebView. Эти переключатели будут игнорироваться, даже если они указаны. Если один и тот же параметр указан несколько раз, последний — один. Обратите внимание, что это также относится и к переключателям `--enable-features` . Попытка слияния разных значений одного и того же переключателя не выполняется. Значения командной строки процесса приложения `--edge-webview-switches` обрабатываются после обработки параметра additionalBrowserArguments. Также обратите внимание на то, что процесс браузера может быть общим для разных представлений, но не гарантируется, кроме первого WebView, запускающего процесс браузера. Если синтаксический анализ для указанных переключателей не удался, они будут пропущены. `nullptr` Запустится процесс браузера без флагов.

environment_created_handler является результатом обработчика асинхронной операции, которая будет содержать созданный WebView2Environment.

Элементы browserExecutableFolder, userDataFolder и additionalBrowserArguments в environmentParams могут быть переопределены значениями, заданными в переменных среды или в реестре.

При создании WebView2Environment проверяются следующие переменные среды:

```cpp
WEBVIEW2_BROWSER_EXECUTABLE_FOLDER
WEBVIEW2_USER_DATA_FOLDER
WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS
WEBVIEW2_RELEASE_CHANNEL_PREFERENCE
```

Если обнаружена переменная среды override, мы используем значения browserExecutableFolder, userDataFolder и additionalBrowserArguments в качестве замены соответствующих значений в CreateWebView2EnvironmentWithDetails параметрах.

Несмотря на то, что не строго переопределяется, существуют дополнительные переменные среды, которые можно установить.

```cpp
WEBVIEW2_WAIT_FOR_SCRIPT_DEBUGGER
```

Если обнаружено непустое значение, это указывает на то, что WebView запускается в отладчике сценариев. В этом случае WebView будет выдать `Page.waitForDebugger` команду CDP, которая приведет к выполнению сценария в WebView для приостановки при запуске, пока отладчик не выдаст соответствующую `Runtime.runIfWaitingForDebugger` команду CDP для возобновления выполнения. Примечание. Этот параметр реестра не эквивалентен данной переменной среды.

```cpp
WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER
```

Если обнаружено непустое значение, это указывает на то, что WebView запускается в отладчике сценария, который также поддерживает хост-приложения, использующие несколько веб-представлений. Это значение используется в качестве идентификатора для именованного канала, который будет открываться и записываться при создании нового WebView в ведущем приложении. Полезные данные будут соответствовать целевому объекту JSON порта удаленной отладки и могут использоваться внешним отладчиком для присоединения к определенному экземпляру WebView. Ниже представлен формат канала, созданного отладчиком `\\.\pipe\WebView2\Debugger\{app_name}\{pipe_name}` :

* `{app_name}` имя файла exe приложения, например WebView2Example. exe

* `{pipe_name}` значение, заданное для WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER.

Чтобы включить отладку целевых объектов, идентифицированных с помощью JSON, вам также потребуется задать переменную среды WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS для отправки `--remote-debugging-port={port_num}` .

* `{port_num}` порт, на который будет привязан сервер CDP.

Имейте в виду, что настройка переменных среды WEBVIEW2_PIPE_FOR_SCRIPT_DEBUGGER и WEBVIEW2_ADDITIONAL_BROWSER_ARGUMENTS приведет к тому, что веб-представления, размещенные в вашем приложении, и их содержимое будут доступны сторонним приложениям, например отладчикам.

Примечание. Этот параметр реестра не эквивалентен данной переменной среды.

Если ни одна из этих переменных среды не существует, далее будет проверяться реестр. Проверяются следующие разделы реестра:

```cpp
[{Root}\Software\Policies\Microsoft\EmbeddedBrowserWebView\LoaderOverride\{AppId}]
"releaseChannelPreference"=dword:00000000
"browserExecutableFolder"=""
"userDataFolder"=""
"additionalBrowserArguments"=""
```

В маловероятном случае, когда некоторые экземпляры WebView открыты во время обновления браузера, мы сможем блокировать удаление старых браузеров Edge. Чтобы не запустить свободное место на диске, новое создание WebView завершится сбоем при следующей ошибке, если обнаружится, что на вашем компьютере установлено множество старых версий.

```cpp
ERROR_DISK_FULL
```

По умолчанию максимально допустимое число версий Edge равно 20.

Максимально допустимое число старых версий Edge может быть переписано значением следующей переменной среды.

```cpp
WEBVIEW2_MAX_INSTANCES
```

Если WebView зависит от установленного края и удалено все последующее создание завершается сбоем при следующей ошибке

```cpp
ERROR_PRODUCT_UNINSTALLED
```

Сначала мы рассмотрим корневой раздел реестра HKLM, а затем HKCU. AppId сначала присваивается идентификатор пользовательской модели приложения для процесса вызывающего объекта, а если соответствующий раздел реестра отсутствует, для AppId задано имя исполняемого процесса вызывающего объекта или если этот раздел не является ключом реестра "*". Если найден раздел реестра override, мы используем значения реестра browserExecutableFolder, userDataFolder и additionalBrowserArguments как замены соответствующих значений в CreateWebView2EnvironmentWithDetails параметрах. Если хотя бы один из этих значений реестра отсутствует, используется параметр, переданный в CreateWebView2Environment.

#### CreateWebView2Environment 

> общедоступная STDAPI [CreateWebView2Environment](#createwebview2environment)([IWebView2CreateWebView2EnvironmentCompletedHandler](IWebView2CreateWebView2EnvironmentCompletedHandler.md) * environment_created_handler)

Создает среду Evergreen WebView2, используя установленную версию Edge.

Это эквивалентно вызову CreateWebView2EnvironmentWithDetails с помощью nullptr для browserExecutableFolder, userDataFolder, additionalBrowserArguments. Более подробную информацию вы увидите в CreateWebView2EnvironmentWithDetails.

#### GetWebView2BrowserVersionInfo 

> общедоступные STDAPI [GetWebView2BrowserVersionInfo](#getwebview2browserversioninfo)(PCWSTR BROWSEREXECUTABLEFOLDER, LPWSTR * versionInfo)

Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.

Названия каналов — это бета-версия, разработка и Канарские. Если для browserExecutableFolder или настройки канала существует переопределение, будет использоваться переопределение. Если переопределение не задано, используется параметр, переданный в GetWebView2BrowserVersionInfo.

#### CompareBrowserVersions 

> общедоступные STDAPI [CompareBrowserVersions](#comparebrowserversions)(PCWSTR Version1, PCWSTR Version2, int * result)

Этот метод предназначен для всех пользователей, которым нужно правильно сравнить версию, чтобы определить, какая версия более поздняя, устаревшая или та же.

Он может использоваться для определения того, следует ли использовать webview2 или определенную базу функций в версии. Задает для результата значение-1, 0 или 1, если Version1 меньше, равно или больше Version2 соответственно. Возвращает E_INVALIDARG, если не удается проанализировать ни одну из строк версии, ни какой из входных параметров имеет значение null. Входные данные могут напрямую использовать versionInfo, полученный от GetWebView2BrowserVersionInfo, сведения о канале будут игнорироваться.

