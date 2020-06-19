---
description: Содержатся сведения о завершенной навигации WebView
title: Объект NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752142"
---
# Объект NavigationCompletedEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Объект, который представляет событие, которое создается, когда [WebView](../webview.md) закончит загрузку текущего содержимого или переход завершился сбоем.  

## Свойства  

### uri  

Универсальный код ресурса (URI) структуры навигации.  

Это свойство доступно только для чтения.  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### Значение свойства  

Type (тип): **DOMString**  

### Удачи  

Возвращает значение, указывающее, успешно ли завершилась Навигация.  

Это свойство доступно только для чтения.  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### Значение свойства  

Тип: **логический**  

### webErrorStatus  

Если навигация завершилась неудачей, получает значение, указывающее, почему.  

Это свойство доступно только для чтения.  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### Значение свойства  

Тип: **Long без знака**  
