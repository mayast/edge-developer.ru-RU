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
# класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Environment 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

Представляет среду WebView2.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.
[CompareBrowserVersions](#comparebrowserversions) | Правильно Сравните версии браузеров, чтобы определить, какая версия более новая или более ранняя.
[CreateAsync](#createasync) | Создает среду Evergreen WebView2, используя установленную версию Edge.
[CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync) | Асинхронно создайте новый WebView для использования с визуальным размещением.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Асинхронно создайте новый WebView.
[CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo) | Создание пустого CoreWebView2PointerInfo.
[CreateWebResourceResponse](#createwebresourceresponse) | Создание нового объекта ответа на веб-ресурс.
[GetAvailableBrowserVersionString](#getavailablebrowserversionstring) | Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.
[GetProviderForHwnd](#getproviderforhwnd) | Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.

Веб – представления, созданные из среды, выполняются в процессе браузера, указанном в параметрах среды, и объекты, созданные из среды, должны использоваться в одной среде. Использование этой функции в разных средах не гарантирует совместимость и может привести к сбою.

## Участников

#### BrowserVersionString 

Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.

> общедоступная строка [BrowserVersionString](#browserversionstring)

Это соответствует формату API GetAvailableCoreWebView2BrowserVersionString. Названия каналов: "бета-версия", "Dev" и "Канарские".

#### NewBrowserVersionAvailable 

Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.

> событие EventHandler< объект > [NewBrowserVersionAvailable](#newbrowserversionavailable)

Для использования более новой версии браузера необходимо создать новую среду и WebView. Это событие будет инициировано только для новой версии из того же канала, из которого выполняется код. Если вы не используете установленный EDGE, событие не срабатывает.

Поскольку папка данных пользователя может использоваться только одним процессом браузера за один раз, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть среду и веб-представления, которые используют более старую версию браузера. Или просто запросите пользователя перезапустить приложение.

#### CompareBrowserVersions 

Правильно Сравните версии браузеров, чтобы определить, какая версия более новая или более ранняя.

> общедоступный статический целочисленный [CompareBrowserVersions](#comparebrowserversions)(строковый Version1, строка Version2)

Возвращает значение-1, 0 или 1 в зависимости от того, является ли Version1 меньше, равно или больше Version2, соответственно.

##### Параметры
* `version1` Одна из строк версии для сравнения. 

* `version2` Другая сравниваемая строка версии.

#### CreateAsync 

Создает среду Evergreen WebView2, используя установленную версию Edge.

> общедоступная статическая асинхронная задача< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(строка browserExecutableFolder, строка userDataFolder, CoreWebView2EnvironmentOptions параметры)

##### Параметры
* `browserExecutableFolder` Относительный путь к папке, содержащей внедренный край. 

* `userDataFolder` userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2. 

* `options` Параметры, используемые для создания среды WebView2.

#### CreateCoreWebView2CompositionControllerAsync 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Асинхронно создайте новый WebView для использования с визуальным размещением.

> открытая асинхронная задача< [CoreWebView2CompositionController](microsoft-web-webview2-core-corewebview2compositioncontroller.md)  >  [CreateCoreWebView2CompositionControllerAsync](#createcorewebview2compositioncontrollerasync)(IntPtr ParentWindow)

parentWindow — это HWND, в котором приложение будет подключаться к визуальному дереву WebView. Это HWND того, что приложение получит ввод указателя или мыши, предназначенное для WebView (и для пересылки потребуется функция SendMouseInput/SendPointerInput). Если приложение перемещает визуальное дерево WebView в другое окно, ему необходимо настроить CoreWebView2CompositionController. ParentWindow, чтобы обновить новый родительский дескриптор HWND визуального дерева.

Задайте свойство RootVisualTarget в созданном CoreWebView2CompositionController, чтобы предоставить визуальное размещение визуального дерева браузера.

Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен. Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.

#### CreateCoreWebView2ControllerAsync 

Асинхронно создайте новый WebView.

> открытая асинхронная задача< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)

parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные. WebView добавит дочернее окно в заданное окно во время создания WebView. Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.

Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен. Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.

#### CreateCoreWebView2PointerInfo 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Создание пустого CoreWebView2PointerInfo.

> общедоступная [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfo](#createcorewebview2pointerinfo)()

Возвращенные CoreWebView2PointerInfo должны быть заполнены всеми соответствующими сведениями перед вызовом SendPointerInput.

#### CreateWebResourceResponse 

Создание нового объекта ответа на веб-ресурс.

> Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(потоковый контент, int StatusCode, String ReasonPhrase, заголовки строк)

Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки. Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать CoreWebView2HttpResponseHeaders для создания заголовков построчно. Сведения о других параметрах смотрите в CoreWebView2WebResourceResponse.

#### GetAvailableBrowserVersionString 

Получение сведений о версии браузера, включая имя канала, если это не стабильный канал или внедренный край.

> общедоступная статическая строка [GetAvailableBrowserVersionString](#getavailablebrowserversionstring)(String browserExecutableFolder)

##### Параметры
* `browserExecutableFolder` Относительный путь к папке, содержащей внедренный край.

#### GetProviderForHwnd 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Возвращает поставщик модели автоматизации пользовательского интерфейса для CoreWebView2CompositionController, соответствующего данному дескриптору HWND.

> общедоступный объект [GetProviderForHwnd](#getproviderforhwnd)(IntPtr HWND)

