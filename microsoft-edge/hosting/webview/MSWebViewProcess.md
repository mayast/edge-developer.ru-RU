---
description: Представляет процесс WebView.
title: Объект MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571303"
---
# Объект MSWebViewProcess

Представляет процесс [WebView](../webview.md) .

```js
var wvprocess = new MSWebViewProcess();
```

## Свойства

### enterpriseId

Корпоративный идентификатор процесса.

```js
var enterpriseId = wvprocess.enterpriseId;
```

Это свойство доступно только для чтения.

#### Значение свойства
Type (тип): **DOMString**

### isPrivateNetworkClientServerCapabilityEnabled

Возвращает значение, показывающее, разрешено ли процессу [WebView](../webview.md) в манифесте приложения *частные сети (клиент & сервер)* [объявление возможностей](/windows/uwp/packaging/app-capability-declarations) универсального приложения для Windows.

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

Это свойство доступно только для чтения.

#### Значение свойства
Тип: **логический**

## Методы

### CreateWebViewAsync

Создает [WebView](../webview.md) в определенном процессе.

```js
wvprocess.createWebviewAsync();
```

#### Возвращаемое значение

Команду**`Promise<MSHTMLWebViewElement>`**

### GetWebViews

Возвращает последовательность объектов **MSWebViewProcess** , размещенных в процессе.

#### Возвращаемое значение

Команду**`sequence<MSHTMLWebViewElement>`**

### Разорван

Завершает процесс.

```js
wvprocess.terminate();
```

#### Возвращаемое значение

Этот метод не возвращает значение.
