---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: ca31ddd3536350d3b3bdd02b445b4c47589f7dba
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011113"
---
# класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft.Web.WebView2.Core.dll

WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[BrowserProcessId](#browserprocessid) | Идентификатор процесса браузера, на котором размещается WebView.
[CanGoBack](#cangoback) | Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.
[CanGoForward](#cangoforward) | Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.
[ContainsFullScreenElement](#containsfullscreenelement) | Указывает, содержит ли WebView элемент HTML на весь экран.
[ContainsFullScreenElementChanged](#containsfullscreenelementchanged) | Уведомляет об изменении свойства ContainsFullScreenElement.
[ContentLoading](#contentloading) | ContentLoading срабатывает перед загрузкой содержимого, в том числе сценариев, добавленных с помощью AddScriptToExecuteOnDocumentCreated ContentLoading, не будет срабатывать при выполнении одной навигации по страницам (например, с помощью навигации фрагментов или журнала. pushState навигации).
[DocumentTitle](#documenttitle) | Название текущего документа верхнего уровня.
[DocumentTitleChanged](#documenttitlechanged) | Событие активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.
[FrameNavigationCompleted](#framenavigationcompleted) | Событие FrameNavigationCompleted вызывается, когда дочерний кадр полностью загружен (Body. onload) или загрузка остановлена с ошибкой.
[FrameNavigationStarting](#framenavigationstarting) | FrameNavigationStarting активируется, когда дочерний кадр в WebView, запрашивающий разрешение на переход к другому URI.
[HistoryChanged](#historychanged) | Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.
[NavigationCompleted](#navigationcompleted) | Событие NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.
[NavigationStarting](#navigationstarting) | NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI.
[NewWindowRequested](#newwindowrequested) | Вызывается, когда содержимое в WebView запросило открыть новое окно, например с помощью Window. Open.
[PermissionRequested](#permissionrequested) | Вызывается, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.
[ProcessFailed](#processfailed) | Активируется, когда WebView процесс неожиданно завершился или перестал отвечать на запросы.
[ScriptDialogOpening](#scriptdialogopening) | Событие активируется, когда диалоговое окно JavaScript (предупреждение, подтверждение или запрос) будет отображаться для WebView.
[Параметры](#settings) | Объект CoreWebView2Settings, содержащий различные изменяемые параметры для выполняющегося
[Источник](#source) | Универсальный код ресурса (URI) текущего документа верхнего уровня.
[SourceChanged](#sourcechanged) | SourceChanged активируется при изменении свойства Source.
[WebMessageReceived](#webmessagereceived) | Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .
[WebResourceRequested](#webresourcerequested) | Активируется, когда WebView выполняет запрос HTTP к соответствующему URL-адресу и фильтру контекста ресурсов, добавленному с помощью AddWebResourceRequestedFilter.
[WebResourceResponseReceived](#webresourceresponsereceived) | Событие WebResourceResponseReceived срабатывает после того, как WebView получил и обработал ответ для запроса на веб-ресурс.
[WindowCloseRequested](#windowcloserequested) | Вызывается, когда содержимое в WebView запрашивает закрытие окна, например после вызова Window. Close.
[AddHostObjectToScript](#addhostobjecttoscript) | Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.
[AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync) | Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.
[CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync) | Вызовите асинхронный метод DevToolsProtocol.
[CapturePreviewAsync](#capturepreviewasync) | Запишите изображение того, что WebView на экране.
[ExecuteScriptAsync](#executescriptasync) | Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.
[GoBack](#goback) | Переход по WebView на предыдущую страницу в истории навигации.
[GoForward](#goforward) | Переход по WebView к следующей странице в истории навигации.
[Которому](#navigate) | Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).
[NavigateToString](#navigatetostring) | Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.
[OpenDevToolsWindow](#opendevtoolswindow) | Открытие окна DevTools для текущего документа в WebView.
[PostWebMessageAsJson](#postwebmessageasjson) | Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.
[Перезагрузить](#reload) | Перезагрузите текущую страницу.
[RemoveHostObjectFromScript](#removehostobjectfromscript) | Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated с указанным идентификатором сценария.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.
[Stop](#stop) | Остановите все переходы и ожидающие выборки ресурсов.

## Участников

#### BrowserProcessId 

Идентификатор процесса браузера, на котором размещается WebView.

> Открытый uint [BrowserProcessId](#browserprocessid)

#### CanGoBack 

Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.

> Открытый логический [CanGoBack](#cangoback)

Событие HistoryChanged будет срабатывать, если CanGoBack изменит значение.

#### CanGoForward 

Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.

> Открытый логический [CanGoForward](#cangoforward)

Событие HistoryChanged будет срабатывать, если CanGoForward изменит значение.

#### ContainsFullScreenElement 

Указывает, содержит ли WebView элемент HTML на весь экран.

> Открытый логический [ContainsFullScreenElement](#containsfullscreenelement)

#### ContainsFullScreenElementChanged 

Уведомляет об изменении свойства ContainsFullScreenElement.

> событие EventHandler< объект > [ContainsFullScreenElementChanged](#containsfullscreenelementchanged)

Это означает, что HTML-элемент, находящиеся внутри WebView, помещается на размер WebView или выходит за экран. Это событие полезно, если, например, элемент видео запрашивается на весь экран. Прослушиватель ContainsFullScreenElementChanged может затем изменить размер WebView в ответе.

#### ContentLoading 

ContentLoading срабатывает перед загрузкой содержимого, в том числе сценариев, добавленных с помощью AddScriptToExecuteOnDocumentCreated ContentLoading, не будет срабатывать при выполнении одной навигации по страницам (например, с помощью навигации фрагментов или журнала. pushState навигации).

> событие EventHandler< [CoreWebView2ContentLoadingEventArgs](microsoft-web-webview2-core-corewebview2contentloadingeventargs.md)  >  [ContentLoading](#contentloading)

Это следует за событиями NavigationStarting и SourceChanged и предшествовать событиям HistoryChanged и NavigationCompleted.

#### DocumentTitle 

Название текущего документа верхнего уровня.

> общедоступная строка [DocumentTitle](#documenttitle)

Если документ не имеет явного заголовка или не является пустым, используется значение по умолчанию, которое может быть или не совпадать с URI документа.

#### DocumentTitleChanged 

Событие активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.

> событие EventHandler< объект > [DocumentTitleChanged](#documenttitlechanged)

#### FrameNavigationCompleted 

Событие FrameNavigationCompleted вызывается, когда дочерний кадр полностью загружен (Body. onload) или загрузка остановлена с ошибкой.

> событие EventHandler< [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [FrameNavigationCompleted](#framenavigationcompleted)

#### FrameNavigationStarting 

FrameNavigationStarting активируется, когда дочерний кадр в WebView, запрашивающий разрешение на переход к другому URI.

> событие EventHandler< [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [FrameNavigationStarting](#framenavigationstarting)

Это будет срабатывать и для перенаправления.

#### HistoryChanged 

Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.

> событие EventHandler< объект > [HistoryChanged](#historychanged)

Используйте Счетовизменение сведений об, чтобы проверить, изменилось ли значение CanGoBack/CanGoForward. HistoryChanged также срабатывает для использования GoBack и GoForward. HistoryChanged срабатывает после SourceChanged и ContentLoading. Добавьте обработчик событий для события HistoryChanged.

#### NavigationCompleted 

Событие NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.

> событие EventHandler< [CoreWebView2NavigationCompletedEventArgs](microsoft-web-webview2-core-corewebview2navigationcompletedeventargs.md)  >  [NavigationCompleted](#navigationcompleted)

#### NavigationStarting 

NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI.

> событие EventHandler< [CoreWebView2NavigationStartingEventArgs](microsoft-web-webview2-core-corewebview2navigationstartingeventargs.md)  >  [NavigationStarting](#navigationstarting)

Это будет срабатывать и для перенаправления.

#### NewWindowRequested 

Вызывается, когда содержимое в WebView запросило открыть новое окно, например с помощью Window. Open.

> событие EventHandler< [CoreWebView2NewWindowRequestedEventArgs](microsoft-web-webview2-core-corewebview2newwindowrequestedeventargs.md)  >  [NewWindowRequested](#newwindowrequested)

Приложение может передавать целевую WebView, которая будет считаться открытым окном.

#### PermissionRequested 

Вызывается, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.

> событие EventHandler< [CoreWebView2PermissionRequestedEventArgs](microsoft-web-webview2-core-corewebview2permissionrequestedeventargs.md)  >  [PermissionRequested](#permissionrequested)

#### ProcessFailed 

Активируется, когда WebView процесс неожиданно завершился или перестал отвечать на запросы.

> событие EventHandler< [CoreWebView2ProcessFailedEventArgs](microsoft-web-webview2-core-corewebview2processfailedeventargs.md)  >  [ProcessFailed](#processfailed)

#### ScriptDialogOpening 

Событие активируется, когда диалоговое окно JavaScript (предупреждение, подтверждение или запрос) будет отображаться для WebView.

> событие EventHandler< [CoreWebView2ScriptDialogOpeningEventArgs](microsoft-web-webview2-core-corewebview2scriptdialogopeningeventargs.md)  >  [ScriptDialogOpening](#scriptdialogopening)

Это событие срабатывает только в том случае, если свойство CoreWebView2Settings. AreDefaultScriptDialogsEnabled имеет значение false. Событие ScriptDialogOpening можно использовать, чтобы подавить диалоговые окна или заменить диалоговые окна по умолчанию пользовательскими диалоговыми окноми.

#### Параметры 

Объект CoreWebView2Settings, содержащий различные изменяемые параметры для выполняющегося

> общедоступные [Параметры](#settings) [CoreWebView2Settings](microsoft-web-webview2-core-corewebview2settings.md)

#### Источник 

Универсальный код ресурса (URI) текущего документа верхнего уровня.

> [источник](#source) общедоступной строки

Это значение может изменяться в рамках обработки события SourceChanged в некоторых случаях, например при переходе к другому сайту или для навигации по фрагменту. Оно останется прежним для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.

#### SourceChanged 

SourceChanged активируется при изменении свойства Source.

> событие EventHandler< [CoreWebView2SourceChangedEventArgs](microsoft-web-webview2-core-corewebview2sourcechangedeventargs.md)  >  [SourceChanged](#sourcechanged)

SourceChanged срабатывает для переходов на другой сайт или элементы навигации фрагментов. Она не будет срабатывать для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы. SourceChanged срабатывает перед ContentLoading для перехода к новому документу. Добавьте обработчик событий для события SourceChanged.

#### WebMessageReceived 

Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .

> событие EventHandler< [CoreWebView2WebMessageReceivedEventArgs](microsoft-web-webview2-core-corewebview2webmessagereceivedeventargs.md)  >  [WebMessageReceived](#webmessagereceived)

Функция i, в `void postMessage(object)` которой объект — это любой объект, поддерживаемый преобразованием JSON. При вызове CoreWebView2WebMessageReceivedEventHandler набор будет вызван с параметром объекта i, преобразованным в строку JSON.

#### WebResourceRequested 

Активируется, когда WebView выполняет запрос HTTP к соответствующему URL-адресу и фильтру контекста ресурсов, добавленному с помощью AddWebResourceRequestedFilter.

> событие EventHandler< [CoreWebView2WebResourceRequestedEventArgs](microsoft-web-webview2-core-corewebview2webresourcerequestedeventargs.md)  >  [WebResourceRequested](#webresourcerequested)

Для срабатывания события необходимо добавить хотя бы один фильтр.

#### WebResourceResponseReceived 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Событие WebResourceResponseReceived срабатывает после того, как WebView получил и обработал ответ для запроса на веб-ресурс.

> событие EventHandler< [CoreWebView2WebResourceResponseReceivedEventArgs](microsoft-web-webview2-core-corewebview2webresourceresponsereceivedeventargs.md)  >  [WebResourceResponseReceived](#webresourceresponsereceived)

Аргументы события включают в себя WebResourceRequest, отправленный по каналу и WebResourceResponse, включая все дополнительные заголовки, добавленные сетевым стеком, которые не были включены как часть связанного события WebResourceRequested, например заголовки проверки подлинности.

#### WindowCloseRequested 

Вызывается, когда содержимое в WebView запрашивает закрытие окна, например после вызова Window. Close.

> событие EventHandler< объект > [WindowCloseRequested](#windowcloserequested)

Приложение должно закрыть окно WebView и связанное приложение, если это понятно приложению.

#### AddHostObjectToScript 

Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.

> Public void [AddHostObjectToScript](#addhostobjecttoscript)(строковое имя, объект rawObject)

Объекты узла предоставляются как прокси объекта hosts через `window.chrome.webview.hostObjects.{name}` . Прокси-серверы объектов являются обещанными и разрешаются в объект, представляющий объект Host. Код JavaScript в WebView сможет получить доступ к appObject следующим образом, а затем получить доступ к атрибутам и методам appObject: 
```
let app_object = await window.chrome.webview.hostObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```
 Обратите внимание, что хотя простые типы, IDispatch и Array поддерживаются, универсальный IUnknown, VT_DECIMAL или VT_RECORD Variant не поддерживается. Удаленные объекты JavaScript, такие как функции обратного вызова, представлены как VT_DISPATCH VARIANT с помощью объекта, реализующего IDispatch. Метод обратного вызова JavaScript можно вызвать с помощью DISPID_VALUE для DISPID. Вложенные массивы поддерживаются до 3 уровней. Массивы по типам ссылок не поддерживаются. VT_EMPTY и VT_NULL сопоставлены в JavaScript как null. В JavaScript NULL и undefine сопоставляются с VT_EMPTY.

Кроме того, все объекты узла предоставляются как `window.chrome.webview.hostObjects.sync.{name}` . Здесь объекты узла предоставляются как синхронные прокси объектов узла. Эти функции не предназначены для того, чтобы синхронно блокировать выполняемые сценарии, ожидающие общения для запуска кода хоста. Таким образом, это может привести к проблемам с надежностью, поэтому рекомендуется использовать асинхронный API на основе Promise, `window.chrome.webview.hostObjects.{name}` описанный выше.

Синхронные прокси-серверы узлов и асинхронные прокси объектов узла могут обоим образом доявляться прокси для одного и того же объекта узла. Удаленные изменения, внесенные одним прокси-сервером, будут отражаться на любом другом прокси того же объекта узла, независимо от того, являются ли они другими прокси-объектами, синхронными или асинхронными.

Несмотря на то, что JavaScript блокируется на синхронный вызов машинного кода, этот машинный код не может снова вызвать JavaScript. При попытке выполнить это действие произойдет сбой с HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Прокси объектов узла — это прокси-объекты JavaScript, которые перехватывают все вызовы свойств Get, Set и Method. Свойства или методы, которые являются частью прототипа функции или объекта, выполняются локально. Кроме того, любое свойство или метод в массиве `chrome.webview.hostObjects.options.forceLocalProperties` также будет выполняться локально. Эти значения по умолчанию включают в себя дополнительные методы, которые имеют значение в JavaScript Like `toJSON` и `Symbol.toPrimitive` . При необходимости вы можете добавить в этот массив дополнительные сведения.

Существует метод `chrome.webview.hostObjects.cleanupSome` , который наилучшим способом является сбор прокси объектов хоста сборщиком мусора.

Прокси-серверы узла дополнительно обладают следующими методами, которые выполняются локально.

* applyHostFunction, getHostProperty, setHostProperty: выполняйте вызов метода, свойство get или свойство Set для объекта Host. Вы можете использовать их, чтобы явным образом запускать метод или свойство, если существует конфликтующий локальный метод или свойство. Например, `proxy.toString()` будет выполнен локальный метод ToString для прокси-объекта. Но `proxy.applyHostFunction('toString')` выполняется `toString` вместо объекта прокси-сервера узла.

* getLocalProperty, setLocalProperty: выполнение свойства Get или установка свойства локально. Эти методы можно использовать, чтобы принудительно получить или задать свойство для прокси объекта основного приложения, а не для объекта узла, который он представляет. Например, `proxy.unknownProperty` будет получено свойство с именем `unknownProperty` из объекта прокси-сервера узла. Но `proxy.getLocalProperty('unknownProperty')` будет получить значение свойства `unknownProperty` для самого объекта прокси.

* Sync: асинхронные прокси-серверы узлов предоставляют метод Sync, возвращающий обещание для прокси объекта хоста синхронный для одного и того же объекта узла. Например, `chrome.webview.hostObjects.sample.methodCall()` возвращает асинхронный прокси объекта хоста. Вы можете использовать этот `sync` метод, чтобы получить для него синхронный прокси-сервер объекта узла: `const syncProxy = await chrome.webview.hostObjects.sample.methodCall().sync()`

* Async: синхронные прокси-серверы узлов предоставляют асинхронный метод, который блокирует и возвращает асинхронный прокси объекта хоста для одного и того же объекта узла. Например, `chrome.webview.hostObjects.sync.sample.methodCall()` возвращает синхронный прокси объекта узла. Вызов `async` метода на этих блоках и возврат прокси-сервера асинхронного объекта узла для того же объекта узла: `const asyncProxy = chrome.webview.hostObjects.sync.sample.methodCall().async()`

* затем: асинхронные прокси-объекты узла имеют метод then. Это позволит им доставлять ожидающие. `then` будет возвращать обещание, которое разрешается с представлением объекта Host. Если прокси представляет литерал JavaScript, то копия, возвращаемая им, будет возвращена локально. Если прокси представляет функцию, возвращается прокси-сервер, не ожидающий ожидания. Если прокси представляет объект JavaScript с сочетанием литеральных свойств и свойств функций, то копия объекта возвращается с некоторыми свойствами в качестве прокси объектов Host.

Все другие вызовы свойств и методов (Кроме описанных выше методов прокси-сервера удаленного объекта, списка forceLocalProperties и свойств прототипов функций и объектов) выполняются удаленно. Асинхронные прокси-объекты узла возвращают обещание, представляющее собой асинхронное завершение удаленного вызова метода или получение свойства. Обещание устраняется после завершения удаленных операций, и обещание разрешается в полученное значение операции. Синхронные прокси объекта узла работают одинаково, но блокируют выполнение JavaScript и дождитесь завершения удаленной операции.

Установка свойства для прокси-сервера асинхронного узла выполняется немного по-другому. Функция Set возвращает значение немедленно и возвращаемое значение является значением, которое будет задано. Это требование для прокси-объекта JavaScript. Если необходимо асинхронно дождаться завершения установки свойства, используйте метод setHostProperty, который возвращает обещание, как описано выше. Синхронно заданное свойство свойства объекта для синхронно блокируется, пока не задано свойство.

#### AddScriptToExecuteOnDocumentCreatedAsync 

Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.

> общедоступная асинхронная задача< String > [AddScriptToExecuteOnDocumentCreatedAsync](#addscripttoexecuteondocumentcreatedasync)(String JavaScript)

##### Дает
Возвращает ИД сценария, который можно передать при вызове [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated). 

Вставленный сценарий будет применяться ко всем документам верхнего уровня и дочерним элементам навигации, пока они не будут удалены с помощью RemoveScriptToExecuteOnDocumentCreated. Это применяется асинхронно, и вы должны дождаться выполнения обработчика завершения, прежде чем можно будет убедиться, что сценарий готов к выполнению для навигации в будущем.

Обратите внимание, что если в HTML-документе есть изолированная [Среда с определенными свойствами или](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [заголовок HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , это повлияет на выполнение сценария. Таким образом, например, если ключевое слово "Allow-Modal" не задано, вызовы `alert` функции будут игнорироваться.

#### AddWebResourceRequestedFilter 

Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.

> Public void [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(строковый URI, CoreWebView2WebResourceContext разделе ResourceContext)

Параметр URI может быть строкой с подстановочными знаками ("": ноль или больше; "?": только один). nullptr эквивалентен L "". Описание фильтров контекста ресурсов приведено в перечислении CoreWebView2WebResourceContext.

#### CallDevToolsProtocolMethodAsync 

Вызовите асинхронный метод DevToolsProtocol.

> общедоступная асинхронная задача< String > [CallDevToolsProtocolMethodAsync](#calldevtoolsprotocolmethodasync)(строка MethodName, String parametersAsJson)

##### Дает
Строка JSON, представляющая возвращаемый объект метода. 

Список и описание доступных методов можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) . Параметр methodName — это полное имя метода в формате `{domain}.{method}` . Параметр parametersAsJson является строкой в формате JSON, содержащей параметры соответствующего метода. Метод Invoke обработчика вызывается, когда метод асинхронно завершается. Вызов Invoke будет вызываться с возвращаемым методом объектом в виде строки JSON.

#### CapturePreviewAsync 

Запишите изображение того, что WebView на экране.

> Public async Task [CapturePreviewAsync](#capturepreviewasync)(CoreWebView2CapturePreviewImageFormat ImageFormat, Stream ImageStream)

Укажите формат изображения с помощью параметра imageFormat. Результирующие двоичные данные изображения записываются в указанный параметр imageStream. Когда CapturePreview закончит запись в поток, вызывается метод Invoke в указанном параметре обработчика.

#### ExecuteScriptAsync 

Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.

> общедоступная асинхронная задача< String > [ExecuteScriptAsync](#executescriptasync)(String JavaScript)

##### Дает
Возвращает строку в кодировке JSON, представляющую результат выполнения указанного кода JavaScript. 

Этот метод асинхронно запускает указанные сценарии JavaScript и возвращает результат указанного кода JavaScript. Если результат указанного в коде JavaScript `undefined` содержит цикл ссылки или не может быть закодирован в JSON, возвращается строка NULL. Если вызываемая функция в указанном коде JavaScript не имеет явного возвращаемого значения, `undefined` возвращается. Если в указанном коде JavaScript возникает неуправляемое исключение, возвращается значение null. Если этот метод вызывается после события NavigationStarting, то при загрузке в новом документе код JavaScript выполняется в то же время, в котором инициируется ContentLoading. ExecuteScriptAsync будет работать даже в том случае, если для IsScriptEnabled установлено значение `FALSE` .

#### GetDevToolsProtocolEventReceiver 

Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.

> общедоступная CoreWebView2DevToolsProtocolEventReceiver [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(строка с префиксом EventName)

Список и описание доступных методов можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) . Параметр methodName — это полное имя метода в формате `{domain}.{method}` . Параметр parametersAsJson является строкой в формате JSON, содержащей параметры соответствующего метода. Метод Invoke обработчика вызывается, когда метод асинхронно завершается. Вызов Invoke будет вызываться с возвращаемым методом объектом в виде строки JSON.

#### GoBack 

Переход по WebView на предыдущую страницу в истории навигации.

> общедоступная void [GoBack](#goback)()

#### GoForward 

Переход по WebView к следующей странице в истории навигации.

> общедоступная void [GoForward](#goforward)()

#### Которому 

Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).

> Открытый void [navigate](#navigate)(строковый URI)

Дополнительные сведения приведены в разделе события навигации. Обратите внимание, что при этом начинается переход и соответствующее событие NavigationStarting будет срабатывать после завершения этого вызова навигации.

#### NavigateToString 

Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.

> Public void [NavigateToString](#navigatetostring)(строка htmlContent)

Параметр htmlContent не может быть больше 2 МБ символов. В качестве источника новой страницы будет указано пустое значение.

#### OpenDevToolsWindow 

Открытие окна DevTools для текущего документа в WebView.

> общедоступная void [OpenDevToolsWindow](#opendevtoolswindow)()

Ничего не происходит, если он вызывается, когда окно DevTools уже открыто.

#### PostWebMessageAsJson 

Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.

> Public void [PostWebMessageAsJson](#postwebmessageasjson)(строка webMessageAsJson)

Срабатывает событие Window. Chrome. WebView для документа верхнего уровня. JavaScript в этом документе может подписываться на событие и отменять подписку с помощью следующих действий:

```
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

Аргументы события представляют собой экземпляр `MessageEvent` . Параметр CoreWebView2Settings. IsWebMessageEnabled должен быть истинным, или этот метод завершится сбоем с E_INVALIDARG. Свойство данных аргумента "событие" — это строковый параметр веб-сообщения, проанализированный как строка JSON, в объект JavaScript. Свойство Source аргумента "событие" является ссылкой на `window.chrome.webview` объект. Сведения о том, как отправлять сообщения из HTML-документа на WebView на узел, можно найти в SetWebMessageReceivedEventHandler. Это сообщение отправляется асинхронно. Если переход выполняется до того, как сообщение будет отправлено на страницу, оно не будет отправлено.

#### PostWebMessageAsString 

Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.

> Public void [PostWebMessageAsString](#postwebmessageasstring)(строка webMessageAsString)

Это выполняется точно так же, как и PostWebMessageAsJson, но `window.chrome.webview` свойство Data события ARG имеет строковое значение с тем же значением, что и webMessageAsString. Используйте это вместо PostWebMessageAsJson, если вы хотите общаться с помощью простых строк, а не объектов JSON.

#### Перезагрузить 

Перезагрузите текущую страницу.

> общедоступный void [Reload](#reload)()

Это похоже на то, что переход к URI текущего документа верхнего уровня, включая все события навигации, которые обрабатывались, и учитывает любые записи в кэше HTTP. Но история «назад» и «вперед» не будет изменена.

#### RemoveHostObjectFromScript 

Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.

> общедоступная void [RemoveHostObjectFromScript](#removehostobjectfromscript)(строковое имя)

Несмотря на то что новые попытки доступа будут отвергнуты, если объект уже получен кодом JavaScript в WebView, код JavaScript продолжит получать доступ к этому объекту. Вызов этого метода для имени, которое уже удалено или не было добавлено, завершается сбоем.

#### RemoveScriptToExecuteOnDocumentCreated 

Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated с указанным идентификатором сценария.

> Public void [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(идентификатор строки)

#### RemoveWebResourceRequestedFilter 

Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.

> Public void [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(строковый URI, [CoreWebView2WebResourceContext](./namespace-microsoft-web-webview2-core.md) разделе ResourceContext)

Если один и тот же фильтр был добавлен несколько значений, его необходимо будет удалить столько, сколько вхождений было добавлено для эффективного. Возвращает E_INVALIDARG для фильтра, который еще не был добавлен.

#### Stop 

Остановите все переходы и ожидающие выборки ресурсов.

> открытая пустая [Отмена](#stop)()

Не останавливает сценарии.

