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
# <span data-ttu-id="b83ce-105">MSApp</span><span class="sxs-lookup"><span data-stu-id="b83ce-105">MSApp</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="b83ce-106">Объект MSApp и его участники поддерживаются только для приложений Windows с использованием JavaScript \(включая доступ к функциям API Windows\).</span><span class="sxs-lookup"><span data-stu-id="b83ce-106">The MSApp object and its members are supported only for Windows apps using JavaScript \(including PWAs accessing Windows API features\).</span></span>  <span data-ttu-id="b83ce-107">Объект MSApp существует только в локальном контексте HTML-документа, загруженного с помощью схемы MS-appx URI; В противном случае объект отсутствует (и, соответствует ни одному из методов и свойств).</span><span class="sxs-lookup"><span data-stu-id="b83ce-107">The MSApp object only exists in the local context of an HTML document in a Windows app loaded via the ms-appx URI scheme; otherwise, the object doesn't exist (and consequently, none of its methods and properties are available).</span></span>  

<span data-ttu-id="b83ce-108">В ней предусмаатываются функции, которые помогают создавать [BLOB-объекты](https://developer.mozilla.org/docs/Web/API/Blob) [и MSStream.](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="b83ce-108">It provides helper functions that enable you to create [Blob](https://developer.mozilla.org/docs/Web/API/Blob) and [MSStream](https://msdn.microsoft.com/library/hh772328(v=vs.85).aspx) objects.</span></span>  

```javascript
var result = MSApp.method;
```  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="b83ce-109">Методы</span><span class="sxs-lookup"><span data-stu-id="b83ce-109">Methods</span></span>](#msapp-methods)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b83ce-110">[clearTemporaryWebDataAsync,](#cleartemporarywebdataasync) [createBlobFromRandomAccessSream,](#createblobfromrandomaccessstream) [createDataPackage,](#createdatapackage) [createDataPackageFromSelection,](#createdatapackagefromselection) [createFileFromStorageFile,](#createfilefromstoragefile) [createStreamFromInputStream,](#createstreamfrominputstream) [execAsyncAtPriority,](#execasyncatpriority) [execAtPriority, execAtP приоритет,](#execatpriority) [getCurrentPriity,](#getcurrentpriority) [getWPrintDocumentSource,](#gethtmlprintdocumentsource)[getHtmlPrintDocumentSourceAsynce,](#gethtmlprintdocumentsourceasync) [getViewId,](#getviewid) [isTaskScheduledAtPriityOrHigher,](#istaskscheduledatpriorityorhigher) [pageHandlesAllApplicationActivations,](#pagehandlesallapplicationactivations) [suppressSubdownloadCredentialPrompts,](#suppresssubdownloadcredentialprompts) [terminateApps, getinateApp.](#terminateapp)</span><span class="sxs-lookup"><span data-stu-id="b83ce-110">[clearTemporaryWebDataAsync](#cleartemporarywebdataasync), [createBlobFromRandomAccessSream](#createblobfromrandomaccessstream), [createDataPackage](#createdatapackage), [createDataPackageFromSelection](#createdatapackagefromselection), [createFileFromStorageFile](#createfilefromstoragefile), [createStreamFromInputStream](#createstreamfrominputstream), [execAsyncAtPriority](#execasyncatpriority), [execAtPriority](#execatpriority), [getCurrentPriority](#getcurrentpriority), [getHtmlPrintDocumentSource](#gethtmlprintdocumentsource),[getHtmlPrintDocumentSourceAsynce](#gethtmlprintdocumentsourceasync), [getViewId](#getviewid), [isTaskScheduledAtPriorityOrHigher](#istaskscheduledatpriorityorhigher), [pageHandlesAllApplicationActivations](#pagehandlesallapplicationactivations), [suppressSubdownloadCredentialPrompts](#suppresssubdownloadcredentialprompts), [terminateApp](#terminateapp).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b83ce-111">Константы</span><span class="sxs-lookup"><span data-stu-id="b83ce-111">Constants</span></span>](#msapp-constants)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="b83ce-112">[текущий,](#current) [высокий,](#high) [статус,](#idle) [нормально.](#normal)</span><span class="sxs-lookup"><span data-stu-id="b83ce-112">[current](#current), [high](#high), [idle](#idle), [normal](#normal).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="b83ce-113">Интерфейс MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="b83ce-113">MSAppAsyncOperation interface</span></span>](#msappasyncoperation)  
   :::column-end:::
   :::column span="2":::
      [<span data-ttu-id="b83ce-114">start</span><span class="sxs-lookup"><span data-stu-id="b83ce-114">start</span></span>](#start)  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="b83ce-115">Методы MSApp</span><span class="sxs-lookup"><span data-stu-id="b83ce-115">MSApp methods</span></span>  

### <span data-ttu-id="b83ce-116">clearTemporaryWebDataAsync</span><span class="sxs-lookup"><span data-stu-id="b83ce-116">clearTemporaryWebDataAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-117">Удаление и индексирование данных из кэша и индексированных данных DB для приложения или [WebView.](../../webview.md)</span><span class="sxs-lookup"><span data-stu-id="b83ce-117">Clears cache and indexedDB data for the app or [WebView](../../webview.md).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.clearTemporaryWebDataAsync(#); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-118">Parameters</span></span>**  
      
      <span data-ttu-id="b83ce-119">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b83ce-119">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-120">Return value</span></span>**  
      
      <span data-ttu-id="b83ce-121">Тип: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span><span class="sxs-lookup"><span data-stu-id="b83ce-121">Type: [IAsyncAction](/uwp/api/windows.foundation.iasyncaction)</span></span>  
      
      <span data-ttu-id="b83ce-122">Представляет асинхронное действие.</span><span class="sxs-lookup"><span data-stu-id="b83ce-122">Represents an asynchronous action.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-123">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-123">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-124">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-124">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-125">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-126">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-126">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-127">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-127">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b83ce-128">createBlobFromRandomAccessStream</span><span class="sxs-lookup"><span data-stu-id="b83ce-128">createBlobFromRandomAccessStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-129">Создает [Blob-объект](https://developer.mozilla.org/docs/Web/API/Blob) из [объекта IRandomAccessStream.](/uwp/api/Windows.Storage.Streams.IRandomAccessStream)</span><span class="sxs-lookup"><span data-stu-id="b83ce-129">Creates a [Blob](https://developer.mozilla.org/docs/Web/API/Blob) from an [IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) object.</span></span>  <span data-ttu-id="b83ce-130">Этот способ следует использовать при работе с объектами в приложениях, чтобы создать на его основе объект `IRandomAccessStream` W3C.</span><span class="sxs-lookup"><span data-stu-id="b83ce-130">This method should be used when dealing with `IRandomAccessStream` objects in apps in order to create a W3C based object from the stream.</span></span>  <span data-ttu-id="b83ce-131">После создания большого двоичного объекта его можно использовать с [FileReader,](https://developer.mozilla.org/docs/Web/API/FileReader) [API-каналами](https://developer.mozilla.org/docs/Web/API/URL) [и XMLHttpRequest.](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest)</span><span class="sxs-lookup"><span data-stu-id="b83ce-131">Once the blob is created, it can be used with the [FileReader](https://developer.mozilla.org/docs/Web/API/FileReader), [URL APIs](https://developer.mozilla.org/docs/Web/API/URL), and [XMLHttpRequest](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createBlobFromRandomAccessStream(type, stream); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-132">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-132">Parameters</span></span>**  
      
      `type` <span data-ttu-id="b83ce-133">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-133">[in]</span></span>  
      
      | <span data-ttu-id="b83ce-134">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-134">Type</span></span> | <span data-ttu-id="b83ce-135">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-135">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-136">Строка</span><span class="sxs-lookup"><span data-stu-id="b83ce-136">String</span></span> | <span data-ttu-id="b83ce-137">Тип контента данных;</span><span class="sxs-lookup"><span data-stu-id="b83ce-137">Content type of the data.</span></span>  <span data-ttu-id="b83ce-138">Эта строка должна быть указана в формате, заданном в маркере 3.7 из RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="b83ce-138">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  |  
      
      `stream` <span data-ttu-id="b83ce-139">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-139">[in]</span></span>  
      
      | <span data-ttu-id="b83ce-140">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-140">Type</span></span> | <span data-ttu-id="b83ce-141">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-141">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-142">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-142">Any</span></span> | <span data-ttu-id="b83ce-143">[IRandomAccessStream,](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) которые хранятся в Blob-файле.</span><span class="sxs-lookup"><span data-stu-id="b83ce-143">[IRandomAccessStream](/uwp/api/Windows.Storage.Streams.IRandomAccessStream) to be stored in the Blob.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-144">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-144">Return value</span></span>**  
      
      | <span data-ttu-id="b83ce-145">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-145">Type</span></span> | <span data-ttu-id="b83ce-146">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-146">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-147">Blob</span><span class="sxs-lookup"><span data-stu-id="b83ce-147">Blob</span></span> | <span data-ttu-id="b83ce-148">Новый объект BLOB-объект, содержащий поток.</span><span class="sxs-lookup"><span data-stu-id="b83ce-148">New blob object that contains the stream.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-149">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-149">Exceptions</span></span>**  
      
      | <span data-ttu-id="b83ce-150">Исключение</span><span class="sxs-lookup"><span data-stu-id="b83ce-150">Exception</span></span> | <span data-ttu-id="b83ce-151">Ошибка</span><span class="sxs-lookup"><span data-stu-id="b83ce-151">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-152">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="b83ce-152">TypeMismatchError</span></span> | <span data-ttu-id="b83ce-153">Тип узла несовместим с ожидаемым типом параметров.</span><span class="sxs-lookup"><span data-stu-id="b83ce-153">The node type is incompatible with the expected parameter type.</span></span>  <span data-ttu-id="b83ce-154">Для версий, предшествующих Internet Explorer 10, возвращается TYPE_MISMATCH_ERR.</span><span class="sxs-lookup"><span data-stu-id="b83ce-154">For versions earlier than Internet Explorer 10, TYPE_MISMATCH_ERR is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-155">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-156">Создает BLOB-объект из типов среды выполнения Windows Runtime с помощью пространства имен MSApp объекта.</span><span class="sxs-lookup"><span data-stu-id="b83ce-156">Creates a Blob from Windows Runtime types via the MSApp namespace on the window object.</span></span>  <span data-ttu-id="b83ce-157">Этот метод создает двоичный объект, который фактически является светло-обтеканием по объекту [RandomAccessStream.](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference)</span><span class="sxs-lookup"><span data-stu-id="b83ce-157">This method will create a blob that is essentially a light wrapper over the [RandomAccessStream](/uwp/api/Windows.Storage.Streams.RandomAccessStreamReference) object provided to it.</span></span>  <span data-ttu-id="b83ce-158">Время существует владельцем этого потока, и поток будет закрыт при универсении blobb.</span><span class="sxs-lookup"><span data-stu-id="b83ce-158">The blob owns the lifetime of this stream and the stream will be closed when the blob is destroyed.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-159">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-159">Example</span></span>**  
      
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

### <span data-ttu-id="b83ce-160">createDataPackage</span><span class="sxs-lookup"><span data-stu-id="b83ce-160">createDataPackage</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-161">Преобразует диапазон пользователя или заданного пользователем диапазон в фрагмент HTML, к которому можно предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="b83ce-161">Converts the user's or the application's specified range to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackage(object); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-162">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-162">Parameters</span></span>**  
      
      `object` <span data-ttu-id="b83ce-163">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-163">[in]</span></span>  
      
      | <span data-ttu-id="b83ce-164">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-164">Type</span></span> | <span data-ttu-id="b83ce-165">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-165">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-166">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-166">Any</span></span> | <span data-ttu-id="b83ce-167">Этот диапазон можно создать на основе объекта выделения, например или `window.selection.getRangeAt(0)` вручную.</span><span class="sxs-lookup"><span data-stu-id="b83ce-167">This range can be created either from a selection object, for example: `window.selection.getRangeAt(0)`, or manually.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-168">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-168">Return value</span></span>**  
      
      | <span data-ttu-id="b83ce-169">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-169">Type</span></span> | <span data-ttu-id="b83ce-170">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-170">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-171">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-171">Any</span></span> | <span data-ttu-id="b83ce-172">Содержит разметку HTML для указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="b83ce-172">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-173">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-173">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-174">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-174">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-175">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-175">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-176">Этот метод поддерживает [только диапазон объектной модели документа (DOM),](https://developer.mozilla.org/docs/Web/API/Range)а не [TextRange.](/uwp/api/windows.ui.xaml.documents.textrange)</span><span class="sxs-lookup"><span data-stu-id="b83ce-176">This method supports only [Document Object Model (DOM) Range](https://developer.mozilla.org/docs/Web/API/Range), not [TextRange](/uwp/api/windows.ui.xaml.documents.textrange).</span></span>  <span data-ttu-id="b83ce-177">Возвращаемый пакет данных для указанного диапазона содержит разметку HTML в формате буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="b83ce-177">The returned data package for the specified range contains HTML markup in clipboard format.</span></span>  
      
      <span data-ttu-id="b83ce-178">Свойства возвращаемом пакета данных недоступны.</span><span class="sxs-lookup"><span data-stu-id="b83ce-178">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-179">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-179">Example</span></span>**  
      
      <span data-ttu-id="b83ce-180">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-180">None.</span></span>  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b83ce-181">createDataPackageFromSelection</span><span class="sxs-lookup"><span data-stu-id="b83ce-181">createDataPackageFromSelection</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-182">Преобразует пользовательский элемент или выбранный фрагмент приложения в фрагмент HTML, к которому можно предоставить общий доступ.</span><span class="sxs-lookup"><span data-stu-id="b83ce-182">Converts the user's or the application's selection to an HTML fragment that can be shared.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createDataPackageFromSelection(); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-183">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-183">Parameters</span></span>**  
      
      <span data-ttu-id="b83ce-184">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b83ce-184">This method has no parameters.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-185">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-185">Return value</span></span>**  
      
      | <span data-ttu-id="b83ce-186">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-186">Type</span></span> | <span data-ttu-id="b83ce-187">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-187">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-188">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-188">Any</span></span> | <span data-ttu-id="b83ce-189">Содержит разметку HTML для указанного диапазона.</span><span class="sxs-lookup"><span data-stu-id="b83ce-189">Contains the HTML markup for the specified range.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-190">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-190">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-191">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-191">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-192">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-192">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-193">Возвращаемый пакет данных для выбранного столбца содержит разметку HTML в формате буфера обмена.</span><span class="sxs-lookup"><span data-stu-id="b83ce-193">The returned data package for the selection contains HTML markup in clipboard format.</span></span>  <span data-ttu-id="b83ce-194">Если пользователь не выбирает пользовательский интерфейс в любом месте пользовательского интерфейса приложения, `createDataPackageFromSelection` возвращается `null` значение.</span><span class="sxs-lookup"><span data-stu-id="b83ce-194">If there is no user selection anywhere within the application's UI, the `createDataPackageFromSelection` returns `null`.</span></span>  
      
      <span data-ttu-id="b83ce-195">Свойства возвращаемом пакета данных недоступны.</span><span class="sxs-lookup"><span data-stu-id="b83ce-195">There are no available properties for the returned data package.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-196">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-196">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
 
### <span data-ttu-id="b83ce-197">createFileFromStorageFile</span><span class="sxs-lookup"><span data-stu-id="b83ce-197">createFileFromStorageFile</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-198">Преобразует [файл хранилища WinRT](/uwp/api/) [в](/uwp/api/windows.storage.storagefile) стандартный объект W3C-файла. [File](https://developer.mozilla.org/docs/Web/API/File)</span><span class="sxs-lookup"><span data-stu-id="b83ce-198">Converts a [WinRT](/uwp/api/) [StorageFile](/uwp/api/windows.storage.storagefile) to a standard W3C [File](https://developer.mozilla.org/docs/Web/API/File) object.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retVal = MSApp.createFileFromStorageFile(storageFile); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-199">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-199">Parameters</span></span>**  
      
      `storageFile` <span data-ttu-id="b83ce-200">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-200">[in]</span></span>
      
      | <span data-ttu-id="b83ce-201">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-201">Type</span></span> | <span data-ttu-id="b83ce-202">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-202">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-203">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-203">Any</span></span> | <span data-ttu-id="b83ce-204">Содержит файл хранилища.</span><span class="sxs-lookup"><span data-stu-id="b83ce-204">Contains the storage file.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-205">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-205">Return value</span></span>**
      
      <span data-ttu-id="b83ce-206">Нет</span><span class="sxs-lookup"><span data-stu-id="b83ce-206">None</span></span>    
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-207">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-207">Exceptions</span></span>**  
      
      | <span data-ttu-id="b83ce-208">Исключение</span><span class="sxs-lookup"><span data-stu-id="b83ce-208">Exception</span></span> | <span data-ttu-id="b83ce-209">Ошибка</span><span class="sxs-lookup"><span data-stu-id="b83ce-209">Condition</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-210">TypeMismatchError</span><span class="sxs-lookup"><span data-stu-id="b83ce-210">TypeMismatchError</span></span> | <span data-ttu-id="b83ce-211">Указанная Викторная ссылка на файл W3C недопустима.</span><span class="sxs-lookup"><span data-stu-id="b83ce-211">The specified W3C file reference is invalid.</span></span>  <span data-ttu-id="b83ce-212">Для версий, предшествующих Internet Explorer 10, `TYPE_MISMATCH_ERR` возвращается значение.</span><span class="sxs-lookup"><span data-stu-id="b83ce-212">For versions earlier than Internet Explorer 10, `TYPE_MISMATCH_ERR` is returned.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-213">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-213">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-214">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-214">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-215">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-215">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b83ce-216">createStreamFromInputStream</span><span class="sxs-lookup"><span data-stu-id="b83ce-216">createStreamFromInputStream</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-217">Создает [MSStream](https://msdn.microsoft.com/library/hh772328) на основе [InputStream.](https://msdn.microsoft.com/library/hh772327)</span><span class="sxs-lookup"><span data-stu-id="b83ce-217">Creates an [MSStream](https://msdn.microsoft.com/library/hh772328) from an [InputStream](https://msdn.microsoft.com/library/hh772327).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var msStream = MSApp.createStreamFromInputStream("image/jpeg", inputStream);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-218">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-218">Parameters</span></span>**  
      
      `type` <span data-ttu-id="b83ce-219">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-219">[in]</span></span>
      
      | <span data-ttu-id="b83ce-220">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-220">Type</span></span> | <span data-ttu-id="b83ce-221">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-221">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-222">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-222">DOMString</span></span> | <span data-ttu-id="b83ce-223">Тип контента данных;</span><span class="sxs-lookup"><span data-stu-id="b83ce-223">Content type of the data.</span></span>  <span data-ttu-id="b83ce-224">Эта строка должна быть указана в формате, заданном в маркере 3.7 из RFC 2616.</span><span class="sxs-lookup"><span data-stu-id="b83ce-224">This string should be in the format specified in the media-type token defined in section 3.7 of RFC 2616.</span></span>  <span data-ttu-id="b83ce-225">\([Просмотр типов MIME,](например, https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) `text/plain` , `text/html` `image/jpeg` `image/png` ,,,,,,,, ,, ,, `audio/mpeg` `audio/ogg` `audio/*` `video/mp4` ,, ,, , , , , , , , , , , , , , , , , , , и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b83ce-225">\([See MIME types,](https://developer.mozilla.org/docs/Web/HTTP/Basics_of_HTTP/MIME_types\) such as `text/plain`, `text/html`, `image/jpeg`, `image/png`, `audio/mpeg`, `audio/ogg`, `audio/*`, `video/mp4`, and so on\).</span></span>  
      
      `inputStream` <span data-ttu-id="b83ce-226">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-226">[in]</span></span>
      
      | <span data-ttu-id="b83ce-227">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-227">Type</span></span> | <span data-ttu-id="b83ce-228">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-228">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-229">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-229">Any</span></span> | <span data-ttu-id="b83ce-230">[IInputStream,](/uwp/api/Windows.Storage.Streams.IInputStream) который будет храниться в. `MSStream`</span><span class="sxs-lookup"><span data-stu-id="b83ce-230">The [IInputStream](/uwp/api/Windows.Storage.Streams.IInputStream) to be stored in the `MSStream`.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-231">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-231">Return value</span></span>**
      
      <span data-ttu-id="b83ce-232">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-232">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-233">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-233">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-234">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-234">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-235">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-235">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-236">Этот метод имеет тип контента и `IInputStream` ссылку.</span><span class="sxs-lookup"><span data-stu-id="b83ce-236">This method takes a content-type, and the `IInputStream` reference.</span></span>  <span data-ttu-id="b83ce-237">Затем проверяет, является ли ссылка на потоковое справочник, является экземпляром `IInputStream` типа, а если нет, выглядит повторяющийся. `DOMException TYPE_MISMATCH_ERR`</span><span class="sxs-lookup"><span data-stu-id="b83ce-237">The method then verifies that the stream reference passed in is an instance of type `IInputStream` and if not, throws `DOMException TYPE_MISMATCH_ERR`.</span></span>  <span data-ttu-id="b83ce-238">Если ошибка не возникает, `createStreamFromInputStream` создается `MSStream` \(на основе входных данных\).)</span><span class="sxs-lookup"><span data-stu-id="b83ce-238">If no error occurs, `createStreamFromInputStream` creates an `MSStream` \(from its inputs\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-239">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-239">Example</span></span>**  
      
      <span data-ttu-id="b83ce-240">Можно `IInputStream` использовать для `MSStream` создания.</span><span class="sxs-lookup"><span data-stu-id="b83ce-240">An `IInputStream` can be used to create an `MSStream`.</span></span>  <span data-ttu-id="b83ce-241">Как и в случае неоднократного использования объектов, все URL-адреса, созданные с помощью объекта изображения, отозваны `MSStreams` `URL.createObjectURL` url-адресами.</span><span class="sxs-lookup"><span data-stu-id="b83ce-241">As `MSStreams` are inherently one-time-use objects, all URLs created by `URL.createObjectURL` are revoked the first time it's resolved by the image element.</span></span>  <span data-ttu-id="b83ce-242">Кроме того, запросы на второй URL-адрес этого объекта после использования потока произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="b83ce-242">Additionally, requests for a second URL on this object after the stream has been used will fail.</span></span>  
      
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

### <span data-ttu-id="b83ce-243">execAsyncAtPriority</span><span class="sxs-lookup"><span data-stu-id="b83ce-243">execAsyncAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-244">Планируются звонки, которые будут проходить позднее в зависимости от заданного приоритета.</span><span class="sxs-lookup"><span data-stu-id="b83ce-244">Schedules a callback to be executed at a later time according to the given priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.execAsyncAtPriority(asynchronousCallback, priority, args); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-245">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-245">Parameters</span></span>**  
      
      `asynchronousCallback` <span data-ttu-id="b83ce-246">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-246">[in]</span></span>
      
      | <span data-ttu-id="b83ce-247">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-247">Type</span></span> | <span data-ttu-id="b83ce-248">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-248">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-249">Функция</span><span class="sxs-lookup"><span data-stu-id="b83ce-249">Function</span></span> | <span data-ttu-id="b83ce-250">Функция вызова, которая позволяет выполнять асинхронно в определенном приоритете.</span><span class="sxs-lookup"><span data-stu-id="b83ce-250">The callback function to run asynchronously, dispatched at the given priority priority.</span></span>  |  
      
      `priority` <span data-ttu-id="b83ce-251">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-251">[in]</span></span>
      
      | <span data-ttu-id="b83ce-252">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-252">Type</span></span> | <span data-ttu-id="b83ce-253">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-253">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-254">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-254">DOMString</span></span> | <span data-ttu-id="b83ce-255">Значение контекстного приоритета, при котором выполнена асинхронный вызов обратных звонков.</span><span class="sxs-lookup"><span data-stu-id="b83ce-255">The contextual priority value at which the asynchronousCallback callback is run.</span></span>  <span data-ttu-id="b83ce-256">См. [константы MSApp.](#msapp-constants)</span><span class="sxs-lookup"><span data-stu-id="b83ce-256">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="b83ce-257">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-257">[in]</span></span>
      
      | <span data-ttu-id="b83ce-258">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-258">Type</span></span> | <span data-ttu-id="b83ce-259">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-259">Description</span></span> |  
      |:---- |:--- |   
      | <span data-ttu-id="b83ce-260">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-260">Any</span></span> | <span data-ttu-id="b83ce-261">Необязательное число аргументов, которые перенаправляются функции синхронных звонков \(в виде параметров 1 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b83ce-261">An optional series of arguments that are passed to the synchronousCallback callback function \(as parameters 1 and so on\).</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-262">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-262">Return value</span></span>**  
      
      <span data-ttu-id="b83ce-263">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b83ce-263">This method does not return a value.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-264">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-264">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-265">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-265">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-266">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-266">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-267">Предоставленная `asynchronousCallback` функция вызова будет проводиться асинхронно позже.</span><span class="sxs-lookup"><span data-stu-id="b83ce-267">The provided `asynchronousCallback` callback function is executed asynchronously later.</span></span>  `asynchronousCallback` <span data-ttu-id="b83ce-268">диспетчер ы диспетчера в зависимости от предоставленного приоритета.</span><span class="sxs-lookup"><span data-stu-id="b83ce-268">will be dispatched according to the provided priority.</span></span>  <span data-ttu-id="b83ce-269">Нормальная приоритет равен существующему [методу Методу.](https://developer.mozilla.org/docs/Web/API/Window/setImmediate)</span><span class="sxs-lookup"><span data-stu-id="b83ce-269">Normal priority is equivalent to the existing [setImmediate](https://developer.mozilla.org/docs/Web/API/Window/setImmediate) method.</span></span>  <span data-ttu-id="b83ce-270">При выполнении вызова текущая контекстная приоритетная приоритетная приоритетра задается для выполнения вызовов.</span><span class="sxs-lookup"><span data-stu-id="b83ce-270">When the callback is run, the current contextual priority is set to the provided priority parameter value for the duration of the callback's execution.</span></span>  
      
      <span data-ttu-id="b83ce-271">Параметры `asynchronousCallback` обратной связи могут быть любыми функциями.</span><span class="sxs-lookup"><span data-stu-id="b83ce-271">The `asynchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="b83ce-272">Если после параметра эти аргументы переносятся, они будут переназываться `priority` функции вызова.</span><span class="sxs-lookup"><span data-stu-id="b83ce-272">If arguments are provided after the `priority` parameter, they will all be passed to the callback function.</span></span>  
      
      <span data-ttu-id="b83ce-273">В `execAtPriority` отличие от сказанного, любой объект, возвращаемый `asynchronousCallback` функцией вызова, игнорируется \(и не возвращается через `execAsyncAtPriority` \).</span><span class="sxs-lookup"><span data-stu-id="b83ce-273">Unlike `execAtPriority`, any object returned by the `asynchronousCallback` callback function is ignored \(and not returned via `execAsyncAtPriority`\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-274">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-274">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="b83ce-275">execAtPriority</span><span class="sxs-lookup"><span data-stu-id="b83ce-275">execAtPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-276">Выполняет указанную функцию вызова в заданном контекстном приоритете.</span><span class="sxs-lookup"><span data-stu-id="b83ce-276">Runs the specified callback function at the given contextual priority.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.execAtPriority(synchronousCallback, priority, args);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-277">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-277">Parameters</span></span>**  
      
      `synchronousCallback` <span data-ttu-id="b83ce-278">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-278">[in]</span></span>  
      
      | <span data-ttu-id="b83ce-279">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-279">Type</span></span> | <span data-ttu-id="b83ce-280">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-280">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-281">Функция</span><span class="sxs-lookup"><span data-stu-id="b83ce-281">Function</span></span> | <span data-ttu-id="b83ce-282">Функция вызова для запуска синхронизируемого контекстного приоритета.</span><span class="sxs-lookup"><span data-stu-id="b83ce-282">The callback function to run synchronously at the given priority contextual priority.</span></span>  |  
      
      `priority` <span data-ttu-id="b83ce-283">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-283">[in]</span></span>  
      
      | <span data-ttu-id="b83ce-284">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-284">Type</span></span> | <span data-ttu-id="b83ce-285">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-285">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-286">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-286">DOMString</span></span> | <span data-ttu-id="b83ce-287">Указанное значение приоритета, которое будет задано при выполнении функции `synchronousCallback` вызова.</span><span class="sxs-lookup"><span data-stu-id="b83ce-287">The specified priority value to which the current contextual priority value will be set when running the `synchronousCallback` callback function.</span></span>  <span data-ttu-id="b83ce-288">См. [константы MSApp.](#msapp-constants)</span><span class="sxs-lookup"><span data-stu-id="b83ce-288">See [MSApp Constants](#msapp-constants).</span></span>  |  
      
      `args` <span data-ttu-id="b83ce-289">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-289">[in]</span></span>  
      
      | <span data-ttu-id="b83ce-290">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-290">Type</span></span> | <span data-ttu-id="b83ce-291">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-291">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-292">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-292">Any</span></span> | <span data-ttu-id="b83ce-293">Необязательное число аргументов, которые были применяться `synchronousCallback` функции callback \(as parameters 1 и т. д.).</span><span class="sxs-lookup"><span data-stu-id="b83ce-293">An optional series of arguments that are passed to the `synchronousCallback` callback function \(as parameters 1 and so on\).</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-294">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-294">Return value</span></span>**  
      
      | <span data-ttu-id="b83ce-295">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-295">Type</span></span> | <span data-ttu-id="b83ce-296">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-296">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-297">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-297">Any</span></span> | <span data-ttu-id="b83ce-298">Возвращает значение возвращаемого `synchronousCallback` вызова \(если применимо\\).</span><span class="sxs-lookup"><span data-stu-id="b83ce-298">Returns the return value of the `synchronousCallback` callback \(as applicable\).</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-299">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-299">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-300">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-300">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-301">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-301">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-302">Предоставленный метод звонков будет запускаться `synchronousCallback` синхронно.</span><span class="sxs-lookup"><span data-stu-id="b83ce-302">The provided `synchronousCallback` callback method is execute synchronously.</span></span>  <span data-ttu-id="b83ce-303">Текущий приоритет изменяется на указанный приоритет (заданное аргументом приоритета) для функции вызова.</span><span class="sxs-lookup"><span data-stu-id="b83ce-303">The current contextual priority is changed to the provided priority value (given by the priority argument) for the duration of the provided callback function.</span></span>  <span data-ttu-id="b83ce-304">По завершении вызова функции вызова приоритет возвращается к предыдущему значению, предшествующем `execAtPriority` узел.</span><span class="sxs-lookup"><span data-stu-id="b83ce-304">Once the callback function finishes executing, priority is returned to the previous value prior to the `execAtPriority` call.</span></span>  <span data-ttu-id="b83ce-305">Возвращаемое значение `execAtPriority` из метода вызова \(как предоставлено\).</span><span class="sxs-lookup"><span data-stu-id="b83ce-305">The return value from `execAtPriority` is the return value of the callback method \(as provided\).</span></span>  
      
      <span data-ttu-id="b83ce-306">Параметры `synchronousCallback` обратной связи могут быть любыми функциями.</span><span class="sxs-lookup"><span data-stu-id="b83ce-306">The `synchronousCallback` callback parameter can be any function.</span></span>  <span data-ttu-id="b83ce-307">Если после параметра приоритета предоставляются любые аргументы, они будут пройдены до предоставленного метода вызова.</span><span class="sxs-lookup"><span data-stu-id="b83ce-307">If any arguments are provided after the priority parameter, they will be passed to the provided callback method.</span></span>  <span data-ttu-id="b83ce-308">Если параметр вызова возвращает значение, то это значение также становится возвращаемое `execAtPriority` значением.</span><span class="sxs-lookup"><span data-stu-id="b83ce-308">If the callback parameter returns a value, this value becomes the return value for `execAtPriority` as well.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-309">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-309">Example</span></span>**  
      
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

### <span data-ttu-id="b83ce-310">getCurrentPriority</span><span class="sxs-lookup"><span data-stu-id="b83ce-310">getCurrentPriority</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-311">Возвращает текущий контекстный приоритет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-311">Returns the current contextual priority.</span></span>  

   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getCurrentPriority();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-312">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-312">Parameters</span></span>**  
      
      <span data-ttu-id="b83ce-313">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-313">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-314">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-314">Return value</span></span>**  
      
      | <span data-ttu-id="b83ce-315">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-315">Type</span></span> | <span data-ttu-id="b83ce-316">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-316">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-317">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-317">DOMString</span></span> | <span data-ttu-id="b83ce-318">Возвращаемое значение представляет собой одну из `MSApp.HIGH` `MSApp.NORMAL` строк, `MSApp.IDLE` или.</span><span class="sxs-lookup"><span data-stu-id="b83ce-318">The return value is one of the strings `MSApp.HIGH`, `MSApp.NORMAL`, or `MSApp.IDLE`.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-319">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-319">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-320">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-320">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-321">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-321">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-322">Этот метод возвращает текущий контекстный приоритет \(см. [константы MSApp),](#msapp-constants)которые можно изменить через `execAtPriority` `execAsyncAtPriority` и.</span><span class="sxs-lookup"><span data-stu-id="b83ce-322">This method returns the current contextual priority \(see [MSApp Constants](#msapp-constants)\), which can be changed via `execAtPriority` and `execAsyncAtPriority`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-323">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-323">Example</span></span>**  
      
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

### <span data-ttu-id="b83ce-324">getHtmlPrintDocumentSource</span><span class="sxs-lookup"><span data-stu-id="b83ce-324">getHtmlPrintDocumentSource</span></span>  

<span data-ttu-id="b83ce-325">Нерекомендуется синхронизировать синхронный API.</span><span class="sxs-lookup"><span data-stu-id="b83ce-325">Synchronous API that has been deprecated.</span></span>  <span data-ttu-id="b83ce-326">Для Windows 10: `getHtmlPrintDocumentSourceAsync`</span><span class="sxs-lookup"><span data-stu-id="b83ce-326">For Windows 10, see `getHtmlPrintDocumentSourceAsync`.</span></span>  <span data-ttu-id="b83ce-327">Сведения Windows 8 и 8.1 см. в записи MSDN для [получения htmlHtmlPrintDocumentSource.](https://msdn.microsoft.com/library/hh772325)</span><span class="sxs-lookup"><span data-stu-id="b83ce-327">For Windows 8 and 8.1 apps, see the MSDN entry for [getHtmlPrintDocumentSource](https://msdn.microsoft.com/library/hh772325).</span></span>  

### <span data-ttu-id="b83ce-328">getHtmlPrintDocumentSourceAsync</span><span class="sxs-lookup"><span data-stu-id="b83ce-328">getHtmlPrintDocumentSourceAsync</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-329">Возвращает исходный контент, который требуется напечатать.</span><span class="sxs-lookup"><span data-stu-id="b83ce-329">Returns the source content that is to be printed.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.getHtmlPrintDocumentSourceAsync(document);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-330">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-330">Parameters</span></span>**  
      
      `htmlDoc` <span data-ttu-id="b83ce-331">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-331">[in]</span></span>  
      
      | <span data-ttu-id="b83ce-332">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-332">Type</span></span> | <span data-ttu-id="b83ce-333">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-333">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-334">Документ</span><span class="sxs-lookup"><span data-stu-id="b83ce-334">Document</span></span> | <span data-ttu-id="b83ce-335">Html-документ, который нужно распечатать.</span><span class="sxs-lookup"><span data-stu-id="b83ce-335">The HTML document to be printed.</span></span>  <span data-ttu-id="b83ce-336">Это может быть корневой документ, документ в iframe, фрагменте документа или документ SVG.</span><span class="sxs-lookup"><span data-stu-id="b83ce-336">This can be the root document, the document in an iframe, a document fragment, or a SVG document.</span></span>  <span data-ttu-id="b83ce-337">Имейте в виду, что HTMLDoc должен быть документ, а не элемент.</span><span class="sxs-lookup"><span data-stu-id="b83ce-337">Be aware that htmlDoc must be a document, not an element.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-338">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-338">Return value</span></span>**
      
      <span data-ttu-id="b83ce-339">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-339">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-340">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-340">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-341">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-341">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-342">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-342">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-343">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-343">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-344">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b83ce-344">Example 1</span></span>**  
      
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
      **<span data-ttu-id="b83ce-345">Пример 2</span><span class="sxs-lookup"><span data-stu-id="b83ce-345">Example 2</span></span>**  
      
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

### <span data-ttu-id="b83ce-346">getViewId</span><span class="sxs-lookup"><span data-stu-id="b83ce-346">getViewId</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-347">Поддержка нескольких окон.</span><span class="sxs-lookup"><span data-stu-id="b83ce-347">Support for multiple windows.</span></span>  
      
      > [!NOTE] 
      > <span data-ttu-id="b83ce-348">В приложениях Win8.1 JavaScript UWP поддерживались несколько окон, используя API DOM MSApp DOM, которые теперь приводятся к описанию.</span><span class="sxs-lookup"><span data-stu-id="b83ce-348">In Win8.1 JavaScript UWP apps supported multiple windows using MSApp DOM APIs which are now depricated.</span></span>  <span data-ttu-id="b83ce-349">В Windows 10 используйте `window.open` `window` и новое `MSApp.getViewId` новое.</span><span class="sxs-lookup"><span data-stu-id="b83ce-349">For Windows 10, use `window.open`, `window`, and the new `MSApp.getViewId`.</span></span>  
      
      | <span data-ttu-id="b83ce-350">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-350">Description</span></span> |<span data-ttu-id="b83ce-351">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="b83ce-351">Windows 10</span></span> | <span data-ttu-id="b83ce-352">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="b83ce-352">Windows 8.1</span></span> |  
      |:---- |:---- |:--- |  
      | <span data-ttu-id="b83ce-353">Создание нового окна</span><span class="sxs-lookup"><span data-stu-id="b83ce-353">Create new window</span></span> | [<span data-ttu-id="b83ce-354">window.open</span><span class="sxs-lookup"><span data-stu-id="b83ce-354">window.open</span></span>](https://developer.mozilla.org/docs/Web/API/Window/open) | [<span data-ttu-id="b83ce-355">MSApp.createNewView</span><span class="sxs-lookup"><span data-stu-id="b83ce-355">MSApp.createNewView</span></span>](https://msdn.microsoft.com/library/dn254975(v=vs.85).aspx) |  
      |<span data-ttu-id="b83ce-356">Объект нового окна</span><span class="sxs-lookup"><span data-stu-id="b83ce-356">New window object</span></span> | [<span data-ttu-id="b83ce-357">окно</span><span class="sxs-lookup"><span data-stu-id="b83ce-357">window</span></span>](https://developer.mozilla.org/docs/Web/API/Window) |[<span data-ttu-id="b83ce-358">MSAppView</span><span class="sxs-lookup"><span data-stu-id="b83ce-358">MSAppView</span></span>](https://msdn.microsoft.com/library/dn268315(v=vs.85).aspx) |  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.getViewId(window); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-359">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-359">Parameters</span></span>**  
      
      `window`
      
      | <span data-ttu-id="b83ce-360">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-360">Type</span></span> | <span data-ttu-id="b83ce-361">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-361">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-362">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-362">DOMString</span></span> | <span data-ttu-id="b83ce-363">Объект, представляющий собой окно с документом DOM.</span><span class="sxs-lookup"><span data-stu-id="b83ce-363">An object representing a window containing a DOM document.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-364">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-364">Return value</span></span>**  
      
      `viewId`
      
      | <span data-ttu-id="b83ce-365">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-365">Type</span></span> | <span data-ttu-id="b83ce-366">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-366">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-367">Число</span><span class="sxs-lookup"><span data-stu-id="b83ce-367">Number</span></span> | <span data-ttu-id="b83ce-368">Может использоваться с различными [AI.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="b83ce-368">Can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-369">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-369">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-370">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-370">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-371">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-371">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-372">Используйте [окно.open](https://developer.mozilla.org/docs/Web/API/Window/open) [и окно](https://developer.mozilla.org/docs/Web/API/Window) для создания новых окон, а затем взаимодействуйте с API WinRT, `MSApp.getViewId` добавив API.</span><span class="sxs-lookup"><span data-stu-id="b83ce-372">Use [window.open](https://developer.mozilla.org/docs/Web/API/Window/open) and [window](https://developer.mozilla.org/docs/Web/API/Window) for creating new windows, but then to interact with WinRT APIs, add the `MSApp.getViewId` API.</span></span>  <span data-ttu-id="b83ce-373">Объект имеет значение параметра и возвращает число, которое можно использовать с `window` `viewId` различными [API Windows.UI.ViewManagement.ApplicationViewSwitcher.](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher)</span><span class="sxs-lookup"><span data-stu-id="b83ce-373">It takes a `window` object as a parameter and returns a `viewId` number that can be used with the various [Windows.UI.ViewManagement.ApplicationViewSwitcher](/uwp/api/windows.ui.viewmanagement.applicationviewswitcher) APIs.</span></span>  
      
      *   <span data-ttu-id="b83ce-374">Видимость задержки</span><span class="sxs-lookup"><span data-stu-id="b83ce-374">Delaying Visibility</span></span>  
          
          <span data-ttu-id="b83ce-375">В WinRT обычно запускаются скрытые представления, а конццы разработчика использует такое представление, как при его `TryShowAsStandaloneAsync` подготовке.</span><span class="sxs-lookup"><span data-stu-id="b83ce-375">Views in WinRT normally start hidden and the end developer uses something like `TryShowAsStandaloneAsync` to display the view once it is fully prepared.</span></span>  <span data-ttu-id="b83ce-376">В Интернете отображается окно, а конечный пользователь может смотреть `window.open` содержимое по мере загрузки и обработки контента.</span><span class="sxs-lookup"><span data-stu-id="b83ce-376">In the web world, `window.open` shows a window immediately and the end user can watch as content is loaded and rendered.</span></span>  <span data-ttu-id="b83ce-377">Чтобы новые окна были такими же, как и представления в WinRT, но не отображались сразу `window.open` же.</span><span class="sxs-lookup"><span data-stu-id="b83ce-377">To have your new windows act like views in WinRT and not display immediately we have added a `window.open` option.</span></span>  <span data-ttu-id="b83ce-378">Например:</span><span class="sxs-lookup"><span data-stu-id="b83ce-378">For example:</span></span>  
          
          ```javascript
          let newWindow = window.open("https://example.com", null, "msHideView=yes");
          ```  
          
      *   <span data-ttu-id="b83ce-379">Различия основного окна</span><span class="sxs-lookup"><span data-stu-id="b83ce-379">Primary Window Differences</span></span>  
          
          <span data-ttu-id="b83ce-380">Первоое окно, открытое ОС, отличается от вспомогательного окна:</span><span class="sxs-lookup"><span data-stu-id="b83ce-380">The primary window that is initially opened by the OS acts differently than the secondary windows that it opens:</span></span>  
          
          | <span data-ttu-id="b83ce-381">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-381">Description</span></span> | <span data-ttu-id="b83ce-382">Основной</span><span class="sxs-lookup"><span data-stu-id="b83ce-382">Primary</span></span> | <span data-ttu-id="b83ce-383">Дополнительная</span><span class="sxs-lookup"><span data-stu-id="b83ce-383">Secondary</span></span> |  
          |:---- |:--- |:--- |  
          | <span data-ttu-id="b83ce-384">window.open</span><span class="sxs-lookup"><span data-stu-id="b83ce-384">window.open</span></span> | <span data-ttu-id="b83ce-385">Разрешено</span><span class="sxs-lookup"><span data-stu-id="b83ce-385">Allowed</span></span> | <span data-ttu-id="b83ce-386">Disallowed</span><span class="sxs-lookup"><span data-stu-id="b83ce-386">Disallowed</span></span> |  
          | <span data-ttu-id="b83ce-387">window.close</span><span class="sxs-lookup"><span data-stu-id="b83ce-387">window.close</span></span> | <span data-ttu-id="b83ce-388">Закрыть приложение</span><span class="sxs-lookup"><span data-stu-id="b83ce-388">Close app</span></span> | <span data-ttu-id="b83ce-389">Закрытие окна</span><span class="sxs-lookup"><span data-stu-id="b83ce-389">Close window</span></span> |  
          | <span data-ttu-id="b83ce-390">Ограничения навигации</span><span class="sxs-lookup"><span data-stu-id="b83ce-390">Navigation restrictions</span></span> | <span data-ttu-id="b83ce-391">Только третье значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-391">ACUR only</span></span> | <span data-ttu-id="b83ce-392">Нет ограничений</span><span class="sxs-lookup"><span data-stu-id="b83ce-392">No restrictions</span></span> |  
          
          <span data-ttu-id="b83ce-393">Ограничение запретить открытие дополнительного окна может изменяться в будущем в зависимости от [отзывов.](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer)</span><span class="sxs-lookup"><span data-stu-id="b83ce-393">The restriction to not allow secondary windows to open could change in the future depending on [feedback](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer).</span></span>  
      
      *   <span data-ttu-id="b83ce-394">Одинаковые ограничения на связь</span><span class="sxs-lookup"><span data-stu-id="b83ce-394">Same Origin Communication Restrictions</span></span>  
          
          <span data-ttu-id="b83ce-395">Техническивозе проблемы, из-за которых синхронизация, однотипичный и перекрестный и перекрестный и окна, звонки скрываются.</span><span class="sxs-lookup"><span data-stu-id="b83ce-395">There is a difficult technical issue preventing proper support for synchronous, same-origin, cross-window, script calls.</span></span>  <span data-ttu-id="b83ce-396">Когда вы открываете такой же или идею, сценарии в одном окне позволяют вызывать функции непосредственно в другом окне, и некоторые из этих звонков произойдут сбой.</span><span class="sxs-lookup"><span data-stu-id="b83ce-396">When you open a window that is same origin, script in one window is allowed to directly call functions in the other window, and some of these calls will fail.</span></span>  `postMessage` <span data-ttu-id="b83ce-397">При вызовах работает нормально и по возможности рекомендуется выполнять различные действия.</span><span class="sxs-lookup"><span data-stu-id="b83ce-397">calls work just fine and is the recommended way to do things if possible.</span></span>  <span data-ttu-id="b83ce-398">Улучшена эта проблема.</span><span class="sxs-lookup"><span data-stu-id="b83ce-398">Work to improve this issue is in progress.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-399">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-399">Example</span></span>**  
      
      ```javascript
      ```   
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
    
### <span data-ttu-id="b83ce-400">isTaskScheduledAtPriorityOrHigher</span><span class="sxs-lookup"><span data-stu-id="b83ce-400">isTaskScheduledAtPriorityOrHigher</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-401">Возвращает логическое значение, определяющее, есть ли ожидаемая процедура на определенный уровень приоритета.</span><span class="sxs-lookup"><span data-stu-id="b83ce-401">Returns a Boolean value indicating whether there is pending work at the given priority level or higher.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSApp.isTaskScheduledAtPriorityOrHigher(priority); 
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-402">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-402">Parameters</span></span>**  
      
      `priority` <span data-ttu-id="b83ce-403">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-403">[in]</span></span>
      
      | <span data-ttu-id="b83ce-404">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-404">Type</span></span> | <span data-ttu-id="b83ce-405">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-405">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-406">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-406">DOMString</span></span> | <span data-ttu-id="b83ce-407">Значение приоритета \(см. [MSApp Constants](#msapp-constants)\), определяющее уровень приоритета и выше для запроса любых негативных работ.</span><span class="sxs-lookup"><span data-stu-id="b83ce-407">A priority value \(see [MSApp Constants](#msapp-constants)\) specifying the priority level and above to query for any outstanding queued work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-408">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-408">Return value</span></span>**  
      
      | <span data-ttu-id="b83ce-409">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-409">Type</span></span> | <span data-ttu-id="b83ce-410">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-410">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-411">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="b83ce-411">Boolean</span></span> | <span data-ttu-id="b83ce-412">Функция возвращает, если в очереди указанного уровня приоритета или `true` выше указанного уровня в качестве `false` значения приоритета.</span><span class="sxs-lookup"><span data-stu-id="b83ce-412">Returns `true` if there is any queued work at the specified priority level or above, `false` otherwise.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-413">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-413">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-414">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-414">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-415">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-415">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-416">Этот способ обеспечивает способ использования кода JavaScript, чтобы определить, нет ли ожидаемых ожиданиях на различных уровнях `isTaskScheduledAtPriorityOrHigher` приоритета \(или более высокого\) с целью того, что код JavaScript может принимать решение о достижении более высокой работы.</span><span class="sxs-lookup"><span data-stu-id="b83ce-416">The `isTaskScheduledAtPriorityOrHigher` method provides a means for JavaScript code to determine if there is pending work at the various priority levels \(or above\) with the intent that the calling JavaScript code can then decide to yield to higher priority work.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-417">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-417">Example</span></span>**  
      
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

### <span data-ttu-id="b83ce-418">pageHandlesAllApplicationActivations</span><span class="sxs-lookup"><span data-stu-id="b83ce-418">pageHandlesAllApplicationActivations</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-419">Используется для избора начального пути (перезагрузка страницы) перед каждым активированным событием \(например, щелчок уведомления или закрепленная плитка\).</span><span class="sxs-lookup"><span data-stu-id="b83ce-419">Used to avoid a refresh of the start path (page reload) before every activate event \(such as clicking a notification or a pinned tile\).</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.pageHandlesAllApplicationActivations(boolean);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-420">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-420">Parameters</span></span>**  
      
      | <span data-ttu-id="b83ce-421">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-421">Type</span></span> | <span data-ttu-id="b83ce-422">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-422">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-423">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="b83ce-423">Boolean</span></span> | <span data-ttu-id="b83ce-424">Используется для всегда пропуска начального пути (страницы) и перехода сразу к `MSApp.pageHandlesAllApplicationActivations(true)` `WebUIApplication` активированное событию.</span><span class="sxs-lookup"><span data-stu-id="b83ce-424">Use `MSApp.pageHandlesAllApplicationActivations(true)` to always skip refreshing the start path (page reload) and instead jump straight to firing the `WebUIApplication` activated event.</span></span>  <span data-ttu-id="b83ce-425">Требуется, чтобы обрабатывать все страницы активации отдельно.</span><span class="sxs-lookup"><span data-stu-id="b83ce-425">Requires that all pages handle activation events separately.</span></span>  <span data-ttu-id="b83ce-426">Если задать этот `true` метод так, то щелкнув активное событие \(например, уведомление\) не будет запускать перезагрузку, а для одностраничных приложений, хранящихся на одностраничных приложениях, не будут перегружаться.</span><span class="sxs-lookup"><span data-stu-id="b83ce-426">By defining this method as `true`, clicking an activated event \(like a notification\) will not trigger the reload, an essential for single-page apps wishing to avoid page reloads.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-427">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-427">Return value</span></span>**
      
      <span data-ttu-id="b83ce-428">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-428">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-429">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-429">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-430">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-430">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-431">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-431">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-432">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-432">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-433">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-433">Example</span></span>**  
      
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

### <span data-ttu-id="b83ce-434">suppressSubdownloadCredentialPrompts</span><span class="sxs-lookup"><span data-stu-id="b83ce-434">suppressSubdownloadCredentialPrompts</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-435">Управляет ли запросы на проверку подлинности в процессе скачивания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b83ce-435">Controls whether an app suppresses possible authentication prompts during the download of resources.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.suppressSubdownloadCredentialPrompts(suppress);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-436">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-436">Parameters</span></span>**  
     
      `suppress` <span data-ttu-id="b83ce-437">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-437">[in]</span></span>
      
      | <span data-ttu-id="b83ce-438">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-438">Type</span></span> | <span data-ttu-id="b83ce-439">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-439">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-440">Boolean (Логическое)</span><span class="sxs-lookup"><span data-stu-id="b83ce-440">Boolean</span></span> | <span data-ttu-id="b83ce-441">Значение истина подтверждает возможные запросы проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b83ce-441">A value of true suppresses potential authentication prompts.</span></span>  <span data-ttu-id="b83ce-442">Значение ложного значения не откладывает потенциальную проверку подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="b83ce-442">A value of false does not suppress any potential authentication prompts from the user.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-443">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-443">Return value</span></span>**  
      
      <span data-ttu-id="b83ce-444">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-444">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-445">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-445">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-446">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-446">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-447">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-447">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-448">Этот способ определяет, подтверждает ли приложение запросы на проверку подлинности во `suppressSubdownloadCredentialPrompts` время скачивания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b83ce-448">The `suppressSubdownloadCredentialPrompts` method controls whether an app suppresses potential authentication prompts during the download of resources.</span></span>  <span data-ttu-id="b83ce-449">По умолчанию поведение не предусмаватывается отключение запросов учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b83ce-449">The default behavior is to not suppress credential prompts.</span></span>  
      
      `suppressSubdownloadCredentialPrompts` <span data-ttu-id="b83ce-450">предназначены для приложений, которые могут загружать лишь большое количество ресурсов, требуемое для проверки подлинности, например почтовое приложение \(может содержать информационный бюллетень с несколькими изображениями, для каждого из которых требуется проверка подлинности\).</span><span class="sxs-lookup"><span data-stu-id="b83ce-450">is intended for use by apps which may load an excessive number of resources that require authentication, such as a mail app \(which could contain a newsletter containing a number of images where each image requires authentication\).</span></span>  
      
      <span data-ttu-id="b83ce-451">Если выключить запрос ы учетных данных, диалоговые окна проверки подлинности на серверах не отображаются при доступе к ресурсам, для которых требуется проверка подлинности, и загрузка ресурса не будет скачан.</span><span class="sxs-lookup"><span data-stu-id="b83ce-451">When suppressing credential prompts, dialogs for authenticating to servers will not be shown when accessing resources that require authentication, and the resource will not be downloaded.</span></span>  <span data-ttu-id="b83ce-452">Обратите внимание на то, что не влияет на другие возможные запросы на проверку подлинности на прокси-сервере или запросы сертификации `suppressSubdownloadCredentialPrompts` клиента, и никак не влияет на XHR.</span><span class="sxs-lookup"><span data-stu-id="b83ce-452">Note that `suppressSubdownloadCredentialPrompts` does not impact other possible prompts such as proxy authentication or client certification request dialogs, nor does it impact XHR.</span></span>  
      
      <span data-ttu-id="b83ce-453">Имейте в виду, что `suppressSubdownloadCredentialPrompts` влияние на все содержимое приложения, включая контент, хранящееся в `webview` элементе.</span><span class="sxs-lookup"><span data-stu-id="b83ce-453">Be aware that `suppressSubdownloadCredentialPrompts` impacts all content in the application, including content hosted in the `webview` element.</span></span>  
      
      > [!IMPORTANT]
      > <span data-ttu-id="b83ce-454">Решения о запросах на ввод учетных данных куплены.</span><span class="sxs-lookup"><span data-stu-id="b83ce-454">Credential prompt decisions are cached.</span></span>  <span data-ttu-id="b83ce-455">Поэтому при выключении запросов учетных данных к сроку действия учетных данных может потребоваться перезагрузить документ.</span><span class="sxs-lookup"><span data-stu-id="b83ce-455">Therefore, while suppressing credential prompts will take effect immediately, allowing credential prompts after suppressing them may need a reload of the document to take effect.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-456">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-456">Example</span></span>**  
      
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

### <span data-ttu-id="b83ce-457">terminateApp</span><span class="sxs-lookup"><span data-stu-id="b83ce-457">terminateApp</span></span>  


:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-458">Завершение текущего приложения и создает отчет об ошибок.</span><span class="sxs-lookup"><span data-stu-id="b83ce-458">Terminates the current application and generates a failure report.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      MSApp.terminateApp(error);
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-459">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-459">Parameters</span></span>**  
      
      `error` <span data-ttu-id="b83ce-460">[в]</span><span class="sxs-lookup"><span data-stu-id="b83ce-460">[in]</span></span>
      
      | <span data-ttu-id="b83ce-461">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-461">Type</span></span> | <span data-ttu-id="b83ce-462">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-462">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-463">Ошибка</span><span class="sxs-lookup"><span data-stu-id="b83ce-463">Error</span></span> | <span data-ttu-id="b83ce-464">Объект, `Error` с помощью которого можно описать ошибку, которая активировала окончание.</span><span class="sxs-lookup"><span data-stu-id="b83ce-464">An `Error` object that you can use to describe the error that triggered the termination.</span></span>  <span data-ttu-id="b83ce-465">Объект `Error` должен содержать свойства номера, описания и стопки, а отчет о сбое не будет создан, если объект не содержит эти свойств.</span><span class="sxs-lookup"><span data-stu-id="b83ce-465">The `Error` object must contain the number, description, and stack properties; a failure report won't be generated if the object doesn't contain these properties.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-466">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-466">Return value</span></span>**
      
      <span data-ttu-id="b83ce-467">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-467">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-468">Исключения</span><span class="sxs-lookup"><span data-stu-id="b83ce-468">Exceptions</span></span>**  
      
      <span data-ttu-id="b83ce-469">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-469">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-470">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b83ce-470">Remarks</span></span>**  
      
      <span data-ttu-id="b83ce-471">Если вы уточнили проблему, выполнив ширину 5 лучших проблем приложения, она будет отображаться на странице `terminateApp` качества приложения.</span><span class="sxs-lookup"><span data-stu-id="b83ce-471">If the issue reported by `terminateApp` becomes one of your app's top 5 issues, it will show up on the app's Quality page.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-472">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-472">Example</span></span>**  
      
      <span data-ttu-id="b83ce-473">В этом примере `terminateApp` возвращаются исключения.</span><span class="sxs-lookup"><span data-stu-id="b83ce-473">This example calls `terminateApp` when an exception is encountered.</span></span>  <span data-ttu-id="b83ce-474">Он использует `Error` объект, предоставленный при обзоре исключения.</span><span class="sxs-lookup"><span data-stu-id="b83ce-474">It uses the `Error` object provided when you catch an exception.</span></span>  
      
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

### <span data-ttu-id="b83ce-475">Константы MSApp</span><span class="sxs-lookup"><span data-stu-id="b83ce-475">MSApp Constants</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-476">Разрешенные значения приоритета, с которыми связаны `execAsyncAtPriority` `execAtPriority` значения `getCurrentPriority` приоритета, `isTaskScheduldAtPriorityOrHigher` и.</span><span class="sxs-lookup"><span data-stu-id="b83ce-476">Allowed priority values associated with `execAsyncAtPriority`, `execAtPriority`, `getCurrentPriority`, and `isTaskScheduldAtPriorityOrHigher`.</span></span>  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="b83ce-477">Текущие</span><span class="sxs-lookup"><span data-stu-id="b83ce-477">Current</span></span>  
      
      `current`  
      
      | <span data-ttu-id="b83ce-478">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-478">Type</span></span> | <span data-ttu-id="b83ce-479">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-479">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-480">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-480">DOMString</span></span> | <span data-ttu-id="b83ce-481">При использовании с указанным методом \(см. также раздел\), при выборе текущего контекстной приоритетной операции будет использоваться текущая `current` приоритетная.</span><span class="sxs-lookup"><span data-stu-id="b83ce-481">When `current` is used with the appropriate method \(See also section\), the method will use the current contextual priority when executing the requested operation.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="b83ce-482">Высока</span><span class="sxs-lookup"><span data-stu-id="b83ce-482">High</span></span>  
      
      `high`  
      
      | <span data-ttu-id="b83ce-483">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-483">Type</span></span> | <span data-ttu-id="b83ce-484">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-484">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-485">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-485">DOMString</span></span> | <span data-ttu-id="b83ce-486">При использовании с соответствующим методом \(см. также раздел\), метод будет использоваться более высокий приоритет при выполнении запрошенной операции и будет `high` утерян недоставлено.</span><span class="sxs-lookup"><span data-stu-id="b83ce-486">When `high` is used with the appropriate method \(See also section\), the method will use higher than normal priority when executing the requested operation and will be dispatch the operation before any existing normal priority work.</span></span>  |  
   :::column-end:::
   :::column span="":::
      #### <span data-ttu-id="b83ce-487">Состояние Idle (в покое)</span><span class="sxs-lookup"><span data-stu-id="b83ce-487">Idle</span></span>  
      
      `idle`  
      
      | <span data-ttu-id="b83ce-488">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-488">Type</span></span> | <span data-ttu-id="b83ce-489">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-489">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-490">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-490">DOMString</span></span> | <span data-ttu-id="b83ce-491">При `ideal` использовании с неприемлемым способом \(см. также раздел\), метод будет использоваться меньше, чем обычно при выполнения запрошенной операции и будет уничтожен после любой существующей нормальной приоритетной приоритетной работы.</span><span class="sxs-lookup"><span data-stu-id="b83ce-491">When `ideal` is used with the appropriate method \(See also section\), the method will use lower than normal priority when executing the requested operation and will be dispatch the operation after any existing normal priority work.</span></span>  |  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      #### <span data-ttu-id="b83ce-492">Обычный</span><span class="sxs-lookup"><span data-stu-id="b83ce-492">Normal</span></span>  
      
      `normal`  
      
      | <span data-ttu-id="b83ce-493">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-493">Type</span></span> | <span data-ttu-id="b83ce-494">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-494">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-495">DOMString</span><span class="sxs-lookup"><span data-stu-id="b83ce-495">DOMString</span></span> | <span data-ttu-id="b83ce-496">При использовании с соответствующим методом (см. также разделе), метод будет использовать существующий приоритет при выполнения `normal` запрошенной операции.</span><span class="sxs-lookup"><span data-stu-id="b83ce-496">When `normal` is used with the appropriate method (See also section), the method will use the normal existing priority when executing the requested operation.</span></span>  |  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-497">Пример.</span><span class="sxs-lookup"><span data-stu-id="b83ce-497">Example</span></span>**  
      
      ```javascript
      if (window.MSApp.CURRENT) {
          document.getElementById('outputMessageDiv').textContent = 'The value of window.MSApp.CURRENT is "current".';
      }
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-498">Требования</span><span class="sxs-lookup"><span data-stu-id="b83ce-498">Requirements</span></span>**  
      
      | <span data-ttu-id="b83ce-499">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-499">Type</span></span> | <span data-ttu-id="b83ce-500">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-500">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-501">IDL</span><span class="sxs-lookup"><span data-stu-id="b83ce-501">IDL</span></span> | <span data-ttu-id="b83ce-502">Mshtml.idl</span><span class="sxs-lookup"><span data-stu-id="b83ce-502">Mshtml.idl</span></span> |  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="b83ce-503">MSAppAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="b83ce-503">MSAppAsyncOperation</span></span>  

```javascript
var asyncOperation = MSApp.clearTemporaryWebDataAsync(); 
asyncOperation.oncomplete = function() { console.log("Temporary web data cleared successfully"); }; 
asyncOperation.onerror = function() { console.log("Failed to clear temporary web data"); }; 
asyncOperation.start(); 
```  

### <span data-ttu-id="b83ce-504">start</span><span class="sxs-lookup"><span data-stu-id="b83ce-504">start</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="b83ce-505">Начало. `MSAppAsyncOperation`</span><span class="sxs-lookup"><span data-stu-id="b83ce-505">Starts the `MSAppAsyncOperation`.</span></span>  
   :::column-end:::
   :::column span="":::
      ```javascript
      var retval = MSAppAsyncOperation.start();
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      **<span data-ttu-id="b83ce-506">Параметры</span><span class="sxs-lookup"><span data-stu-id="b83ce-506">Parameters</span></span>**  
      
      <span data-ttu-id="b83ce-507">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-507">None.</span></span>  
   :::column-end:::
   :::column span="":::
      **<span data-ttu-id="b83ce-508">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b83ce-508">Return value</span></span>**
      
      <span data-ttu-id="b83ce-509">Нет.</span><span class="sxs-lookup"><span data-stu-id="b83ce-509">None.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="":::
      
      **<span data-ttu-id="b83ce-510">Свойства</span><span class="sxs-lookup"><span data-stu-id="b83ce-510">Properties</span></span>**  
      
      `error` <span data-ttu-id="b83ce-511">свойство</span><span class="sxs-lookup"><span data-stu-id="b83ce-511">property</span></span>  
      
      | <span data-ttu-id="b83ce-512">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-512">Type</span></span> | <span data-ttu-id="b83ce-513">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-513">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-514">DOMError</span><span class="sxs-lookup"><span data-stu-id="b83ce-514">DOMError</span></span> | <span data-ttu-id="b83ce-515">Представляет `MSAppAsyncOperation` ошибку.</span><span class="sxs-lookup"><span data-stu-id="b83ce-515">Represents an error in `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.error
      ```  
      
      `oncomplete` <span data-ttu-id="b83ce-516">свойство</span><span class="sxs-lookup"><span data-stu-id="b83ce-516">property</span></span>  
      
      | <span data-ttu-id="b83ce-517">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-517">Type</span></span> | <span data-ttu-id="b83ce-518">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-518">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-519">EventHandler</span><span class="sxs-lookup"><span data-stu-id="b83ce-519">EventHandler</span></span> | <span data-ttu-id="b83ce-520">Свойство для настройки обработчика события по завершающему `MSAppAsyncOperation` моменту.</span><span class="sxs-lookup"><span data-stu-id="b83ce-520">Property for setting an event handler on completion of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.oncomplete
      ```  
      
      `onerror` <span data-ttu-id="b83ce-521">свойство</span><span class="sxs-lookup"><span data-stu-id="b83ce-521">property</span></span>  
      
      | <span data-ttu-id="b83ce-522">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-522">Type</span></span> | <span data-ttu-id="b83ce-523">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-523">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-524">EventHandler</span><span class="sxs-lookup"><span data-stu-id="b83ce-524">EventHandler</span></span> | <span data-ttu-id="b83ce-525">Свойство для настройки обработчика события во время `MSAppAsyncOperation` ошибки.</span><span class="sxs-lookup"><span data-stu-id="b83ce-525">Property for setting an event handler upon an error during `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.onerror
      ```  
      
      `readyState` <span data-ttu-id="b83ce-526">свойство</span><span class="sxs-lookup"><span data-stu-id="b83ce-526">property</span></span>  
      
      | <span data-ttu-id="b83ce-527">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-527">Type</span></span> | <span data-ttu-id="b83ce-528">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-528">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-529">Число</span><span class="sxs-lookup"><span data-stu-id="b83ce-529">Number</span></span> | <span data-ttu-id="b83ce-530">Представляет состояние асинхронной операции в приложении Для Windows с помощью JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b83ce-530">Represents the state of the asynchronous operation within the Windows app using JavaScript.</span></span>  <span data-ttu-id="b83ce-531">К значениям относятся: `Started[0]` `Completed[1]` , `Error[2]` .</span><span class="sxs-lookup"><span data-stu-id="b83ce-531">Values include: `Started[0]`, `Completed[1]`, `Error[2]`.</span></span>  |  
      
      ```javascript
      p = object.readyState
      ```  
      
      `result` <span data-ttu-id="b83ce-532">свойство</span><span class="sxs-lookup"><span data-stu-id="b83ce-532">property</span></span>  
      
      | <span data-ttu-id="b83ce-533">Тип</span><span class="sxs-lookup"><span data-stu-id="b83ce-533">Type</span></span> | <span data-ttu-id="b83ce-534">Описание</span><span class="sxs-lookup"><span data-stu-id="b83ce-534">Description</span></span> |  
      |:---- |:--- |  
      | <span data-ttu-id="b83ce-535">Любой</span><span class="sxs-lookup"><span data-stu-id="b83ce-535">Any</span></span> |<span data-ttu-id="b83ce-536">Представляет `MSAppAsyncOperation` результат.</span><span class="sxs-lookup"><span data-stu-id="b83ce-536">Represents the result of `MSAppAsyncOperation`.</span></span>  |  
      
      ```javascript
      p = object.result
      ```  
   :::column-end:::
   :::column span="":::
      &nbsp;  
   :::column-end:::
:::row-end:::  
