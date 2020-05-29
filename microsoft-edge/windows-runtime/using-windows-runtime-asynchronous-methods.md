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
# Использование асинхронных методов среды выполнения Windows  

Многие методы среды выполнения Windows, особенно методы, выполнение которых может занять много времени, являются асинхронными.  Эти методы обычно возвращают асинхронное действие или операцию (например, `Windows.Foundation.IAsyncAction` , `Windows.Foundation.IAsyncOperation` `Windows.Foundation.IAsyncActionWithProgress` или `Windows.Foundation.IAsyncOperationWithProgress` ).  Эти методы представлены в JavaScript с помощью [шаблона CommonJS/обещает/A][CommonjsWikiPromises].  То есть они возвращают объект Promise, имеющий [функцию then][PreviousVersionsWindowsAppsBr229728], для которой необходимо предоставить `completed` функцию, которая обрабатывает результат при успешном выполнении операции.  Если вы не хотите предоставлять обработчик ошибок, вместо функции следует использовать [функцию готово][PreviousVersionsWindowsAppsHr701079] `then` .  

> [!IMPORTANT]
> Функции среды выполнения Windows недоступны для приложений, работающих в Internet Explorer.  

## Примеры асинхронных методов  

В приведенном ниже примере `then` функция принимает параметр, представляющий завершенное значение `createResourceAsync` метода.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
    .then(function(newItem) {
        console.log("New item is: " + newItem.id);
            });
```  

В этом случае, если `createResourceAsync` метод завершает работу со сбоем, он возвращает обещание в состоянии ошибки, но не создает исключение.  Вы можете обработать ошибку с помощью функции, `then` как описано ниже.  

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

Если вы не хотите явно обрабатывать ошибку, но хотите, чтобы она вывызывала исключение, `done` вместо этого можно использовать функцию.  

```javascript
client.createResourceAsync(uri, description, item)
    // Success.
      .done(function(newItem) {
               console.log("New item is: " + newItem.id);
            });
```  

Вы также можете отобразить ход выполнения в направлении завершения, используя третью функцию.  

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

Дополнительные сведения об асинхронном программировании можно найти [в разделе Асинхронное программирование в JavaScript][PreviousVersionsWindowsAppsHh700330].  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Использование среды выполнения Windows в JavaScript"  

[PreviousVersionsWindowsAppsBr229728]: /previous-versions/windows/apps/br229728(v=win.10) "Метод Promise. then"  
[PreviousVersionsWindowsAppsHh700330]: /previous-versions/windows/apps/hh700330(v=win.10) "Асинхронное программирование в JavaScript (HTML)"
[PreviousVersionsWindowsAppsHr701079]: /previous-versions/windows/apps/hh701079(v=win.10) "Метод Promise. Готово"  

[CommonjsWikiPromises]: http://wiki.commonjs.org/wiki/Promises "Обещает | Вики-сайт спецификаций CommonJS"  
