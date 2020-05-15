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
# Класс Microsoft. Web. WebView2. Core. CoreWebView2Environment 

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Представляет среду WebView2.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[BrowserVersionString](#browserversionstring) | Сведения о версии браузера для текущего CoreWebView2Environment, включая имя канала, если он не является стабильным каналом.
[NewBrowserVersionAvailable](#newbrowserversionavailable) | Событие NewBrowserVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.
[CreateAsync](#createasync) | Создает среду Evergreen WebView2, используя установленную версию Edge.
[CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync) | Асинхронно создайте новый WebView.
[CreateWebResourceResponse](#createwebresourceresponse) | Создание нового объекта ответа на веб-ресурс.

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

#### CreateAsync 

Создает среду Evergreen WebView2, используя установленную версию Edge.

> открытая асинхронная задача< [CoreWebView2Environment](microsoft-web-webview2-core-corewebview2environment.md)  >  [CreateAsync](#createasync)(строка browserExecutableFolder, строка userDataFolder, CoreWebView2EnvironmentOptions параметры)

##### Параметры
* `browserExecutableFolder` Относительный путь к папке, содержащей внедренный край. 

* `userDataFolder` userDataFolder можно указать, чтобы изменить расположение папки данных пользователя по умолчанию для WebView2. 

* `options` Параметры, используемые для создания среды WebView2.

#### CreateCoreWebView2ControllerAsync 

Асинхронно создайте новый WebView.

> открытая асинхронная задача< [CoreWebView2Controller](microsoft-web-webview2-core-corewebview2controller.md)  >  [CreateCoreWebView2ControllerAsync](#createcorewebview2controllerasync)(IntPtr ParentWindow)

parentWindow — HWND, в котором нужно отобразить WebView и из которого принимаются входные данные. WebView добавит дочернее окно в заданное окно во время создания WebView. Z-порядок и другие элементы, которые влияют на родственный порядок окон, будут затронуты соответствующим образом.

Рекомендуется, чтобы идентификатор пользовательской модели приложения "Настройка приложения" для процесса или окна приложения был установлен. Если не задано значение None, во время создания WebView для созданного идентификатора пользовательской модели приложения задается корневое окно parentWindow.

#### CreateWebResourceResponse 

Создание нового объекта ответа на веб-ресурс.

> Public HttpResponseMessage [CreateWebResourceResponse](#createwebresourceresponse)(потоковый контент, int StatusCode, String ReasonPhrase, заголовки строк)

Заголовки — это строка заголовков необработанного ответа, ограниченная символом новой строки. Кроме того, можно создать этот объект с пустой строкой заголовков, а затем использовать CoreWebView2HttpResponseHeaders для создания заголовков построчно. Сведения о других параметрах смотрите в CoreWebView2WebResourceResponse.

