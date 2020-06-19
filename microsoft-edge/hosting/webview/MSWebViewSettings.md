---
description: Определяет свойства, которые включают и отключают функции WebView
title: Объект MSWebViewSettings
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 147f852f8fbcb2a748c00b472814e9cc45b9c9da
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752180"
---
# Объект MSWebViewSettings  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Определяет свойства, которые включают и отключают функции [WebView](../webview.md) .  

## Свойства  

### isIndexedDBEnabled  

Возвращает или задает значение, указывающее, разрешено ли использование IndexedDB в [WebView](../webview.md).  

```javascript
var isIndexedDBEnabled = MSWebViewSettings.isIndexedDBEnabled;
MSWebViewSettings.isIndexedDBEnabled = isIndexedDBEnabled;
```  

#### Значение свойства  

Тип: **логический**  

**Значение true** , если IndexedDB можно использовать в **WebView**; в противном случае — **значение false**.  

### isJavaScriptEnabled  

Возвращает или задает значение, указывающее, разрешено ли использование JavaScript в [WebView](../webview.md).  

```javascript
var isJavaScriptEnabled = MSWebViewSettings.isJavaScriptEnabled;
MSWebViewSettings.isJavaScriptEnabled = isJavaScriptEnabled;
```  

#### Значение свойства  

Тип: **логический**  

**Значение истина** JavaScript разрешен в [WebView](../webview.md); в противном случае — **значение false**.  

### isScriptNotifyAllowed  

Возвращает или задает значение, указывающее, разрешено ли использование [ScriptNotifyEvent](ScriptNotifyEvent.md) в [WebView](../webview.md).  

```javascript
var isScriptNotifyAllowed = MSWebViewSettings.isScriptNotifyAllowed;
MSWebViewSettings.isScriptNotifyAllowed = isScriptNotifyAllowed;
```  

#### Значение свойства  

Тип: **логический**  

**Значение true** [ScriptNotifyEvent](ScriptNotifyEvent.md) разрешено в [WebView](../webview.md); в противном случае — **значение false**.  
