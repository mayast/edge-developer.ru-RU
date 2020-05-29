---
description: Отправленный объект из события Focus, содержащего причины навигации и расположение
title: Объект FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: b988bcd7ff252b9972bef9a31339a34b4b58d9ee
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571311"
---
# Объект FocusNavigationEvent

Отправленный объект из [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) , содержащего [**NavigationReason**](#navigationreason) и Location. 

## Методы

### requestFocus

Вызывается для перемещения фокуса из приложения в WebView.

### Параметры

У этого метода нет параметров.

### Возвращаемое значение

Этот метод не возвращает значение.

## Свойства
    
### navigationReason

Перечисляемый тип **NavigationReason**, "Left", "стрелка вверх", "вправо" или "вниз". 

Это свойство доступно только для чтения.

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### Значение свойства
Type (тип): **NavigationReason**

### originHeight

Положение начальной высоты элемента, на который будет передан фокус.

Это свойство доступно только для чтения.

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### Значение свойства
Тип: с **плавающей точкой**

### originLeft

Расположение элемента, на котором находится фокус, в исходном расположении слева от него.

Это свойство доступно только для чтения.

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### Значение свойства
Тип: с **плавающей точкой**

### originTop

Верхнее расположение элемента, на который будет наделена фокус.

Это свойство доступно только для чтения.

```js
var originTop = FocusNavigationEvent.originTop;
```

#### Значение свойства
Тип: с **плавающей точкой**

### originWidth

Положение начальной ширины элемента, на который будет передан фокус.

Это свойство доступно только для чтения.

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### Значение свойства
Тип: с **плавающей точкой**

