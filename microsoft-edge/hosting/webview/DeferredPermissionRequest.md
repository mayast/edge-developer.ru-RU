---
description: Представляет отложенный запрос на разрешение пользователя на доступ к функциям устройства.
title: Объект DeferredPermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/15/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 6013f20195fc0f5d4f33b871a9c1b01392bf023e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571313"
---
# Объект DeferredPermissionRequest

Представляет отложенный запрос содержимого [WebView](../webview.md) для разрешения конечным пользователем на доступ к специализированной функциональности устройства (например, географическое расположение или блокировку указателя).

```js
// In this sample, when we receive a permission request we construct some basic UI to ask the
// user if they want to give permission.
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    const requestContainer = document.createElement("div");

    // We use this function as the handler for the allow and deny buttons.
    function completeDeferredPermissionRequest(allow) {
        // Find the DeferredPermissionRequest using the id of the PermissionRequest we deferred.
        const deferredPermissionRequest = webview.getDeferredPermissionRequestById(permissionRequest.id);
        if (allow) {
            deferredPermissionRequest.allow();
        }
        else {
            deferredPermissionRequest.deny();
        }
        requestContainer.parentElement.removeChild(requestContainer);
    }

    // Construct some simple UI to tell the user about the permission request and get their
    // feedback via the allow and deny buttons
    const description = document.createElement("span");
    description.textContent = "Allow " + uri + " to access " + type + "?";

    const allow = document.createElement("button");
    allow.textContent = "Allow";
    allow.addEventListener("click", () => completeDeferredPermissionRequest(true));

    const deny = document.createElement("button");
    deny.textContent = "Deny";
    deny.addEventListener("click", () => completeDeferredPermissionRequest(false));

    requestContainer.appendChild(description);
    requestContainer.appendChild(allow);
    requestContainer.appendChild(deny);
    document.body.appendChild(requestContainer);

    permissionRequest.defer();
});
```

## Методы

### Пуск

Разрешает запрос на разрешение.

```js
deferredPermissionRequest.allow();
```

#### Параметры

У этого метода нет параметров.

#### Возвращаемое значение

Этот метод не возвращает значение.

### запретить

Отклоняет запрос на разрешение.

```js
deferredPermissionRequest.deny();
```

#### Параметры

У этого метода нет параметров.

#### Возвращаемое значение

Этот метод не возвращает значение.

## Свойства

### id

Уникальный идентификатор, который можно использовать для сопоставления текущего DeferredPermissionRequest с объектом PermissionRequest из предыдущего события MSWebViewPermissionRequested. Просмотрите метод **PermissionRequested. отсрочки** .

Это свойство доступно только для чтения.

```js
var id = deferredPermissionRequest.id;
```

##### Значение свойства

Тип: **Long без знака**

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

```js
var type = deferredPermissionRequest.type;
```

#### Значение свойства

Тип: **строка**

### uri

Универсальный код ресурса (URI) документа, запросившего разрешение.

Это свойство доступно только для чтения.

```js
var uri = deferredPermissionRequest.uri;
```

##### Значение свойства

Тип: **строка**

## Требования

|                                           |                                      |
|-------------------------------------------|--------------------------------------|
| <strong>Минимальный поддерживаемый клиент</strong> | Windows 10 [только приложения Магазина Windows] |
| <strong>Минимальный поддерживаемый сервер</strong> |            Не поддерживается.             |
| <strong>Минимальный поддерживаемый телефон</strong>  |            Не поддерживается.             |
