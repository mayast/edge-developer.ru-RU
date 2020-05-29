---
description: Содержатся сведения об источнике ссылки для навигации
title: Объект NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571294"
---
# Объект NavigationEventWithReferrer

Объект, представляющий событие, которое создается, когда инициируется Навигация, и навигация содержит ссылку.

## Свойства

### раздел

Универсальный код ресурса (URI) страницы в [WebView](../webview.md) , запрашивающей навигацию.

Это свойство доступно только для чтения.

#### Значение свойства
Type (тип): **DOMString**


```js
var referer = NavigationEventWithReferrer.referer;
```

### uri

Универсальный код ресурса (URI) целевого объекта навигации.

Это свойство доступно только для чтения.

```js
var uri = NavigationEventWithReferrer.uri;
```

#### Значение свойства
Type (тип): **DOMString**
