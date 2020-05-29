---
title: Справочник по API MSApp
description: Предоставляет вспомогательные функции, позволяющие создавать объекты BLOB и MSStream. Объекты и участники MSApp поддерживаются в приложениях для Windows, использующих JavaScript.
author: mattwojo
ms.author: mattwoj
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, отправка файлов, блог, MSStream, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 0ed8cefa918bd44f3b2c4e8312d2c1d3b4ace8fc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572854"
---
# MSApp

Объект MSApp и его члены поддерживаются только в приложениях для Windows, использующих JavaScript (в том числе PWAs доступ к функциям API Windows). Объект MSApp существует только в локальном контексте HTML-документа в приложении Windows, загруженном с помощью схемы URI ms-appx. в противном случае объект не существует (и следовательно, ни один из его методов и свойств не доступен).

Она предоставляет вспомогательные функции, позволяющие создавать объекты [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) и [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**Методы**](#msapp-methods) | [clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream)и [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority,](#getcurrentpriority)getHtmlPrintDocumentSource,[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync)getHtmlPrintDocumentSourceAsynce и [getViewId](#getviewid)getViewId. [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher) [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource) [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations) [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts) [terminateApp](#terminateapp) |

| | |
| :--- | :--- |
| [**Постоянные**](#msapp-constants) | [Текущее](#current), [высокое](#high), [бездействующее](#idle), [обычное](#normal).|

| | |
| :--- | :--- |
| [Интерфейс **MSAppAsyncOperation**](#msappasyncoperation) | [start](#start) |

## Методы MSApp

### clearTemporaryWebDataAsync 
Очищает данные кэша и indexedDB для приложения или [WebView](../../webview.md).

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### Параметры
У этого метода нет параметров.

#### Возвращаемое значение
Команду[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)

Представляет асинхронное действие.

### createBlobFromRandomAccessStream
Создает [большой двоичный](https://developer.mozilla.org/docs/Web/API/Blob) объект из [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) объекта. Этот метод следует использовать при работе с `IRandomAccessStream` объектами в приложениях для создания объекта на базе W3C из потока. После создания большого двоичного объекта его можно использовать с [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL-интерфейсами](https://developer.mozilla.org/docs/Web/API/URL)и [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest). 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### Параметры

`type` возврата

|Тип | Описание |
|:---- |:--- |
|Строка | Тип контента данных. Эта строка должна иметь формат, заданный в токене типа мультимедиа, определенном в разделе 3,7 из RFC 2616.

`stream` возврата

|Тип | Описание |
|:---- |:--- |
|Любой | [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) храниться в большом двоичном объекте.

#### Возвращаемое значение
|Тип | Описание |
|:---- |:--- |
|Большом | Новый объект BLOB, содержащий поток.

#### Исключения
|Ошибка | Ошибка |
|:---- |:--- |
|TypeMismatchError | Тип узла несовместим с ожидаемым типом параметра. Для версий более ранних, чем Internet Explorer 10, возвращается TYPE_MISMATCH_ERR.

#### Комментарии
Создает большой двоичный объект из типов среды выполнения Windows через пространство имен MSApp в объекте Window. Этот метод создает большой двоичный объект, который, по сути, является облегченной оберткой по отношению к объекту, переданному [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) на него. Большой двоичный объект владеет временем существования этого потока, и поток будет закрыт при уничтожении большого двоичного объекта. 

#### Пример.

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### createDataPackage
Преобразует указанный диапазон пользователя или приложения в фрагмент HTML, к которому можно предоставить общий доступ.

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### Параметры
`object` возврата

|Тип | Описание |
|:---- |:--- |
|Любой | Этот диапазон можно создать из объекта выделения, например: `window.selection.getRangeAt(0)` или вручную.

#### Возвращаемое значение
|Тип | Описание |
|:---- |:--- |
|Любой | В этом разделе содержится разметка HTML для указанного диапазона.

#### Комментарии
Этот метод поддерживает только [диапазон объектной модели документов (DOM)](https://developer.mozilla.org/docs/Web/API/Range), а не [TextRange](/uwp/api/windows.ui.xaml.documents.textrange). Возвращенный пакет данных для указанного диапазона включает HTML-разметку в формате буфера обмена.

Для возвращенного пакета данных нет доступных свойств.

### createDataPackageFromSelection 
Преобразуются в фрагмент кода HTML, к которому можно предоставить общий доступ.

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### Параметры
У этого метода нет параметров.

#### Возвращаемое значение
|Тип | Описание |
|:---- |:--- |
|Любой | В этом разделе содержится разметка HTML для указанного диапазона.

#### Комментарии
Возвращенный пакет данных для выделенного фрагмента включает HTML-разметку в формате буфера обмена. Если вы не выделять ни одного пользователя в пользовательском интерфейсе приложения, функция `createDataPackageFromSelection` возвращает значение null.

Для возвращенного пакета данных нет доступных свойств.
 
### createFileFromStorageFile 
Преобразует [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) в стандартный [`File`](https://developer.mozilla.org/docs/Web/API/File) объект W3C.

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### Параметры
`storageFile` возврата

|Тип | Описание |
|:---- |:--- |
|Любой | Файл, содержащий хранилище.

#### Исключения
|Ошибка | Ошибка |
|:---- |:--- |
|TypeMismatchError | Указана недопустимая ссылка на файл в формате W3C. Для версий более ранних, чем Internet Explorer 10, возвращается TYPE_MISMATCH_ERR.

### createStreamFromInputStream  

Создание элемента [`MSStream`](https://msdn.microsoft.com/library/hh772328) FROM [`InputStream`](https://msdn.microsoft.com/library/hh772327) .  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### Параметры
`type` возврата

|Тип | Описание |
|:---- |:--- |
|DOMString | Тип контента данных. Эта строка должна иметь формат, заданный в токене типа мультимедиа, определенном в разделе 3,7 из RFC 2616. ([См. типы MIME,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. text/plain, Text/HTML, Image/JPEG, Image/PNG, Audio/MPEG, Audio/OGG, Audio/*, видео, MP4 и т. д.). 

`inputStream` возврата

|Тип | Описание |
|:---- |:--- |
|Любой | Значение, которое [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) будет храниться в `MSStream` .

#### Комментарии
Этот метод принимает тип содержимого и `IInputStream` ссылку. Затем метод проверяет, переданный ли ссылка на поток является экземпляром типа, `IInputStream` а если нет — исключением `DOMException TYPE_MISMATCH_ERR` . Если ошибка не возникнет, `createStreamFromInputStream` создается `MSStream` (из входных данных).

#### Пример.
`IInputStream`Можно использовать для создания `MSStream` . Как `MSStreams` и объекты по отдельности, все URL-адреса, созданные с помощью `URL.createObjectURL` элемента Image, будут отозваны при первом разрешении. Кроме того, запросы на второй URL-адрес на этом объекте после использования потока завершатся сбоем.

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### execAsyncAtPriority 
Планирует выполнение обратного вызова в более позднее время согласно заданному приоритету. 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### Параметры
`asynchronousCallback` возврата

|Тип | Описание |
|:---- |:--- |
|Функция | Функция обратного вызова, предназначенная для асинхронного выполнения, с указанным приоритетом.

`priority` возврата

|Тип | Описание |
|:---- |:--- |
|DOMString | Значение приоритета контекста, для которого выполняется обратный вызов asynchronousCallback. Смотрите [MSApp константы](#msapp-constants).

`args` возврата

|Тип | Описание |
|:---- |:--- |
|Любой | Необязательный ряд аргументов, передаваемых в функцию обратного вызова synchronousCallback (в параметрах 1 и on).

#### Возвращаемое значение
Этот метод не возвращает значение.

#### Комментарии
Указанная `asynchronousCallback` функция обратного вызова выполняется асинхронно позднее. `asynchronousCallback` будет отправлено согласно указанному приоритету. Обычный приоритет эквивалентен существующему [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) методу. При выполнении обратного вызова текущим контекстным приоритетом задается указанное значение параметра Priority для продолжительности выполнения обратного вызова.

`asynchronousCallback`Параметр обратного вызова может быть любой функцией. Если аргументы указаны после `priority` параметра, они будут переданы в функцию обратного вызова.

В отличие от него `execAtPriority` , любой объект, возвращенный `asynchronousCallback` функцией обратного вызова, игнорируется (и не возвращается через `execAsyncAtPriority` ).

### execAtPriority 
Запускает указанную функцию обратного вызова с заданным приоритетом контекста.

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### Параметры
`synchronousCallback` возврата

|Тип | Описание |
|:---- |:--- |
|Функция | Функция обратного вызова, выполняющаяся синхронно на заданном приоритете контекста.

`priority` возврата

|Тип | Описание |
|:---- |:--- |
|DOMString | Указанное значение приоритета, которое будет задано текущим значением приоритета контекста при запуске `synchronousCallback` функции обратного вызова. Смотрите [MSApp константы](#msapp-constants).

`args` возврата

|Тип | Описание |
|:---- |:--- |
|Любой | Необязательный ряд аргументов, передаваемых в `synchronousCallback` функцию обратного вызова (в качестве параметров 1 и on).

#### Возвращаемое значение
|Тип | Описание |
|:---- |:--- |
|Любой | Возвращает возвращаемое значение `synchronousCallback` обратного вызова (как применимо).

#### Комментарии
Указанный `synchronousCallback` метод обратного вызова выполняется синхронно. Текущий контекстный приоритет меняется на предоставленное значение приоритета (заданное аргументом Priority) для длительности указанной функции обратного вызова. После того как функция обратного вызова завершит выполнение, перед вызовом будет возвращено значение Priority (приоритет) `execAtPriority` . Возвращаемое значение `execAtPriority` является возвращаемым значением метода обратного вызова (как указано).
 
`synchronousCallback`Параметр обратного вызова может быть любой функцией. Если после параметра Priority указаны какие либо аргументы, они будут переданы в указанный метод обратного вызова. Если параметр обратного вызова возвращает значение, это значение также становится возвращаемым значением `execAtPriority` .

#### Пример.

```javascript
var user = Windows.System.UserProfile.UserInformation;

MSApp.execAtPriority(function () { // This callback executes synchronously.
  user.getFirstNameAsync().then(function () { // Dispatches at high priority.
    return user.getLastNameAsync();
  }).done(function () { // Dispatches at high priority.
    // USEFUL CODE HERE
  });
}, MSApp.HIGH); // The second argument of the execAtPriority method.
```

### getCurrentPriority 
Возвращает текущий приоритет по контексту.

```javascript
var retval = MSApp.getCurrentPriority();
```

#### Параметры
Нет. 

#### Возвращаемое значение
|Тип | Описание |
|:---- |:--- |
|DOMString | Возвращаемое значение является одной из строк `MSApp.HIGH` , `MSApp.NORMAL` или `MSApp.IDLE` .

#### Комментарии
Этот метод возвращает текущий приоритет контекста (см [`MSApp Constants`](#msapp-constants) .), который можно изменить с помощью `execAtPriority` и `execAsyncAtPriority` .

#### Пример.

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### getHtmlPrintDocumentSource  

Нерекомендуемый синхронный API. В Windows 10 вы видите `getHtmlPrintDocumentSourceAsync` . Приложения для Windows 8 и 8,1 можно найти в статье MSDN для [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).  

### getHtmlPrintDocumentSourceAsync
Возвращает исходное содержимое, которое нужно распечатать.

#### Параметры
`htmlDoc` возврата

|Тип | Описание |
|:---- |:--- |
|Документ | Документ HTML для печати. Это может быть корневой документ, документ в окне IFRAME, фрагмент документа или документ SVG. Имейте в виду, что htmlDoc должен быть документом, а не элементом.

#### Пример 1

```javascript
var printTask = event.request.createPrintTask(title, function (args) {
                var deferral = args.getDeferral();
                var getPrintDocumentSourceAsync;
                if (MSApp.getHtmlPrintDocumentSourceAsync) { // Windows 10
                    getPrintDocumentSourceAsync = MSApp.getHtmlPrintDocumentSourceAsync(document);
                } else {
                    getPrintDocumentSourceAsync = WinJS.Promise.as(MSApp.getHtmlPrintDocumentSource(document));
                }
                getPrintDocumentSourceAsync.then(function (source) {
                    args.setSource(source);
                    deferral.complete();
                }, function (error) {
                    console.error(error);
                    deferral.complete();
                });
            });
```

#### Пример 2

```javascript
    function registerForPrintContract() {
            var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
            printManager.onprinttaskrequested = onPrintTaskRequested;
            console.log("Print Contract registered. Use the Print button to print.", "sample", "status");
    }
    
    // Variable to hold the document source to print
    var gHtmlPrintDocumentSource = null;
    
    // Print event handler for printing via the PrintManager API.
    function onPrintTaskRequested(printEvent) {
        var printTask = printEvent.request.createPrintTask("Print Sample", function (args) {
            args.setSource(gHtmlPrintDocumentSource);
    
            // Register the handler for print task completion event
            printTask.oncompleted = onPrintTaskCompleted;
        });
    }
    
    // Print Task event handler is invoked when the print job is completed.
    function onPrintTaskCompleted(printTaskCompletionEvent) {
        // Notify the user about the failure
        if (printTaskCompletionEvent.completion === Windows.Graphics.Printing.PrintTaskCompletion.failed) {
            console.log("Failed to print.", "sample", "error");
        }
    }
    
    // Executed just before printing.
    var beforePrint = function () {
        // Replace with code to be executed just before printing the current document:
    };
    
    // Executed immediately after printing.
    var afterPrint = function () {
        // Replace with code to be executed immediately after printing the current document:
    };
    
    function printButtonHandler() {
        // Optionally, functions to be executed immediately before and after printing can be configured as following:
        window.document.body.onbeforeprint = beforePrint;
        window.document.body.onafterprint = afterPrint;
    
        // Get document source to print
        MSApp.getHtmlPrintDocumentSourceAsync(document).then(function (htmlPrintDocumentSource) {
            gHtmlPrintDocumentSource = htmlPrintDocumentSource;
    
            // If the print contract is registered, the print experience is invoked.
            Windows.Graphics.Printing.PrintManager.showPrintUIAsync();
        });
    }
```

### getViewId 
Поддержка нескольких окон. 

> [!NOTE] 
> В Win 8.1 JavaScript для приложений UWP поддерживалось несколько окон, использующих API MSApp DOM, которые теперь depricated. Для Windows 10, использование `window.open` `window` и новый `MSApp.getViewId` .

| Описание |Windows 10; | Windows 8.1 |  
|:---- |:---- |:--- |  
| Создание нового окна | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|Новый объект Window | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### Параметры
`window`

|Тип | Описание |
|:---- |:--- |
|DOMString | Объект, представляющий окно, содержащее документ DOM. | 

#### Возвращаемое значение

`viewId`

|Тип | Описание |
|:---- |:--- |
|Число | Может использоваться с различными [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API. 

#### Комментарии
Используйте [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) и [`window`](https://developer.mozilla.org/docs/Web/API/Window) для создания новых окон, но для взаимодействия с API WinRT добавьте `MSApp.getViewId` API. Он принимает `window` объект в качестве параметра и возвращает `viewId` число, которое можно использовать с различными [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API. 

##### Задержка отображения 
Представления в WinRT, как правило, отображаются в скрытом режиме, а конечный разработчик использует нечто вроде `TryShowAsStandaloneAsync` для отображения представления после его полной подготовки. В Интернете `window.open` показывает окно немедленно, и пользователь может просматривать содержимое, которое загружается и отображается. Если вы хотите, чтобы новое приложение Windows было похоже на представления в WinRT и не отображалось сразу, мы добавили `window.open` параметр. Пример
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### Различия между основными окнами
Основное окно, которое первоначально открывается в операционной системе, отличается от того, какое приложение открывается для них. 

|Описание | Основной | Дополнительная |
|:---- |:--- |:--- |
|Window. Open | Разрешено | Disallowed |
|Window. Close | Закрыть приложение | Закрыть окно |
| Ограничения навигации | Только ACUR | Без ограничений |

Ограничение, не позволяющее открыть вспомогательную систему Windows, может измениться в будущем в зависимости от [отзыва](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).

##### Ограничения для связи с одинаковыми исходными данными 
Существует сложная техническая неполадка, препятствующая надлежащей поддержке синхронных и идентичных вызовов между окнами и сценариями. При открытии одного и того же исходного окна сценарий в одном окне может напрямую вызывать функции в другом окне, а некоторые из этих вызовов завершатся сбоем. `postMessage` звонки прекрасно работают и являются рекомендуемым способом, если это возможно. Чтобы улучшить работу, выполните указанные ниже действия.


### isTaskScheduledAtPriorityOrHigher 
Возвращает логическое значение, определяющее наличие ожидающих трудозатрат на заданном уровне приоритета или более высоком.

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### Параметры
`priority` возврата

|Тип | Описание |
|:---- |:--- |
|DOMString | Значение приоритета (в разделе [константы MSApp](#msapp-constants)) с указанием уровня приоритета и более поздних значений для запроса всех незавершенных трудозатрат в очереди.

#### Возвращаемое значение
|Тип | Описание |
|:---- |:--- |
|Boolean (Логическое) | Возвращает `true` значение, если в очереди есть трудозатраты с указанным уровнем приоритета или выше, `false` в противном случае.

#### Комментарии
Этот `isTaskScheduledAtPriorityOrHigher` метод предоставляет средства для кода JavaScript, чтобы определить, есть ли ожидающие трудозатраты на различных уровнях приоритета (или выше), с целью, по которой код JavaScript может получить повышенную приоритетную работу.

#### Пример.

```javascript
function performIdleWork(array_in) {
  var idx = 0;

  function performIdleWorkHelper() {
    for (; idx < array_in.length; ++idx) {

      // USEFUL CODE HERE 

      if (MSApp.isTaskScheduledAtPriorityOrHigher(MSApp.NORMAL)) {
        MSApp.execAsyncAtPriority(performIdleWorkHelper, msPriority.IDLE);
        break;
      } // if
    } // for
  } // performIdleWorkHelper

  performIdleWorkHelper();
} // performIdleWork
```

### pageHandlesAllApplicationActivations
Используется, чтобы избежать обновления начального пути (перезагрузка страницы) перед каждым событием активации (IE. щелчок на уведомлении или закрепленной плитке). 

#### Параметры

|Тип | Описание |
|:---- |:--- |
Boolean (Логическое) | Используется `MSApp.pageHandlesAllApplicationActivations(true)` для постоянного пропуска обновления пути начала (повторной загрузки страницы), а также для обработки `WebUIApplication` события activated. Требует, чтобы все страницы обрабатывали события активации отдельно. Определяя этот метод как `true` , щелчок активированного события (например, notificaiton) не приведет к повторной загрузке, очень важно для одностраничных приложений, в которых не требуется перегрузка страниц.

#### Пример. 

```javascript
// Without this, the app will first refresh to the start path before every activate event
window.MSApp.pageHandlesAllApplicationActivations(true); 

// This must not be deffered so that it can receive the initial `activated` event in time
window.Windows.UI.WebUI.WebUIApplication.addEventListener(
    `activated`,
    e =>
        microsoftInterface.handleActivatedEvent(e);
    }),
    false
);
```

### suppressSubdownloadCredentialPrompts 
Определяет, отключаются ли в приложении возможные запросы на проверку подлинности при загрузке ресурсов.

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### Параметры
`suppress` возврата

|Тип | Описание |
|:---- |:--- |
|Boolean (Логическое) | Значение true подавляет возможные запросы на проверку подлинности. Если задано значение false, запросы на проверку подлинности от пользователя не отключаются.

#### Значение Returan
Нет.

#### Комментарии
Этот `suppressSubdownloadCredentialPrompts` метод определяет, будет ли приложение подавить запросы на проверку подлинности при загрузке ресурсов. По умолчанию запросы учетных данных не отключаются.

`suppressSubdownloadCredentialPrompts` предназначен для использования приложениями, которые могут загружать чрезмерное количество ресурсов, требующих проверки подлинности, например почтового приложения (которое может содержать информационный бюллетень с несколькими изображениями, требующих проверки подлинности).

При подавлении запросов учетных данных диалоговые окна для проверки подлинности на серверах не отображаются при доступе к ресурсам, требующим проверки подлинности, а сам ресурс не загружается. Обратите внимание, что `suppressSubdownloadCredentialPrompts` не влияет на другие возможные запросы, такие как проверка подлинности прокси-сервера или запросов на сертификацию клиента, а также не влияет на XHR.

Имейте в виду, что `suppressSubdownloadCredentialPrompts` влияют на все содержимое приложения, включая содержимое, размещенное в `webview` элементе.
 
**Внимание!**  Запрос учетных данных кэшируется. Таким образом, несмотря на то, что запросы учетных данных вступят в силу немедленно, для того чтобы подавить их, возможно, потребуется перезагрузить документ, чтобы он вступил в силу.

#### Пример.

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### terminateApp
Завершение работы текущего приложения и создание отчета об ошибке. 

```javascript
MSApp.terminateApp(error); 
```

#### Параметры
`error` возврата

Тип | Описание |
|:---- |:--- |
|Ошибка | `Error`Объект, который можно использовать для описания ошибки, которая вызвала завершение. `Error`Объект должен содержать число, описание и свойства стека; отчет об ошибке не создается, если объект не содержит этих свойств.

#### Возвращаемое значение
Нет.

#### Комментарии
Если проблема, о которой сообщается, `terminateApp` становится одной из первых 5 проблем приложения, она будет отображаться на странице качества приложения.

#### Пример.
Этот пример вызывается `terminateApp` , когда возникает исключение. Он использует `Error` объект, указанный при перехвате исключения. 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### Константы MSApp
Допустимые значения приоритетов `execAsyncAtPriority` , связанные с,, `execAtPriority` `getCurrentPriority` и `isTaskScheduldAtPriorityOrHigher` .

#### Текущие
`current`

|Тип | Описание |
|:---- |:--- |
|DOMString | Когда `current` используется в соответствующем методе (см. также раздел), при выполнении запрошенной операции метод будет использовать текущий приоритет по контексту.

#### Высока
`high`

|Тип | Описание |
|:---- |:--- |
|DOMString | Когда `high` используется в соответствующем методе (см. также раздел), метод будет использовать более высокий приоритет при выполнении запрошенной операции и будет отправлять операцию перед всеми существующими нормальными приоритетами трудозатрат.

#### Состояние Idle (в покое)
`idle`

|Тип | Описание |
|:---- |:--- |
|DOMString | Когда `ideal` используется в соответствующем методе (см. также раздел), метод будет использовать меньше обычного приоритета при выполнении запрошенной операции и будет обрабатывать операцию после того, как все существующие обычные приоритеты будут выполняться.

#### Обычный
`normal`

|Тип | Описание |
|:---- |:--- |
|DOMString | Когда `normal` используется в соответствующем методе (см. также раздел), метод будет использовать обычный существующий приоритет при выполнении запрошенной операции.

#### Пример.

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### Требования
|IDL | MSHTML. idl |
|:---- |:--- |

## MSAppAsyncOperation

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### start
Запускает `MSAppAsyncOperation` .

```javascript
var retval = MSAppAsyncOperation.start();
```

#### Параметры
Нет.

#### Возвращаемое значение
Нет.

#### Свойства
`error` Property

|Тип | Описание |
|:---- |:--- |
|DOMError | Представляет ошибку `MSAppAsyncOperation` .

```javascript
p = object.error
```

`oncomplete` Property

|Тип | Описание |
|:---- |:--- |
|EventHandler | Свойство для установки обработчика событий по завершении `MSAppAsyncOperation` .

```javascript
p = object.oncomplete
```

`onerror` Property

|Тип | Описание |
|:---- |:--- |
|EventHandler | Свойство для установки обработчика событий при возникновении ошибки `MSAppAsyncOperation` .

```javascript
p = object.onerror
```

`readyState` Property

|Тип | Описание |
|:---- |:--- |
|Число | Представляет состояние асинхронной операции в приложении для Windows с помощью JavaScript. Возможны следующие значения: запущен [0], завершен [1], ошибка [2].

```javascript
p = object.readyState
```

`result` Property

|Тип | Описание |
|:---- |:--- |
|Любой |Представляет результат `MSAppAsyncOperation` .

```javascript
p = object.result
```
