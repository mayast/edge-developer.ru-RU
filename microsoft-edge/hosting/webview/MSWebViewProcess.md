---
description: Представляет процесс WebView.
title: Объект MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: bb70b0e8eb12c7a7c23d71f01ea24e9084caa156
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752158"
---
# Объект MSWebViewProcess  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Представляет процесс [WebView](../webview.md) .  

```javascript
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

```javascript
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```  

Это свойство доступно только для чтения.  

#### Значение свойства  

Тип: **логический**  

## Методы  

### CreateWebViewAsync  

Создает [WebView](../webview.md) в определенном процессе.  

```javascript
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

```javascript
wvprocess.terminate();
```  

#### Возвращаемое значение  

Этот метод не возвращает значение.  
