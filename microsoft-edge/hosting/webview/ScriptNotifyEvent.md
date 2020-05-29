---
description: Представляет строку уведомления, переданную из содержимого WebView в приложение.
title: Объект ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570827"
---
# Объект ScriptNotifyEvent

Объект, представляющий событие, которое создается, когда содержимое, содержащееся в [WebView](../webview.md) , передает строку приложению с помощью JavaScript.

## Свойства
    
### callingUri

Возвращает универсальный код ресурса (URI) страницы, содержащей сценарий, сгенерировавший **ScriptNotifyEvent**.

Это свойство доступно только для чтения.

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### Значение свойства
Type (тип): **DOMString**

### value

Имя метода, переданное приложению.

Это свойство доступно только для чтения.

```js
var value = ScriptNotifyEvent.value;
```

#### Значение свойства
Type (тип): **DOMString**