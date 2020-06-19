---
description: Содержатся сведения об источнике ссылки для навигации
title: Объект NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752130"
---
# Объект NavigationEventWithReferrer  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Объект, представляющий событие, которое создается, когда инициируется Навигация, и навигация содержит ссылку.  

## Свойства  

### раздел

Универсальный код ресурса (URI) страницы в [WebView](../webview.md) , запрашивающей навигацию.  

Это свойство доступно только для чтения.  

#### Значение свойства  

Type (тип): **DOMString**  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### uri  

Универсальный код ресурса (URI) целевого объекта навигации.  

Это свойство доступно только для чтения.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Значение свойства  

Type (тип): **DOMString**  
