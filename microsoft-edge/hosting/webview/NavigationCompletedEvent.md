---
description: Содержатся сведения о завершенной навигации WebView
title: Объект NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571300"
---
# Объект NavigationCompletedEvent

Объект, который представляет событие, которое создается, когда [WebView](../webview.md) закончит загрузку текущего содержимого или переход завершился сбоем.

## Свойства
    
### uri

Универсальный код ресурса (URI) структуры навигации.

Это свойство доступно только для чтения.

```js
var uri = NavigationCompletedEvent.uri;
```

#### Значение свойства
Type (тип): **DOMString**

### Удачи

Возвращает значение, указывающее, успешно ли завершилась Навигация.

Это свойство доступно только для чтения

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### Значение свойства
Тип: **логический**

### webErrorStatus

Если навигация завершилась неудачей, получает значение, указывающее, почему.

Это свойство доступно только для чтения

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### Значение свойства
Тип: **Long без знака**
