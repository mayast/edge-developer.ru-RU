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
# <span data-ttu-id="16e94-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="16e94-105">MSApp</span></span>

<span data-ttu-id="16e94-106">Объект MSApp и его члены поддерживаются только в приложениях для Windows, использующих JavaScript (в том числе PWAs доступ к функциям API Windows).</span><span class="sxs-lookup"><span data-stu-id="16e94-106">The MSApp object and its members are supported only for Windows apps using JavaScript (including PWAs accessing Windows API features).</span></span> <span data-ttu-id="16e94-107">Объект MSApp существует только в локальном контексте HTML-документа в приложении Windows, загруженном с помощью схемы URI ms-appx. в противном случае объект не существует (и следовательно, ни один из его методов и свойств не доступен).</span><span class="sxs-lookup"><span data-stu-id="16e94-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>

<span data-ttu-id="16e94-108">Она предоставляет вспомогательные функции, позволяющие создавать объекты [BLOB](https://developer.mozilla.org/docs/Web/API/Blob) и [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="16e94-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>

```javascript
var result = MSApp.method;
```

| | |
| :--- | :--- |
| [**<span data-ttu-id="16e94-109">Методы</span><span class="sxs-lookup"><span data-stu-id="16e94-109">Methods</span></span>**](#msapp-methods) | <span data-ttu-id="16e94-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream)и [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority,](#getcurrentpriority)getHtmlPrintDocumentSource,[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync)getHtmlPrintDocumentSourceAsynce и [getViewId](#getviewid)getViewId. [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher) [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource) [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations) [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts) [terminateApp](#terminateapp)</span><span class="sxs-lookup"><span data-stu-id="16e94-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span> |

| | |
| :--- | :--- |
| [**<span data-ttu-id="16e94-111">Постоянные</span><span class="sxs-lookup"><span data-stu-id="16e94-111">Constants</span></span>**](#msapp-constants) | <span data-ttu-id="16e94-112">[Текущее](#current), [высокое](#high), [бездействующее](#idle), [обычное](#normal).</span><span class="sxs-lookup"><span data-stu-id="16e94-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>|

| | |
| :--- | :--- |
| [<span data-ttu-id="16e94-113">Интерфейс **MSAppAsyncOperation**</span><span class="sxs-lookup"><span data-stu-id="16e94-113">**MSAppAsyncOperation** interface</span></span>](#msappasyncoperation) | [<span data-ttu-id="16e94-114">start</span><span class="sxs-lookup"><span data-stu-id="16e94-114">start</span></span>](#start) |

## <span data-ttu-id="16e94-115">Методы MSApp</span><span class="sxs-lookup"><span data-stu-id="16e94-115">MSApp Methods</span></span>

### <span data-ttu-id="16e94-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="16e94-116">clearTemporaryWebDataAsync</span></span> 
<span data-ttu-id="16e94-117">Очищает данные кэша и indexedDB для приложения или [WebView](../../webview.md).</span><span class="sxs-lookup"><span data-stu-id="16e94-117">Clears cache and indexedDB data for the app or [WebView](../../webview.md).</span></span>

```javascript
var retval = MSApp.clearTemporaryWebDataAsync(#); 
```

#### <span data-ttu-id="16e94-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-118">Parameters</span></span>
<span data-ttu-id="16e94-119">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="16e94-119">This method has no parameters.</span></span>

#### <span data-ttu-id="16e94-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-120">Return value</span></span>
<span data-ttu-id="16e94-121">Команду[`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="16e94-121">Type: [`IAsyncAction`](/uwp/api/windows.foundation.iasyncaction)</span></span>

<span data-ttu-id="16e94-122">Представляет асинхронное действие.</span><span class="sxs-lookup"><span data-stu-id="16e94-122">Represents an asynchronous action.</span></span>

### <span data-ttu-id="16e94-123">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="16e94-123">createBlobFromRandomAccessStream</span></span>
<span data-ttu-id="16e94-124">Создает [большой двоичный](https://developer.mozilla.org/docs/Web/API/Blob) объект из [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) объекта.</span><span class="sxs-lookup"><span data-stu-id="16e94-124">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [`IRandomAccessStream`](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span> <span data-ttu-id="16e94-125">Этот метод следует использовать при работе с `IRandomAccessStream` объектами в приложениях для создания объекта на базе W3C из потока.</span><span class="sxs-lookup"><span data-stu-id="16e94-125">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span> <span data-ttu-id="16e94-126">После создания большого двоичного объекта его можно использовать с [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL-интерфейсами](https://developer.mozilla.org/docs/Web/API/URL)и [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span><span class="sxs-lookup"><span data-stu-id="16e94-126">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span> 

```javascript
var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
```

#### <span data-ttu-id="16e94-127">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-127">Parameters</span></span>

`type` <span data-ttu-id="16e94-128">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-128">[in]</span></span>

|<span data-ttu-id="16e94-129">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-129">Type</span></span> | <span data-ttu-id="16e94-130">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-130">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-131">Строка</span><span class="sxs-lookup"><span data-stu-id="16e94-131">String</span></span> | <span data-ttu-id="16e94-132">Тип контента данных.</span><span class="sxs-lookup"><span data-stu-id="16e94-132">Content type of the data.</span></span> <span data-ttu-id="16e94-133">Эта строка должна иметь формат, заданный в токене типа мультимедиа, определенном в разделе 3,7 из RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="16e94-133">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>

`stream` <span data-ttu-id="16e94-134">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-134">[in]</span></span>

|<span data-ttu-id="16e94-135">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-135">Type</span></span> | <span data-ttu-id="16e94-136">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-136">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-137">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-137">Any</span></span> | <span data-ttu-id="16e94-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) храниться в большом двоичном объекте.</span><span class="sxs-lookup"><span data-stu-id="16e94-138">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>

#### <span data-ttu-id="16e94-139">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-139">Return value</span></span>
|<span data-ttu-id="16e94-140">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-140">Type</span></span> | <span data-ttu-id="16e94-141">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-141">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-142">Большом</span><span class="sxs-lookup"><span data-stu-id="16e94-142">Blob</span></span> | <span data-ttu-id="16e94-143">Новый объект BLOB, содержащий поток.</span><span class="sxs-lookup"><span data-stu-id="16e94-143">New blob object that contains the stream.</span></span>

#### <span data-ttu-id="16e94-144">Исключения</span><span class="sxs-lookup"><span data-stu-id="16e94-144">Exceptions</span></span>
|<span data-ttu-id="16e94-145">Ошибка</span><span class="sxs-lookup"><span data-stu-id="16e94-145">Exception</span></span> | <span data-ttu-id="16e94-146">Ошибка</span><span class="sxs-lookup"><span data-stu-id="16e94-146">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-147">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="16e94-147">TypeMismatchError</span></span> | <span data-ttu-id="16e94-148">Тип узла несовместим с ожидаемым типом параметра.</span><span class="sxs-lookup"><span data-stu-id="16e94-148">The node type is incompatible with the expected parameter type.</span></span> <span data-ttu-id="16e94-149">Для версий более ранних, чем Internet Explorer 10, возвращается TYPE_MISMATCH_ERR.</span><span class="sxs-lookup"><span data-stu-id="16e94-149">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

#### <span data-ttu-id="16e94-150">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-150">Remarks</span></span>
<span data-ttu-id="16e94-151">Создает большой двоичный объект из типов среды выполнения Windows через пространство имен MSApp в объекте Window.</span><span class="sxs-lookup"><span data-stu-id="16e94-151">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span> <span data-ttu-id="16e94-152">Этот метод создает большой двоичный объект, который, по сути, является облегченной оберткой по отношению к объекту, переданному [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) на него.</span><span class="sxs-lookup"><span data-stu-id="16e94-152">This method will create a blob that is essentially a light wrapper over the [`RandomAccessStream`](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span> <span data-ttu-id="16e94-153">Большой двоичный объект владеет временем существования этого потока, и поток будет закрыт при уничтожении большого двоичного объекта.</span><span class="sxs-lookup"><span data-stu-id="16e94-153">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span> 

#### <span data-ttu-id="16e94-154">Пример.</span><span class="sxs-lookup"><span data-stu-id="16e94-154">Example</span></span>

```javascript
var randomAccessStream = dataPackage.GetData("image/bmp");
var blob = window.MSApp.createBlobFromRandomAccessStream("image/bmp", randomAccessStream);
var url = window.URL.createObjectURL(blob, {oneTimeOnly:true});

document.getElementById("imagetag").src = url; 
```

### <span data-ttu-id="16e94-155">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="16e94-155">createDataPackage</span></span>
<span data-ttu-id="16e94-156">Преобразует указанный диапазон пользователя или приложения в фрагмент HTML, к которому можно предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="16e94-156">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackage(object); 
```

#### <span data-ttu-id="16e94-157">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-157">Parameters</span></span>
`object` <span data-ttu-id="16e94-158">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-158">[in]</span></span>

|<span data-ttu-id="16e94-159">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-159">Type</span></span> | <span data-ttu-id="16e94-160">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-160">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-161">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-161">Any</span></span> | <span data-ttu-id="16e94-162">Этот диапазон можно создать из объекта выделения, например: `window.selection.getRangeAt(0)` или вручную.</span><span class="sxs-lookup"><span data-stu-id="16e94-162">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>

#### <span data-ttu-id="16e94-163">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-163">Return value</span></span>
|<span data-ttu-id="16e94-164">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-164">Type</span></span> | <span data-ttu-id="16e94-165">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-165">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-166">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-166">Any</span></span> | <span data-ttu-id="16e94-167">В этом разделе содержится разметка HTML для указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="16e94-167">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="16e94-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-168">Remarks</span></span>
<span data-ttu-id="16e94-169">Этот метод поддерживает только [диапазон объектной модели документов (DOM)](https://developer.mozilla.org/docs/Web/API/Range), а не [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span><span class="sxs-lookup"><span data-stu-id="16e94-169">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span> <span data-ttu-id="16e94-170">Возвращенный пакет данных для указанного диапазона включает HTML-разметку в формате буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="16e94-170">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>

<span data-ttu-id="16e94-171">Для возвращенного пакета данных нет доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="16e94-171">There are no available properties for the returned data package.</span></span>

### <span data-ttu-id="16e94-172">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="16e94-172">createDataPackageFromSelection</span></span> 
<span data-ttu-id="16e94-173">Преобразуются в фрагмент кода HTML, к которому можно предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="16e94-173">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>

```javascript
var retVal = MSApp.createDataPackageFromSelection(); 
```

#### <span data-ttu-id="16e94-174">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-174">Parameters</span></span>
<span data-ttu-id="16e94-175">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="16e94-175">This method has no parameters.</span></span>

#### <span data-ttu-id="16e94-176">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-176">Return value</span></span>
|<span data-ttu-id="16e94-177">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-177">Type</span></span> | <span data-ttu-id="16e94-178">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-178">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-179">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-179">Any</span></span> | <span data-ttu-id="16e94-180">В этом разделе содержится разметка HTML для указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="16e94-180">Contains the HTML markup for the specified range.</span></span>

#### <span data-ttu-id="16e94-181">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-181">Remarks</span></span>
<span data-ttu-id="16e94-182">Возвращенный пакет данных для выделенного фрагмента включает HTML-разметку в формате буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="16e94-182">The returned data package for the selection contains HTML markup in clipboard format.</span></span> <span data-ttu-id="16e94-183">Если вы не выделять ни одного пользователя в пользовательском интерфейсе приложения, функция `createDataPackageFromSelection` возвращает значение null.</span><span class="sxs-lookup"><span data-stu-id="16e94-183">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns null.</span></span>

<span data-ttu-id="16e94-184">Для возвращенного пакета данных нет доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="16e94-184">There are no available properties for the returned data package.</span></span>
 
### <span data-ttu-id="16e94-185">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="16e94-185">createFileFromStorageFile</span></span> 
<span data-ttu-id="16e94-186">Преобразует [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) в стандартный [`File`](https://developer.mozilla.org/docs/Web/API/File) объект W3C.</span><span class="sxs-lookup"><span data-stu-id="16e94-186">Converts a [WinRT](/uwp/api/) [`StorageFile`](/uwp/api/windows.storage.storagefile) to a standard W3C [`File`](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>

```javascript
var retVal = MSApp.createFileFromStorageFile(storageFile); 
```

#### <span data-ttu-id="16e94-187">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-187">Parameters</span></span>
`storageFile` <span data-ttu-id="16e94-188">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-188">[in]</span></span>

|<span data-ttu-id="16e94-189">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-189">Type</span></span> | <span data-ttu-id="16e94-190">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-190">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-191">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-191">Any</span></span> | <span data-ttu-id="16e94-192">Файл, содержащий хранилище.</span><span class="sxs-lookup"><span data-stu-id="16e94-192">Contains the storage file.</span></span>

#### <span data-ttu-id="16e94-193">Исключения</span><span class="sxs-lookup"><span data-stu-id="16e94-193">Exceptions</span></span>
|<span data-ttu-id="16e94-194">Ошибка</span><span class="sxs-lookup"><span data-stu-id="16e94-194">Exception</span></span> | <span data-ttu-id="16e94-195">Ошибка</span><span class="sxs-lookup"><span data-stu-id="16e94-195">Condition</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-196">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="16e94-196">TypeMismatchError</span></span> | <span data-ttu-id="16e94-197">Указана недопустимая ссылка на файл в формате W3C.</span><span class="sxs-lookup"><span data-stu-id="16e94-197">The specified W3C file reference is invalid.</span></span> <span data-ttu-id="16e94-198">Для версий более ранних, чем Internet Explorer 10, возвращается TYPE_MISMATCH_ERR.</span><span class="sxs-lookup"><span data-stu-id="16e94-198">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>

### <span data-ttu-id="16e94-199">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="16e94-199">createStreamFromInputStream</span></span>  

<span data-ttu-id="16e94-200">Создание элемента [`MSStream`](https://msdn.microsoft.com/library/hh772328) FROM [`InputStream`](https://msdn.microsoft.com/library/hh772327) .</span><span class="sxs-lookup"><span data-stu-id="16e94-200">Creates an [`MSStream`](https://msdn.microsoft.com/library/hh772328) from an [`InputStream`](https://msdn.microsoft.com/library/hh772327).</span></span>  


```javascript
var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
```

#### <span data-ttu-id="16e94-201">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-201">Parameters</span></span>
`type` <span data-ttu-id="16e94-202">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-202">[in]</span></span>

|<span data-ttu-id="16e94-203">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-203">Type</span></span> | <span data-ttu-id="16e94-204">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-204">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-205">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-205">DOMString</span></span> | <span data-ttu-id="16e94-206">Тип контента данных.</span><span class="sxs-lookup"><span data-stu-id="16e94-206">Content type of the data.</span></span> <span data-ttu-id="16e94-207">Эта строка должна иметь формат, заданный в токене типа мультимедиа, определенном в разделе 3,7 из RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="16e94-207">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span> <span data-ttu-id="16e94-208">([См. типы MIME,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) IE. text/plain, Text/HTML, Image/JPEG, Image/PNG, Audio/MPEG, Audio/OGG, Audio/\*, видео, MP4 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="16e94-208">([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types) ie. text/plain, text/html, image/jpeg, image/png, audio/mpeg, audio/ogg, audio/\*, video/mp4, etc.).</span></span> 

`inputStream` <span data-ttu-id="16e94-209">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-209">[in]</span></span>

|<span data-ttu-id="16e94-210">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-210">Type</span></span> | <span data-ttu-id="16e94-211">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-211">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-212">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-212">Any</span></span> | <span data-ttu-id="16e94-213">Значение, которое [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) будет храниться в `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="16e94-213">The [`IInputStream`](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>

#### <span data-ttu-id="16e94-214">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-214">Remarks</span></span>
<span data-ttu-id="16e94-215">Этот метод принимает тип содержимого и `IInputStream` ссылку.</span><span class="sxs-lookup"><span data-stu-id="16e94-215">This method takes a content-type, and the `IInputStream` reference.</span></span> <span data-ttu-id="16e94-216">Затем метод проверяет, переданный ли ссылка на поток является экземпляром типа, `IInputStream` а если нет — исключением `DOMException TYPE_MISMATCH_ERR` .</span><span class="sxs-lookup"><span data-stu-id="16e94-216">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span> <span data-ttu-id="16e94-217">Если ошибка не возникнет, `createStreamFromInputStream` создается `MSStream` (из входных данных).</span><span class="sxs-lookup"><span data-stu-id="16e94-217">If no error occurs, `createStreamFromInputStream` creates an `MSStream` (from its inputs).</span></span>

#### <span data-ttu-id="16e94-218">Пример.</span><span class="sxs-lookup"><span data-stu-id="16e94-218">Example</span></span>
<span data-ttu-id="16e94-219">`IInputStream`Можно использовать для создания `MSStream` .</span><span class="sxs-lookup"><span data-stu-id="16e94-219">An `IInputStream` can be used to create an `MSStream`.</span></span> <span data-ttu-id="16e94-220">Как `MSStreams` и объекты по отдельности, все URL-адреса, созданные с помощью `URL.createObjectURL` элемента Image, будут отозваны при первом разрешении.</span><span class="sxs-lookup"><span data-stu-id="16e94-220">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span> <span data-ttu-id="16e94-221">Кроме того, запросы на второй URL-адрес на этом объекте после использования потока завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="16e94-221">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>

```javascript
var inputStream = myInputStream; //get InputStream from socket API, etc.
var stream = MSApp.createStreamFromInputStream("image/bmp", inputstream);
document.getElementById("imagetag").src = URL.createObjectURL(stream); 
```

### <span data-ttu-id="16e94-222">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="16e94-222">execAsyncAtPriority</span></span> 
<span data-ttu-id="16e94-223">Планирует выполнение обратного вызова в более позднее время согласно заданному приоритету.</span><span class="sxs-lookup"><span data-stu-id="16e94-223">Schedules a callback to be executed at a later time according to the given priority.</span></span> 

```javascript
MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
```

#### <span data-ttu-id="16e94-224">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-224">Parameters</span></span>
`asynchronousCallback` <span data-ttu-id="16e94-225">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-225">[in]</span></span>

|<span data-ttu-id="16e94-226">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-226">Type</span></span> | <span data-ttu-id="16e94-227">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-227">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-228">Функция</span><span class="sxs-lookup"><span data-stu-id="16e94-228">Function</span></span> | <span data-ttu-id="16e94-229">Функция обратного вызова, предназначенная для асинхронного выполнения, с указанным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="16e94-229">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>

`priority` <span data-ttu-id="16e94-230">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-230">[in]</span></span>

|<span data-ttu-id="16e94-231">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-231">Type</span></span> | <span data-ttu-id="16e94-232">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-232">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-233">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-233">DOMString</span></span> | <span data-ttu-id="16e94-234">Значение приоритета контекста, для которого выполняется обратный вызов asynchronousCallback.</span><span class="sxs-lookup"><span data-stu-id="16e94-234">The contextual priority value at which the asynchronousCallback callback is run.</span></span> <span data-ttu-id="16e94-235">Смотрите [MSApp константы](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="16e94-235">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="16e94-236">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-236">[in]</span></span>

|<span data-ttu-id="16e94-237">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-237">Type</span></span> | <span data-ttu-id="16e94-238">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-238">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-239">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-239">Any</span></span> | <span data-ttu-id="16e94-240">Необязательный ряд аргументов, передаваемых в функцию обратного вызова synchronousCallback (в параметрах 1 и on).</span><span class="sxs-lookup"><span data-stu-id="16e94-240">An optional series of arguments that are passed to the synchronousCallback callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="16e94-241">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-241">Return value</span></span>
<span data-ttu-id="16e94-242">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="16e94-242">This method does not return a value.</span></span>

#### <span data-ttu-id="16e94-243">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-243">Remarks</span></span>
<span data-ttu-id="16e94-244">Указанная `asynchronousCallback` функция обратного вызова выполняется асинхронно позднее.</span><span class="sxs-lookup"><span data-stu-id="16e94-244">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span> `asynchronousCallback` <span data-ttu-id="16e94-245">будет отправлено согласно указанному приоритету.</span><span class="sxs-lookup"><span data-stu-id="16e94-245">will be dispatched according to the provided priority.</span></span> <span data-ttu-id="16e94-246">Обычный приоритет эквивалентен существующему [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) методу.</span><span class="sxs-lookup"><span data-stu-id="16e94-246">Normal priority is equivalent to the existing [`setImmediate`](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span> <span data-ttu-id="16e94-247">При выполнении обратного вызова текущим контекстным приоритетом задается указанное значение параметра Priority для продолжительности выполнения обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="16e94-247">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>

<span data-ttu-id="16e94-248">`asynchronousCallback`Параметр обратного вызова может быть любой функцией.</span><span class="sxs-lookup"><span data-stu-id="16e94-248">The `asynchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="16e94-249">Если аргументы указаны после `priority` параметра, они будут переданы в функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="16e94-249">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>

<span data-ttu-id="16e94-250">В отличие от него `execAtPriority` , любой объект, возвращенный `asynchronousCallback` функцией обратного вызова, игнорируется (и не возвращается через `execAsyncAtPriority` ).</span><span class="sxs-lookup"><span data-stu-id="16e94-250">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored (and not returned via `execAsyncAtPriority`).</span></span>

### <span data-ttu-id="16e94-251">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="16e94-251">execAtPriority</span></span> 
<span data-ttu-id="16e94-252">Запускает указанную функцию обратного вызова с заданным приоритетом контекста.</span><span class="sxs-lookup"><span data-stu-id="16e94-252">Runs the specified callback function at the given contextual priority.</span></span>

```javascript
var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
```

#### <span data-ttu-id="16e94-253">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-253">Parameters</span></span>
`synchronousCallback` <span data-ttu-id="16e94-254">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-254">[in]</span></span>

|<span data-ttu-id="16e94-255">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-255">Type</span></span> | <span data-ttu-id="16e94-256">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-256">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-257">Функция</span><span class="sxs-lookup"><span data-stu-id="16e94-257">Function</span></span> | <span data-ttu-id="16e94-258">Функция обратного вызова, выполняющаяся синхронно на заданном приоритете контекста.</span><span class="sxs-lookup"><span data-stu-id="16e94-258">The callback function to run synchronously at the given priority contextual priority.</span></span>

`priority` <span data-ttu-id="16e94-259">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-259">[in]</span></span>

|<span data-ttu-id="16e94-260">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-260">Type</span></span> | <span data-ttu-id="16e94-261">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-261">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-262">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-262">DOMString</span></span> | <span data-ttu-id="16e94-263">Указанное значение приоритета, которое будет задано текущим значением приоритета контекста при запуске `synchronousCallback` функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="16e94-263">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span> <span data-ttu-id="16e94-264">Смотрите [MSApp константы](#msapp-constants).</span><span class="sxs-lookup"><span data-stu-id="16e94-264">See [MSApp Constants](#msapp-constants).</span></span>

`args` <span data-ttu-id="16e94-265">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-265">[in]</span></span>

|<span data-ttu-id="16e94-266">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-266">Type</span></span> | <span data-ttu-id="16e94-267">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-267">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-268">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-268">Any</span></span> | <span data-ttu-id="16e94-269">Необязательный ряд аргументов, передаваемых в `synchronousCallback` функцию обратного вызова (в качестве параметров 1 и on).</span><span class="sxs-lookup"><span data-stu-id="16e94-269">An optional series of arguments that are passed to the `synchronousCallback` callback function (as parameters 1 and on).</span></span>

#### <span data-ttu-id="16e94-270">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-270">Return value</span></span>
|<span data-ttu-id="16e94-271">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-271">Type</span></span> | <span data-ttu-id="16e94-272">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-272">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-273">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-273">Any</span></span> | <span data-ttu-id="16e94-274">Возвращает возвращаемое значение `synchronousCallback` обратного вызова (как применимо).</span><span class="sxs-lookup"><span data-stu-id="16e94-274">Returns the return value of the `synchronousCallback` callback (as applicable).</span></span>

#### <span data-ttu-id="16e94-275">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-275">Remarks</span></span>
<span data-ttu-id="16e94-276">Указанный `synchronousCallback` метод обратного вызова выполняется синхронно.</span><span class="sxs-lookup"><span data-stu-id="16e94-276">The provided `synchronousCallback` callback method is execute synchronously.</span></span> <span data-ttu-id="16e94-277">Текущий контекстный приоритет меняется на предоставленное значение приоритета (заданное аргументом Priority) для длительности указанной функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="16e94-277">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span> <span data-ttu-id="16e94-278">После того как функция обратного вызова завершит выполнение, перед вызовом будет возвращено значение Priority (приоритет) `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="16e94-278">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span> <span data-ttu-id="16e94-279">Возвращаемое значение `execAtPriority` является возвращаемым значением метода обратного вызова (как указано).</span><span class="sxs-lookup"><span data-stu-id="16e94-279">The return value from `execAtPriority` is the return value of the callback method (as provided).</span></span>
 
<span data-ttu-id="16e94-280">`synchronousCallback`Параметр обратного вызова может быть любой функцией.</span><span class="sxs-lookup"><span data-stu-id="16e94-280">The `synchronousCallback` callback parameter can be any function.</span></span> <span data-ttu-id="16e94-281">Если после параметра Priority указаны какие либо аргументы, они будут переданы в указанный метод обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="16e94-281">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span> <span data-ttu-id="16e94-282">Если параметр обратного вызова возвращает значение, это значение также становится возвращаемым значением `execAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="16e94-282">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>

#### <span data-ttu-id="16e94-283">Пример.</span><span class="sxs-lookup"><span data-stu-id="16e94-283">Example</span></span>

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

### <span data-ttu-id="16e94-284">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="16e94-284">getCurrentPriority</span></span> 
<span data-ttu-id="16e94-285">Возвращает текущий приоритет по контексту.</span><span class="sxs-lookup"><span data-stu-id="16e94-285">Returns the current contextual priority.</span></span>

```javascript
var retval = MSApp.getCurrentPriority();
```

#### <span data-ttu-id="16e94-286">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-286">Parameters</span></span>
<span data-ttu-id="16e94-287">Нет.</span><span class="sxs-lookup"><span data-stu-id="16e94-287">None.</span></span> 

#### <span data-ttu-id="16e94-288">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-288">Return value</span></span>
|<span data-ttu-id="16e94-289">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-289">Type</span></span> | <span data-ttu-id="16e94-290">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-290">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-291">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-291">DOMString</span></span> | <span data-ttu-id="16e94-292">Возвращаемое значение является одной из строк `MSApp.HIGH` , `MSApp.NORMAL` или `MSApp.IDLE` .</span><span class="sxs-lookup"><span data-stu-id="16e94-292">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>

#### <span data-ttu-id="16e94-293">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-293">Remarks</span></span>
<span data-ttu-id="16e94-294">Этот метод возвращает текущий приоритет контекста (см [`MSApp Constants`](#msapp-constants) .), который можно изменить с помощью `execAtPriority` и `execAsyncAtPriority` .</span><span class="sxs-lookup"><span data-stu-id="16e94-294">This method returns the current contextual priority (see [`MSApp Constants`](#msapp-constants)), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>

#### <span data-ttu-id="16e94-295">Пример.</span><span class="sxs-lookup"><span data-stu-id="16e94-295">Example</span></span>

```javascript
if (MSApp.getCurrentPriority() === MSApp.IDLE) { 
  // YOUR CODE HERE
}
```

### <span data-ttu-id="16e94-296">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="16e94-296">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="16e94-297">Нерекомендуемый синхронный API.</span><span class="sxs-lookup"><span data-stu-id="16e94-297">Synchronous API that has been deprecated.</span></span> <span data-ttu-id="16e94-298">В Windows 10 вы видите `getHtmlPrintDocumentSourceAsync` .</span><span class="sxs-lookup"><span data-stu-id="16e94-298">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span> <span data-ttu-id="16e94-299">Приложения для Windows 8 и 8,1 можно найти в статье MSDN для [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span><span class="sxs-lookup"><span data-stu-id="16e94-299">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="16e94-300">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="16e94-300">getHtmlPrintDocumentSourceAsync</span></span>
<span data-ttu-id="16e94-301">Возвращает исходное содержимое, которое нужно распечатать.</span><span class="sxs-lookup"><span data-stu-id="16e94-301">Returns the source content that is to be printed.</span></span>

#### <span data-ttu-id="16e94-302">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-302">Parameters</span></span>
`htmlDoc` <span data-ttu-id="16e94-303">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-303">[in]</span></span>

|<span data-ttu-id="16e94-304">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-304">Type</span></span> | <span data-ttu-id="16e94-305">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-305">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-306">Документ</span><span class="sxs-lookup"><span data-stu-id="16e94-306">Document</span></span> | <span data-ttu-id="16e94-307">Документ HTML для печати.</span><span class="sxs-lookup"><span data-stu-id="16e94-307">The HTML document to be printed.</span></span> <span data-ttu-id="16e94-308">Это может быть корневой документ, документ в окне IFRAME, фрагмент документа или документ SVG.</span><span class="sxs-lookup"><span data-stu-id="16e94-308">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span> <span data-ttu-id="16e94-309">Имейте в виду, что htmlDoc должен быть документом, а не элементом.</span><span class="sxs-lookup"><span data-stu-id="16e94-309">Be aware that htmlDoc must be a document, not an element.</span></span>

#### <span data-ttu-id="16e94-310">Пример 1</span><span class="sxs-lookup"><span data-stu-id="16e94-310">Example 1</span></span>

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

#### <span data-ttu-id="16e94-311">Пример 2</span><span class="sxs-lookup"><span data-stu-id="16e94-311">Example 2</span></span>

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

### <span data-ttu-id="16e94-312">getViewId</span><span class="sxs-lookup"><span data-stu-id="16e94-312">getViewId</span></span> 
<span data-ttu-id="16e94-313">Поддержка нескольких окон.</span><span class="sxs-lookup"><span data-stu-id="16e94-313">Support for multiple windows.</span></span> 

> [!NOTE] 
> <span data-ttu-id="16e94-314">В Win 8.1 JavaScript для приложений UWP поддерживалось несколько окон, использующих API MSApp DOM, которые теперь depricated.</span><span class="sxs-lookup"><span data-stu-id="16e94-314">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span> <span data-ttu-id="16e94-315">Для Windows 10, использование `window.open` `window` и новый `MSApp.getViewId` .</span><span class="sxs-lookup"><span data-stu-id="16e94-315">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>

| <span data-ttu-id="16e94-316">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-316">Description</span></span> |<span data-ttu-id="16e94-317">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="16e94-317">Windows 10</span></span> | <span data-ttu-id="16e94-318">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="16e94-318">Windows 8.1</span></span> |  
|:---- |:---- |:--- |  
| <span data-ttu-id="16e94-319">Создание нового окна</span><span class="sxs-lookup"><span data-stu-id="16e94-319">Create new window</span></span> | [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) | [`MSApp.createNewView`](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
|<span data-ttu-id="16e94-320">Новый объект Window</span><span class="sxs-lookup"><span data-stu-id="16e94-320">New window object</span></span> | [`window`](https://developer.mozilla.org/docs/Web/API/Window) |[`MSAppView`](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  

```javascript
var retval = MSApp.getViewId(window); 
```

#### <span data-ttu-id="16e94-321">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-321">Parameters</span></span>
`window`

|<span data-ttu-id="16e94-322">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-322">Type</span></span> | <span data-ttu-id="16e94-323">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-323">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-324">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-324">DOMString</span></span> | <span data-ttu-id="16e94-325">Объект, представляющий окно, содержащее документ DOM.</span><span class="sxs-lookup"><span data-stu-id="16e94-325">An object representing a window containing a DOM document.</span></span> | 

#### <span data-ttu-id="16e94-326">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-326">Return value</span></span>

`viewId`

|<span data-ttu-id="16e94-327">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-327">Type</span></span> | <span data-ttu-id="16e94-328">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-328">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-329">Число</span><span class="sxs-lookup"><span data-stu-id="16e94-329">Number</span></span> | <span data-ttu-id="16e94-330">Может использоваться с различными [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API.</span><span class="sxs-lookup"><span data-stu-id="16e94-330">Can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

#### <span data-ttu-id="16e94-331">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-331">Remarks</span></span>
<span data-ttu-id="16e94-332">Используйте [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) и [`window`](https://developer.mozilla.org/docs/Web/API/Window) для создания новых окон, но для взаимодействия с API WinRT добавьте `MSApp.getViewId` API.</span><span class="sxs-lookup"><span data-stu-id="16e94-332">Use [`window.open`](https://developer.mozilla.org/docs/Web/API/Window/open) and [`window`](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span> <span data-ttu-id="16e94-333">Он принимает `window` объект в качестве параметра и возвращает `viewId` число, которое можно использовать с различными [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) API.</span><span class="sxs-lookup"><span data-stu-id="16e94-333">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [`Windows.UI.ViewManagement.ApplicationViewSwitcher`](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span> 

##### <span data-ttu-id="16e94-334">Задержка отображения</span><span class="sxs-lookup"><span data-stu-id="16e94-334">Delaying Visibility</span></span> 
<span data-ttu-id="16e94-335">Представления в WinRT, как правило, отображаются в скрытом режиме, а конечный разработчик использует нечто вроде `TryShowAsStandaloneAsync` для отображения представления после его полной подготовки.</span><span class="sxs-lookup"><span data-stu-id="16e94-335">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span> <span data-ttu-id="16e94-336">В Интернете `window.open` показывает окно немедленно, и пользователь может просматривать содержимое, которое загружается и отображается.</span><span class="sxs-lookup"><span data-stu-id="16e94-336">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span> <span data-ttu-id="16e94-337">Если вы хотите, чтобы новое приложение Windows было похоже на представления в WinRT и не отображалось сразу, мы добавили `window.open` параметр.</span><span class="sxs-lookup"><span data-stu-id="16e94-337">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span> <span data-ttu-id="16e94-338">Пример</span><span class="sxs-lookup"><span data-stu-id="16e94-338">For example:</span></span>
`let newWindow = window.open("https://example.com", null, "msHideView=yes");`

##### <span data-ttu-id="16e94-339">Различия между основными окнами</span><span class="sxs-lookup"><span data-stu-id="16e94-339">Primary Window Differences</span></span>
<span data-ttu-id="16e94-340">Основное окно, которое первоначально открывается в операционной системе, отличается от того, какое приложение открывается для них.</span><span class="sxs-lookup"><span data-stu-id="16e94-340">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span> 

|<span data-ttu-id="16e94-341">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-341">Description</span></span> | <span data-ttu-id="16e94-342">Основной</span><span class="sxs-lookup"><span data-stu-id="16e94-342">Primary</span></span> | <span data-ttu-id="16e94-343">Дополнительная</span><span class="sxs-lookup"><span data-stu-id="16e94-343">Secondary</span></span> |
|:---- |:--- |:--- |
|<span data-ttu-id="16e94-344">Window. Open</span><span class="sxs-lookup"><span data-stu-id="16e94-344">window.open</span></span> | <span data-ttu-id="16e94-345">Разрешено</span><span class="sxs-lookup"><span data-stu-id="16e94-345">Allowed</span></span> | <span data-ttu-id="16e94-346">Disallowed</span><span class="sxs-lookup"><span data-stu-id="16e94-346">Disallowed</span></span> |
|<span data-ttu-id="16e94-347">Window. Close</span><span class="sxs-lookup"><span data-stu-id="16e94-347">window.close</span></span> | <span data-ttu-id="16e94-348">Закрыть приложение</span><span class="sxs-lookup"><span data-stu-id="16e94-348">Close app</span></span> | <span data-ttu-id="16e94-349">Закрыть окно</span><span class="sxs-lookup"><span data-stu-id="16e94-349">Close window</span></span> |
| <span data-ttu-id="16e94-350">Ограничения навигации</span><span class="sxs-lookup"><span data-stu-id="16e94-350">Navigation restrictions</span></span> | <span data-ttu-id="16e94-351">Только ACUR</span><span class="sxs-lookup"><span data-stu-id="16e94-351">ACUR only</span></span> | <span data-ttu-id="16e94-352">Без ограничений</span><span class="sxs-lookup"><span data-stu-id="16e94-352">No restrictions</span></span> |

<span data-ttu-id="16e94-353">Ограничение, не позволяющее открыть вспомогательную систему Windows, может измениться в будущем в зависимости от [отзыва](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span><span class="sxs-lookup"><span data-stu-id="16e94-353">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>

##### <span data-ttu-id="16e94-354">Ограничения для связи с одинаковыми исходными данными</span><span class="sxs-lookup"><span data-stu-id="16e94-354">Same Origin Communication Restrictions</span></span> 
<span data-ttu-id="16e94-355">Существует сложная техническая неполадка, препятствующая надлежащей поддержке синхронных и идентичных вызовов между окнами и сценариями.</span><span class="sxs-lookup"><span data-stu-id="16e94-355">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span> <span data-ttu-id="16e94-356">При открытии одного и того же исходного окна сценарий в одном окне может напрямую вызывать функции в другом окне, а некоторые из этих вызовов завершатся сбоем.</span><span class="sxs-lookup"><span data-stu-id="16e94-356">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span> `postMessage` <span data-ttu-id="16e94-357">звонки прекрасно работают и являются рекомендуемым способом, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="16e94-357">calls work just fine and is the recommended way to do things if possible.</span></span> <span data-ttu-id="16e94-358">Чтобы улучшить работу, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="16e94-358">Work to improve this issue is in progress.</span></span>


### <span data-ttu-id="16e94-359">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="16e94-359">isTaskScheduledAtPriorityOrHigher</span></span> 
<span data-ttu-id="16e94-360">Возвращает логическое значение, определяющее наличие ожидающих трудозатрат на заданном уровне приоритета или более высоком.</span><span class="sxs-lookup"><span data-stu-id="16e94-360">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>

```javascript
var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
```

#### <span data-ttu-id="16e94-361">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-361">Parameters</span></span>
`priority` <span data-ttu-id="16e94-362">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-362">[in]</span></span>

|<span data-ttu-id="16e94-363">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-363">Type</span></span> | <span data-ttu-id="16e94-364">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-364">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-365">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-365">DOMString</span></span> | <span data-ttu-id="16e94-366">Значение приоритета (в разделе [константы MSApp](#msapp-constants)) с указанием уровня приоритета и более поздних значений для запроса всех незавершенных трудозатрат в очереди.</span><span class="sxs-lookup"><span data-stu-id="16e94-366">A priority value (see [MSApp Constants](#msapp-constants)) specifying the priority level and above to query for any outstanding queued work.</span></span>

#### <span data-ttu-id="16e94-367">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-367">Return value</span></span>
|<span data-ttu-id="16e94-368">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-368">Type</span></span> | <span data-ttu-id="16e94-369">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-369">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-370">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="16e94-370">Boolean</span></span> | <span data-ttu-id="16e94-371">Возвращает `true` значение, если в очереди есть трудозатраты с указанным уровнем приоритета или выше, `false` в противном случае.</span><span class="sxs-lookup"><span data-stu-id="16e94-371">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>

#### <span data-ttu-id="16e94-372">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-372">Remarks</span></span>
<span data-ttu-id="16e94-373">Этот `isTaskScheduledAtPriorityOrHigher` метод предоставляет средства для кода JavaScript, чтобы определить, есть ли ожидающие трудозатраты на различных уровнях приоритета (или выше), с целью, по которой код JavaScript может получить повышенную приоритетную работу.</span><span class="sxs-lookup"><span data-stu-id="16e94-373">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels (or above) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>

#### <span data-ttu-id="16e94-374">Пример.</span><span class="sxs-lookup"><span data-stu-id="16e94-374">Example</span></span>

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

### <span data-ttu-id="16e94-375">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="16e94-375">pageHandlesAllApplicationActivations</span></span>
<span data-ttu-id="16e94-376">Используется, чтобы избежать обновления начального пути (перезагрузка страницы) перед каждым событием активации (IE. щелчок на уведомлении или закрепленной плитке).</span><span class="sxs-lookup"><span data-stu-id="16e94-376">Used to avoid a refresh of the start path (page reload) before every activate event (ie. clicking a notification or a pinned tile).</span></span> 

#### <span data-ttu-id="16e94-377">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-377">Parameters</span></span>

|<span data-ttu-id="16e94-378">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-378">Type</span></span> | <span data-ttu-id="16e94-379">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-379">Description</span></span> |
|:---- |:--- |
<span data-ttu-id="16e94-380">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="16e94-380">Boolean</span></span> | <span data-ttu-id="16e94-381">Используется `MSApp.pageHandlesAllApplicationActivations(true)` для постоянного пропуска обновления пути начала (повторной загрузки страницы), а также для обработки `WebUIApplication` события activated.</span><span class="sxs-lookup"><span data-stu-id="16e94-381">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span> <span data-ttu-id="16e94-382">Требует, чтобы все страницы обрабатывали события активации отдельно.</span><span class="sxs-lookup"><span data-stu-id="16e94-382">Requires that all pages handle activation events separately.</span></span> <span data-ttu-id="16e94-383">Определяя этот метод как `true` , щелчок активированного события (например, notificaiton) не приведет к повторной загрузке, очень важно для одностраничных приложений, в которых не требуется перегрузка страниц.</span><span class="sxs-lookup"><span data-stu-id="16e94-383">By defining this method as `true`, clicking an activated event (like a notificaiton) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>

#### <span data-ttu-id="16e94-384">Пример.</span><span class="sxs-lookup"><span data-stu-id="16e94-384">Example</span></span> 

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

### <span data-ttu-id="16e94-385">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="16e94-385">suppressSubdownloadCredentialPrompts</span></span> 
<span data-ttu-id="16e94-386">Определяет, отключаются ли в приложении возможные запросы на проверку подлинности при загрузке ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16e94-386">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>

```javascript
MSApp.suppressSubdownloadCredentialPrompts(suppress); 
```

#### <span data-ttu-id="16e94-387">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-387">Parameters</span></span>
`suppress` <span data-ttu-id="16e94-388">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-388">[in]</span></span>

|<span data-ttu-id="16e94-389">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-389">Type</span></span> | <span data-ttu-id="16e94-390">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-390">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-391">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="16e94-391">Boolean</span></span> | <span data-ttu-id="16e94-392">Значение true подавляет возможные запросы на проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="16e94-392">A value of true suppresses potential authentication prompts.</span></span> <span data-ttu-id="16e94-393">Если задано значение false, запросы на проверку подлинности от пользователя не отключаются.</span><span class="sxs-lookup"><span data-stu-id="16e94-393">A value of false does not suppress any potential authentication prompts from the user.</span></span>

#### <span data-ttu-id="16e94-394">Значение Returan</span><span class="sxs-lookup"><span data-stu-id="16e94-394">Returan value</span></span>
<span data-ttu-id="16e94-395">Нет.</span><span class="sxs-lookup"><span data-stu-id="16e94-395">None.</span></span>

#### <span data-ttu-id="16e94-396">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-396">Remarks</span></span>
<span data-ttu-id="16e94-397">Этот `suppressSubdownloadCredentialPrompts` метод определяет, будет ли приложение подавить запросы на проверку подлинности при загрузке ресурсов.</span><span class="sxs-lookup"><span data-stu-id="16e94-397">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span> <span data-ttu-id="16e94-398">По умолчанию запросы учетных данных не отключаются.</span><span class="sxs-lookup"><span data-stu-id="16e94-398">The default behavior is to not suppress credential prompts.</span></span>

`suppressSubdownloadCredentialPrompts` <span data-ttu-id="16e94-399">предназначен для использования приложениями, которые могут загружать чрезмерное количество ресурсов, требующих проверки подлинности, например почтового приложения (которое может содержать информационный бюллетень с несколькими изображениями, требующих проверки подлинности).</span><span class="sxs-lookup"><span data-stu-id="16e94-399">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app (which could contain a newsletter containing a number of images where each image requires authentication).</span></span>

<span data-ttu-id="16e94-400">При подавлении запросов учетных данных диалоговые окна для проверки подлинности на серверах не отображаются при доступе к ресурсам, требующим проверки подлинности, а сам ресурс не загружается.</span><span class="sxs-lookup"><span data-stu-id="16e94-400">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span> <span data-ttu-id="16e94-401">Обратите внимание, что `suppressSubdownloadCredentialPrompts` не влияет на другие возможные запросы, такие как проверка подлинности прокси-сервера или запросов на сертификацию клиента, а также не влияет на XHR.</span><span class="sxs-lookup"><span data-stu-id="16e94-401">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>

<span data-ttu-id="16e94-402">Имейте в виду, что `suppressSubdownloadCredentialPrompts` влияют на все содержимое приложения, включая содержимое, размещенное в `webview` элементе.</span><span class="sxs-lookup"><span data-stu-id="16e94-402">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>
 
<span data-ttu-id="16e94-403">**Внимание!**  Запрос учетных данных кэшируется.</span><span class="sxs-lookup"><span data-stu-id="16e94-403">**Important:**  Credential prompt decisions are cached.</span></span> <span data-ttu-id="16e94-404">Таким образом, несмотря на то, что запросы учетных данных вступят в силу немедленно, для того чтобы подавить их, возможно, потребуется перезагрузить документ, чтобы он вступил в силу.</span><span class="sxs-lookup"><span data-stu-id="16e94-404">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>

#### <span data-ttu-id="16e94-405">Пример.</span><span class="sxs-lookup"><span data-stu-id="16e94-405">Example</span></span>

```javascript
/ Set to true to suppress potenial credential prompts:
MSApp.suppressSubdownloadCredentialPrompts(true); 
// Now one can load content or navigate iframe/webview to some other site.
```

### <span data-ttu-id="16e94-406">terminateApp</span><span class="sxs-lookup"><span data-stu-id="16e94-406">terminateApp</span></span>
<span data-ttu-id="16e94-407">Завершение работы текущего приложения и создание отчета об ошибке.</span><span class="sxs-lookup"><span data-stu-id="16e94-407">Terminates the current application and generates a failure report.</span></span> 

```javascript
MSApp.terminateApp(error); 
```

#### <span data-ttu-id="16e94-408">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-408">Parameters</span></span>
`error` <span data-ttu-id="16e94-409">возврата</span><span class="sxs-lookup"><span data-stu-id="16e94-409">[in]</span></span>

<span data-ttu-id="16e94-410">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-410">Type</span></span> | <span data-ttu-id="16e94-411">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-411">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-412">Ошибка</span><span class="sxs-lookup"><span data-stu-id="16e94-412">Error</span></span> | <span data-ttu-id="16e94-413">`Error`Объект, который можно использовать для описания ошибки, которая вызвала завершение.</span><span class="sxs-lookup"><span data-stu-id="16e94-413">An `Error` object that you can use to describe the error that triggered the termination.</span></span> <span data-ttu-id="16e94-414">`Error`Объект должен содержать число, описание и свойства стека; отчет об ошибке не создается, если объект не содержит этих свойств.</span><span class="sxs-lookup"><span data-stu-id="16e94-414">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>

#### <span data-ttu-id="16e94-415">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-415">Return value</span></span>
<span data-ttu-id="16e94-416">Нет.</span><span class="sxs-lookup"><span data-stu-id="16e94-416">None.</span></span>

#### <span data-ttu-id="16e94-417">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16e94-417">Remarks</span></span>
<span data-ttu-id="16e94-418">Если проблема, о которой сообщается, `terminateApp` становится одной из первых 5 проблем приложения, она будет отображаться на странице качества приложения.</span><span class="sxs-lookup"><span data-stu-id="16e94-418">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>

#### <span data-ttu-id="16e94-419">Пример.</span><span class="sxs-lookup"><span data-stu-id="16e94-419">Example</span></span>
<span data-ttu-id="16e94-420">Этот пример вызывается `terminateApp` , когда возникает исключение.</span><span class="sxs-lookup"><span data-stu-id="16e94-420">This example calls `terminateApp` when an exception is encountered.</span></span> <span data-ttu-id="16e94-421">Он использует `Error` объект, указанный при перехвате исключения.</span><span class="sxs-lookup"><span data-stu-id="16e94-421">It uses the `Error` object provided when you catch an exception.</span></span> 

```javascript
try {  
        var obj2 = null;  
        obj2.val = 5;  
    }  
    catch(e) {  
        window.MSApp.terminateApp(e);  
    }  
```

### <span data-ttu-id="16e94-422">Константы MSApp</span><span class="sxs-lookup"><span data-stu-id="16e94-422">MSApp Constants</span></span>
<span data-ttu-id="16e94-423">Допустимые значения приоритетов `execAsyncAtPriority` , связанные с,, `execAtPriority` `getCurrentPriority` и `isTaskScheduldAtPriorityOrHigher` .</span><span class="sxs-lookup"><span data-stu-id="16e94-423">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>

#### <span data-ttu-id="16e94-424">Текущие</span><span class="sxs-lookup"><span data-stu-id="16e94-424">Current</span></span>
`current`

|<span data-ttu-id="16e94-425">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-425">Type</span></span> | <span data-ttu-id="16e94-426">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-426">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-427">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-427">DOMString</span></span> | <span data-ttu-id="16e94-428">Когда `current` используется в соответствующем методе (см. также раздел), при выполнении запрошенной операции метод будет использовать текущий приоритет по контексту.</span><span class="sxs-lookup"><span data-stu-id="16e94-428">When `current` is used with the appropriate method (See also section), the method will use the current contextual priority when executing the requested operation.</span></span>

#### <span data-ttu-id="16e94-429">Высока</span><span class="sxs-lookup"><span data-stu-id="16e94-429">High</span></span>
`high`

|<span data-ttu-id="16e94-430">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-430">Type</span></span> | <span data-ttu-id="16e94-431">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-431">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-432">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-432">DOMString</span></span> | <span data-ttu-id="16e94-433">Когда `high` используется в соответствующем методе (см. также раздел), метод будет использовать более высокий приоритет при выполнении запрошенной операции и будет отправлять операцию перед всеми существующими нормальными приоритетами трудозатрат.</span><span class="sxs-lookup"><span data-stu-id="16e94-433">When `high` is used with the appropriate method (See also section), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>

#### <span data-ttu-id="16e94-434">Состояние Idle (в покое)</span><span class="sxs-lookup"><span data-stu-id="16e94-434">Idle</span></span>
`idle`

|<span data-ttu-id="16e94-435">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-435">Type</span></span> | <span data-ttu-id="16e94-436">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-436">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-437">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-437">DOMString</span></span> | <span data-ttu-id="16e94-438">Когда `ideal` используется в соответствующем методе (см. также раздел), метод будет использовать меньше обычного приоритета при выполнении запрошенной операции и будет обрабатывать операцию после того, как все существующие обычные приоритеты будут выполняться.</span><span class="sxs-lookup"><span data-stu-id="16e94-438">When `ideal` is used with the appropriate method (See also section), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>

#### <span data-ttu-id="16e94-439">Обычный</span><span class="sxs-lookup"><span data-stu-id="16e94-439">Normal</span></span>
`normal`

|<span data-ttu-id="16e94-440">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-440">Type</span></span> | <span data-ttu-id="16e94-441">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-441">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-442">DOMString</span><span class="sxs-lookup"><span data-stu-id="16e94-442">DOMString</span></span> | <span data-ttu-id="16e94-443">Когда `normal` используется в соответствующем методе (см. также раздел), метод будет использовать обычный существующий приоритет при выполнении запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="16e94-443">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>

#### <span data-ttu-id="16e94-444">Пример.</span><span class="sxs-lookup"><span data-stu-id="16e94-444">Example</span></span>

```javascript
if (window.MSApp.CURRENT) {
  document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
}
```

#### <span data-ttu-id="16e94-445">Требования</span><span class="sxs-lookup"><span data-stu-id="16e94-445">Requirements</span></span>
|<span data-ttu-id="16e94-446">IDL</span><span class="sxs-lookup"><span data-stu-id="16e94-446">IDL</span></span> | <span data-ttu-id="16e94-447">MSHTML. idl</span><span class="sxs-lookup"><span data-stu-id="16e94-447">Mshtml.idl</span></span> |
|:---- |:--- |

## <span data-ttu-id="16e94-448">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="16e94-448">MSAppAsyncOperation</span></span>

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```

### <span data-ttu-id="16e94-449">start</span><span class="sxs-lookup"><span data-stu-id="16e94-449">start</span></span>
<span data-ttu-id="16e94-450">Запускает `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="16e94-450">Starts the `MSAppAsyncOperation`.</span></span>

```javascript
var retval = MSAppAsyncOperation.start();
```

#### <span data-ttu-id="16e94-451">Параметры</span><span class="sxs-lookup"><span data-stu-id="16e94-451">Parameters</span></span>
<span data-ttu-id="16e94-452">Нет.</span><span class="sxs-lookup"><span data-stu-id="16e94-452">None.</span></span>

#### <span data-ttu-id="16e94-453">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16e94-453">Return value</span></span>
<span data-ttu-id="16e94-454">Нет.</span><span class="sxs-lookup"><span data-stu-id="16e94-454">None.</span></span>

#### <span data-ttu-id="16e94-455">Свойства</span><span class="sxs-lookup"><span data-stu-id="16e94-455">Properties</span></span>
`error` <span data-ttu-id="16e94-456">Property</span><span class="sxs-lookup"><span data-stu-id="16e94-456">property</span></span>

|<span data-ttu-id="16e94-457">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-457">Type</span></span> | <span data-ttu-id="16e94-458">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-458">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-459">DOMError</span><span class="sxs-lookup"><span data-stu-id="16e94-459">DOMError</span></span> | <span data-ttu-id="16e94-460">Представляет ошибку `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="16e94-460">Represents an error in `MSAppAsyncOperation`.</span></span>

```javascript
p = object.error
```

`oncomplete` <span data-ttu-id="16e94-461">Property</span><span class="sxs-lookup"><span data-stu-id="16e94-461">property</span></span>

|<span data-ttu-id="16e94-462">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-462">Type</span></span> | <span data-ttu-id="16e94-463">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-463">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-464">EventHandler</span><span class="sxs-lookup"><span data-stu-id="16e94-464">EventHandler</span></span> | <span data-ttu-id="16e94-465">Свойство для установки обработчика событий по завершении `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="16e94-465">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.oncomplete
```

`onerror` <span data-ttu-id="16e94-466">Property</span><span class="sxs-lookup"><span data-stu-id="16e94-466">property</span></span>

|<span data-ttu-id="16e94-467">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-467">Type</span></span> | <span data-ttu-id="16e94-468">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-468">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-469">EventHandler</span><span class="sxs-lookup"><span data-stu-id="16e94-469">EventHandler</span></span> | <span data-ttu-id="16e94-470">Свойство для установки обработчика событий при возникновении ошибки `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="16e94-470">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>

```javascript
p = object.onerror
```

`readyState` <span data-ttu-id="16e94-471">Property</span><span class="sxs-lookup"><span data-stu-id="16e94-471">property</span></span>

|<span data-ttu-id="16e94-472">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-472">Type</span></span> | <span data-ttu-id="16e94-473">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-473">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-474">Число</span><span class="sxs-lookup"><span data-stu-id="16e94-474">Number</span></span> | <span data-ttu-id="16e94-475">Представляет состояние асинхронной операции в приложении для Windows с помощью JavaScript.</span><span class="sxs-lookup"><span data-stu-id="16e94-475">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span> <span data-ttu-id="16e94-476">Возможны следующие значения: запущен [0], завершен [1], ошибка [2].</span><span class="sxs-lookup"><span data-stu-id="16e94-476">Values include: Started[0], Completed[1], Error[2].</span></span>

```javascript
p = object.readyState
```

`result` <span data-ttu-id="16e94-477">Property</span><span class="sxs-lookup"><span data-stu-id="16e94-477">property</span></span>

|<span data-ttu-id="16e94-478">Тип</span><span class="sxs-lookup"><span data-stu-id="16e94-478">Type</span></span> | <span data-ttu-id="16e94-479">Описание</span><span class="sxs-lookup"><span data-stu-id="16e94-479">Description</span></span> |
|:---- |:--- |
|<span data-ttu-id="16e94-480">Любой</span><span class="sxs-lookup"><span data-stu-id="16e94-480">Any</span></span> |<span data-ttu-id="16e94-481">Представляет результат `MSAppAsyncOperation` .</span><span class="sxs-lookup"><span data-stu-id="16e94-481">Represents the result of `MSAppAsyncOperation`.</span></span>

```javascript
p = object.result
```
