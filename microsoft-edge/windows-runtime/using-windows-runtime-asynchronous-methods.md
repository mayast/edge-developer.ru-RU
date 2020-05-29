---
title: Использование асинхронных методов среды выполнения Windows
ms.custom: ''
ms.date: 04/01/2020
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
ms.openlocfilehash: 6d0f174d22d0d13571d78bc215356ad90a0ae7fa
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572843"
---
# <span data-ttu-id="4f0a9-102">Использование асинхронных методов среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="4f0a9-102">Using Windows Runtime Asynchronous Methods</span></span>  

<span data-ttu-id="4f0a9-103">Многие методы среды выполнения Windows, особенно методы, выполнение которых может занять много времени, являются асинхронными.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-103">Many Windows Runtime methods, especially methods that might take a long time to complete, are asynchronous.</span></span>  <span data-ttu-id="4f0a9-104">Эти методы обычно возвращают асинхронное действие или операцию (например, `Windows.Foundation.IAsyncAction` , `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` или `Windows.Foundation.IAsyncOperationWithProgress` ).</span><span class="sxs-lookup"><span data-stu-id="4f0a9-104">These methods generally return an asynchronous action or operation (for example, `Windows.Foundation.IAsyncAction`, `Windows.Foundation.IAsyncOperation`, `Windows.Foundation.IAsyncActionWithProgress`, or `Windows.Foundation.IAsyncOperationWithProgress`).</span></span>  <span data-ttu-id="4f0a9-105">Эти методы представлены в JavaScript с помощью [шаблона CommonJS/обещает/A][CommonjsWikiPromises].</span><span class="sxs-lookup"><span data-stu-id="4f0a9-105">These methods are represented in JavaScript by the [CommonJS/Promises/A pattern][CommonjsWikiPromises].</span></span>  <span data-ttu-id="4f0a9-106">То есть они возвращают объект Promise, имеющий [функцию then][PreviousVersionsWindowsAppsBr229728], для которой необходимо предоставить `completed` функцию, которая обрабатывает результат при успешном выполнении операции.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-106">That is, they return a Promise object that has a [then function][PreviousVersionsWindowsAppsBr229728], for which you must provide a `completed` function that handles the result if the operation succeeds.</span></span>  <span data-ttu-id="4f0a9-107">Если вы не хотите предоставлять обработчик ошибок, вместо функции следует использовать [функцию готово][PreviousVersionsWindowsAppsHr701079] `then` .</span><span class="sxs-lookup"><span data-stu-id="4f0a9-107">If you don't want to provide an error handler, you should use the [done function][PreviousVersionsWindowsAppsHr701079] instead of the `then` function.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="4f0a9-108">Функции среды выполнения Windows недоступны для приложений, работающих в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-108">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="4f0a9-109">Примеры асинхронных методов</span><span class="sxs-lookup"><span data-stu-id="4f0a9-109">Examples of Asynchronous Methods</span></span>  

<span data-ttu-id="4f0a9-110">В приведенном ниже примере `then` функция принимает параметр, представляющий завершенное значение `createResourceAsync` метода.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-110">In the following example, the `then` function takes a parameter that represents the completed value of the `createResourceAsync` method.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="4f0a9-111">В этом случае, если `createResourceAsync` метод завершает работу со сбоем, он возвращает обещание в состоянии ошибки, но не создает исключение.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-111">In this case, if the `createResourceAsync` method fails, it returns a promise in the error state, but does not throw an exception.</span></span>  <span data-ttu-id="4f0a9-112">Вы можете обработать ошибку с помощью функции, `then` как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-112">You can handle an error by using the `then` function as follows.</span></span>  

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

<span data-ttu-id="4f0a9-113">Если вы не хотите явно обрабатывать ошибку, но хотите, чтобы она вывызывала исключение, `done` вместо этого можно использовать функцию.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-113">If you don't want to handle the error explicitly, but do want it to throw an exception, you can use the `done` function instead.</span></span>  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

<span data-ttu-id="4f0a9-114">Вы также можете отобразить ход выполнения в направлении завершения, используя третью функцию.</span><span class="sxs-lookup"><span data-stu-id="4f0a9-114">You can also display the progress made towards completion by using a third function.</span></span>  

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

<span data-ttu-id="4f0a9-115">Дополнительные сведения об асинхронном программировании можно найти [в разделе Асинхронное программирование в JavaScript][PreviousVersionsWindowsAppsHh700330].</span><span class="sxs-lookup"><span data-stu-id="4f0a9-115">For more information about asynchronous programming, see [Asynchronous Programming in JavaScript][PreviousVersionsWindowsAppsHh700330].</span></span>  

## <span data-ttu-id="4f0a9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="4f0a9-116">See Also</span></span>  

[<span data-ttu-id="4f0a9-117">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="4f0a9-117">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Использование среды выполнения Windows в JavaScript"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Метод Promise. then"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Асинхронное программирование в JavaScript (HTML)"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Метод Promise. Готово"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Обещает | Вики-сайт спецификаций CommonJS"  
