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
# <span data-ttu-id="91ba8-104">Объект MSWebViewAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="91ba8-104">MSWebViewAsyncOperation object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="91ba8-105">Показывает, успешно ли завершилась операция или завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="91ba8-105">Exposes whether the operation completed successfully or failed.</span></span>  

## <span data-ttu-id="91ba8-106">Мероприятия</span><span class="sxs-lookup"><span data-stu-id="91ba8-106">Events</span></span>  

### <span data-ttu-id="91ba8-107">завершение</span><span class="sxs-lookup"><span data-stu-id="91ba8-107">complete</span></span>  

<span data-ttu-id="91ba8-108">Указывает на то, что операция завершена.</span><span class="sxs-lookup"><span data-stu-id="91ba8-108">Indicates that the operation completed.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```  

#### <span data-ttu-id="91ba8-109">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="91ba8-109">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="91ba8-110">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="91ba8-110">Interface</span></span>** | **<span data-ttu-id="91ba8-111">Событие</span><span class="sxs-lookup"><span data-stu-id="91ba8-111">Event</span></span>** |  
| **<span data-ttu-id="91ba8-112">Синхронный</span><span class="sxs-lookup"><span data-stu-id="91ba8-112">Synchronous</span></span>** |<span data-ttu-id="91ba8-113">Да</span><span class="sxs-lookup"><span data-stu-id="91ba8-113">Yes</span></span> |  
| **<span data-ttu-id="91ba8-114">Давать</span><span class="sxs-lookup"><span data-stu-id="91ba8-114">Bubbles</span></span>** |<span data-ttu-id="91ba8-115">Нет</span><span class="sxs-lookup"><span data-stu-id="91ba8-115">No</span></span> |   
| **<span data-ttu-id="91ba8-116">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="91ba8-116">Cancelable</span></span>** |<span data-ttu-id="91ba8-117">Нет</span><span class="sxs-lookup"><span data-stu-id="91ba8-117">No</span></span> |  

### <span data-ttu-id="91ba8-118">ошибка</span><span class="sxs-lookup"><span data-stu-id="91ba8-118">error</span></span>  

<span data-ttu-id="91ba8-119">Указывает, что при выполнении операции произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="91ba8-119">Indicates that there was an error with the operation.</span></span>  

```javascript
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```  

#### <span data-ttu-id="91ba8-120">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="91ba8-120">Event Information</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="91ba8-121">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="91ba8-121">Interface</span></span>** | **<span data-ttu-id="91ba8-122">Событие</span><span class="sxs-lookup"><span data-stu-id="91ba8-122">Event</span></span>** |  
| **<span data-ttu-id="91ba8-123">Синхронный</span><span class="sxs-lookup"><span data-stu-id="91ba8-123">Synchronous</span></span>** | <span data-ttu-id="91ba8-124">Да</span><span class="sxs-lookup"><span data-stu-id="91ba8-124">Yes</span></span> |  
| **<span data-ttu-id="91ba8-125">Давать</span><span class="sxs-lookup"><span data-stu-id="91ba8-125">Bubbles</span></span>** | <span data-ttu-id="91ba8-126">Нет</span><span class="sxs-lookup"><span data-stu-id="91ba8-126">No</span></span> |  
| **<span data-ttu-id="91ba8-127">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="91ba8-127">Cancelable</span></span>** | <span data-ttu-id="91ba8-128">Нет</span><span class="sxs-lookup"><span data-stu-id="91ba8-128">No</span></span> |  

## <span data-ttu-id="91ba8-129">Методы</span><span class="sxs-lookup"><span data-stu-id="91ba8-129">Methods</span></span>  

### <span data-ttu-id="91ba8-130">start</span><span class="sxs-lookup"><span data-stu-id="91ba8-130">start</span></span>  

<span data-ttu-id="91ba8-131">Вызывается для запуска асинхронной задачи.</span><span class="sxs-lookup"><span data-stu-id="91ba8-131">Called to start the async task.</span></span>  

```javascript
MSWebViewAsyncOperation.start();
```  

### <span data-ttu-id="91ba8-132">Параметры</span><span class="sxs-lookup"><span data-stu-id="91ba8-132">Parameters</span></span>  

<span data-ttu-id="91ba8-133">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="91ba8-133">This method does not have parameters.</span></span>  

### <span data-ttu-id="91ba8-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="91ba8-134">Return value</span></span>  

<span data-ttu-id="91ba8-135">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="91ba8-135">This method does not return a value.</span></span>  

## <span data-ttu-id="91ba8-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="91ba8-136">Properties</span></span>  

### <span data-ttu-id="91ba8-137">ошибка</span><span class="sxs-lookup"><span data-stu-id="91ba8-137">error</span></span>  

<span data-ttu-id="91ba8-138">Возникшая ошибка.</span><span class="sxs-lookup"><span data-stu-id="91ba8-138">The error that occurred.</span></span>  

<span data-ttu-id="91ba8-139">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91ba8-139">This property is read-only.</span></span>  

```javascript
var error = MSWebViewAsyncOperation.error;
```  

#### <span data-ttu-id="91ba8-140">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="91ba8-140">Property value</span></span>  

<span data-ttu-id="91ba8-141">Type (тип): **DOMError**</span><span class="sxs-lookup"><span data-stu-id="91ba8-141">Type: **DOMError**</span></span>  

### <span data-ttu-id="91ba8-142">OnComplete</span><span class="sxs-lookup"><span data-stu-id="91ba8-142">oncomplete</span></span>  

<span data-ttu-id="91ba8-143">Обработчик событий **Complete** .</span><span class="sxs-lookup"><span data-stu-id="91ba8-143">The **complete** event handler.</span></span>  

```javascript
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```  

#### <span data-ttu-id="91ba8-144">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="91ba8-144">Property value</span></span>  

<span data-ttu-id="91ba8-145">Тип: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="91ba8-145">Type: **EventHandler**</span></span>  

### <span data-ttu-id="91ba8-146">ПриОшибке</span><span class="sxs-lookup"><span data-stu-id="91ba8-146">onerror</span></span>  

<span data-ttu-id="91ba8-147">Обработчик событий **ошибки** .</span><span class="sxs-lookup"><span data-stu-id="91ba8-147">The **error** event handler.</span></span>  

```javascript
var onerror = MSWebViewAsyncOperation.onerror;
```  

#### <span data-ttu-id="91ba8-148">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="91ba8-148">Property value</span></span>  

<span data-ttu-id="91ba8-149">Тип: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="91ba8-149">Type: **EventHandler**</span></span>  

### <span data-ttu-id="91ba8-150">readyState</span><span class="sxs-lookup"><span data-stu-id="91ba8-150">readyState</span></span>  

<span data-ttu-id="91ba8-151">Описывает состояние готовности объекта.</span><span class="sxs-lookup"><span data-stu-id="91ba8-151">Describes the ready state of the object.</span></span>  

<span data-ttu-id="91ba8-152">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91ba8-152">This property is read-only.</span></span>  

```javascript
var readyState = MSWebViewAsyncOperation.readyState;
```  

#### <span data-ttu-id="91ba8-153">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="91ba8-153">Property value</span></span>  

<span data-ttu-id="91ba8-154">Тип: **короткий без знака**</span><span class="sxs-lookup"><span data-stu-id="91ba8-154">Type: **unsigned short**</span></span>  

### <span data-ttu-id="91ba8-155">завершил</span><span class="sxs-lookup"><span data-stu-id="91ba8-155">result</span></span>  

<span data-ttu-id="91ba8-156">Результат операции.</span><span class="sxs-lookup"><span data-stu-id="91ba8-156">The result of the operation.</span></span>  

<span data-ttu-id="91ba8-157">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91ba8-157">This property is read-only.</span></span>  

```javascript
var result = MSWebViewAsyncOperation.result;
```  

#### <span data-ttu-id="91ba8-158">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="91ba8-158">Property value</span></span>  

<span data-ttu-id="91ba8-159">Type (тип): Any</span><span class="sxs-lookup"><span data-stu-id="91ba8-159">Type: any</span></span>  

### <span data-ttu-id="91ba8-160">target</span><span class="sxs-lookup"><span data-stu-id="91ba8-160">target</span></span>  

<span data-ttu-id="91ba8-161">Целевой объект операции.</span><span class="sxs-lookup"><span data-stu-id="91ba8-161">The target of the operation.</span></span>  

<span data-ttu-id="91ba8-162">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91ba8-162">This property is read-only.</span></span>  

```javascript
var target = MSWebViewAsyncOperation.target;
```  

#### <span data-ttu-id="91ba8-163">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="91ba8-163">Property value</span></span>  

<span data-ttu-id="91ba8-164">Type (тип): [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="91ba8-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>  

### <span data-ttu-id="91ba8-165">Тип</span><span class="sxs-lookup"><span data-stu-id="91ba8-165">type</span></span>  

<span data-ttu-id="91ba8-166">Тип операции.</span><span class="sxs-lookup"><span data-stu-id="91ba8-166">The type of the operation.</span></span>  

<span data-ttu-id="91ba8-167">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="91ba8-167">This property is read-only.</span></span>  

```javascript
var type = MSWebViewAsyncOperation.type;
```  

#### <span data-ttu-id="91ba8-168">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="91ba8-168">Property value</span></span>  

<span data-ttu-id="91ba8-169">Тип: **короткий без знака**</span><span class="sxs-lookup"><span data-stu-id="91ba8-169">Type: **unsigned short**</span></span>  
