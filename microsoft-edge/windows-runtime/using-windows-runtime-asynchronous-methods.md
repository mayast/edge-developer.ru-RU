---
title: Использование асинхронных методов среды выполнения Windows
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime asynchronous methods
ms.assetid: 70756833-44f7-4383-827f-2ac781558082
caps.latest.revision: 15
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: d9d59fb8b97e34feb002de1477dbe38709bde713
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942073"
---
# <span data-ttu-id="31fa5-102">Использование асинхронных методов среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="31fa5-102">Using Windows Runtime asynchronous methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="31fa5-103">Многие методы Windows runtime, особенно в том числе слишком много времени, которые могут занимать долгое время.</span><span class="sxs-lookup"><span data-stu-id="31fa5-103">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="31fa5-104">Эти методы обычно возвращаются асинхронное действие или операцию \(например, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` , , или `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).</span><span class="sxs-lookup"><span data-stu-id="31fa5-104">These methods generally return an asynchronous action or operation \(for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`\).</span></span>  <span data-ttu-id="31fa5-105">Эти методы представлены в JavaScript по [типичным JJS, Promises/A.][CommonjsWikiPromises]</span><span class="sxs-lookup"><span data-stu-id="31fa5-105">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="31fa5-106">Это значит, что он возвращает объект "Прогноз", содержащий [функцию,][PreviousVersionsWindowsAppsBr229728]которая должна предоставить функцию, которая обрабатывает результат в случае успешного `completed` выполнения операции.</span><span class="sxs-lookup"><span data-stu-id="31fa5-106">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="31fa5-107">Если вы не хотите использовать обработчик ошибок, вместо функции используйте функцию [DOne.][PreviousVersionsWindowsAppsHr701079] `then`</span><span class="sxs-lookup"><span data-stu-id="31fa5-107">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="31fa5-108">Функции windows Runtime недоступны для приложений, работающих в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="31fa5-108">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="31fa5-109">Примеры асинхронных методов</span><span class="sxs-lookup"><span data-stu-id="31fa5-109">Examples of asynchronous methods</span></span>  

<span data-ttu-id="31fa5-110">В следующем примере функция `then` имеет параметр, представляющий полное значение метода. `createResourceAsync`</span><span class="sxs-lookup"><span data-stu-id="31fa5-110">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="31fa5-111">В этом случае при ошибке возвращается исключение в состоянии ошибки, но не вызывает `createResourceAsync` исключение.</span><span class="sxs-lookup"><span data-stu-id="31fa5-111">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="31fa5-112">Обработку ошибки можно обрабатывать с `then` помощью описанной ниже функции.</span><span class="sxs-lookup"><span data-stu-id="31fa5-112">You can handle an error by using the `then` function as follows.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
              console.log("New item is: " + newItem.id);
          }
          function(err) {
              console.log("Got error: " + err.message);
          });
```  

<span data-ttu-id="31fa5-113">Если вы не хотите обрабатывать ошибку явно, но вы хотите, чтобы при этом возникло исключение, используйте вместо `done` этой функции.</span><span class="sxs-lookup"><span data-stu-id="31fa5-113">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="31fa5-114">Вы также можете отобразить ход выполнения, продолжающее ся, используя третью функцию.</span><span class="sxs-lookup"><span data-stu-id="31fa5-114">You can also display the progress made towards completion by using a third function.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .then(function(newItem) {
               console.log("New item is: " + newItem.id);
            },
    // Error.
            function(error) {
               alert("Failed to create a resource.");
            },
    // Progress.
            function(progress, resultSoFar) {
               setProgressBar(progress);
            });
```  

<span data-ttu-id="31fa5-115">Дополнительные сведения об асинхронном принадлежности см. в [асинхронном программировании в JavaScript.][PreviousVersionsWindowsAppsHh700330]</span><span class="sxs-lookup"><span data-stu-id="31fa5-115">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <span data-ttu-id="31fa5-116">См. также</span><span class="sxs-lookup"><span data-stu-id="31fa5-116">See also</span></span>  

[<span data-ttu-id="31fa5-117">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="31fa5-117">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование Windows Runtime в JavaScript | Документы Майкрософт"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promise.затем метод | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Асинхронный программный код в JavaScript (HTML) | Документы Майкрософт"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Promise.done : | Документы Майкрософт"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Промежуточные | CommonJS Spec Wiki"  
