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
# <span data-ttu-id="e28f9-104">Объект MSWebViewAsyncOperation</span><span class="sxs-lookup"><span data-stu-id="e28f9-104">MSWebViewAsyncOperation object</span></span>

<span data-ttu-id="e28f9-105">Показывает, успешно ли завершилась операция или завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="e28f9-105">Exposes whether the operation completed successfully or failed.</span></span> 

## <span data-ttu-id="e28f9-106">События</span><span class="sxs-lookup"><span data-stu-id="e28f9-106">Events</span></span>

### <span data-ttu-id="e28f9-107">завершение</span><span class="sxs-lookup"><span data-stu-id="e28f9-107">complete</span></span>

<span data-ttu-id="e28f9-108">Указывает на то, что операция завершена.</span><span class="sxs-lookup"><span data-stu-id="e28f9-108">Indicates that the operation completed.</span></span> 

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("complete", handler);
MSWebViewAsyncOperation.removeEventListener("complete", handler);
```

#### <span data-ttu-id="e28f9-109">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="e28f9-109">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="e28f9-110">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="e28f9-110">Interface</span></span>** | **<span data-ttu-id="e28f9-111">Событие</span><span class="sxs-lookup"><span data-stu-id="e28f9-111">Event</span></span>**
|**<span data-ttu-id="e28f9-112">Синхронный</span><span class="sxs-lookup"><span data-stu-id="e28f9-112">Synchronous</span></span>** |<span data-ttu-id="e28f9-113">Да</span><span class="sxs-lookup"><span data-stu-id="e28f9-113">Yes</span></span> |    
|**<span data-ttu-id="e28f9-114">Давать</span><span class="sxs-lookup"><span data-stu-id="e28f9-114">Bubbles</span></span>**     |<span data-ttu-id="e28f9-115">Нет</span><span class="sxs-lookup"><span data-stu-id="e28f9-115">No</span></span> |   
|**<span data-ttu-id="e28f9-116">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="e28f9-116">Cancelable</span></span>**  |<span data-ttu-id="e28f9-117">Нет</span><span class="sxs-lookup"><span data-stu-id="e28f9-117">No</span></span> |        


### <span data-ttu-id="e28f9-118">ошибка</span><span class="sxs-lookup"><span data-stu-id="e28f9-118">error</span></span>

<span data-ttu-id="e28f9-119">Указывает, что при выполнении операции произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="e28f9-119">Indicates that there was an error with the operation.</span></span>

```js
function handler(eventInfo) { /* Your code */ }
 
