---
description: Указывает, что WebView пытается загрузить неподдерживаемый файл.
title: Объект UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752015"
---
# Объект UnviewableContentIdentifiedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Указывает, что [WebView](../webview.md) пытается перейти к файлу неподдерживаемого типа контента.  

## Свойства  

### Носителя  

Возвращает тип контента для непредставленного содержимого.  

Это свойство доступно только для чтения  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### Значение свойства  

Type (тип): **DOMString**  

### раздел  

Универсальный код ресурса (URI) страницы в [WebView](../webview.md) , запрашивающей навигацию.  

Это свойство доступно только для чтения.  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### Значение свойства  

Type (тип): **DOMString**  

### uri  

Универсальный код ресурса (URI) целевого объекта навигации.  

Это свойство доступно только для чтения.  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### Значение свойства  

Type (тип): **DOMString**  
