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
# <span data-ttu-id="f2815-104">Объект FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="f2815-104">FocusNavigationEvent object</span></span>

<span data-ttu-id="f2815-105">Отправленный объект из [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) , содержащего [**NavigationReason**](#navigationreason) и Location.</span><span class="sxs-lookup"><span data-stu-id="f2815-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span> 

## <span data-ttu-id="f2815-106">Методы</span><span class="sxs-lookup"><span data-stu-id="f2815-106">Methods</span></span>

### <span data-ttu-id="f2815-107">requestFocus</span><span class="sxs-lookup"><span data-stu-id="f2815-107">requestFocus</span></span>

<span data-ttu-id="f2815-108">Вызывается для перемещения фокуса из приложения в WebView.</span><span class="sxs-lookup"><span data-stu-id="f2815-108">Called to move focus from the app to the webview.</span></span>

### <span data-ttu-id="f2815-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="f2815-109">Parameters</span></span>

<span data-ttu-id="f2815-110">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="f2815-110">This method does not have parameters.</span></span>

### <span data-ttu-id="f2815-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f2815-111">Return value</span></span>

<span data-ttu-id="f2815-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="f2815-112">This method does not return a value.</span></span>

## <span data-ttu-id="f2815-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2815-113">Properties</span></span>
    
### <span data-ttu-id="f2815-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="f2815-114">navigationReason</span></span>

<span data-ttu-id="f2815-115">Перечисляемый тип **NavigationReason**, "Left", "стрелка вверх", "вправо" или "вниз".</span><span class="sxs-lookup"><span data-stu-id="f2815-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span> 

<span data-ttu-id="f2815-116">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f2815-116">This property is read-only.</span></span>

```js
var navigationReason = FocusNavigationEvent.navigationReason;
```

#### <span data-ttu-id="f2815-117">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2815-117">Property value</span></span>
<span data-ttu-id="f2815-118">Type (тип): **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="f2815-118">Type: **NavigationReason**</span></span>

### <span data-ttu-id="f2815-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="f2815-119">originHeight</span></span>

<span data-ttu-id="f2815-120">Положение начальной высоты элемента, на который будет передан фокус.</span><span class="sxs-lookup"><span data-stu-id="f2815-120">The origin height location of the element to be given focus.</span></span>

<span data-ttu-id="f2815-121">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f2815-121">This property is read-only.</span></span>

```js
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```

#### <span data-ttu-id="f2815-122">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2815-122">Property value</span></span>
<span data-ttu-id="f2815-123">Тип: с **плавающей точкой**</span><span class="sxs-lookup"><span data-stu-id="f2815-123">Type: **float**</span></span>

### <span data-ttu-id="f2815-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="f2815-124">originLeft</span></span>

<span data-ttu-id="f2815-125">Расположение элемента, на котором находится фокус, в исходном расположении слева от него.</span><span class="sxs-lookup"><span data-stu-id="f2815-125">The origin left location of the element to be given focus.</span></span>

<span data-ttu-id="f2815-126">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f2815-126">This property is read-only.</span></span>

```js
var originLeft = FocusNavigationEvent.originLeft;
```

#### <span data-ttu-id="f2815-127">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2815-127">Property value</span></span>
<span data-ttu-id="f2815-128">Тип: с **плавающей точкой**</span><span class="sxs-lookup"><span data-stu-id="f2815-128">Type: **float**</span></span>

### <span data-ttu-id="f2815-129">originTop</span><span class="sxs-lookup"><span data-stu-id="f2815-129">originTop</span></span>

<span data-ttu-id="f2815-130">Верхнее расположение элемента, на который будет наделена фокус.</span><span class="sxs-lookup"><span data-stu-id="f2815-130">The origin top location of the element to be given focus.</span></span>

<span data-ttu-id="f2815-131">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f2815-131">This property is read-only.</span></span>

```js
var originTop = FocusNavigationEvent.originTop;
```

#### <span data-ttu-id="f2815-132">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2815-132">Property value</span></span>
<span data-ttu-id="f2815-133">Тип: с **плавающей точкой**</span><span class="sxs-lookup"><span data-stu-id="f2815-133">Type: **float**</span></span>

### <span data-ttu-id="f2815-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="f2815-134">originWidth</span></span>

<span data-ttu-id="f2815-135">Положение начальной ширины элемента, на который будет передан фокус.</span><span class="sxs-lookup"><span data-stu-id="f2815-135">The origin width location of the element to be given focus.</span></span>

<span data-ttu-id="f2815-136">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f2815-136">This property is read-only.</span></span>

```js
var originWidth = FocusNavigationEvent.originWidth;
```

#### <span data-ttu-id="f2815-137">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f2815-137">Property value</span></span>
<span data-ttu-id="f2815-138">Тип: с **плавающей точкой**</span><span class="sxs-lookup"><span data-stu-id="f2815-138">Type: **float**</span></span>

