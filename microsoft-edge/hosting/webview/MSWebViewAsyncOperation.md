---
description: Показывает, успешно ли завершилась операция или завершилась сбоем.
title: Объект MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: ebb89c0fc645ebcd97357af10af2be650d8218b9
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571304"
---
# Объект MSWebViewAsyncOperation

Показывает, успешно ли завершилась операция или завершилась сбоем. 

## События

### завершение

Указывает на то, что операция завершена. 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### Сведения о событии

|            |      |
|------------|------|
|**Интерфейс** | **Событие**
|**Синхронный** |Да |    
|**Давать**     |Нет |   
|**Отменяемая**  |Нет |        


### ошибка

Указывает, что при выполнении операции произошла ошибка.

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### Сведения о событии

|            |      |
|------------|------|
|**Интерфейс** | **Событие**
|**Синхронный** |Да |    
|**Давать**     |Нет |   
|**Отменяемая**  |Нет |            


## Методы

### start

Вызывается для запуска асинхронной задачи. 

```js
MSWebViewAsyncOperation.start();
```

### Параметры

У этого метода нет параметров.

### Возвращаемое значение

Этот метод не возвращает значение.

## Свойства

### ошибка

Возникшая ошибка.

Это свойство доступно только для чтения.

```js
var error = MSWebViewAsyncOperation.error;
```

#### Значение свойства
Type (тип): **DOMError**

### OnComplete

Обработчик событий **Complete** . 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### Значение свойства
Тип: **EventHandler**

### ПриОшибке

Обработчик событий **ошибки** . 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### Значение свойства
Тип: **EventHandler**

### readyState

Описывает состояние готовности объекта.

Это свойство доступно только для чтения.

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### Значение свойства
Тип: **короткий без знака**

### завершил

Результат операции.

Это свойство доступно только для чтения.

```js
var result = MSWebViewAsyncOperation.result;
```

#### Значение свойства
Type (тип): Any

### target

Целевой объект операции. 

Это свойство доступно только для чтения.

```js
var target = MSWebViewAsyncOperation.target;
```

#### Значение свойства
Type (тип): [ **MSHTMLWebViewElement**](../webview.md)

### Тип

Тип операции.

Это свойство доступно только для чтения.

```js
var type = MSWebViewAsyncOperation.type;
```

#### Значение свойства
Тип: **короткий без знака**
