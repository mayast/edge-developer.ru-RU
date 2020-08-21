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
# Использование асинхронных методов среды выполнения Windows  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Многие методы Windows runtime, особенно в том числе слишком много времени, которые могут занимать долгое время.  Эти методы обычно возвращаются асинхронное действие или операцию \(например, `Windows.Foundation.IAsyncAction` `Windows.Foundation.IAsyncOperation` , , или `Windows.Foundation.IAsyncActionWithProgress` `Windows.Foundation.IAsyncOperationWithProgress` \).  Эти методы представлены в JavaScript по [типичным JJS, Promises/A.][CommonjsWikiPromises]  Это значит, что он возвращает объект "Прогноз", содержащий [функцию,][PreviousVersionsWindowsAppsBr229728]которая должна предоставить функцию, которая обрабатывает результат в случае успешного `completed` выполнения операции.  Если вы не хотите использовать обработчик ошибок, вместо функции используйте функцию [DOne.][PreviousVersionsWindowsAppsHr701079] `then`  

> [!IMPORTANT]
> Функции windows Runtime недоступны для приложений, работающих в Internet Explorer.  

## Примеры асинхронных методов  

В следующем примере функция `then` имеет параметр, представляющий полное значение метода. `createResourceAsync`  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

В этом случае при ошибке возвращается исключение в состоянии ошибки, но не вызывает `createResourceAsync` исключение.  Обработку ошибки можно обрабатывать с `then` помощью описанной ниже функции.  

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

Если вы не хотите обрабатывать ошибку явно, но вы хотите, чтобы при этом возникло исключение, используйте вместо `done` этой функции.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Вы также можете отобразить ход выполнения, продолжающее ся, используя третью функцию.  

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

Дополнительные сведения об асинхронном принадлежности см. в [асинхронном программировании в JavaScript.][PreviousVersionsWindowsAppsHh700330]  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование Windows Runtime в JavaScript | Документы Майкрософт"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Promise.затем метод | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Асинхронный программный код в JavaScript (HTML) | Документы Майкрософт"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Promise.done : | Документы Майкрософт"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Промежуточные | CommonJS Spec Wiki"  
