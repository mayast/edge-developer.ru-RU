---
title: Справочник по API MSAppI
description: В рамках функций справки можно создавать объекты BLOB и MSStream.  Объекты MSApp поддерживаются для приложений Windows с помощью JavaScript.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/29/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: MSapp, PWA, upload file, Upload, Blog, MSStream, приложения для Windows 10, UWP, edge
ms.openlocfilehash: 4966f6afbe4e971d6a366de7e9b4f5a6cd2305e0
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942169"
---
# MSApp  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Объект MSApp и его участники поддерживаются только для приложений Windows с использованием JavaScript \(включая доступ к функциям API Windows\).  Объект MSApp существует только в локальном контексте HTML-документа, загруженного с помощью схемы MS-appx URI; В противном случае объект отсутствует (и, соответствует ни одному из методов и свойств).  

В ней предусмаатываются функции, которые помогают создавать [BLOB-объекты](https://developer.mozilla.org/docs/Web/API/Blob) [и MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [Методы](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      [clearTemporaryWebDataAsync,](#cleartemporarywebdataasync) [createBlobFromRandomAccessSream,](#createblobfromrandomaccessstream) [createDataPackage,](#createdatapackage) [createDataPackageFromSelection,](#createdatapackagefromselection) [createFileFromStorageFile,](#createfilefromstoragefile) [createStreamFromInputStream,](#createstreamfrominputstream) [execAsyncAtPriority,](#execasyncatpriority) [execAtPriority, execAtP приоритет,](#execatpriority) [getCurrentPriity,](#getcurrentpriority) [getWPrintDocumentSource,](#gethtmlprintdocumentsource)[getHtmlPrintDocumentSourceAsynce,](#gethtmlprintdocumentsourceasync) [getViewId,](#getviewid) [isTaskScheduledAtPriityOrHigher,](#istaskscheduledatpriorityorhigher) [pageHandlesAllApplicationActivations,](#pagehandlesallapplicationactivations) [suppressSubdownloadCredentialPrompts,](#suppresssubdownloadcredentialprompts) [terminateApps, getinateApp.](#terminateapp)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Константы](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      [текущий,](#current) [высокий,](#high) [статус,](#idle) [нормально.](#normal)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [Интерфейс MSAppAsyncOperation](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [start](#start)  
   :::column-end:::
:::row-end:::  

## Методы MSApp  

### clearTemporaryWebDataAsync  

:::row:::
   :::column span="":::
      Удаление и индексирование данных из кэша и индексированных данных DB для приложения или [WebView.](../../webview.md)  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      Этот метод не имеет параметров.  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      Тип: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)  
      
      Представляет асинхронное действие.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createBlobFromRandomAccessStream  

:::row:::
   :::column span="":::
      Создает [Blob-объект](https://developer.mozilla.org/docs/Web/API/Blob) из [объекта IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)  Этот способ следует использовать при работе с объектами в приложениях, чтобы создать на его основе объект `IRandomAccessStream` W3C.  После создания большого двоичного объекта его можно использовать с [FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [API-каналами](https://developer.mozilla.org/docs/Web/API/URL) [и XMLHttpRequest.](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `type` [в]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Строка | Тип контента данных;  Эта строка должна быть указана в формате, заданном в маркере 3.7 из RFC 2616.  |  
      
      `stream` [в]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | [IRandomAccessStream,](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) которые хранятся в Blob-файле.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Blob | Новый объект BLOB-объект, содержащий поток.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      | Исключение | Ошибка |  
      |:---- |:--- |  
      | TypeMismatchError | Тип узла несовместим с ожидаемым типом параметров.  Для версий, предшествующих Internet Explorer 10, возвращается TYPE_MISMATCH_ERR.  |  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Создает BLOB-объект из типов среды выполнения Windows Runtime с помощью пространства имен MSApp объекта.  Этот метод создает двоичный объект, который фактически является светло-обтеканием по объекту [RandomAccessStream.](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference)  Время существует владельцем этого потока, и поток будет закрыт при универсении blobb.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      var randomAccessStream = dataPackage.GetData("image/bmp");
      var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
      var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});
      
      document.getElementById("imagetag").src = url; 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createDataPackage  

