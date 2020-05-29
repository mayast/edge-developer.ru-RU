---
description: Указывает, что WebView пытается загрузить неподдерживаемый файл.
title: Объект UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570826"
---
# Объект UnviewableContentIdentifiedEvent

Указывает, что [WebView](../webview.md) пытается перейти к файлу неподдерживаемого типа контента. 

## Свойства

### Носителя

Возвращает тип контента для непредставленного содержимого.

Это свойство доступно только для чтения

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### Значение свойства
Type (тип): **DOMString**

### раздел

Универсальный код ресурса (URI) страницы в [WebView](../webview.md) , запрашивающей навигацию.

Это свойство доступно только для чтения.


```js
var referer = NavigationEventWithReferrer.referer;
```

#### Значение свойства
Type (тип): **DOMString**

### uri

Универсальный код ресурса (URI) целевого объекта навигации.

Это свойство доступно только для чтения.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Значение свойства
Type (тип): **DOMString**
