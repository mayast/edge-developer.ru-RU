---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Заметки о выпуске Microsoft Edge WebView2 для Win32, WPF и WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 68a32b8e7175f2e52960e7c3a7fe16b66e5a043d
ms.sourcegitcommit: de171a8e7ccd9f23846f3cd06519e4a0104f1c52
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757615"
---
# Заметки о выпуске SDK для WebView2  

Группа WebView2 будет предоставлять обновления [SDK WebView2][WebView2NuGetGallery] на 6 недель. Эта страница будет храниться в актуальном состоянии: объявления о продукте, дополнения и изменения поверхности API и критические изменения.

> [!NOTE]
> Повторно скомпилируйте приложение после обновления пакета NuGet.

> [!IMPORTANT]
> Несмотря на то, что WebView2 является предварительной версией, интерфейсы API .NET будут находиться в **предварительной версии пакета**.

## 0.9.538

[Пакет NuGet][WebView2NuGetGallery0.9.538] | Минимальная версия Microsoft Edge 85.0.538.0.

#### Общее

* Удаление поддержки SDK версии [0.8.149](#08149). Рекомендуем установить последнюю версию WebView2.
* Новая групповая политика для учетной записи при изменении пути к профилю в браузере Microsoft EDGE ([#179](https://github.com/MicrosoftEdge/WebViewFeedback/issues/179))

#### Win32 C/C++

* Добавлена [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures](reference/win32/0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md#get_windowfeatures) , которая вызывается, когда вызывается метод Window. Open () и ему сопоставляется [ICoreWebView2ExperimentalWindowFeatures](reference/win32/0-9-538/icorewebview2experimentalwindowfeatures.md). ([#70](https://github.com/MicrosoftEdge/WebViewFeedback/issues/70))
* **Коренные изменения:** [CreateCoreWebView2EnvironmentWithDetails](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails) устарели и заменены на [CreateCoreWebView2EnvironmentWithOptions](reference/win32/0-9-538/webview2-idl.md#createcorewebview2environmentwithoptions)
* **Коренные изменения:** Чтобы обеспечить соответствие нашего API соглашениям об именовании Windows API, мы обновили следующие имена:
  * [AreRemoteObjectsAllowed](reference/win32/0-9-488/icorewebview2settings.md#get_areremoteobjectsallowed) сейчас [AreHostObjectsAllowed](reference/win32/0-9-538/icorewebview2settings.md#get_arehostobjectsallowed)
* Обновленные [AddHostObjectToScript](reference/win32/0-9-538/icorewebview2.md#addhostobjecttoscript) , чтобы убедиться в том, что маркеры сериализации исходного объекта узла заданы для прокси-объектов и сериализованы обратно в качестве объекта узла, передаваемого в качестве параметра обратного вызова JavaScript. ([#148](https://github.com/MicrosoftEdge/WebViewFeedback/issues/148))

#### .NET (Предварительная версия 0.9.538)

* Выпущены примеры WebView2API для WinForms и WPF, которые являются исчерпывающими руководствами по нашему комплекту SDK. Посмотрите [репозиторий примеров WebView2](https://github.com/MicrosoftEdge/WebView2Samples).
* Добавлена поддержка функций размещения и работы с окнами для [экспериментальных API](./concepts/versioning.md#experimental-apis)
* **Коренные изменения:** Следующие РБП теперь реализуют интерфейс IDisposable: [ScriptDialogOpening](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#scriptdialogopening), [NewWindowRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#newwindowrequested), [WebResourceRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#webresourcerequested)и [PermissionRequested](./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#permissionrequested).
* Добавлены [GetAvailableBrowserVersionString](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#getavailablebrowserversionstring) и [CompareBrowserVersions](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#comparebrowserversions) в качестве [CoreWebView2Environment](reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md) static.

## предварительный выпуск 0.9.515

[Пакет NuGet][WebView2NuGetGallery0.9.515-prerelease] | Минимальная версия Microsoft Edge 84.0.515.0.

* **Объявление:** WebView2 теперь поддерживает Windows Forms и WPF на платформе .NET Framework 4.6.2 или более поздней версии, а также .NET Core 3,0 или более поздней версии в **предварительной версии пакета**
* Извлеките [руководство по началу работы](./gettingstarted/wpf.md) с WPF, чтобы приступить к созданию приложений WPF и [справочника по WPF](./reference/wpf/0-9-515-reference-webview2.md) для API, которые относятся к WPF.
* Извлеките [руководство по началу работы](./gettingstarted/winforms.md) с Windows Forms, чтобы приступить к созданию приложений для Windows Forms и [Справочник по Windows Forms](./reference/winforms/0-9-515-reference-webview2.md) для API Windows Forms.
* Извлечение [ссылки .NET](./reference/dotnet/0-9-515-reference-webview2.md) для API CoreWebView2
* **Известные проблемы:** Мы знаем о некоторых проблемах, описанных в этом предварительном выпуске, которые мы будем решать в будущих выпусках.
  * **Осведомленность о DPI:** WebView2 для WPF — в настоящее время не поддерживается DPI. При инициализации WebView2 для мониторов с высоким разрешением существует известная ситуация, когда WebView сначала инициализируется как часть окна, пока не будет изменен размер окна.
  * **Конструктор WPF:** Этот выпуск в настоящее время не поддерживает конструктор WPF. Поместите элемент управления WebView2 в свое приложение, напрямую изменив соответствующий XAML в текстовом редакторе.

## 0.9.488

[Пакет NuGet][WebView2NuGetGallery0.9.488] | Минимальная версия Microsoft Edge 84.0.488.0.

* **Объявление:** Начиная с предстоящей версии Microsoft Edge 83, Evergreen WebView больше не будут работать с стабильным каналом браузера. Вместо этого он будет указывать на другой набор двоичных файлов с фирменной [WebView2 исполняющей среды Microsoft Edge](./concepts/distribution.md#microsoft-edge-webview2-runtime), которая может быть установлена посредством установщика, разрабатываемого в настоящее время. Дополнительные сведения о [распространении приложений](./concepts/distribution.md).
* **Объявление:** В дальнейшем мы выпустим два пакета: пакет предварительной версии с экспериментальными API (для пробного использования) и стабильный пакет выпусков с стабильными API (вы можете зависеть от него). Извлеките [Microsoft Edge WEBVIEW2 SDK](./concepts/versioning.md) , чтобы узнать о различиях.
* **Коренные изменения:** Чтобы обеспечить соответствие нашего API соглашениям об именовании Windows API, мы обновили имена указанных ниже интерфейсов.
  * Префикс CORE_WEBVIEW2_ * теперь COREWEBVIEW2_ *.
  * [GetCoreWebView2BrowserVersionInfo](reference/win32/0-9-430/webview2-idl.md#getcorewebview2browserversioninfo) сейчас [GetAvailableCoreWebView2BrowserVersionString](reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring)
  * [get_BrowserVersionInfo](reference/win32/0-9-430/icorewebview2environment.md#get_browserversioninfo) теперь [get_BrowserVersionString](reference/win32/0-9-488/icorewebview2environment.md#get_browserversionstring)
  * [AddRemoteObject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) сейчас [AddHostObjectToScript](reference/win32/0-9-488/icorewebview2.md#addhostobjecttoscript)
  * [RemoveRemoteObject](reference/win32/0-9-430/icorewebview2.md#removeremoteobject) сейчас [RemoveHostObjectFromScript](reference/win32/0-9-488/icorewebview2.md#removehostobjectfromscript)
  * Chrome. WebView. remoteObjects теперь является Chrome. WebView. hostObjects
* **Коренные изменения:** Прокси-методы AddRemoteObject JS также были переименованы.
  * getLocalProperty
  * Команда setLocal теперь setLocalProperty
  * getHostProperty
  * setRemote сейчас setHostProperty
  * applyRemote сейчас applyHostFunction
* **Критическое изменение:** [CreateCoreWebView2EnvironmentWithDetails](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails) является устаревшим и заменено на [CreateCoreWebView2EnvironmentWithOptions](reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).  
* Добавлено событие [FrameNavigationCompleted](reference/win32/0-9-488/icorewebview2.md#add_framenavigationcompleted) . Теперь, когда IFRAME завершает навигацию, инициируется событие, которое возвращает успешное перемещение и идентификатор навигации.
* Добавлен интерфейс [ICoreWebView2EnvironmentOptions](reference/win32/0-9-488/ICoreWebView2EnvironmentOptions.md) , который можно использовать для определения версии среды выполнения WebView2, целью которой является приложение.
* Добавлен параметр [IsBuiltInErrorPageEnabled](reference/win32/0-9-488/ICoreWebView2Settings.md#get_isbuiltinerrorpageenabled) . Теперь вы можете включить или отключить страницу встроенной ошибки для навигации в случае сбоя и обработки ошибок процесса отображения.
* Обновленный удаленный объект Injection для поддержки реализаций .NET IDispatch. ([#113](https://github.com/MicrosoftEdge/WebViewFeedback/issues/113))
* Событие [NewWindowRequested](reference/win32/0-9-488/icorewebview2.md#add_newwindowrequested) Обновлено для обработки запросов из контекстных меню. ([#108](https://github.com/MicrosoftEdge/WebViewFeedback/issues/108))
* Выпущен первый отдельный пакет предварительной версии, где можно получить доступ к API визуального размещения. Мы обновили [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) , чтобы добавить новые экспериментальные API-интерфейсы.
  * Добавлен интерфейс [ICoreWebView2ExperimentalCompositionController](reference/win32/0-9-488/ICoreWebView2ExperimentalCompositionController.md) , который используется для подключения к дереву композиции и предоставления входных данных для WebView.
  * Добавлены [ICoreWebView2ExperimentalPointerInfo](reference/win32/0-9-488/ICoreWebView2ExperimentalPointerInfo.md) , содержащие все данные из POINTER_INFO. Он передается в SendPointerInput для вставки ввода указателя в WebView.
  * Добавлен [ICoreWebView2ExperimentalCursorChangedEventHandler](reference/win32/0-9-488/ICoreWebView2ExperimentalCursorChangedEventHandler.md) , который сообщает приложению о том, что указатель мыши на WebView необходимо изменить. При наведении указателя мыши на текстовое поле в WebView курсор меняется с стрелки на элемент Selector. Свойство Cursor в CompositionController указывает приложению, что должен быть в данный момент указатель мыши для WebView.

## 0.9.430

[Пакет NuGet][WebView2NuGetGallery0.9.430] | Минимальная версия Microsoft Edge 82.0.430.0.

Этот пакет SDK — это официальная бета-версия Win32 C++, в которой есть несколько запросов на получение функций. Мы попытались ограничить количество выпусков с коренными изменениями, но в связи с тем, что мы рекомендуем использовать нашу бета-версию, вы можете внести в нее несколько существенных изменений.

* **Коренные изменения:**  По мере использования нашего окончательного выпуска мы переименовали префикс *IWebView2WebView* в *ICoreWebView2* , чтобы обеспечить соответствие нашего API соглашению об именовании Windows API. Кроме того, чтобы сделать комплект SDK более расширяемым для использования платформами пользовательского интерфейса, мы разICoreWebView2 в [ICoreWebView2](reference/win32/0-9-430/icorewebview2.md) и [ICoreWebView2Host](reference/win32/0-9-430/icorewebview2host.md). ICoreWebView2Host поддерживает изменение размеров, отображение и скрытие, фокусировку и другие функциональные возможности, связанные с окнами и композицией. ICoreWebView2 поддерживает все другие функции WebView2. Чтобы узнать больше о том, как вносить эти изменения, [Вытяните наш запрос на включение внесенных](https://github.com/MicrosoftEdge/WebView2Samples/pull/17) изменений в наш проект [WebView2APISample](https://github.com/MicrosoftEdge/WebView2Samples) .
* **Коренные изменения:** Разделите [DocumentStateChanged](reference/win32/0-8-190/iwebview2webview.md#add_documentstatechanged) на три компонента: [SourceChanged](reference/win32/0-9-430/icorewebview2.md#add_sourcechanged), [ContentLoading](reference/win32/0-9-430/icorewebview2.md#add_contentloading)и [HistoryChanged](reference/win32/0-9-430/icorewebview2.md#add_historychanged). Теперь при изменении исходного URL-адреса возникает событие SourceChanged. После изменения состояния журнала возникает событие HistoryChanged. Событие ContentLoading инициируется перед начальным сценарием при загрузке нового документа.
* Добавлена поддержка архитектуры ARM64
* Добавлена поддержка панели мягкого ввода (SIP) для устройств с сенсорным экраном
* Добавлена поддержка `Windows Server 2008 R2` , `Windows Server 2012/2012 R2` и `Windows Server 2016`
* Добавлен [NotifyParentWindowPositionChanged](reference/win32/0-9-430/icorewebview2host.md#notifyparentwindowpositionchanged) , который позволяет строке состояния отслеживать окно в оконном режиме. Это также необходимо для того, чтобы обеспечить доступность функций специальных возможностей в режиме без окон.
* Добавлены параметры [AreRemoteObjectsAllowed](reference/win32/0-9-430/icorewebview2settings.md#get_areremoteobjectsallowed) , позволяющие глобально управлять тем, возможен ли доступ к странице любым удаленным объектам. По умолчанию AreRemoteObjectsAllowed включается, то есть удаленные объекты, добавленные [AddRemoteObject](reference/win32/0-9-430/icorewebview2.md#addremoteobject) , доступны на странице. Если AreRemoteObjectsAllowed отключен, объекты не будут доступны на странице. Изменения будут применены к следующему событию навигации.
* Добавлена настройка [IsZoomControlEnabled](reference/win32/0-9-430/icorewebview2settings.md#get_iszoomcontrolenabled) , не позволяющая пользователям влиять на масштаб WebView с помощью `ctrl`  +  `+` / `-` или `ctrl` + колесика мыши. Вы можете настроить масштаб по-прежнему с помощью [put_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#put_zoomfactor) , если этот параметр отключен.  
* Измененные ZoomFactor применяются только к текущему WebView. Изменение масштаба для текущего WebView не влияет на другие веб-представления, которые будут находиться на одном и том же сайте происхождения. Дополнительные сведения вы видите в разделе [get_ZoomFactor](reference/win32/0-9-430/icorewebview2host.md#get_zoomfactor) .
* Пользовательский интерфейс HID ZoomView для WebView. ([#95](https://github.com/MicrosoftEdge/WebViewFeedback/issues/95))
* Добавлены [SetBoundsAndZoomFactor](reference/win32/0-9-430/icorewebview2host.md#setboundsandzoomfactor). Теперь можно задать коэффициент масштабирования и границы WebViewа.
* Добавлено событие [WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) . Дополнительные сведения вы видите в разделе [add_WindowCloseRequested](reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested) . ([#119](https://github.com/MicrosoftEdge/WebViewFeedback/issues/119))
* Добавлена поддержка типа диалогового окна beforeunload для событий диалогового окна JavaScript и добавлена [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD](reference/win32/0-9-430/icorewebview2.md#core_webview2_script_dialog_kind) элемент перечисления.
* В [HttpRequestHeaders, HttpResponseHeaders](reference/win32/0-9-430/icorewebview2httpresponseheaders.md#getheader) и [get_HasCurrentHeader](reference/win32/0-9-430/icorewebview2httpheaderscollectioniterator.md#get_hascurrentheader) свойства добавляются [коголовки](reference/win32/0-9-430/icorewebview2httprequestheaders.md#getheaders) в HttpHeadersCollectionIterator.
* **Коренные изменения:** Изменено поведение DevToolsProtocolEventReceived. Теперь вы можете создать [DevToolsProtocolEventReceiver](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md) для определенного события протокола DevTools и подписаться на него и отказаться от подписки с помощью [add_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#add_devtoolsprotocoleventreceived) / [remove_DevToolsProtocolEventReceived](reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#remove_devtoolsprotocoleventreceived).
* **Коренные изменения:** Изменение свойства WebMessageReceivedEventArgs [get_WebMessageAsString](reference/win32/0-8-190/iwebview2webmessagereceivedeventargs.md#get_webmessageasstring) на метод [TryGetWebMessageAsString](reference/win32/0-9-430/icorewebview2webmessagereceivedeventargs.md#trygetwebmessageasstring) .
* **Коренные изменения:** Изменение метода [обработки](reference/win32/0-8-190/iwebview2acceleratorkeypressedeventargs.md#handle) AcceleratorKeyPressedEventArgs на свойство [get_Handled](reference/win32/0-9-430/icorewebview2acceleratorkeypressedeventargs.md#get_handled) .

## 0.8.355

[Пакет NuGet][WebView2NuGetGallery0.8.355] | Минимальная версия Microsoft Edge 80.0.355.0.

* Выпущенный WebView2API-образец — подробное руководство по нашему комплекту SDK. Посмотрите [здесь](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample)!
* Добавлена поддержка IME для всех языков, кроме английского. ([#30](https://github.com/MicrosoftEdge/WebViewFeedback/issues/30))
* Обновлена поверхность API события WebResourceRequested в ответ на отчеты об ошибках.  Одновременное указание фильтра и событие для создания теперь не рекомендуются.  Чтобы создать запрашиваемое веб-ресурсом событие, используйте [add_WebResourceRequested](reference/win32/0-8-190/iwebview2webview5.md#add_webresourcerequested) , чтобы добавить событие и [AddWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#addwebresourcerequestedfilter) , чтобы добавить фильтр.  [RemoveWebResourceRequestedFilter](reference/win32/0-8-190/iwebview2webview5.md#removewebresourcerequestedfilter) удаляет фильтр.  ([#36](https://github.com/MicrosoftEdge/WebViewFeedback/issues/36)) ([#74](https://github.com/MicrosoftEdge/WebViewFeedback/issues/74))  
* **Коренные изменения:**  Изменены параметры полноэкранного режима. Устаревший [IsFullScreenAllowed](reference/win32/0-8-190/IWebView2Settings.md#get_isfullscreenallowed_deprecated).  Теперь по умолчанию, если для элемента в WebView (например, видео) задано значение во весь экран, он заполняет границы WebView.  Используйте событие [ContainsFullScreenElementChanged](reference/win32/0-8-190/IWebView2ContainsFullScreenElementChangedEventHandler.md#interface-iwebview2containsfullscreenelementchangedeventhandler) и [get_ContainsFullScreenElement](reference/win32/0-8-190/iwebview2webview5.md#get_containsfullscreenelement) , чтобы указать, как приложение должно изменить размер WebView, если элемент хочет войти в полноэкранный режим.  

## 0.8.314

[Пакет NuGet][WebView2NuGetGallery0.8.314] | Минимальная версия Microsoft Edge 80.0.314.0.

* Добавлена поддержка Windows 7, Windows 8/8.1.
* Добавлена поддержка отладки кода Visual Studio и Visual Studio для WebView2. Теперь вы можете выполнять отладку сценария в WebView2 прямо из вашей среды разработки. Щелкните [здесь](/microsoft-edge/hosting/webview2#debugging-webview2) , чтобы получить дополнительные сведения.  
* Добавлена возможность `Native Object Injection` передачи объекта IDispatch из компонента Win32 приложения и получения доступа к свойствам объекта IDispatch в WebView2.  Более подробную информацию вы увидите в [AddRemoteObject](reference/win32/0-8-190/iwebview2webview4.md#addremoteobject) .  ([#17](https://github.com/MicrosoftEdge/WebViewFeedback/issues/17)).  
* Добавлено `AcceleratorKeyPressed` событие.  Дополнительные сведения вы видите в разделе [add_AcceleratorKeyPressed](reference/win32/0-8-190/iwebview2webview4.md#add_acceleratorkeypressed) .  ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)).  
* Отключено `Context Menus` .  Для получения дополнительных сведений смотрите [put_AreDefaultContextMenusEnabled](reference/win32/0-8-190/iwebview2settings2.md#put_aredefaultcontextmenusenabled) ([#57](https://github.com/MicrosoftEdge/WebViewFeedback/issues/57)).  
* Обновлены `DPI Awareness` . В настоящее время поддержка DPI WebView будет такой же, как и для ведущего приложения. Обратите внимание, что если другое гибридное приложение запускается с определением разрешения DPI, чем исходное WebView, новый WebView не будет запущен, если каталог данных пользователя совпадает ([#1](https://github.com/MicrosoftEdge/WebViewFeedback/issues/1)).
* Обновлен `Notification Change Behavior` таким образом, WebView2 автоматически отвергает запросы разрешений на уведомления, заданные в веб-содержимом, расположенном в WebView.

## 0.8.270  

[Пакет NuGet][WebView2NuGetGallery0.8.270] | Минимальная версия Microsoft Edge 78.0.270.0.  

* Добавлено `DocumentTitleChanged` событие для указания на изменение названия документа \ ([\ #27][MicrosoftEdgeWebViewFeedbackIssue27]\).  
* Добавлен `GetWebView2BrowserVersionInfo` API \ ([\ #18][MicrosoftEdgeWebViewFeedbackIssue18]\).  
* Добавлено `NewWindowRequested` событие.  
* Обновленная `CreateWebView2EnvironmentWithDetails` функция для удаления `releaseChannelPreference` .  Для получения дополнительных сведений ознакомьтесь с функцией [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] .  Переопределение реестра и переменной среды по-прежнему поддерживается.  Параметр канала по умолчанию используется, если он не переопределен.  
    Во время поиска канала мы будем пропускать все старые версии каналов, несовместимые с WebView2 SDK.  
    Мы выбираем более стабильный канал, чтобы обеспечить наиболее устойчивое поведение для конечного пользователя.  При тестировании с использованием последних сборок Канарские необходимо создать сценарий, чтобы задать переменную среды `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` до `1` запуска приложения.  
* Обновленная `CreateWebView2EnvironmentWithDetails` функция с логикой выбора, `userDataFolder` если не указана.  Для получения дополнительных сведений ознакомьтесь с функцией [CreateWebView2EnvironmentWithDetails][WebViewsGlobalsCreateWebView2EnvironmentWithDetails] .  Если ранее вы использовали расположение по умолчанию `userDataFolder` при переходе на новый пакет SDK, по умолчанию `userDataFolder` сбрасывается (устанавливается новое расположение в каталоге кода узла), и состояние также сбрасывается.  
    Если ведущий процесс не имеет разрешения на запись в указанный каталог, `CreateWebView2EnvironmentWithDetails` может произойти сбой.  Вы можете скопировать данные из старого каталога данных пользователя в новый каталог.  

## 0.8.230  

[Пакет NuGet][WebView2NuGetGallery0.8.230] | Минимальная версия Microsoft Edge 77.0.230.0.  

* Добавлен `Stop` API для остановки всех функций навигации и ожидающих выборок ресурсов \ ([\ #28][MicrosoftEdgeWebViewFeedbackIssue28]\).  
* Файл. tlb добавлен в пакет NuGet \ ([\ #22][MicrosoftEdgeWebViewFeedbackIssue22]\).  
* Добавлены проекты .NET в список установщиков в пакете NuGet \ ([\ #32][MicrosoftEdgeWebViewFeedbackIssue32]\).  

## 0.8.190  

[Пакет NuGet][WebView2NuGetGallery0.8.190] | Минимальная версия Microsoft Edge 77.0.190.0.  

* Добавлены `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` в элемент управления, если пользователи смогут открывать DevTools \ ([\ #16][MicrosoftEdgeWebViewFeedbackIssue16]\).  
* Добавляется `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` к элементу управления, если отображается строка состояния \ ([\ #19][MicrosoftEdgeWebViewFeedbackIssue19]\).  
* Добавляется `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` для перемещения вперед и назад по журналу переходов.  
* Добавлены типы заголовков HTTP ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` ) для просмотра и изменения заголовков HTTP в WebView.  
* Добавлена поддержка 32-bit WebView на 64-разрядных компьютерах \ ([\ #13][MicrosoftEdgeWebViewFeedbackIssue13]\).  
* Добавил WebView IDL в SDK \ ([\ #14][MicrosoftEdgeWebViewFeedbackIssue14]\).  
* Добавлена библиотека для поддержки объектов ID интерфейса IID\_\ * \ ([\ #12][MicrosoftEdgeWebViewFeedbackIssue12]\).  
* Добавлены путь включения, связывание и автоматическое копирование DLL-файлов в конечный файл NuGet в SDK.  
* Включены запросы `window.open` в сценарии.  

## 0.8.149  

[Пакет NuGet][WebView2NuGetGallery0.8.149] | Минимальная версия Microsoft Edge 76.0.149.0.  

Первоначальная версия предварительной версии для разработчиков.  

<!-- image links -->

<!-- Links -->
[MicrosoftEdgeWebViewFeedbackIssue12]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Репозиторий отзывов для MicrosoftEdge и WebViewFeedback, выпуска 12"  
[MicrosoftEdgeWebViewFeedbackIssue13]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Вопрос в репозитории отзыва для MicrosoftEdge и WebViewFeedback 13"  
[MicrosoftEdgeWebViewFeedbackIssue14]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Вопрос в репозитории отзыва для MicrosoftEdge и WebViewFeedback 14"  
[MicrosoftEdgeWebViewFeedbackIssue16]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "MicrosoftEdge/WebViewFeedback, подающий отзыв"  
[MicrosoftEdgeWebViewFeedbackIssue18]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Репозиторий отзывов для MicrosoftEdge/WebViewFeedback, выпуска 18"  
[MicrosoftEdgeWebViewFeedbackIssue19]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Репозиторий отзывов для MicrosoftEdge и WebViewFeedback, выпуска 19"  
[MicrosoftEdgeWebViewFeedbackIssue22]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Вопрос в репозитории отзыва для MicrosoftEdge и WebViewFeedback 22"  
[MicrosoftEdgeWebViewFeedbackIssue27]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Репозиторий отзывов для MicrosoftEdge/WebViewFeedback, выпуска 27"  
[MicrosoftEdgeWebViewFeedbackIssue28]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "MicrosoftEdge/WebViewFeedback в репозитории обратной связи 28"  
[MicrosoftEdgeWebViewFeedbackIssue32]: https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 32"  

[WebView2NuGetGallery]: https://aka.ms/webviewnuget "Коллекция NuGet | Microsoft. Web. WebView2"  
[WebView2NuGetGallery0.8.149]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.149"  
[WebView2NuGetGallery0.8.190]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.190"  
[WebView2NuGetGallery0.8.230]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.230"  
[WebView2NuGetGallery0.8.270]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.270"  
[WebView2NuGetGallery0.8.314]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.314"  
[WebView2NuGetGallery0.8.355]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.355"  
[WebView2NuGetGallery0.9.430]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.430"
[WebView2NuGetGallery0.9.488]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.488"
[WebView2NuGetGallery0.9.515-prerelease]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Коллекция NuGet | Предварительная версия Microsoft. Web. WebView2 v 0.9.515"
[WebView2NuGetGallery0.9.538]: https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.538"

[WebViewsGlobalsCreateWebView2EnvironmentWithDetails]: reference/win32/0-8-190/webview2-idl.md#createwebview2environmentwithdetails "WebView Globals-CreateWebView2EnvironmentWithDetails"  