// addEventListener syntax
MSWebViewAsyncOperation.addEventListener("error", handler);
MSWebViewAsyncOperation.removeEventListener("error", handler);
```

#### <span data-ttu-id="e28f9-120">Сведения о событии</span><span class="sxs-lookup"><span data-stu-id="e28f9-120">Event Information</span></span>

|            |      |
|------------|------|
|**<span data-ttu-id="e28f9-121">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="e28f9-121">Interface</span></span>** | **<span data-ttu-id="e28f9-122">Событие</span><span class="sxs-lookup"><span data-stu-id="e28f9-122">Event</span></span>**
|**<span data-ttu-id="e28f9-123">Синхронный</span><span class="sxs-lookup"><span data-stu-id="e28f9-123">Synchronous</span></span>** |<span data-ttu-id="e28f9-124">Да</span><span class="sxs-lookup"><span data-stu-id="e28f9-124">Yes</span></span> |    
|**<span data-ttu-id="e28f9-125">Давать</span><span class="sxs-lookup"><span data-stu-id="e28f9-125">Bubbles</span></span>**     |<span data-ttu-id="e28f9-126">Нет</span><span class="sxs-lookup"><span data-stu-id="e28f9-126">No</span></span> |   
|**<span data-ttu-id="e28f9-127">Отменяемая</span><span class="sxs-lookup"><span data-stu-id="e28f9-127">Cancelable</span></span>**  |<span data-ttu-id="e28f9-128">Нет</span><span class="sxs-lookup"><span data-stu-id="e28f9-128">No</span></span> |            


## <span data-ttu-id="e28f9-129">Методы</span><span class="sxs-lookup"><span data-stu-id="e28f9-129">Methods</span></span>

### <span data-ttu-id="e28f9-130">start</span><span class="sxs-lookup"><span data-stu-id="e28f9-130">start</span></span>

<span data-ttu-id="e28f9-131">Вызывается для запуска асинхронной задачи.</span><span class="sxs-lookup"><span data-stu-id="e28f9-131">Called to start the async task.</span></span> 

```js
MSWebViewAsyncOperation.start();
```

### <span data-ttu-id="e28f9-132">Параметры</span><span class="sxs-lookup"><span data-stu-id="e28f9-132">Parameters</span></span>

<span data-ttu-id="e28f9-133">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="e28f9-133">This method does not have parameters.</span></span>

### <span data-ttu-id="e28f9-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e28f9-134">Return value</span></span>

<span data-ttu-id="e28f9-135">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="e28f9-135">This method does not return a value.</span></span>

## <span data-ttu-id="e28f9-136">Свойства</span><span class="sxs-lookup"><span data-stu-id="e28f9-136">Properties</span></span>

### <span data-ttu-id="e28f9-137">ошибка</span><span class="sxs-lookup"><span data-stu-id="e28f9-137">error</span></span>

<span data-ttu-id="e28f9-138">Возникшая ошибка.</span><span class="sxs-lookup"><span data-stu-id="e28f9-138">The error that occured.</span></span>

<span data-ttu-id="e28f9-139">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e28f9-139">This property is read-only.</span></span>

```js
var error = MSWebViewAsyncOperation.error;
```

#### <span data-ttu-id="e28f9-140">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e28f9-140">Property value</span></span>
<span data-ttu-id="e28f9-141">Type (тип): **DOMError**</span><span class="sxs-lookup"><span data-stu-id="e28f9-141">Type: **DOMError**</span></span>

### <span data-ttu-id="e28f9-142">OnComplete</span><span class="sxs-lookup"><span data-stu-id="e28f9-142">oncomplete</span></span>

<span data-ttu-id="e28f9-143">Обработчик событий **Complete** .</span><span class="sxs-lookup"><span data-stu-id="e28f9-143">The **complete** event handler.</span></span> 

```js
var oncomplete = MSWebViewAsyncOperation.oncomplete;
```

#### <span data-ttu-id="e28f9-144">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e28f9-144">Property value</span></span>
<span data-ttu-id="e28f9-145">Тип: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="e28f9-145">Type: **EventHandler**</span></span>

### <span data-ttu-id="e28f9-146">ПриОшибке</span><span class="sxs-lookup"><span data-stu-id="e28f9-146">onerror</span></span>

<span data-ttu-id="e28f9-147">Обработчик событий **ошибки** .</span><span class="sxs-lookup"><span data-stu-id="e28f9-147">The **error** event handler.</span></span> 

```js
var onerror = MSWebViewAsyncOperation.onerror;
```

#### <span data-ttu-id="e28f9-148">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e28f9-148">Property value</span></span>
<span data-ttu-id="e28f9-149">Тип: **EventHandler**</span><span class="sxs-lookup"><span data-stu-id="e28f9-149">Type: **EventHandler**</span></span>

### <span data-ttu-id="e28f9-150">readyState</span><span class="sxs-lookup"><span data-stu-id="e28f9-150">readyState</span></span>

<span data-ttu-id="e28f9-151">Описывает состояние готовности объекта.</span><span class="sxs-lookup"><span data-stu-id="e28f9-151">Describes the ready state of the object.</span></span>

<span data-ttu-id="e28f9-152">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e28f9-152">This property is read-only.</span></span>

```js
var readyState = MSWebViewAsyncOperation.readyState;
```

#### <span data-ttu-id="e28f9-153">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e28f9-153">Property value</span></span>
<span data-ttu-id="e28f9-154">Тип: **короткий без знака**</span><span class="sxs-lookup"><span data-stu-id="e28f9-154">Type: **unsigned short**</span></span>

### <span data-ttu-id="e28f9-155">завершил</span><span class="sxs-lookup"><span data-stu-id="e28f9-155">result</span></span>

<span data-ttu-id="e28f9-156">Результат операции.</span><span class="sxs-lookup"><span data-stu-id="e28f9-156">The result of the operation.</span></span>

<span data-ttu-id="e28f9-157">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e28f9-157">This property is read-only.</span></span>

```js
var result = MSWebViewAsyncOperation.result;
```

#### <span data-ttu-id="e28f9-158">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e28f9-158">Property value</span></span>
<span data-ttu-id="e28f9-159">Type (тип): Any</span><span class="sxs-lookup"><span data-stu-id="e28f9-159">Type: any</span></span>

### <span data-ttu-id="e28f9-160">target</span><span class="sxs-lookup"><span data-stu-id="e28f9-160">target</span></span>

<span data-ttu-id="e28f9-161">Целевой объект операции.</span><span class="sxs-lookup"><span data-stu-id="e28f9-161">The target of the operation.</span></span> 

<span data-ttu-id="e28f9-162">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e28f9-162">This property is read-only.</span></span>

```js
var target = MSWebViewAsyncOperation.target;
```

#### <span data-ttu-id="e28f9-163">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e28f9-163">Property value</span></span>
<span data-ttu-id="e28f9-164">Type (тип): [ **MSHTMLWebViewElement**](../webview.md)</span><span class="sxs-lookup"><span data-stu-id="e28f9-164">Type: [**MSHTMLWebViewElement**](../webview.md)</span></span>

### <span data-ttu-id="e28f9-165">Тип</span><span class="sxs-lookup"><span data-stu-id="e28f9-165">type</span></span>

<span data-ttu-id="e28f9-166">Тип операции.</span><span class="sxs-lookup"><span data-stu-id="e28f9-166">The type of the operation.</span></span>

<span data-ttu-id="e28f9-167">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e28f9-167">This property is read-only.</span></span>

```js
var type = MSWebViewAsyncOperation.type;
```

#### <span data-ttu-id="e28f9-168">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e28f9-168">Property value</span></span>
<span data-ttu-id="e28f9-169">Тип: **короткий без знака**</span><span class="sxs-lookup"><span data-stu-id="e28f9-169">Type: **unsigned short**</span></span>
