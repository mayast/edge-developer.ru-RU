---
description: Размещение веб-содержимого в приложении для Windows 10 с помощью элемента управления WebView (EdgeHTML)
title: Microsoft Edge WebView для приложений для Windows 10
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: приложения x-MS-WebView, MSHTMLWebViewElement, WebView, Windows 10, UWP, EDGE
ms.openlocfilehash: aa9bef7bf214cf4f4ffdb4d68ad3a1a86ac2977b
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752208"
---
# WebView (EdgeHTML) для приложений для Windows 10  

[!INCLUDE [deprecation-note](./includes/deprecation-note.md)]  

Элемент управления WebView (EdgeHTML) позволяет размещать веб-содержимое в приложении для Windows 10.  

Его можно использовать в качестве элемента XAML (для приложений [универсальной платформы Windows (UWP)](/uwp/api/Windows.UI.Xaml.Controls.WebView) , [Windows Forms и классических приложений WPF](/windows/communitytoolkit/controls/wpf-winforms/webview)) либо HTML-элемента (x-MS-WebView)/DOM (MSHTMLWebViewElement) для приложений на базе Windows 10 на основе JavaScript, как описано здесь.  

|  |  |  
|:--- |:--- |  
| [**Мероприятия**](#events) | [departingFocus](#departingfocus), [MSWebViewContainsFullScreenElementChanged](#mswebviewcontainsfullscreenelementchanged), [MSWebViewContentLoading](#mswebviewcontentloading), [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded), [MSWebViewFrameContentLoading](#mswebviewframecontentloading), [MSWebViewFrameDOMContentLoaded](#mswebviewframedomcontentloaded), [MSWebViewFrameNavigationCompleted](#mswebviewframenavigationcompleted), [MSWebViewFrameNavigationStarting](#mswebviewframenavigationstarting)и [MSWebViewLongRunningScriptDetected](#mswebviewlongrunningscriptdetected), [MSWebViewNavigationCompleted,](#mswebviewnavigationcompleted) [,](#mswebviewpermissionrequested) [, MSWebViewNavigationStarting](#mswebviewnavigationstarting) [, MSWebViewNewWindowRequested](#mswebviewnewwindowrequested)и [MSWebViewPermissionRequested](#mswebviewwebresourcerequested) [MSWebViewProcessExited](#mswebviewprocessexited) [MSWebViewScriptNotify](#mswebviewscriptnotify) [MSWebViewUnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying) [MSWebViewUnsupportedUriSchemeIdentified](#mswebviewunsupportedurischemeidentified) [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) |  
| [**Методы**](#methods) | [addWebAllowedObject](#addweballowedobject), [buildlocalStreamUri](#buildlocalstreamuri), [capturePreviewToBlobAsync](#capturepreviewtoblobasync), [captureSelectedContentToDataPackageAsync](#captureselectedcontenttodatapackageasync), [invokeScriptAsync](#invokescriptasync), [getDeferredPermissionRequests](#getdeferredpermissionrequests), [getDeferredPermissionRequestById](#getdeferredpermissionrequestbyid), [goBack](#goback), [goForward,](#goforward), [navigateFocus](#navigatefocus) [navigateFocus](#navigatewithhttprequestmessage), [navigateTolocalStreamUri,](#navigatetolocalstreamuri) [Обновить](#refresh), [остановить](#stop) [navigate](#navigate) [navigateToString](#navigatetostring) |  
| [**Свойства**](#properties) | [canGoBack](#cangoback), [canGoForward](#cangoforward), [containsFullScreenElement](#containsfullscreenelement), [DocumentTitle](#documenttitle), [Высота](#height), [процесс](#process), [Параметры](#settings), [src](#src), [Ширина](#width) |  

## Синтаксис  

```javascript
// Feature detect for webview support
if (MSHTMLWebViewElement) {
    let wv = document.createElement('x-ms-webview'); // Use CSS to set width, height and other styles
    wv.navigate("https://www.example.com");
    document.body.appendChild(wv);
}
```  

## Комментарии  

### WebView и IFRAME  

Как и стандартный HTML-элемент [IFRAME](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) , вы можете использовать WebView для загрузки удаленных страниц по протоколу HTTP и локальным страницам (*MS-appx-web:///*) из пакета приложения.  Однако WebView также может:  

*   Загрузка страниц и ресурсов из [ApplicationData](/uwp/api/Windows.Storage.ApplicationData) (локальных, перемещаемых, временных папок) (*MS-appdata:///*) и [потоков в памяти](/microsoft-edge/hosting/webview#buildlocalstreamuri) (*MS-Memory-Stream:///*)  
*   Предоставьте элементы управления, подобные браузеру: для [возврата](#goback) и [пересылки](#goforward) по журналу навигации, а также для [остановки](#stop) или [обновления](#refresh) текущей страницы.  
*   Создавайте [снимки экрана веб-содержимого](#capturepreviewtoblobasync) , чтобы упростить реализацию контракта на [использование общего доступа к](/windows/uwp/app-to-app/share-data) приложениям для Windows 10.  
*   Разрешите JavaScript-код, выполняющийся в WebView, вызвать пользовательские события ([MSWebViewScriptNotify](#mswebviewscriptnotify)) для вашего приложения и разрешить приложению запускать JavaScript в WebView ([invokeScriptAsync](#invokescriptasync)).  
*   Предоставьте вам детально настроенные события WebView содержимого:  
    
    | Событие WebView DOM | Описание |  
    |:--- |:--- |  
    | [MSWebViewNavigationStarting](#mswebviewnavigationstarting) | Указывает, что WebView начинает навигацию.  |  
    | [MSWebViewContentLoading](#mswebviewcontentloading) | HTML-содержимое загружается и загружается в элемент управления.  |  
    | [MSWebViewDOMContentLoaded](#mswebviewdomcontentloaded) | Указывает на то, что основные элементы DOM завершили загрузку.  |  
    | [MSWebViewNavigationCompleted](#mswebviewnavigationcompleted) | Указывает на то, что Навигация завершена, и все элементы мультимедиа обрабатываются.  |  
    | [MSWebViewUnviewableContentIdentified](#mswebviewunviewablecontentidentified) | WebView обнаружил, что содержимое не является HTML-кодом.  |  
    | [UnsafeContentWarningDisplaying](#mswebviewunsafecontentwarningdisplaying) | В WebView показана страница с предупреждением о том, что *Фильтр SmartScreen*Windows сообщил о небезопасном содержимом.  |  
    
    ... включая соответствующие [события](#events) для содержимого IFRAME, загруженного в WebView (например, [MSWebView**Frame**NavigationStarting](#mswebviewframenavigationstarting) и т. д.). 

### Вывод на печать  

При печати приложения для Windows с использованием JavaScript теги преобразуются `<x-ms-webview>` в `<iframe>` теги перед печатью.  Помимо обычной разницы между отображением на экране и отрисовкой для печати, стили CSS, примененные к `<iframe>` элементам, затем применяются к `<iframe>` преобразованным `<x-ms-webview>` .  

### Обслуживание сотрудников  

Начиная с [обновления Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) (EdgeHTML 18), [сотрудники служб поддерживаются в элементе управления WebView](/microsoft-edge/dev-guide#service-workers) (в дополнение к обозревателю Microsoft EDGE и приложениям для Windows 10 с поддержкой JavaScript).  

архитектуры приложений для архитектуры x64 требуются нейтральные (любые ЦП) или 64-разрядные пакеты, так как работники служб не поддерживаются в процессах WoW64.  (Для экономии места на диске версия WoW необходимых DLL не включена в Windows.)  

### Модель потоков и надежность  

Создание WebView посредством `document.createElement("x-ms-webview")` `<x-ms-webview>` разметки создает WebView в новом уникальном потоке в процессе приложения.  Выполнение в новом уникальном потоке означает, что долго выполняемый сценарий из одного WebView не может зависнуть приложение или другие веб-представления.  Создание WebView через `new MSWebView()` конструктор создает WebView в отдельном WebView процессе.  Выполнение в уникальных процессах означает, что в дополнение к защите от длительно выполняемого сценария приложение также защищено от веб-содержимого, которое не зависает в процессе WebView.  Создание WebView с помощью [`MSWebViewProcess.createWebViewAsync`](./webview/MSWebViewProcess.md#createwebviewasync) метода также создает WebView в отдельном процессе, но позволяет вызывающему объекту больше управлять параметрами процесса и группового просмотра в WebView процессах.  Дополнительные сведения см. в статье `MSWebViewProcess`.  

### Доступ к API WinRT  

Приложение UWP может допускает доступ документов HTML в веб-представлениях к API-интерфейсам WinRT.  Это осуществляется с помощью атрибута WindowsRuntimeAccess дочерних элементов правила для элемента ApplicationContentUriRules в AppxManifest.xml приложения UWP.  Установить для WindowsRuntimeAccess значение "все", а документы HTML с соответствующими URI будут разрешены использовать WinRT.  Это то же, что и предоставление доступа к контенту HTML в приложениях UWP в JavaScript, поэтому для получения дополнительных сведений ознакомьтесь [с API вызова WinRT из PWA](/microsoft-edge/progressive-web-apps-edgehtml/windows-features#call-winrt-apis-from-your-pwa) .  

API-интерфейсы WinRT, связанные с пользовательским интерфейсом, могут не работать при вызове из WebView, запущенного на своем собственном потоке, но может работать при вызове из WebView, выполняющегося в отдельном WebView процессе.  При использовании WebView для собственного уникального потока этот поток не является потоком представления приложения.  Некоторые API-интерфейсы WinRT, связанные с пользовательским интерфейсом, должны вызываться из потока представления приложения.  Представления веб-приложения, созданные в отдельном WebView процессе, выполняются для потока представления и не должны иметь те же ограничения, что и WebView, запущенные для собственного уникального потока.  Если у вас возникли проблемы с API-интерфейсами, относящимися к пользовательскому интерфейсу, в WebView убедитесь в том, что вы используете WebView в своем собственном процессе WebView, как описано выше.  

### Ограничения хранилища AppCache  

В приложениях, использующих поддержку JavaScript API кэша приложения (или AppCache), как определено в [спецификации HTML5](https://go.microsoft.com/fwlink/p/?LinkId=228542), для создания автономных веб-приложений необходимо учитывать ограничения на доступ к хранилищу.  Особенно это относится к устройствам с ограниченным объемом памяти.  Практические ограничения на размер AppCache всегда являются функцией доступного места для дискового хранилища.  Общие рекомендации указаны ниже.  

| Размер тома |AppCache на домен | AppCache для каждого пользователя |  
|:--- |:--- |:--- |  
| До 4 Гбайт | СВЯЗЬ | 50 МБ |  
| 4 ГБ – 16 ГБ | 50 МБ | 500MB |  
| от 16 до 32 ГБ | 50 МБ | Гбайт |  

Все приложения Windows10 должны использовать одну и ту же модель квоты AppCache, поэтому доступное ограничение дискового пространства распространяется на приложения для настольных компьютеров и для телефонов.  Кроме того, при использовании страниц, загруженных внутри **WebView** , на жестком диске занимают 1 ГБ *AppCache* места. запросы на дополнительное хранилище *AppCache* выше этого ограничения будут отвергнуты.  

Дополнительные сведения можно найти в разделе [Пример элемента управления WebView HTML](https://go.microsoft.com/fwlink/p/?linkid=309825) и JSBrowser с документацией по [элементу управления WebView](https://github.com/MicrosoftEdge/JSBrowser#harnessing-the-webview-control) .  

## Мероприятия  

### departingFocus  

Указывает на то, что фокус не входит в **WebView** в приложение.  Активируется, когда документ верхнего уровня WebView вызывает Window. departFocus.  Аргументы FocusNavigationEvent в событии departingFocus совпадают с параметрами, предоставленными departFocus, за исключением того, что параметры начала переводятся из document's координатного пространства WebView в пространство координат в документе хоста WebView.  Просмотрите метод WebView. navigateFocus и соответствующее событие окна navigatingFocus для перемещения фокуса с узла на WebView.  В этой статье приведены примеры реализации навигации по фокусу с помощью клавиатуры или игрового планшета, обрабатывающего данное событие, в [библиотеке навигации направления TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("departingFocus", handler);
webview.removeEventListener("departingFocus", handler);
```  

#### Сведения о событии  

|            |      |  
|:--- |:--- |  
| **Интерфейс** | [FocusNavigationEvent](./webview/FocusNavigationEvent.md) |  
| **Синхронный** | Да |   
| **Давать** | Да |  
| **Отменяемая** | Нет |  

### MSWebViewContainsFullScreenElementChanged  

Возникает при изменении состояния, если **WebView** в настоящее время включает элемент на весь экран.  Используйте свойство containsFullScreenElement для текущего значения.  Элемент "полный экран" — это представление полного элемента [API DOM](https://developer.mozilla.org/docs/Web/API/Fullscreen_API) с помощью функций DOM Elements. requestFullScreen и Document. exitFullScreen.  

```javascript
function containsFullScreenElementChangedHandler(eventInfo) {
    const applicationView = Windows.UI.ViewManagement.ApplicationView.getForCurrentView();
    if (webview.containsFullScreenElement) {
        webview.classList.add("fullscreen"); // Have the webview fill the app view
        applicationView.tryEnterFullScreenMode(); // Have the app view fill the screen
    }
    else {
        webview.classList.remove("fullscreen"); // Return webview to normal
        applicationView.exitFullScreenMode(); // Return app view to normal
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
webview.removeEventListener("MSWebViewContainsFullScreenElementChanged", containsFullScreenElementChangedHandler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | **Событие** |  
| **Синхронный** | Да |  
| **Давать** | Нет |   
| **Отменяемая** | Нет |  

### MSWebViewContentLoading  

Указывает на то, что содержимое HTML загружается и загружается в элемент управления.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewContentLoading", handler);
webview.removeEventListener("MSWebViewContentLoading", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Синхронный** | Да  |  
| **Давать** | Нет |   
| **Отменяемая** | Нет |  

### MSWebViewDOMContentLoaded  

Указывает на то, что основные элементы DOM завершили загрузку.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewDOMContentLoaded", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Синхронный** |Да |  
| **Давать** | Нет |  
| **Отменяемая** | Нет |   

### MSWebViewFrameContentLoading  

Указывает на то, что содержимое HTML загружено и загружено в `<iframe>` элемент управления.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameContentLoading", handler);
webview.removeEventListener("MSWebViewFrameContentLoading", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |  
| **Отменяемая** | Нет |   

### MSWebViewFrameDOMContentLoaded  

Указывает на то, что основные элементы DOM завершили загрузку в `<iframe>` .  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameDOMContentLoaded", handler);
webview.removeEventListener("MSWebViewFrameDOMContentLoaded", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |   
| **Отменяемая** | Нет |  

### MSWebViewFrameNavigationCompleted  

Указывает на то, что Навигация завершена, и все элементы мультимедиа отображаются в файле `<iframe>` .  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationCompleted", handler);
webview.removeEventListener("MSWebViewFrameNavigationCompleted", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |   
| **Отменяемая** | Нет |  

### MSWebViewFrameNavigationStarting  

Указывает, что `<iframe>` начинается Навигация в **WebView** .  Это происходит перед получением каких – либо ресурсов из сети для навигации.  Навигация не будет запущена, пока все обработчики событий MSWebViewFrameNavigationStarting не будут завершены.  Это событие можно отменить через вызов `eventArgs.preventDefault()` .  Если вы отменили, WebView не будет выполнять навигацию.  

```javascript
function frameNavigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
webview.removeEventListener("MSWebViewFrameNavigationStarting", frameNavigationStartingHandler);
```  

#### Сведения о событии  

|  |  |
|:--- |:--- |  
| **Интерфейс** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Синхронный** | Да |  
| **Давать** |Нет |   
| **Отменяемая** | Да |  

### MSWebViewLongRunningScriptDetected  

Периодически возникает в **WebView**, что позволяет прервать выполнение сценария.  

```javascript
function handler(eventInfo) {
    const stopPageScriptThreshold = 5 * 1000;
    if (eventInfo.executionTime > stopPageScriptThreshold) {
        eventInfo.stopPageScriptExecution = true; // Stop the long running script if it goes over our threshold
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewLongRunningScriptDetected", handler);
webview.removeEventListener("MSWebViewLongRunningScriptDetected", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [LongRunningScriptDetectedEvent](./webview/LongRunningScriptDetectedEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |  
| **Отменяемая** | Нет |  

### MSWebViewNavigationCompleted  

Указывает на то, что Навигация завершена, и все элементы мультимедиа отображаются либо произошла ошибка навигации.  Убедитесь в том, что навигация была выполнена успешно, а свойство webErrorStatus для сведений об ошибке навигации — в свойстве "событие".  Ошибки навигации могут возникать перед получением содержимого из сети для экземпляра, если имя узла URI не разрешается, в этом случае событие MSWebViewNavigationStarted будет срабатывать после события MSWebViewNavigationCompleted.  Ошибки навигации также могут возникать после получения страницы ошибки на веб-сервере (например, страница 404 на HTTP-сервере, в этом случае все события навигации будут срабатывать, MSWebViewNavigationStarting, MSWebViewContentLoading, MSWebViewDOMContentLoaded, а затем MSWebViewNavigationCompleted.  Чтобы предоставить страницу ошибки навигации приложения для случаев, когда веб-сервер не предоставил страницу ошибки, необходимо проверить, не была ли MSWebViewContentLoading выполнена для неудачной навигации, указывающей на то, что сервер не предоставил страницу ошибки.  

```javascript
let hasContent = false;
webview.addEventListener("MSWebViewNavigationStarting", () => { hasContent = false; });
webview.addEventListener("MSWebViewContentLoading", () => { hasContent = true; });

webview.addEventListener("MSWebViewNavigationCompleted", navigationCompletedEventArgs => {
    // Navigation failures may or may not come after getting an error page from the web server.
    // We keep track of the ContentLoading event with hasContent to tell if we have an error page from the server.
    // So we only navigate to our app error page when there's no server provided error page.
    if (!navigationCompletedEventArgs.isSuccess && !hasContent) {
        // Pass our failed URI and error details in the query and the error page script can read it as appropriate.
        webview.navigate("ms-appx-web:///appErrorPage.html?" + 
            "uri=" + encodeURIComponent(navigationCompletedEventArgs.uri) + "&" +
            "webErrorStatus=" + encodeURIComponent(navigationCompletedEventArgs.webErrorStatus));
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationCompleted", handler);
webview.removeEventListener("MSWebViewNavigationCompleted", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [NavigationCompletedEvent](./webview/NavigationCompletedEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |   
| **Отменяемая** | Нет |  

### MSWebViewNavigationStarting  

Указывает, что **WebView** начинает навигацию.  Это происходит перед получением каких – либо ресурсов из сети для навигации.  Навигация не будет запущена, пока все обработчики событий MSWebViewNavigationStarting не будут завершены.  Это событие можно отменить через вызов `eventArgs.preventDefault()` .  Если вы отменили, WebView не будет выполнять навигацию.  

```javascript
function navigationStartingHandler(navigationEventArgs) {
    // Cancel all navigations that don't meet some criteria.
    if (!navigationEventArgs.uri.startsWith("https://example.com/")) {
        navigationEventArgs.preventDefault();
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
webview.removeEventListener("MSWebViewNavigationStarting", navigationStartingHandler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Синхронный** | Нет |  
| **Давать** | Да |   
| **Отменяемая** | Да |  

### MSWebViewNewWindowRequested  

Вызывается, когда содержимое в **WebView** пытается открыть новое окно.  Если событие не отменено, WebView запустит URI нового запроса окна в браузере пользователя по умолчанию.  

```javascript
function handler(eventInfo) {
    // Prevent the webview from opening URIs in the default browser.
    eventInfo.preventDefault();
    
    // Only allow https://example.com/ to open new windows.
    if (eventInfo.referer === "https://example.com/") {
        // Perform some custom handling of the URI.
        openUri(eventInfo.uri);
    }
}
 
// addEventListener syntax
webview.addEventListener("MSWebViewNewWindowRequested", handler);
webview.removeEventListener("MSWebViewNewWindowRequested", handler);
```  

#### Сведения о событии  

|  |  |  
|:---|:--- |  
| **Интерфейс** | [NavigationEventWithReferrer](./webview/NavigationEventWithReferrer.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |  
| **Отменяемая** | Да |  

### MSWebViewPermissionRequested  

Указывает на то, что содержимое в **WebView** пытается получить доступ к функциональным возможностям (например, географическое расположение или доступ к блокировкам указателей), для которых обычно требуются разрешения конечных пользователей.  Если обработчик событий не зарегистрирован или обработчик событий не вызывает eventArgs. permissionRequest. Allow (), отсрочка () или Deny (), по умолчанию запрос разрешения будет отвергнут.  Если вам нужно решить, разрешено или запрещено ли разрешение асинхронно для экземпляра, если вам нужно запрашивать пользователя, используйте eventArgs. permissionRequest. Отсрочка ().  Запрос на разрешение будет отложен до тех пор, пока не будет использоваться WebView. getDeferredPermissionRequestById или WebView. getDeferredPermissionRequests и метод Allow () или Deny () в DeferredPermissionRequest с соответствующим значением идентификатора.  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});

// addEventListener syntax
webview.addEventListener("MSWebViewPermissionRequested", handler);
webview.removeEventListener("MSWebViewPermissionRequested", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [PermissionRequestedEvent](./webview/PermissionRequestedEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |   
| **Отменяемая** | Нет |  

### MSWebViewProcessExited  

Указывает на то, что компонент **WebView** Process crashsed.  Это относится только к незавершенному WebView.  Ознакомьтесь с разделом "Примечания", чтобы создать WebView, не являющиеся процессами, а не попроцессными WebView.  После того как это событие срабатывает, соответствующая WebView будет переведена в состояние сбоя.  Вызов большинства специальных методов WebView или доступ к большинству WebView определенных свойств в случае сбоя WebView приведет к созданию исключения.  Чтобы восстановить состояние после этого события, удалите сбойный WebView из DOM и замените его новым WebView.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewProcessExited", handler);
webview.removeEventListener("MSWebViewProcessExited", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | **Событие** |  
| **Синхронный** | Да |  
| **Давать** | Нет |   
| **Отменяемая** | Нет |  

### MSWebViewWebResourceRequested  

Вызывается, когда страница внутри элемента **WebView** запрашивает ресурс.  

```javascript
// A handler that completes synchronously with a custom HTTP response built from a string.
function handlerWithSyncString(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        const Http = Windows.Web.Http;
        // Create the custom response using a string
        webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(Http.HttpStatusCode.ok);
        webResourceRequestedEventArgs.args.response.content = new Http.HttpStringContent("<H1>Example</H1>");
    }
});

// A more complicated handler that completes asynchronously with a custom HTTP response built from a stream.
function handlerWithAsyncStream(webResourceRequestedEventArgs) {
    // Only provide custom HTTP responses for particular HTTP requests
    if (webResourceRequestedEventArgs.args.request.requestUri.absoluteUri === "https://www.bing.com/") {
        // Take a deferral on the WebResourceRequested event so that we can create the custom HTTP response asynchronously.
        const deferral = webResourceRequestedEventArgs.args.getDeferral();

        // Use fetch to get a Blob of the content of the URI
        fetch("ms-appx:///replacement.html").then(fetchResponse => {
            return fetchResponse.blob();
        }).then(fetchResponseBlob => {
            const Http = Windows.Web.Http;
            webResourceRequestedEventArgs.args.response = new Http.HttpResponseMessage(
                Http.HttpStatusCode.ok);

            // Use Blob.msDetachStream to convert the Blob to a Windows.Storage.Streams.IInputStream
            webResourceRequestedEventArgs.args.response.content = new Http.HttpStreamContent(
                fetchResponseBlob.msDetachStream());

        }).finally(() => {
            // Use a finally call to complete the deferral so even if there is an error we will unblock the event.
            deferral.complete();
        });
    }
});
 
// addEventListener syntax
webview.addEventListener("MSWebViewWebResourceRequested", handler);
webview.removeEventListener("MSWebViewWebResourceRequested", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [WebResourceRequestedEvent](./webview/WebResourceRequestedEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |   
| **Отменяемая** | Нет |  


### MSWebViewScriptNotify  

Вызывается, когда страница внутри элемента **WebView** вызывает метод **Window. external. notify** .  Метод Window. external. notify доступен только для документов с URI-идентификаторами, которые соответствуют правилам в manifest's ApplicationContentUriRules или программно разрешены с помощью задания WebView. Settings. isScriptNotifyAllowed в true.  Кроме того, Window. external. notify доступен только для документов верхнего уровня WebView.  

```javascript
webview.addEventListener("MSWebViewScriptNotify", eventInfo => {
    console.log("The URI " + eventInfo.callingUri + 
        " has sent notification " + eventInfo.value);
});

// Allow the next URI to which we navigate access to window.external.notify
webview.settings.isScriptNotifyAllowed = true;
webview.navigate("https://example.com/");

webview.addEventListener("MSWebViewNavigationCompleted", () => {
    // Inject script to the webview that will send a notification back.
    const asyncOp = webview.invokeScriptAsync("eval", "window.external.notify('example notification')");
    asyncOp.start();
});
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [ScriptNotifyEvent](./webview/ScriptNotifyEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |  
| **Отменяемая** | Нет |  

### MSWebViewUnsafeContentWarningDisplaying  

Возникает, когда в **WebView** показана страница предупреждения для содержимого, обнаруженного как небезопасное фильтром SmartScreen.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
webview.removeEventListener("MSWebViewUnsafeContentWarningDisplaying", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | **Событие** |  
| **Синхронный** |Да |  
| **Давать** |Нет |   
| **Отменяемая** |Нет |  

### MSWebViewUnsupportedUriSchemeIdentified  

Вызывается при переходе на универсальный код ресурса (URI), который не поддерживает **WebView** .  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
webview.addEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
webview.removeEventListener("MSWebViewUnsupportedUriSchemeIdentified", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [NavigationEvent](./webview/NavigationEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |  
| **Отменяемая** | Да |  

### MSWebViewUnviewableContentIdentified  

Вызывается, когда **WebView** пытается перейти к веб-контенту с неподдерживаемым типом контента.  Например, в настоящее время PDF-файлы не поддерживаются WebView и для навигации по документам PDF они не будут перемещаться, а затем вызывать это событие.  

```javascript
function handler(args) {
    if (args.mediaType === "application/pdf") {
        Windows.System.Launcher.launchUriAsync(new Windows.Foundation.Uri(args.uri));
    }
}

// addEventListener syntax
webview.addEventListener("MSWebViewUnviewableContentIdentified", handler);
webview.removeEventListener("MSWebViewUnviewableContentIdentified", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | [UnviewableContentIdentifiedEvent](./webview/UnviewableContentIdentifiedEvent.md) |  
| **Синхронный** | Да |  
| **Давать** | Нет |   
| **Отменяемая** | Нет |  

## Методы  

### addWebAllowedObject  

Добавляет собственный объект среды выполнения Windows в качестве глобального параметра в документ верхнего уровня в **WebView**.  

Объект не был добавлен в текущий документ, а в следующий документ верхнего уровня, в который WebView переходит.  Объект будет вставлен перед выполнением любого сценария HTML-документа, чтобы можно было полагаться на объект в глобальном сценарии документа.  

AddWebAllowedObject следует использовать либо во время события MSWebViewNavigationStarting, либо перед явным вызовом метода Navigate.  В этих случаях объект вставляется в документ соответствующей навигации.  Звонить в какой-либо другой контекст, вы не можете быть уверены в том, какой документ вы хотите вставить в объект.  

Многократное вызов addWebAllowedObject в строке приводит к вставке нескольких объектов в документ.  Если вы вызываете метод перед явным вызовом навигации, а затем снова во время соответствующего события MSWebViewNavigationStarting, оба звонка будут успешными, и вы увидите несколько объектов, которые добавлены.  Если вы звоните несколько раз с одним и тем же параметром name, последний вызов WINS и предыдущие вызовы с этим именем игнорируются.  

Если навигация завершается ошибкой или перенаправлена, вызовы addWebAllowedObject для этой навигации игнорируются.  Если вы хотите обрабатывать переадресацию, вы можете подписаться на событие MSWebViewNavigationStarting, чтобы перенаправлять и повторно вызвать addWebAllowedObject, в зависимости от того, какие условия подходит для вашего приложения.  Аналогичным образом, после того как документ перейдет к следующему документу, вы перейдете на него, и вам потребуется явно вызвать addWebAllowedObject, если вы хотите, чтобы они переходили их.  

Если вы вызываете addWebAllowedObject для документа, у которого нет доступа WinRT, или у него есть [AllowForWebOnly доступ через ApplicationContentUriRules](/uwp/schemas/appxpackage/uapmanifestschema/element-uap-rule) , этот объект будет добавлен только в том случае, если объект имеет атрибут метаданных Windows. Foundation. Metadata. AllowForWeb.  В противном случае введение завершится ошибкой, и в консоль разработчика JavaScript появится сообщение об ошибке.  При вызове для документа, имеющего полный доступ к WinRT, этот объект будет вставлен независимо от атрибута AllowForWeb.  

Кроме того, объект должен реализовывать интерфейс IAgileObject.  Это обусловлено тем, что элементы XAML и WebView выполняются на потоках представлений ASTA приложения, а поток JavaScript WebView — это другой ASTA поток, и мы хотели бы посоветовать разработчикам приложения, чтобы убедиться, что их объект может выполняться в потоке JavaScript, не блокируя поток представления приложения, если это возможно.  

Параметр Name должен быть допустимым именем свойства JavaScript, в противном случае звонок не будет выполнен автоматически.  Если имя имеет свойство, которое уже есть в глобальном объекте, то это свойство перезаписывается, если свойство может быть настроено.  Ненастраиваемые свойства глобального объекта не перезаписываются, а вызов addWebAllowedObject завершается сбоем.  Свойства JavaScript, созданные с помощью addWebAllowedObject, доступны для записи, настраиваемые и перечислимые.  

```javascript
let name = "exampleProperty";
webview.addWebAllowedObject(name, applicationObject);
webview.navigate("https://example.com/"); // applicationObject will be available as window.exampleProperty on https://example.com
```  

#### Параметры  

*name*  

*   Тип: **строка**  
*   Имя объекта, доступного для документа в **WebView**.  

*applicationObject*  

*   Тип: **объект**  
*   Объект, который необходимо предоставить документу в **WebView**.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

#### Дополнительные функции и требования  

|  |  |  
|:--- |:--- |  
| **Минимальный поддерживаемый клиент** | Windows10 (только для приложений Магазина Windows) |    
| **Минимальный поддерживаемый сервер** | Ничего не поддерживается |   
| **Минимальный поддерживаемый телефон** | Ничего не поддерживается |  

### buildLocalStreamUri  

Создает универсальный код ресурса (URI), который можно передать в [navigateToLocalStreamUri](#methods).  

```javascript
var string = webview.buildLocalStreamUri(contentIdentifier, relativePath);
```  

#### Параметры  

*contentIdentifier*  

*   Тип: **строка**  
*   Уникальный идентификатор содержимого, на который ссылается URI.  Этот элемент определяет корневой элемент универсального кода ресурса (URI).  

*relativePath*  

*  Тип: **строка**  
*  Путь к ресурсу относительно корня.  

#### Возвращаемое значение  

Тип: **строка**  

Универсальный код ресурса (URI), созданный путем объединения и нормализации *contentIdentifier* и *relativePath*.  

#### Пример.  

В следующем примере показан типичный вариант использования.  

```javascript
var webview = document.createElement("x-ms-webview"); //Instantiate the webview element
var localStreamUri = webview.buildLocalStreamUri(contentIdentifier, relativePath); //Create URI to pass to navigateToLocalStreamUri method
webview.navigateToLocalStreamUri(localStreamUri, streamResolver); //Load the local web content 
```  

### capturePreviewToBlobAsync  

Создает изображение текущего [элемента WebView](./webview.md) и записывает его в указанный элемент изображения.  

```javascript
var capturePreviewToBlobAsync = webview.capturePreviewToBlobAsync();
```  

#### Параметры  

У этого метода нет параметров.  

#### Возвращаемое значение  

Type (тип): **MSWebViewAsyncOperation**  

Объект **MSWebViewAsyncOperation** , который после его завершения предоставляет объект **BLOB** , содержащий изображение.  При использовании **capturePreviewToBlobAsync**необходимо определить обработчики успехов и ошибок после определения операции.  После применения обработчиков событий вызовите метод Start объекта [MSWebViewAsyncOperation](./webview/MSWebViewAsyncOperation.md) , чтобы выполнить операцию.  

### captureSelectedContentToDataPackageAsync  

> [!IMPORTANT]
> Этот метод устарел и имеет известную ошибку.  Старайтесь не использовать этот метод в рабочем коде.  

Асинхронно возвращает [пакет](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) данных, содержащий выбранное содержимое в **WebView**.  

```javascript
var msWebViewAsyncOperation = webview.captureSelectedContentToDataPackageAsync();
```  

#### Параметры  

У этого метода нет параметров.  

#### Возвращаемое значение  

Type (тип): **MSWebViewAsyncOperation**  

Объект **MSWebViewAsyncOperation** , который после его завершения предоставляет объект [Package](https://docs.microsoft.com/uwp/api/Windows.ApplicationModel.DataTransfer.DataPackage) , содержащий изображение.  При использовании **captureSelectedContentToDataPackageAsync**необходимо определить обработчики успехов и ошибок после определения операции.  После применения обработчиков событий вызовите метод Start объекта MSWebViewAsyncOperation, чтобы выполнить операцию.  

```javascript
 var operation = webview.captureSelectedContentToDataPackageAsync();
    operation.oncomplete = function () {
        // operation.result is a package object that contains the selected data.
        var url = URL.createObjectURL(operation.result, { oneTimeOnly: true });
        // After converting the package to a URI, put it in an image element.
        document.getElementById('webviewPreview').src = url;
    };
    operation.start();
```  

### invokeScriptAsync  

Как асинхронное действие выполняет указанную функцию сценария из загруженного HTML-кода с определенными аргументами.  

```javascript
webview.invokeScriptAsync(functionName, ...args)
```  

#### Параметры  

**functionName**  

*   Тип: **строка**  
*   Имя вызываемой функции.  Это имя свойства в объекте глобального окна документа верхнего уровня WebView.  Это может быть Встроенная глобальная функция, например eval или Open, а также функция, определенная сценарием, для объекта глобального окна.  Только функции в документе верхнего уровня WebView могут быть вызваны.  

**аргументы**  

*   Тип: **строка**  
*   Необязательные строковые параметры для передачи в вызываемую функцию.  После аргумента functionName любые дополнительные параметры invokeScriptAsync являются строками, передаваемыми вызываемой функции.  

#### Возвращаемое значение  

Type (тип): **MSWebViewAsyncOperation**  

При использовании **invokeScriptAsync**необходимо определить обработчики успехов и ошибок после определения операции.  После применения обработчиков событий вызовите метод **MSWebViewAsyncOperation. Start** , чтобы выполнить операцию.  При возникновении события Complete MSWebViewAsyncOperation свойство Result MSWebViewAsyncOperation является строковым возвращаемым значением из вызова функции.  Использование возвращаемого значения вызываемой функции обеспечивает синхронное взаимодействие содержимого WebView с узлом WebView.  Чтобы получить содержимое WebView асинхронно обратно на узел WebView, просмотрите событие MSWebViewScriptNotify.  Если функция вызывается из-за неуправляемого исключения, возникает событие ошибки MSWebViewAsyncOperation.  

```javascript
const functionName = "eval";
const args = ["'Current URL: ' + document.location.href"];

const asyncOp = webview.invokeScriptAsync(functionName, ...args);

asyncOp.onerror = () => console.error("Error: " + asyncOp.error);
asyncOp.oncomplete = () => console.log("Result: " + asyncOp.result); // Logs 'Current URL: about:blank'
asyncOp.start();
```  

### getDeferredPermissionRequests  

Возвращает список отложенных запросов разрешений, выданных содержимым в элементе управления **WebView** .  

```javascript
var sequence<PermissionRequest> = x-ms-webview.getDeferredPermissionRequests();
```  

#### Параметры  

У этого метода нет параметров.  

#### Возвращаемое значение  

Type (тип): [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)  

Указанный запрос на отложенный доступ.  

#### Дополнительные функции и требования  

|  | |  
|:--- |:--- |  
| **Минимальный поддерживаемый клиент** | Windows10 (только для приложений Магазина Windows) |  
| **Минимальный поддерживаемый сервер** | Ничего не поддерживается |  
| **Минимальный поддерживаемый телефон** | Ничего не поддерживается |  


### getDeferredPermissionRequestById  

Возвращает указанный запрос на отложенный доступ.  

```javascript
var deferredPermissionRequest = x-ms-webview.getDeferredPermissionRequestById(id);
```  

#### Параметры  

*id*  

*   Тип: **Long без знака**  
*   Идентификатор запроса отложенного разрешения, который вы хотите получить.  

#### Возвращаемое значение  

Type (тип): [DeferredPermissionRequest](./webview/DeferredPermissionRequest.md)  

Указанный запрос на отложенный доступ.  

#### Дополнительные функции и требования  

|  |  |  
|:--- |:--- |  
| **Минимальный поддерживаемый клиент** | Windows10 (только для приложений Магазина Windows) |  
| **Минимальный поддерживаемый сервер** | Ничего не поддерживается |  
| **Минимальный поддерживаемый телефон** | Ничего не поддерживается |  

### goBack  

Переход по **WebView** на предыдущую страницу в истории навигации.  

```javascript
webview.goBack();
```  

#### Параметры  

У этого метода нет параметров.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

### goForward  

Переход по **WebView** к следующей странице в истории навигации.  

```javascript
webview.goForward();
```  

#### Параметры  

У этого метода нет параметров.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

### переход  

Загружает HTML-содержимое по указанному универсальному идентификатору ресурса (URI).  

```javascript
webview.navigate(uri);
```  

#### Параметры  

**uri**  

*   Тип: **строка**  
*   URI для загрузки.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

### navigateFocus  

Перемещение фокуса на **WebView**.  Вызывает событие WebView window's navigatingfocus документа верхнего уровня.  Аргументы FocusNavigationEvent, используемые в событии navigatingfocus, совпадают с параметрами, предоставленными navigateFocus, за исключением параметров происхождения, которые преобразуются из пространства координат основного документа в пространство координат документа верхнего уровня WebView.  Просмотрите событие WebView departingFocus и соответствующий метод Window. departFocus для перемещения фокуса с WebView на узел.  Пример реализации навигации по фокусу с помощью клавиатуры или игрового приложения, использующего этот метод, можно найти в [библиотеке навигации направления TVJS](https://github.com/Microsoft/TVHelpers/wiki/Using-DirectionalNavigation) .  

```javascript
const activeElementBounds = document.activeElement.getBoundingClientRect();
const origin = { 
    originLeft: activeElementBounds.left,
    originTop: activeElementBounds.top,
    originWidth: activeElementBounds.width,
    originHeight: activeElementBounds.height
};
webview.navigateFocus(navigationReason, origin);
```  

#### Параметры  

*navigationReason*  

*   Тип: **строка**  
*   Причина для навигации.  Это значение должно быть "Left", "стрелка вверх", "вправо" или "вниз".  Это направление, в котором фокус перемещается от элемента, на который Вы ориентированы в данный момент.  

*исходных*  

*   Тип: **объект**  
*   Источник навигации.  Это объект JavaScript со свойствами "originLeft", "originTop", "originWidth" и "originHeight".  Эти значения должны описывать расположение и размер элемента, в котором находится фокус, вне которой перемещается фокус.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

### navigateToLocalStreamUri  

Загружает локальное веб-содержимое по указанному URI с помощью [**UriToStreamResolver**](/uwp/api/windows.web.iuritostreamresolver.uritostreamasync).  

```javascript
webview.navigateToLocalStreamUri(source, streamResolver); 
```  

#### Параметры  

*исходный*  

*   Тип: **строка**  
*   Универсальный код ресурса (URI) MS-Stream, который определяет локальное HTML-содержимое для загрузки.  Создайте эту строку с помощью [**buildLocalStreamUri**](/uwp/api/windows.web.ui.iwebviewcontrol.buildlocalstreamuri).  

*streamResolver*  

*   Type (тип): Any  
*   Сопоставитель, преобразующий URI в поток для загрузки.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

### navigateToString  

Загружает указанное HTML-содержимое в новый документ.  

```javascript
webview.navigateToString(contents);
```  

#### Параметры  

*содержимое*  

*   Тип: **строка**  
*   Отображаемое содержимое HTML.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

### navigateWithHttpRequestMessage  

Переход по WebView на универсальный код ресурса (URI) с запросом POST и заголовками HTTP.  

```javascript
webview.navigateWithHttpRequestMessage(requestMessage);
```  

#### Параметры  

*requestMessage*  

*   Type (тип): **HttpRequestMessage**  
*   Сведения о запросе HTTP.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

#### Комментарии  

> [!WARNING]
> Если вы добавите в этот запрос дополнительные заголовки, например учетные данные для проверки подлинности, помните, что эти заголовки также будут включены в любые последующие дочерние запросы.  Будьте внимательны, чтобы предотвратить случайное раскрытие конфиденциальных и персональных данных.  

### Обновлен  

Перезагружает текущее содержимое в **WebView**.  

```javascript
webview.refresh();
```  

#### Параметры  

У этого метода нет параметров.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

### stop  

Останавливает текущую навигацию по **WebView** или загрузку.  

```javascript
webview.stop();
```  

#### Параметры  

У этого метода нет параметров.  

#### Возвращаемое значение  

Этот метод не возвращает значение.  

## Свойства  

### canGoBack  

Возвращает значение, указывающее, может ли **WebView** переход назад.  

Это свойство доступно только для чтения.  

```javascript
var canGoBack = webview.canGoBack;
```  

#### Значение свойства  

Тип: **логический**  

**Значение true** , если **WebView** может перейти назад; в противном случае — **значение false**.  

### canGoForward  

Возвращает значение, указывающее, может ли **WebView** переход вперед.  

Это свойство доступно только для чтения.  

```javascript
var canGoForward = webview.canGoForward;
```  

#### Значение свойства  

Тип: **логический**  

**Значение true** , если **WebView** может перейти вперед; в противном случае — **значение false**.  

### containsFullScreenElement  

Возвращает значение, указывающее, содержит ли **WebView** элемент, поддерживающий полноэкранный режим.  Дополнительные сведения вы видите в событии MSWebViewContainsFullScreenElementChanged.  

Это свойство доступно только для чтения.  

```javascript
var containsFullScreenElement = webview.containsFullScreenElement;
```  

#### Значение свойства  

Тип: **логический**  

**Значение true** , если **WebView** включает элемент, поддерживающий полный экран; в противном случае — **значение false**.  

### documentTitle  

Получает заголовок страницы, отображаемой в данный момент в **WebView**.  

Это свойство доступно только для чтения.  

```javascript
var documentTitle = webview.documentTitle;
```  

#### Значение свойства  

Тип: **строка**  

Заголовок страницы.  

### height  

Возвращает или задает высоту **WebView**.  

```javascript
var height = webview.height;
webview.height = height;
```  

#### Значение свойства  

Тип: **номер**  

Высота **WebView**.  

### работу другого  

Возвращает процесс **WebView** .  

Это свойство доступно только для чтения.  

```javascript
var process = webview.process;
webview.process = process;
```  

#### Значение свойства  

Type (тип): [MSWebViewProcess](./webview/MSWebViewProcess.md)  

### settings  

Возвращает объект [MSWebViewSettings](./webview/MSWebViewSettings.md) , содержащий свойства для включения или отключения функций **WebView** .  

Это свойство доступно только для чтения.  

```javascript
var settings = webview.settings;
webview.settings = settings;
```  

#### Значение свойства  

Type (тип): [MSWebViewSettings](./webview/MSWebViewSettings.md)  

Объект [MSWebViewSettings](./webview/MSWebViewSettings.md) , содержащий свойства для включения или отключения функций **WebView** .  

### src  

Возвращает или задает универсальный код ресурса (URI) для содержимого HTML, которое будет отображаться в элементе управления **WebView** .  

```javascript
var src = webview.src;
webview.src = src;
```  

#### Значение свойства  

Тип: **строка**  

Источник универсального кода ресурса (URI) для содержимого HTML, которое будет отображаться в элементе управления **WebView** .  

### width  

Возвращает или задает ширину **WebView**.  

```javascript
var width = webview.width;
webview.width = width;
```  

#### Значение свойства  

Тип: **номер**  

Ширина **WebView**.  
