---
description: Представляет строку уведомления, переданную из содержимого WebView в приложение.
title: Объект ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752026"
---
# Объект ScriptNotifyEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Объект, представляющий событие, которое создается, когда содержимое, содержащееся в [WebView](../webview.md) , передает строку приложению с помощью JavaScript.  

## Свойства  

### callingUri  

Возвращает универсальный код ресурса (URI) страницы, содержащей сценарий, сгенерировавший **ScriptNotifyEvent**.  

Это свойство доступно только для чтения.  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### Значение свойства  

Type (тип): **DOMString**  

### value  

Имя метода, переданное приложению.  

Это свойство доступно только для чтения.  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### Значение свойства  

Type (тип): **DOMString**  