:::row:::
   :::column span="":::
      Преобразует диапазон пользователя или заданного пользователем диапазон в фрагмент HTML, к которому можно предоставить общий доступ.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `object` [в]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Этот диапазон можно создать на основе объекта выделения, например или `window.selection.getRangeAt(0)` вручную.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Содержит разметку HTML для указанного диапазона.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод поддерживает [только диапазон объектной модели документа (DOM),](https://developer.mozilla.org/docs/Web/API/Range)а не [TextRange.](/uwp/api/windows.ui.xaml.documents.textrange)  Возвращаемый пакет данных для указанного диапазона содержит разметку HTML в формате буфера обмена.  
      
      Свойства возвращаемом пакета данных недоступны.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createDataPackageFromSelection  

:::row:::
   :::column span="":::
      Преобразует пользовательский элемент или выбранный фрагмент приложения в фрагмент HTML, к которому можно предоставить общий доступ.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      Этот метод не имеет параметров.  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Содержит разметку HTML для указанного диапазона.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Возвращаемый пакет данных для выбранного столбца содержит разметку HTML в формате буфера обмена.  Если пользователь не выбирает пользовательский интерфейс в любом месте пользовательского интерфейса приложения, `createDataPackageFromSelection` возвращается `null` значение.  
      
      Свойства возвращаемом пакета данных недоступны.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### createFileFromStorageFile  

:::row:::
   :::column span="":::
      Преобразует [файл хранилища WinRT](/uwp/api/) [в](/uwp/api/windows.storage.storagefile) стандартный объект W3C-файла. [File](https://developer.mozilla.org/docs/Web/API/File)  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `storageFile` [в]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Содержит файл хранилища.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      | Исключение | Ошибка |  
      |:---- |:--- |  
      | TypeMismatchError | Указанная Викторная ссылка на файл W3C недопустима.  Для версий, предшествующих Internet Explorer 10, `TYPE_MISMATCH_ERR` возвращается значение.  |  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### createStreamFromInputStream  

:::row:::
   :::column span="":::
      Создает [MSStream](https://msdn.microsoft.com/library/hh772328) на основе [InputStream.](https://msdn.microsoft.com/library/hh772327)  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `type` [в]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Тип контента данных;  Эта строка должна быть указана в формате, заданном в маркере 3.7 из RFC 2616.  \([Просмотр типов MIME,](например, https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) `text/plain` , `text/html` `image/jpeg` `image/png` ,,,,,,,, ,, ,, `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` ,, ,, , , , , , , , , , , , , , , , , , , и т. д.).  
      
      `inputStream` [в]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | [IInputStream,](/uwp/api/Windows.Storage.Streams.IInputStream) который будет храниться в. `MSStream`  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод имеет тип контента и `IInputStream` ссылку.  Затем проверяет, является ли ссылка на потоковое справочник, является экземпляром `IInputStream` типа, а если нет, выглядит повторяющийся. `DOMException TYPE_MISMATCH_ERR`  Если ошибка не возникает, `createStreamFromInputStream` создается `MSStream` \(на основе входных данных\).)  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      Можно `IInputStream` использовать для `MSStream` создания.  Как и в случае неоднократного использования объектов, все URL-адреса, созданные с помощью объекта изображения, отозваны `MSStreams` `URL.createObjectURL` url-адресами.  Кроме того, запросы на второй URL-адрес этого объекта после использования потока произойдет сбой.  
      
      ```javascript
      var inputStream = myInputStream; //get InputStream from socket API, and so on
      var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
      document.getElementById("imagetag").src = URL.createObjectURL(stream); 
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### execAsyncAtPriority  

:::row:::
   :::column span="":::
      Планируются звонки, которые будут проходить позднее в зависимости от заданного приоритета.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `asynchronousCallback` [в]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Функция | Функция вызова, которая позволяет выполнять асинхронно в определенном приоритете.  |  
      
      `priority` [в]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Значение контекстного приоритета, при котором выполнена асинхронный вызов обратных звонков.  См. [константы MSApp.](#msapp-constants)  |  
      
      `args` [в]
      
      | Тип | Описание |  
      |:---- |:--- |   
      | Любой | Необязательное число аргументов, которые перенаправляются функции синхронных звонков \(в виде параметров 1 и т. д.).  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      Этот метод не возвращает значение.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Предоставленная `asynchronousCallback` функция вызова будет проводиться асинхронно позже.  `asynchronousCallback` диспетчер ы диспетчера в зависимости от предоставленного приоритета.  Нормальная приоритет равен существующему [методу Методу.](https://developer.mozilla.org/docs/Web/API/Window/setImmediate)  При выполнении вызова текущая контекстная приоритетная приоритетная приоритетра задается для выполнения вызовов.  
      
      Параметры `asynchronousCallback` обратной связи могут быть любыми функциями.  Если после параметра эти аргументы переносятся, они будут переназываться `priority` функции вызова.  
      
      В `execAtPriority` отличие от сказанного, любой объект, возвращаемый `asynchronousCallback` функцией вызова, игнорируется \(и не возвращается через `execAsyncAtPriority` \).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### execAtPriority  

:::row:::
   :::column span="":::
      Выполняет указанную функцию вызова в заданном контекстном приоритете.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `synchronousCallback` [в]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Функция | Функция вызова для запуска синхронизируемого контекстного приоритета.  |  
      
      `priority` [в]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Указанное значение приоритета, которое будет задано при выполнении функции `synchronousCallback` вызова.  См. [константы MSApp.](#msapp-constants)  |  
      
      `args` [в]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Необязательное число аргументов, которые были применяться `synchronousCallback` функции callback \(as parameters 1 и т. д.).  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой | Возвращает значение возвращаемого `synchronousCallback` вызова \(если применимо\\).  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Предоставленный метод звонков будет запускаться `synchronousCallback` синхронно.  Текущий приоритет изменяется на указанный приоритет (заданное аргументом приоритета) для функции вызова.  По завершении вызова функции вызова приоритет возвращается к предыдущему значению, предшествующем `execAtPriority` узел.  Возвращаемое значение `execAtPriority` из метода вызова \(как предоставлено\).  
      
      Параметры `synchronousCallback` обратной связи могут быть любыми функциями.  Если после параметра приоритета предоставляются любые аргументы, они будут пройдены до предоставленного метода вызова.  Если параметр вызова возвращает значение, то это значение также становится возвращаемое `execAtPriority` значением.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### getCurrentPriority  

:::row:::
   :::column span="":::
      Возвращает текущий контекстный приоритет.  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Возвращаемое значение представляет собой одну из `MSApp.HIGH` `MSApp.NORMAL` строк, `MSApp.IDLE` или.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот метод возвращает текущий контекстный приоритет \(см. [константы MSApp),](#msapp-constants)которые можно изменить через `execAtPriority` `execAsyncAtPriority` и.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
          // YOUR CODE HERE
      }
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### getHtmlPrintDocumentSource  

Нерекомендуется синхронизировать синхронный API.  Для Windows 10: `getHtmlPrintDocumentSourceAsync`  Сведения Windows 8 и 8.1 см. в записи MSDN для [получения htmlHtmlPrintDocumentSource.](https://msdn.microsoft.com/library/hh772325)  

### getHtmlPrintDocumentSourceAsync  

:::row:::
   :::column span="":::
      Возвращает исходный контент, который требуется напечатать.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `htmlDoc` [в]  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Документ | Html-документ, который нужно распечатать.  Это может быть корневой документ, документ в iframe, фрагменте документа или документ SVG.  Имейте в виду, что HTMLDoc должен быть документ, а не элемент.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример 1**  
      
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
   :::column-end:::
   :::column span="":::
      **Пример 2**  
      
      ```javascript
      function registerForPrintContract() {
              var printManager = Windows.Graphics.Printing.PrintManager.getForCurrentView();
              printManager.onprinttaskrequested = onPrintTaskRequested;
              console.log("Print Contract registered.  Use the Print button to print.", "sample", "status");
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
   :::column-end:::
:::row-end:::  

### getViewId  

:::row:::
   :::column span="":::
      Поддержка нескольких окон.  
      
      > [!NOTE] 
      > В приложениях Win8.1 JavaScript UWP поддерживались несколько окон, используя API DOM MSApp DOM, которые теперь приводятся к описанию.  В Windows 10 используйте `window.open` `window` и новое `MSApp.getViewId` новое.  
      
      | Описание |Windows 10; | Windows 8.1 |  
      |:---- |:---- |:--- |  
      | Создание нового окна | [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) | [MSApp.createNewView](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |Объект нового окна | [окно](https://developer.mozilla.org/docs/Web/API/Window) |[MSAppView](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `window`
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Объект, представляющий собой окно с документом DOM.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      `viewId`
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Число | Может использоваться с различными [AI.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Используйте [окно.open](https://developer.mozilla.org/docs/Web/API/Window/open) [и окно](https://developer.mozilla.org/docs/Web/API/Window) для создания новых окон, а затем взаимодействуйте с API WinRT, `MSApp.getViewId` добавив API.  Объект имеет значение параметра и возвращает число, которое можно использовать с `window` `viewId` различными [API Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)  
      
      *   Видимость задержки  
          
          В WinRT обычно запускаются скрытые представления, а конццы разработчика использует такое представление, как при его `TryShowAsStandaloneAsync` подготовке.  В Интернете отображается окно, а конечный пользователь может смотреть `window.open` содержимое по мере загрузки и обработки контента.  Чтобы новые окна были такими же, как и представления в WinRT, но не отображались сразу `window.open` же.  Например:  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   Различия основного окна  
          
          Первоое окно, открытое ОС, отличается от вспомогательного окна:  
          
          | Описание | Основной | Дополнительная |  
          |:---- |:--- |:--- |  
          | window.open | Разрешено | Disallowed |  
          | window.close | Закрыть приложение | Закрытие окна |  
          | Ограничения навигации | Только третье значение | Нет ограничений |  
          
          Ограничение запретить открытие дополнительного окна может изменяться в будущем в зависимости от [отзывов.](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer)  
      
      *   Одинаковые ограничения на связь  
          
          Техническивозе проблемы, из-за которых синхронизация, однотипичный и перекрестный и перекрестный и окна, звонки скрываются.  Когда вы открываете такой же или идею, сценарии в одном окне позволяют вызывать функции непосредственно в другом окне, и некоторые из этих звонков произойдут сбой.  `postMessage` При вызовах работает нормально и по возможности рекомендуется выполнять различные действия.  Улучшена эта проблема.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### isTaskScheduledAtPriorityOrHigher  

:::row:::
   :::column span="":::
      Возвращает логическое значение, определяющее, есть ли ожидаемая процедура на определенный уровень приоритета.  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `priority` [в]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | Значение приоритета \(см. [MSApp Constants](#msapp-constants)\), определяющее уровень приоритета и выше для запроса любых негативных работ.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Boolean (Логическое) | Функция возвращает, если в очереди указанного уровня приоритета или `true` выше указанного уровня в качестве `false` значения приоритета.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот способ обеспечивает способ использования кода JavaScript, чтобы определить, нет ли ожидаемых ожиданиях на различных уровнях `isTaskScheduledAtPriorityOrHigher` приоритета \(или более высокого\) с целью того, что код JavaScript может принимать решение о достижении более высокой работы.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### pageHandlesAllApplicationActivations  

:::row:::
   :::column span="":::
      Используется для избора начального пути (перезагрузка страницы) перед каждым активированным событием \(например, щелчок уведомления или закрепленная плитка\).  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Boolean (Логическое) | Используется для всегда пропуска начального пути (страницы) и перехода сразу к `MSApp.pageHandlesAllApplicationActivations(true)` `WebUIApplication` активированное событию.  Требуется, чтобы обрабатывать все страницы активации отдельно.  Если задать этот `true` метод так, то щелкнув активное событие \(например, уведомление\) не будет запускать перезагрузку, а для одностраничных приложений, хранящихся на одностраничных приложениях, не будут перегружаться.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
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
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### suppressSubdownloadCredentialPrompts  

:::row:::
   :::column span="":::
      Управляет ли запросы на проверку подлинности в процессе скачивания ресурсов.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
     
      `suppress` [в]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Boolean (Логическое) | Значение истина подтверждает возможные запросы проверки подлинности.  Значение ложного значения не откладывает потенциальную проверку подлинности пользователя.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**  
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Этот способ определяет, подтверждает ли приложение запросы на проверку подлинности во `suppressSubdownloadCredentialPrompts` время скачивания ресурсов.  По умолчанию поведение не предусмаватывается отключение запросов учетных данных.  
      
      `suppressSubdownloadCredentialPrompts` предназначены для приложений, которые могут загружать лишь большое количество ресурсов, требуемое для проверки подлинности, например почтовое приложение \(может содержать информационный бюллетень с несколькими изображениями, для каждого из которых требуется проверка подлинности\).  
      
      Если выключить запрос ы учетных данных, диалоговые окна проверки подлинности на серверах не отображаются при доступе к ресурсам, для которых требуется проверка подлинности, и загрузка ресурса не будет скачан.  Обратите внимание на то, что не влияет на другие возможные запросы на проверку подлинности на прокси-сервере или запросы сертификации `suppressSubdownloadCredentialPrompts` клиента, и никак не влияет на XHR.  
      
      Имейте в виду, что `suppressSubdownloadCredentialPrompts` влияние на все содержимое приложения, включая контент, хранящееся в `webview` элементе.  
      
      > [!IMPORTANT]
      > Решения о запросах на ввод учетных данных куплены.  Поэтому при выключении запросов учетных данных к сроку действия учетных данных может потребоваться перезагрузить документ.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      // Set to true to suppress potential credential prompts:
      MSApp.suppressSubdownloadCredentialPrompts(true);
      // Now one can load content or navigate iframe/webview to some other site.
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### terminateApp  


:::row:::
   :::column span="":::
      Завершение текущего приложения и создает отчет об ошибок.  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      `error` [в]
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Ошибка | Объект, `Error` с помощью которого можно описать ошибку, которая активировала окончание.  Объект `Error` должен содержать свойства номера, описания и стопки, а отчет о сбое не будет создан, если объект не содержит эти свойств.  |  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Исключения**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Комментарии**  
      
      Если вы уточнили проблему, выполнив ширину 5 лучших проблем приложения, она будет отображаться на странице `terminateApp` качества приложения.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Пример.**  
      
      В этом примере `terminateApp` возвращаются исключения.  Он использует `Error` объект, предоставленный при обзоре исключения.  
      
      ```javascript
      try {  
          var obj2 = null;  
          obj2.val = 5;  
      }  
      catch(e) {  
          window.MSApp.terminateApp(e);  
      }  
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### Константы MSApp  

:::row:::
   :::column span="":::
      Разрешенные значения приоритета, с которыми связаны `execAsyncAtPriority` `execAtPriority` значения `getCurrentPriority` приоритета, `isTaskScheduldAtPriorityOrHigher` и.  
   :::column-end:::
   :::column span="":::
      #### Текущие  
      
      `current`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании с указанным методом \(см. также раздел\), при выборе текущего контекстной приоритетной операции будет использоваться текущая `current` приоритетная.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### Высока  
      
      `high`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании с соответствующим методом \(см. также раздел\), метод будет использоваться более высокий приоритет при выполнении запрошенной операции и будет `high` утерян недоставлено.  |  
   :::column-end:::
   :::column span="":::
      #### Состояние Idle (в покое)  
      
      `idle`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При `ideal` использовании с неприемлемым способом \(см. также раздел\), метод будет использоваться меньше, чем обычно при выполнения запрошенной операции и будет уничтожен после любой существующей нормальной приоритетной приоритетной работы.  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### Обычный  
      
      `normal`  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMString | При использовании с соответствующим методом (см. также разделе), метод будет использовать существующий приоритет при выполнения `normal` запрошенной операции.  |  
   :::column-end:::
   :::column span="":::
      **Пример.**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Требования**  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | IDL | Mshtml.idl |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## MSAppAsyncOperation  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### start  

:::row:::
   :::column span="":::
      Начало. `MSAppAsyncOperation`  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **Параметры**  
      
      Нет.  
   :::column-end:::
   :::column span="":::
      **Возвращаемое значение**
      
      Нет.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **Свойства**  
      
      `error` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | DOMError | Представляет `MSAppAsyncOperation` ошибку.  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | EventHandler | Свойство для настройки обработчика события по завершающему `MSAppAsyncOperation` моменту.  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | EventHandler | Свойство для настройки обработчика события во время `MSAppAsyncOperation` ошибки.  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Число | Представляет состояние асинхронной операции в приложении Для Windows с помощью JavaScript.  К значениям относятся: `Started[0]` `Completed[1]` , `Error[2]` .  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` свойство  
      
      | Тип | Описание |  
      |:---- |:--- |  
      | Любой |Представляет `MSAppAsyncOperation` результат.  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
