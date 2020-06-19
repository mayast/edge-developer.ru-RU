---
description: Отправленный объект из события Focus, содержащего причины навигации и расположение
title: Объект FocusNavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 88f0a4ef8834c6e851f81ee10bf4202a0429f969
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752166"
---
# Объект FocusNavigationEvent  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

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

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### Значение свойства  

Type (тип): **NavigationReason**  

### originHeight  

Положение начальной высоты элемента, на который будет передан фокус.  

Это свойство доступно только для чтения.  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### Значение свойства  

Тип: с **плавающей точкой**  

### originLeft  

Расположение элемента, на котором находится фокус, в исходном расположении слева от него.  

Это свойство доступно только для чтения.  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### Значение свойства  

Тип: с **плавающей точкой**  

### originTop  

Верхнее расположение элемента, на который будет наделена фокус.  

Это свойство доступно только для чтения.  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### Значение свойства  

Тип: с **плавающей точкой**  

### originWidth  

Положение начальной ширины элемента, на который будет передан фокус.  

Это свойство доступно только для чтения.  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### Значение свойства  

Тип: с **плавающей точкой**  
