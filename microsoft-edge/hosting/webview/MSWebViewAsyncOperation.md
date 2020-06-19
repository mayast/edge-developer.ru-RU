---
description: Показывает, успешно ли завершилась операция или завершилась сбоем.
title: Объект MSWebViewAsyncOperation
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: d6e03af2a0205938f19120076aa0ad622539d7e5
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752128"
---
# Объект MSWebViewAsyncOperation  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Показывает, успешно ли завершилась операция или завершилась сбоем.  

## Мероприятия  

### завершение  

Указывает на то, что операция завершена.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | **Событие** |  
| **Синхронный** |Да |  
| **Давать** |Нет |   
| **Отменяемая** |Нет |  

### ошибка  

Указывает, что при выполнении операции произошла ошибка.  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### Сведения о событии  

|  |  |  
|:--- |:--- |  
| **Интерфейс** | **Событие** |  
| **Синхронный** | Да |  
| **Давать** | Нет |  
| **Отменяемая** | Нет |  

## Методы  

### start  

Вызывается для запуска асинхронной задачи.  

```javascript
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

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### Значение свойства  

Type (тип): **DOMError**  

### OnComplete  

Обработчик событий **Complete** .  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### Значение свойства  

Тип: **EventHandler**  

### ПриОшибке  

Обработчик событий **ошибки** .  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### Значение свойства  

Тип: **EventHandler**  

### readyState  

Описывает состояние готовности объекта.  

Это свойство доступно только для чтения.  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### Значение свойства  

Тип: **короткий без знака**  

### завершил  

Результат операции.  

Это свойство доступно только для чтения.  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### Значение свойства  

Type (тип): Any  

### target  

Целевой объект операции.  

Это свойство доступно только для чтения.  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### Значение свойства  

Type (тип): [ **MSHTMLWebViewElement**](../webview.md)  

### Тип  

Тип операции.  

Это свойство доступно только для чтения.  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### Значение свойства  

Тип: **короткий без знака**  
