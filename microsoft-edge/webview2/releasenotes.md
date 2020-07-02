---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Заметки о выпуске Microsoft Edge WebView2 для Win32, WPF и WinForms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 1f229474d4de416f9f6516ce62ab88097f2bc1aa
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844420"
---
# Заметки о выпуске SDK для WebView2  

Группа WebView2 предоставляет обновления [SDK WebView2][NuGetGallery] на 6 недель.  Ознакомьтесь со следующими материалами, чтобы получить сведения о объявлениях, дополнениях и изменениях в поверхности API и критических изменениях.  

> [!NOTE]
> Повторно скомпилируйте приложение после обновления пакета NuGet.  

> [!IMPORTANT]
> Несмотря на то, что WebView2 является предварительным просмотром, API .NET находятся в `pre-release package` .  

## 0.9.538  

[Пакет NuGet][NuGetGallery0.9.538] \ | Минимальная версия Microsoft Edge 85.0.538.0.  

#### Общее  

*   Удаление поддержки WebView2 версии SDK для [0.8.149](#08149).  Команда WebView рекомендует поддерживать последние версии WebView2.  
*   Обновлена групповая политика для учетной записи при изменении пути к профилю в браузере Microsoft EDGE ([#179][GithubMicrosoftedgeWebviewfeedbackIssue179]).  

#### Win32 C/C++  

*   Добавлена [ICoreWebView2ExperimentalNewWindowRequestedEventArgs:: get_WindowFeatures][ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures] , которая вызывается `window.open()` , когда вызывается и связывается [ICoreWebView2ExperimentalWindowFeatures][ReferenceWin3209538Icorewebview2experimentalwindowfeatures] \ ([#70][GithubMicrosoftedgeWebviewfeedbackIssue70]\).  
*   > [!IMPORTANT]
    > **Критическое изменение**: [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] устарело и заменено на [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209538Webview2IdlCreatecorewebview2environmentwithoptions].  
*   > [!IMPORTANT]
    > **Коренные изменения**: чтобы обеспечить соответствие API WebView2 с соглашениями об именовании Windows API, Группа WebView обновила имена указанных ниже элементов.  
    > *   [AreRemoteObjectsAllowed][ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed] теперь [AreHostObjectsAllowed][ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed].  
*   Обновленные [AddHostObjectToScript][ReferenceWin3209538Icorewebview2Addhostobjecttoscript] , чтобы убедиться в том, что маркеры преобразователя исходного объекта узла были установлены на прокси-объекты и сериализованы обратно как объект узла, передаваемый в качестве параметра обратного вызова JavaScript \ ([#148][GithubMicrosoftedgeWebviewfeedbackIssue148]\).  

#### .NET (Предварительная версия 0.9.538)  

*   Выпущены примеры WebView2API для WinForms и WPF, которые являются исчерпывающими руководствами по WebView2 SDK.  Дополнительные сведения можно найти в [репозитории примеров][GithubMicrosoftedgeWebview2samplesMain].  
*   Добавлена поддержка визуального размещения и функций окон для [экспериментальных API][ConceptsVersioningExperimentalApis].  
*   > [!IMPORTANT]
    > **Коренные изменения**: следующие РБП теперь реализуют интерфейс IDisposable: [ScriptDialogOpening][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Scriptdialogopening], [NewWindowRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Newwindowrequested], [WebResourceRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Webresourcerequested]и [PermissionRequested][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Permissionrequested].  
*   Добавлены [GetAvailableBrowserVersionString][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring] и [CompareBrowserVersions][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions] в качестве [CoreWebView2Environment][ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environment] static.  

## предварительный выпуск 0.9.515  

[Пакет NuGet][NuGetGallery0.9.515-prerelease] \ | Минимальная версия Microsoft Edge 84.0.515.0.  

*   > [!IMPORTANT]
    > **Объявление**: WebView2 теперь поддерживает Windows Forms и WPF на платформе .NET Framework 4.6.2 или более поздней версии, а также .net Core 3,0 или более поздней версии в **предварительной версии пакета**.  
*   Дополнительные сведения о создании приложений WPF и [справочнике по WPF][ReferenceWpf09515Reference] для API WebView2 можно найти в [руководстве Приступая к работе][GettingstartedWpf]с WPF.  
*   Дополнительные сведения о создании приложений для Windows Forms и [справочнике по Windows Forms][ReferenceWinforms09515Reference] для WebView2 API для Windows Forms можно найти в [руководстве Приступая к работе с Windows Forms][GettingstartedWinforms].  
*   Дополнительные сведения об API CoreWebView2 можно найти в [справочнике по .NET][ReferenceDotnet09515Reference].  
*   > [!CAUTION]
    > **Известные проблемы**: команда WebView отслеживает некоторые проблемы в предварительной версии, которые разрешаются в будущих выпусках.  
    > *   **Осведомленность о dpi**: WEBVIEW2 для WPF — в настоящее время не поддерживается dpi.  При инициализации WebView2 для мониторов с высоким разрешением существует известная ситуация, когда WebView сначала инициализируется как часть окна, пока не будет изменен размер окна.  
    > *   **Конструктор WPF**: конструктор WPF в настоящее время не поддерживается.  Добавьте элемент управления WebView2 в свое приложение, напрямую изменив соответствующий XAML в текстовом редакторе.  

## 0.9.488  

[Пакет NuGet][NuGetGallery0.9.488] \ | Минимальная версия Microsoft Edge 84.0.488.0.  

*   > [!IMPORTANT]
    > **Объявление**: начиная с предстоящей версии Microsoft Edge 83, Evergreen WebView больше не ориентирован на стабильный канал браузера.  Вместо этого он указывает на другой набор двоичных файлов с фирменной [Evergreen WebView2 среды выполнения][ConceptsDistributionEvergreenMode], который можно установить с помощью установщика, который в настоящее время разрабатывается группой WebView.  Дополнительные сведения можно найти в разделе [распространение приложений][ConceptsDistribution].  
*   > [!IMPORTANT]
    > **Извещение**. команда WebView выпускает два пакета: пакет предварительной версии с экспериментальными API \ (для пробного использования) и стабильный пакет выпусков с стабильными API \ (для вашего доверия).  Сведения о различиях можно найти в статье [сведения о версиях браузеров и WebView2][ConceptsVersioning].  
*   > [!IMPORTANT]
    > **Коренные изменения**: чтобы обеспечить соответствие API WebView2 с соглашениями об именовании Windows API, Группа WebView обновила имена указанных ниже интерфейсов.  
    > *   `CORE_WEBVIEW2_*` Теперь префикс `COREWEBVIEW2_*` .  
    > *   [GetCoreWebView2BrowserVersionInfo][ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo] теперь [GetAvailableCoreWebView2BrowserVersionString][ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring].  
    > *   [get_BrowserVersionInfo][ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo] теперь [get_BrowserVersionString][ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring].  
    > *   [AddRemoteObject][ReferenceWin3209430Icorewebview2Addremoteobject] теперь [AddHostObjectToScript][ReferenceWin3209488Icorewebview2Addhostobjecttoscript].  
    > *   [RemoveRemoteObject][ReferenceWin3209430Icorewebview2Removeremoteobject] теперь [RemoveHostObjectFromScript][ReferenceWin3209488Icorewebview2Removehostobjectfromscript].  
    > *   `chrome.webview.remoteObjects` Сейчас `chrome.webview.hostObjects` .  
*   > [!IMPORTANT]
    > **Коренные изменения**: `AddRemoteObject` методы прокси-сервера также переименовываются.  
    > *   `getLocal` Сейчас `getLocalProperty` .  
    > *   `setLocal` Сейчас `setLocalProperty` .  
    > *   `getRemote` Сейчас `getHostProperty` .  
    > *   `setRemote` Сейчас `setHostProperty` .  
    > *   `applyRemote` Сейчас `applyHostFunction` .  
*   > [!IMPORTANT]
    > **Критическое изменение**: [CreateCoreWebView2EnvironmentWithDetails][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails] устарело и заменено на [CreateCoreWebView2EnvironmentWithOptions][ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions].  
*   Добавлено событие [FrameNavigationCompleted][ReferenceWin3209488Icorewebview2AddFramenavigationcompleted] .  Теперь, когда IFRAME завершает навигацию, инициируется событие, которое возвращает успешное перемещение и идентификатор навигации.  
*   Добавлен интерфейс [ICoreWebView2EnvironmentOptions][ReferenceWin3209488Icorewebview2environmentoptions] , который можно использовать для определения версии среды выполнения WebView2, целью которой является приложение.  
*   Добавлен параметр [IsBuiltInErrorPageEnabled][ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled] .  Теперь вы можете включить или отключить страницу встроенной ошибки для навигации в случае сбоя и обработки ошибок процесса отображения.  
*   Обновленный удаленный объект Injection для поддержки реализаций .NET IDispatch ([#113][GithubMicrosoftedgeWebviewfeedbackIssue113]\).  
*   Обновлено событие [NewWindowRequested][ReferenceWin3209488Icorewebview2AddNewwindowrequested] для обработки запросов из контекстных меню \ ([#108][GithubMicrosoftedgeWebviewfeedbackIssue108]\).  
*   Выпущен первый отдельный пакет предварительной версии WebView2, в который можно получить доступ к API визуального размещения.  Группа WebView обновила [APISample][GithubMicrosoftedgeWebview2samplesMain] , чтобы добавить новые экспериментальные API.  
    *   Добавлен интерфейс [ICoreWebView2ExperimentalCompositionController][ReferenceWin3209488Icorewebview2experimentalcompositioncontroller] , который используется для подключения к дереву композиции и предоставления входных данных для WebView.  
    *   Добавлены [ICoreWebView2ExperimentalPointerInfo][ReferenceWin3209488Icorewebview2experimentalpointerinfo] , содержащие все данные из a `POINTER_INFO` .  Он передается в SendPointerInput для вставки ввода указателя в WebView.  
    *   Добавлен [ICoreWebView2ExperimentalCursorChangedEventHandler][ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler] , который сообщает приложению о том, что указатель мыши на WebView необходимо изменить.  При наведении указателя мыши на текстовое поле в WebView курсор меняется с стрелки на элемент Selector.  Свойство Cursor в поле `CompositionController` сообщает приложению, что в данный момент должен находиться указатель мыши для WebView.  

## 0.9.430  

[Пакет NuGet][NuGetGallery0.9.430] \ | Минимальная версия Microsoft Edge 82.0.430.0.  

WebView2 SDK — это официальная бета-версия C++ для Win32, включающая в себя несколько запросов на функции отзыва.  Команда WebView пытается ограничить количество выпусков с коренными изменениями, но по мере использования бета-версии, в рамках которого можно внести несколько существенных изменений в одном месте.  

*   > [!IMPORTANT]
    > **Коренные изменения**: в последнем выпуске команда WebView переименовала префикс *IWebView2WebView* в *ICoreWebView2* , чтобы убедиться, что API WebView2 соответствует соглашению об именовании Windows API.  Кроме того, чтобы использовать пакет WebView2 SDK из платформ пользовательского интерфейса, Группа WebView, разделенная `ICoreWebView2` на [ICoreWebView2][ReferenceWin3209430Icorewebview2] и [ICoreWebView2Host][ReferenceWin3209430Icorewebview2host].  `ICoreWebView2Host` Поддержка изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.  ICoreWebView2 поддерживает все другие функции WebView2.  Чтобы узнать больше о том, как внести изменения, ознакомьтесь с WebView2 [запросом на включение][GithubMicrosoftedgeWebview2samplesPr17] внесенных изменений в проект [APISample][GithubMicrosoftedgeWebview2samplesMain] WebView2.  
*   > [!IMPORTANT]
    > **Коренные изменения**: разделение [DocumentStateChanged][ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged] на три компонента: [SourceChanged][ReferenceWin3209430Icorewebview2AddSourcechanged], [ContentLoading][ReferenceWin3209430Icorewebview2AddContentloading]и [HistoryChanged][ReferenceWin3209430Icorewebview2AddHistorychanged].  Теперь, когда URL-адрес источника изменит `SourceChanged` событие, будет запущено.  После изменения состояния журнала возникает событие HistoryChanged.  `ContentLoading`Событие срабатывает перед начальным сценарием при загрузке нового документа.  
*   Добавлена поддержка архитектуры ARM64.  
*   Добавлена поддержка панели мягкого ввода \ (SIP \) для устройств с сенсорным экраном.  
*   Добавлена поддержка для Windows Server 2008 R2, Windows Server 2012, Windows Server 2012 R2 и Windows Server 2016.  
*   Добавлен [NotifyParentWindowPositionChanged][ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged] , который позволяет строке состояния отслеживать окно в оконном режиме.  Кроме того, это изменение должно быть реализовано в режиме без окон, чтобы обеспечить доступность функций специальных возможностей.  
*   Добавлены параметры [AreRemoteObjectsAllowed][ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed] , определяющие, возможен ли доступ к странице для удаленных объектов.  По умолчанию, `AreRemoteObjectsAllowed` это означает, что удаленные объекты, добавленные с помощью [AddRemoteObject][ReferenceWin3209430Icorewebview2Addremoteobject] , доступны на странице.  Если `AreRemoteObjectsAllowed` этот элемент отключен, объекты недоступны со страницы.  Изменения применяются к следующему событию навигации.  
*   Добавлена настройка [IsZoomControlEnabled][ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled] , не позволяющая пользователям влиять на масштаб WebView с помощью `ctrl` + `+` и `ctrl` + `-` \ (или `ctrl` + колесом мыши).  При отключенном параметре Масштаб по-прежнему можно настроить с помощью [put_ZoomFactor][ReferenceWin3209430Icorewebview2hostPutZoomfactor] .  
*   Измененные ZoomFactor применяются только к текущему WebView.  Изменение масштаба для текущего WebView не влияет на другие веб-представления, к которым вы перешли на тот же самый источник.  Дополнительные сведения можно найти в разделе [get_ZoomFactor][ReferenceWin3209430Icorewebview2hostGetZoomfactor].  
*   Пользовательский интерфейс HID ZoomView для WebView \ ([#95][GithubMicrosoftedgeWebviewfeedbackIssue95]\).  
*   Добавлены [SetBoundsAndZoomFactor][ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor].  Теперь вы можете задать коэффициент масштабирования и границы WebViewа одновременно.  
*   Добавлено событие [WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] .  Для получения дополнительных сведений смотрите [add_WindowCloseRequested][ReferenceWin3209430Icorewebview2AddWindowcloserequested] ([#119][GithubMicrosoftedgeWebviewfeedbackIssue119]).  
*   Добавлена поддержка типа диалогового окна beforeunload для событий диалогового окна JavaScript и добавлена [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD][ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind] элемент перечисления.  
*   В [HttpRequestHeaders, HttpResponseHeaders][ReferenceWin3209430Icorewebview2httpresponseheadersGetheader] и [get_HasCurrentHeader][ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader] свойства добавляются [коголовки][ReferenceWin3209430Icorewebview2httprequestheadersGetheaders] в HttpHeadersCollectionIterator.  
*   > [!IMPORTANT]
    > **Коренные изменения**: изменение поведения DevToolsProtocolEventReceived.  Теперь вы можете создать [DevToolsProtocolEventReceiver][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver] для определенного события протокола DevTools и подписаться на него и отказаться от подписки с помощью [add_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived] / [remove_DevToolsProtocolEventReceived][ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived].
*   > [!IMPORTANT]
    > **Коренные изменения**: свойство " [get_WebMessageAsString][ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring] " изменено на WebMessageReceivedEventArgs в метод [TryGetWebMessageAsString][ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring] .  
*   > [!IMPORTANT]
    > **Прерывание изменения**: метод [обработки][ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle] AcceleratorKeyPressedEventArgs "изменено" на свойство [get_Handled][ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled] .  

## 0.8.355

[Пакет NuGet][NuGetGallery0.8.355] \ | Минимальная версия Microsoft Edge 80.0.355.0.

*   Выпущен пример WebView2API, подробное руководство по WebView2 SDK.  Дополнительные сведения можно найти в разделе [APISample][GithubMicrosoftedgeWebview2samplesApisample].  
*   Добавлена поддержка IME для всех языков, кроме английского \ ([#30][GithubMicrosoftedgeWebviewfeedbackIssue30]\).  
*   Обновлена поверхность API события WebResourceRequested в ответ на отчеты об ошибках.  Одновременное указание фильтра и событие для создания теперь не рекомендуются.  Чтобы создать запрашиваемое веб-ресурсом событие, используйте [add_WebResourceRequested][ReferenceWin3208190Iwebview2webview5AddWebresourcerequested] , чтобы добавить событие и [AddWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter] , чтобы добавить фильтр.  [RemoveWebResourceRequestedFilter][ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter] удаляет фильтр \ ([#36][GithubMicrosoftedgeWebviewfeedbackIssue36]\) \ ([#74][GithubMicrosoftedgeWebviewfeedbackIssue74]\).  
*   > [!IMPORTANT]
    > **Коренные изменения**: изменено поведение во весь экран.  Устаревший [IsFullScreenAllowed][ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated].  Теперь по умолчанию, если элемент в WebView \ (например, видео \) настроен на полный экран, он заполняет границы WebView.  Используйте событие [ContainsFullScreenElementChanged][ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler] и [get_ContainsFullScreenElement][ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement] , чтобы указать, как приложение должно изменить размер WebView, если элемент хочет войти в полноэкранный режим.  

## 0.8.314  

[Пакет NuGet][NuGetGallery0.8.314] \ | Минимальная версия Microsoft Edge 80.0.314.0.  

*   Добавлена поддержка для Windows 7, Windows 8 и Windows 8,1.  
*   Добавлена поддержка отладки кода Visual Studio и Visual Studio для WebView2.  Теперь Проведите отладку вашего сценария в WebView2 прямо из вашей среды разработки.  Дополнительные сведения [можно найти в разделе Отладка при разработке с помощью элементов управления WebView2][HowtoDebug].  
*   Добавлена `Native Object Injection` возможность для сценария, выполняющегося в WebView2, получить доступ к объекту IDispatch из компонента Win32 приложения и получить доступ к свойствам объекта IDispatch.  Дополнительные сведения можно найти в разделе [AddRemoteObject][ReferenceWin3208190Iwebview2webview4Addremoteobject] \ ([#17][GithubMicrosoftedgeWebviewfeedbackIssue17]\).  
*   Добавлено `AcceleratorKeyPressed` событие.  Дополнительные сведения можно найти в разделе [add_AcceleratorKeyPressed][ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Отключено `Context Menus` .  Дополнительные сведения можно найти в разделе [put_AreDefaultContextMenusEnabled][ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled] \ ([#57][GithubMicrosoftedgeWebviewfeedbackIssue57]\).  
*   Обновлены `DPI Awareness` .  Теперь сведения о DPI в WebView совпадают с определением DPI для ведущего приложения.  
    
    > [!NOTE] 
    > Если другое гибридное приложение запускается с определением разрешения DPI, чем исходное WebView, новый WebView не запускается, если каталог данных пользователя совпадает ([#1][GithubMicrosoftedgeWebviewfeedbackIssue1]).  
    
*   Обновлен `Notification Change Behavior` таким образом, WebView2 автоматически отвергает запросы разрешений на уведомления, заданные в веб-содержимом, расположенном в WebView.  

## 0.8.270  

[Пакет NuGet][NuGetGallery0.8.270] \ | Минимальная версия Microsoft Edge 78.0.270.0.  

*   Добавлено `DocumentTitleChanged` событие для указания на изменение названия документа \ ([\ #27][GithubMicrosoftedgeWebviewfeedbackIssue27]\).  
*   Добавлен `GetWebView2BrowserVersionInfo` API \ ([\ #18][GithubMicrosoftedgeWebviewfeedbackIssue18]\).  
*   Добавлено `NewWindowRequested` событие.  
*   Обновленная `CreateWebView2EnvironmentWithDetails` функция для удаления `releaseChannelPreference` .  Для получения дополнительных сведений ознакомьтесь с функцией [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails] .  Переопределение реестра и переменной среды по-прежнему поддерживается.  Параметр канала по умолчанию используется, если он не переопределен.  
    Во время поиска по каналам команда WebView пропускает все старые версии канала, несовместимые с пакетом SDK для WebView2.  
    Команда WebView выбирает более стабильный канал для обеспечения наибольшего соответствия поведения для конечного пользователя.  При тестировании с использованием последних сборок Канарские необходимо создать сценарий, чтобы задать `WEBVIEW2_RELEASE_CHANNEL_PREFERENCE` переменную среды `1` перед запуском приложения.  
*   Функция, которая была обновлена `CreateWebView2EnvironmentWithDetails` с помощью логики для выбора, `userDataFolder` если не указана.  Для получения дополнительных сведений ознакомьтесь с функцией [CreateWebView2EnvironmentWithDetails][ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails] .  Если ранее вы использовали расположение по умолчанию `userDataFolder` при переходе на новый пакет SDK, по умолчанию `userDataFolder` сбрасывается (устанавливается новое расположение в каталоге кода узла), и состояние также сбрасывается.  
    Если ведущий процесс не имеет разрешения на запись в указанный каталог, эта `CreateWebView2EnvironmentWithDetails` функция может завершиться ошибкой.  Вы можете скопировать данные из старого каталога данных пользователя в новый каталог.  

## 0.8.230  

[Пакет NuGet][NuGetGallery0.8.230] \ | Минимальная версия Microsoft Edge 77.0.230.0.  

*   Добавлен `Stop` API для остановки всех функций навигации и ожидающих выборок ресурсов \ ([\ #28][GithubMicrosoftedgeWebviewfeedbackIssue28]\).  
*   Файл. tlb добавлен в пакет NuGet \ ([\ #22][GithubMicrosoftedgeWebviewfeedbackIssue22]\).  
*   Добавлены проекты .NET в список установщиков в пакете NuGet \ ([\ #32][GithubMicrosoftedgeWebviewfeedbackIssue32]\).  

## 0.8.190  

[Пакет NuGet][NuGetGallery0.8.190] \ | Минимальная версия Microsoft Edge 77.0.190.0.  

*   Добавлены `get_AreDevToolsEnabled` / `put_AreDevToolsEnabled` в элемент управления, если пользователи смогут открывать DevTools \ ([\ #16][GithubMicrosoftedgeWebviewfeedbackIssue16]\).  
*   Добавляется `get_IsStatusBarEnabled` / `put_IsStatusBarEnabled` к элементу управления, если отображается строка состояния \ ([\ #19][GithubMicrosoftedgeWebviewfeedbackIssue19]\).  
*   Добавляется `get_CanGoBack` / `GoBack` / `get_CanGoForward` / `GoForward` для перемещения вперед и назад по журналу переходов.  
*   Добавлены типы заголовков HTTP ( `IWebView2HttpHeadersCollectionIterator` / `IWebView2HttpRequestHeaders` / `IWebView2HttpRequestHeaders` ) для просмотра и изменения заголовков HTTP в WebView.  
*   Добавлена поддержка 32-bit WebView на 64-разрядных компьютерах \ ([\ #13][GithubMicrosoftedgeWebviewfeedbackIssue13]\).  
*   Добавил WebView IDL в SDK \ ([\ #14][GithubMicrosoftedgeWebviewfeedbackIssue14]\).  
*   Добавлена библиотека для поддержки объектов ID интерфейса IID\_\ * \ ([\ #12][GithubMicrosoftedgeWebviewfeedbackIssue12]\).  
*   Добавлены путь включения, связывание и автоматическое копирование DLL-файлов в конечный файл NuGet в SDK.  
*   Включены запросы `window.open` в сценарии.  

## 0.8.149  

[Пакет NuGet][NuGetGallery0.8.149] \ | Минимальная версия Microsoft Edge 76.0.149.0.  

Первоначальная версия предварительной версии для разработчиков.  

<!-- Links -->  

[ConceptsDistribution]: ./concepts/distribution.md "Распространение приложений с помощью WebView2 | Документы Microsoft"  
[ConceptsDistributionEvergreenMode]: ./concepts/distribution.md#evergreen-distribution-mode "Режим распространения Evergreen — распространение приложений с помощью WebView2 | Документы Microsoft"  
[ConceptsVersioning]: ./concepts/versioning.md "Общие сведения о версиях браузеров и WebView2 | Документы Microsoft"  
[ConceptsVersioningExperimentalApis]: ./concepts/versioning.md#experimental-apis "Экспериментальные API — основные сведения о версиях браузеров и WebView2 | Документы Microsoft"  
[GettingstartedWinforms]: ./gettingstarted/winforms.md "Начало работы с WebView2 в приложениях для Windows Forms | Документы Microsoft"  
[GettingstartedWpf]: ./gettingstarted/wpf.md "Начало работы с WebView2 в WPF | Документы Microsoft"  
[HowtoDebug]: ./howto/debug.md "Отладка при разработке с помощью элементов управления WebView2 | Документы Microsoft"  

[ReferenceWin3208190Iwebview2acceleratorkeypressedeventargsHandle]: ./reference/win32/0-8-190/iwebview2acceleratorkeypressedeventargs.md#handle "Handle-Interface IWebView2AcceleratorKeyPressedEventArgs | Документы Microsoft"  
[ReferenceWin3208190Iwebview2containsfullscreenelementchangedeventhandler]: ./reference/win32/0-8-190/iwebview2containsfullscreenelementchangedeventhandler.md "интерфейс IWebView2ContainsFullScreenElementChangedEventHandler | Документы Microsoft"  
[ReferenceWin3208190Iwebview2settings2PutAredefaultcontextmenusenabled]: ./reference/win32/0-8-190/iwebview2settings2.md#put_aredefaultcontextmenusenabled "put_AreDefaultContextMenusEnabled-интерфейс IWebView2Settings2 | Документы Microsoft"  
[ReferenceWin3208190Iwebview2settingsGetIsfullscreenallowedDeprecated]: ./reference/win32/0-8-190/iwebview2settings.md#get_isfullscreenallowed_deprecated "get_IsFullscreenAllowed_deprecated-интерфейс IWebView2Settings | Документы Microsoft"  
[ReferenceWin3208190Iwebview2webmessagereceivedeventargsGetWebmessageasstring]: ./reference/win32/0-8-190/iwebview2webmessagereceivedeventargs.md#get_webmessageasstring "get_WebMessageAsString-интерфейс IWebView2WebMessageReceivedEventArgs | Документы Microsoft"  
[ReferenceWin3208190Iwebview2webview4AddAcceleratorkeypressed]: ./reference/win32/0-8-190/iwebview2webview4.md#add_acceleratorkeypressed "add_AcceleratorKeyPressed-интерфейс IWebView2WebView4 | Документы Microsoft"  
[ReferenceWin3208190Iwebview2webviewAddDocumentstatechanged]: ./reference/win32/0-8-190/iwebview2webview.md#add_documentstatechanged "add_DocumentStateChanged-интерфейс IWebView2WebView | Документы Microsoft"  
[ReferenceWin3208190Iwebview2webview4Addremoteobject]: ./reference/win32/0-8-190/iwebview2webview4.md#addremoteobject "AddRemoteObject-Interface IWebView2WebView4 | Документы Microsoft"  
[ReferenceWin3208190Iwebview2webview5AddWebresourcerequested]: ./reference/win32/0-8-190/iwebview2webview5.md#add_webresourcerequested "add_WebResourceRequested-интерфейс IWebView2WebView5 | Документы Microsoft"  
[ReferenceWin3208190Iwebview2webview5Addwebresourcerequestedfilter]: ./reference/win32/0-8-190/iwebview2webview5.md#addwebresourcerequestedfilter "AddWebResourceRequestedFilter-Interface IWebView2WebView5 | Документы Microsoft"  
[ReferenceWin3208190Iwebview2webview5GetContainsfullscreenelement]: ./reference/win32/0-8-190/iwebview2webview5.md#get_containsfullscreenelement "get_ContainsFullScreenElement-интерфейс IWebView2WebView5 | Документы Microsoft"  
[ReferenceWin3208190Iwebview2webview5Removewebresourcerequestedfilter]: ./reference/win32/0-8-190/iwebview2webview5.md#removewebresourcerequestedfilter "RemoveWebResourceRequestedFilter-Interface IWebView2WebView5 | Документы Microsoft"  
[ReferenceWin3208190WebView2IdlCreatewebview2environmentwithdetails]:  ./reference/win32/0-8-190/webview2-idl.md#createwebview2environmentwithdetails "CreateWebView2EnvironmentWithDetails-Globals | Документы Microsoft"  

[ReferenceWin3209430Icorewebview2]: ./reference/win32/0-9-430/icorewebview2.md "интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2acceleratorkeypressedeventargsGetHandled]: ./reference/win32/0-9-430/icorewebview2acceleratorkeypressedeventargs.md#get_handled "get_Handled-интерфейс ICoreWebView2AcceleratorKeyPressedEventArgs | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2AddContentloading]: ./reference/win32/0-9-430/icorewebview2.md#add_contentloading "add_ContentLoading-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2AddHistorychanged]: ./reference/win32/0-9-430/icorewebview2.md#add_historychanged "add_HistoryChanged-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2Addremoteobject]: ./reference/win32/0-9-430/icorewebview2.md#addremoteobject "AddRemoteObject-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2AddSourcechanged]: ./reference/win32/0-9-430/icorewebview2.md#add_sourcechanged "add_SourceChanged-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2AddWindowcloserequested]: ./reference/win32/0-9-430/icorewebview2.md#add_windowcloserequested "add_WindowCloseRequested-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2CoreWebview2ScriptDialogKind]: ./reference/win32/0-9-430/icorewebview2.md#core_webview2_script_dialog_kind "CORE_WEBVIEW2_SCRIPT_DIALOG_KIND-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiver]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md "интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverAddDevtoolsprotocoleventreceived]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#add_devtoolsprotocoleventreceived "add_DevToolsProtocolEventReceived-интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2devtoolsprotocoleventreceiverRemoveDevtoolsprotocoleventreceived]: ./reference/win32/0-9-430/icorewebview2devtoolsprotocoleventreceiver.md#remove_devtoolsprotocoleventreceived "remove_DevToolsProtocolEventReceived-интерфейс ICoreWebView2DevToolsProtocolEventReceiver | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2environmentGetBrowserversioninfo]: ./reference/win32/0-9-430/icorewebview2environment.md#get_browserversioninfo "get_BrowserVersionInfo-интерфейс ICoreWebView2Environment | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2host]: ./reference/win32/0-9-430/icorewebview2host.md "интерфейс ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin3209430Webview2IdlGetcorewebview2browserversioninfo]: ./reference/win32/0-9-430/webview2-idl.md#getcorewebview2browserversioninfo "GetCoreWebView2BrowserVersionInfo-Globals | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2hostGetZoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#get_zoomfactor "get_ZoomFactor-интерфейс ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2hostNotifyparentwindowpositionchanged]: ./reference/win32/0-9-430/icorewebview2host.md#notifyparentwindowpositionchanged "NotifyParentWindowPositionChanged-Interface ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2hostPutZoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#put_zoomfactor "put_ZoomFactor-интерфейс ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2hostSetboundsandzoomfactor]: ./reference/win32/0-9-430/icorewebview2host.md#setboundsandzoomfactor "SetBoundsAndZoomFactor-Interface ICoreWebView2Host | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2httpheaderscollectioniteratorGetHascurrentheader]: ./reference/win32/0-9-430/icorewebview2httpheaderscollectioniterator.md#get_hascurrentheader "get_HasCurrentHeader-интерфейс ICoreWebView2HttpHeadersCollectionIterator | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2httprequestheadersGetheaders]: ./reference/win32/0-9-430/icorewebview2httprequestheaders.md#getheaders "Коголовки — интерфейс ICoreWebView2HttpRequestHeaders | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2httpresponseheadersGetheader]: ./reference/win32/0-9-430/icorewebview2httpresponseheaders.md#getheader "-Интерфейс ICoreWebView2HttpResponseHeaders | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2Removeremoteobject]: ./reference/win32/0-9-430/icorewebview2.md#removeremoteobject "RemoveRemoteObject-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2settingsGetAreremoteobjectsallowed]: ./reference/win32/0-9-430/icorewebview2settings.md#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-интерфейс ICoreWebView2Settings | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2settingsGetIszoomcontrolenabled]: ./reference/win32/0-9-430/icorewebview2settings.md#get_iszoomcontrolenabled "get_IsZoomControlEnabled-интерфейс ICoreWebView2Settings | Документы Microsoft"  
[ReferenceWin3209430Icorewebview2webmessagereceivedeventargsTrygetwebmessageasstring]: ./reference/win32/0-9-430/icorewebview2webmessagereceivedeventargs.md#trygetwebmessageasstring "TryGetWebMessageAsString-Interface ICoreWebView2WebMessageReceivedEventArgs | Документы Microsoft"  

[ReferenceWin3209488Icorewebview2AddFramenavigationcompleted]: ./reference/win32/0-9-488/icorewebview2.md#add_framenavigationcompleted "add_FrameNavigationCompleted-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209488Icorewebview2Addhostobjecttoscript]: ./reference/win32/0-9-488/icorewebview2.md#addhostobjecttoscript "AddHostObjectToScript-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209488Icorewebview2AddNewwindowrequested]: ./reference/win32/0-9-488/icorewebview2.md#add_newwindowrequested "add_NewWindowRequested-интерфейс ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209488Icorewebview2environmentGetBrowserversionstring]: ./reference/win32/0-9-488/icorewebview2environment.md#get_browserversionstring "| Документы Microsoft"  
[ReferenceWin3209488Icorewebview2environmentoptions]: ./reference/win32/0-9-488/icorewebview2environmentoptions.md "интерфейс ICoreWebView2EnvironmentOptions | Документы Microsoft"  
[ReferenceWin3209488Icorewebview2experimentalcompositioncontroller]: ./reference/win32/0-9-488/icorewebview2experimentalcompositioncontroller.md "интерфейс ICoreWebView2ExperimentalCompositionController | Документы Microsoft"  
[ReferenceWin3209488Icorewebview2experimentalcursorchangedeventhandler]: ./reference/win32/0-9-488/icorewebview2experimentalcursorchangedeventhandler.md "интерфейс ICoreWebView2ExperimentalCursorChangedEventHandler | Документы Microsoft"  
[ReferenceWin3209488Icorewebview2experimentalpointerinfo]: ./reference/win32/0-9-488/icorewebview2experimentalpointerinfo.md "интерфейс ICoreWebView2ExperimentalPointerInfo | Документы Microsoft"  
[ReferenceWin3209488Icorewebview2Removehostobjectfromscript]: ./reference/win32/0-9-488/icorewebview2.md#removehostobjectfromscript "RemoveHostObjectFromScript-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209488Icorewebview2settingsGetAreremoteobjectsallowed]: ./reference/win32/0-9-488/icorewebview2settings.md#get_areremoteobjectsallowed "get_AreRemoteObjectsAllowed-интерфейс ICoreWebView2Settings | Документы Microsoft"  
[ReferenceWin3209488Icorewebview2settingsGetIsbuiltinerrorpageenabled]: ./reference/win32/0-9-488/icorewebview2settings.md#get_isbuiltinerrorpageenabled "| Документы Microsoft"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithdetails]: ./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithdetails "CreateCoreWebView2EnvironmentWithDetails-Globals | Документы Microsoft"  
[ReferenceWin3209488Webview2IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Документы Microsoft"  
[ReferenceWin3209488Webview2IdlGetavailablecorewebview2browserversionstring]: ./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring "GetAvailableCoreWebView2BrowserVersionString-Globals | Документы Microsoft"  

[ReferenceDotnet09515Reference]: ./reference/dotnet/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWinforms09515Reference]: ./reference/winforms/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWpf09515Reference]: ./reference/wpf/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  

[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environment]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md "Класс Microsoft. Web. WebView2. Core. CoreWebView2Environment | Документы Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentComparebrowserversions]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#comparebrowserversions "Класс CompareBrowserVersions-Microsoft. Web. WebView2. Core. CoreWebView2Environment | Документы Microsoft"
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2environmentGetavailablebrowserversionstring]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2environment.md#getavailablebrowserversionstring "Класс GetAvailableBrowserVersionString-Microsoft. Web. WebView2. Core. CoreWebView2Environment | Документы Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Newwindowrequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#newwindowrequested "Класс NewWindowRequested-Microsoft. Web. WebView2. Core. CoreWebView2 | Документы Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Permissionrequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#permissionrequested "Класс PermissionRequested-Microsoft. Web. WebView2. Core. CoreWebView2 | Документы Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Scriptdialogopening]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#scriptdialogopening "Класс ScriptDialogOpening-Microsoft. Web. WebView2. Core. CoreWebView2 | Документы Microsoft"  
[ReferenceDotnet09538MicrosoftWebWebview2CoreCorewebview2Webresourcerequested]: ./reference/dotnet/0-9-538/microsoft-web-webview2-core-corewebview2.md#webresourcerequested "Класс WebResourceRequested-Microsoft. Web. WebView2. Core. CoreWebView2 | Документы Microsoft"  
[ReferenceWin3209538Icorewebview2Addhostobjecttoscript]: ./reference/win32/0-9-538/icorewebview2.md#addhostobjecttoscript "AddHostObjectToScript-Interface ICoreWebView2 | Документы Microsoft"  
[ReferenceWin3209538Icorewebview2experimentalnewwindowrequestedeventargsGetWindowfeatures]: ./reference/win32/0-9-538/icorewebview2experimentalnewwindowrequestedeventargs.md#get_windowfeatures "get_WindowFeatures-интерфейс ICoreWebView2ExperimentalNewWindowRequestedEventArgs | Документы Microsoft"  
[ReferenceWin3209538Icorewebview2experimentalwindowfeatures]: ./reference/win32/0-9-538/icorewebview2experimentalwindowfeatures.md "интерфейс ICoreWebView2ExperimentalWindowFeatures | Документы Microsoft"  
[ReferenceWin3209538Icorewebview2settingsGetArehostobjectsallowed]: ./reference/win32/0-9-538/icorewebview2settings.md#get_arehostobjectsallowed "get_AreHostObjectsAllowed-интерфейс ICoreWebView2Settings | Документы Microsoft"  
[ReferenceWin3209538Webview2IdlCreatecorewebview2environmentwithoptions]: ./reference/win32/0-9-538/webview2-idl.md#createcorewebview2environmentwithoptions "CreateCoreWebView2EnvironmentWithOptions-Globals | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackIssue1]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/1 "Репозиторий отзывов для MicrosoftEdge и WebViewFeedback, выпуска 1"  
[GithubMicrosoftedgeWebviewfeedbackIssue12]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/12 "Репозиторий отзывов для MicrosoftEdge и WebViewFeedback, выпуска 12"  
[GithubMicrosoftedgeWebviewfeedbackIssue13]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/13 "Вопрос в репозитории отзыва для MicrosoftEdge и WebViewFeedback 13"  
[GithubMicrosoftedgeWebviewfeedbackIssue14]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/14 "Вопрос в репозитории отзыва для MicrosoftEdge и WebViewFeedback 14"  
[GithubMicrosoftedgeWebviewfeedbackIssue16]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/16 "MicrosoftEdge/WebViewFeedback, подающий отзыв"  
[GithubMicrosoftedgeWebviewfeedbackIssue17]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/17 "Вопрос в репозитории отзывов о MicrosoftEdge/WebViewFeedback 17"  
[GithubMicrosoftedgeWebviewfeedbackIssue18]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/18 "Репозиторий отзывов для MicrosoftEdge/WebViewFeedback, выпуска 18"  
[GithubMicrosoftedgeWebviewfeedbackIssue19]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/19 "Репозиторий отзывов для MicrosoftEdge и WebViewFeedback, выпуска 19"  
[GithubMicrosoftedgeWebviewfeedbackIssue22]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/22 "Вопрос в репозитории отзыва для MicrosoftEdge и WebViewFeedback 22"  
[GithubMicrosoftedgeWebviewfeedbackIssue27]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/27 "Репозиторий отзывов для MicrosoftEdge/WebViewFeedback, выпуска 27"  
[GithubMicrosoftedgeWebviewfeedbackIssue28]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/28 "MicrosoftEdge/WebViewFeedback в репозитории обратной связи 28"  
[GithubMicrosoftedgeWebviewfeedbackIssue30]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/30 "MicrosoftEdgeный и WebViewFeedbackный репозиторий в виде обратной связи 30"  
[GithubMicrosoftedgeWebviewfeedbackIssue32]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/32 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 32"  
[GithubMicrosoftedgeWebviewfeedbackIssue36]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/36 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 36"  
[GithubMicrosoftedgeWebviewfeedbackIssue57]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/57 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 57"  
[GithubMicrosoftedgeWebviewfeedbackIssue70]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/70 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 70"  
[GithubMicrosoftedgeWebviewfeedbackIssue74]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/74 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 74"  
[GithubMicrosoftedgeWebviewfeedbackIssue95]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/95 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 95"  
[GithubMicrosoftedgeWebviewfeedbackIssue108]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/108 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 108"  
[GithubMicrosoftedgeWebviewfeedbackIssue113]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/113 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 113"  
[GithubMicrosoftedgeWebviewfeedbackIssue119]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/119 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 119" 
[GithubMicrosoftedgeWebviewfeedbackIssue148]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/148 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 148"  
[GithubMicrosoftedgeWebviewfeedbackIssue179]:  https://github.com/MicrosoftEdge/WebViewFeedback/issues/179 "Репозиторий отзывов о MicrosoftEdgeах и WebViewFeedback проблемах с 179"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesPr17]: https://github.com/MicrosoftEdge/WebView2Samples/pull/17 "Перемещение проекта для использования новейшего WebView2 SDK 0.9.430-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebview2samplesApisample]: https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample "Образец API WebView2-MicrosoftEdge/WebView2Samples | GitHub"  

[NuGetGallery]:  https://www.nuget.org/packages/Microsoft.Web.WebView2 "Коллекция NuGet | Microsoft. Web. WebView2"  
[NuGetGallery0.8.149]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.149 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.149"  
[NuGetGallery0.8.190]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.190 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.190"  
[NuGetGallery0.8.230]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.230 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.230"  
[NuGetGallery0.8.270]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.270 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.270"  
[NuGetGallery0.8.314]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.314 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.314"  
[NuGetGallery0.8.355]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.8.355 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.8.355"  
[NuGetGallery0.9.430]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.430 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.430"  
[NuGetGallery0.9.488]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.488 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.488"  
[NuGetGallery0.9.515-prerelease]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.515-prerelease "Коллекция NuGet | Предварительная версия Microsoft. Web. WebView2 v 0.9.515"  
[NuGetGallery0.9.538]:  https://www.nuget.org/packages/Microsoft.Web.WebView2/0.9.538 "Коллекция NuGet | Microsoft. Web. WebView2 v 0.9.538"  
