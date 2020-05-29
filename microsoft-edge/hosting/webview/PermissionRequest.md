---
description: Предоставляет сведения о запросе разрешения
title: Объект PermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/15/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 023f19170e7b5cdb52a1de9d5d4d7c755c89edbe
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571290"
---
# Объект PermissionRequest

Предоставляет сведения о запросе разрешений. Этот объект доступен из свойства permissionRequest аргументов события из события [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) WebView.

```js
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
```

## Методы

### Пуск

Разрешает запрос на разрешение.

#### Параметры

У этого метода нет параметров.

#### Возвращаемое значение

Этот метод не возвращает значение.

### отложить

Если вместо синхронно разрешенных или запрещенных PermissionRequest, вам требуется время для взаимодействия с пользователем или выполнения какого-либо другого асинхронного действия, вызовите функцию отсрочки () в PermissionRequest. PermissionRequest теперь будет доступен как DeferredPermissionRequest из getDeferredPermissionRequests и getDeferredPermissionRequestById. Вы можете сопоставить текущую PermissionRequest с соответствующей DeferredPermissionRequest с помощью свойства Match ID.

#### Параметры

У этого метода нет параметров.

#### Возвращаемое значение

Этот метод не возвращает значение.

### запретить

Отклоняет запрос на разрешение.

#### Параметры

У этого метода нет параметров.

#### Возвращаемое значение

Этот метод не возвращает значение.

## Свойства

### id

Уникальный идентификатор, который можно использовать для сопоставления текущего PermissionRequest с соответствующим DeferredPermissionRequest при использовании метода отсрочки. Просмотрите метод "отложить".

Это свойство доступно только для чтения.

##### Значение свойства

Тип: **Long без знака**

### состояни

Возвращает значение "неизвестно", "отложить", "разрешить" или "запретить", чтобы показать текущее состояние запроса разрешения. Строка состояния будет соответствовать тому, какой метод допускает, запрещает или задерживается (Последнее или неизвестное), если ни один из методов не был вызван.

Это свойство доступно только для чтения.

#### Значение свойства

Тип: **строка**

### Тип

Тип запрашиваемого разрешения. Это может быть одно из следующих строковых значений:

- **географическое расположение**: доступ к данным о расположении с помощью навигатора. Географическое положение.
- **unlimitedIndexedDBQuota**: позволяет IndexedDB API игнорировать обычное ограничение на размер сохраненных данных.
- **носители**: доступ к микрофону и камере с помощью навигатора. getUserMedia.
- **pointerlock**: возможность блокировки и управления указателем мыши с помощью элемента. requestPointerLock.
- **уведомления**: возможность отображения уведомлений на рабочем столе через окно. Извещен.
- **экран**: возможность делать снимки экрана с помощью API захвата мультимедиа.
- **immersiveview**: возможность управления выводом на экран в VR.

Это свойство доступно только для чтения.

#### Значение свойства

Тип: **строка**

### uri

Универсальный код ресурса (URI) документа, запросившего разрешение.

Это свойство доступно только для чтения.

#### Значение свойства

Тип: **строка**
