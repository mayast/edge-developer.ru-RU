---
description: Определяет свойства, которые включают и отключают функции WebView
title: Объект MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/10/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 0e164e7eb44edc636201f283ec4bbe866a122b8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571301"
---
# Объект MSWebViewSettings

Определяет свойства, которые включают и отключают функции [WebView](../webview.md) .

## Свойства

### isIndexedDBEnabled

Возвращает или задает значение, указывающее, разрешено ли использование IndexedDB в [WebView](../webview.md).

```js
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```

#### Значение свойства
Тип: **логический**

**Значение true** , если IndexedDB можно использовать в **WebView**; в противном случае — **значение false**. 

### isJavaScriptEnabled

Возвращает или задает значение, указывающее, разрешено ли использование JavaScript в [WebView](../webview.md).

```js
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```

#### Значение свойства
Тип: **логический**

**Значение истина** JavaScript разрешен в [WebView](../webview.md); в противном случае — **значение false**. 

### isScriptNotifyAllowed

Возвращает или задает значение, указывающее, разрешено ли использование [ScriptNotifyEvent](ScriptNotifyEvent.md) в [WebView](../webview.md).

```js
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```

#### Значение свойства
Тип: **логический**

**Значение true** [ScriptNotifyEvent](ScriptNotifyEvent.md) разрешено в [WebView](../webview.md); в противном случае — **значение false**. 
