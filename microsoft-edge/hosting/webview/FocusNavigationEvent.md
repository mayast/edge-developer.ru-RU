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
# <span data-ttu-id="9c584-104">Объект FocusNavigationEvent</span><span class="sxs-lookup"><span data-stu-id="9c584-104">FocusNavigationEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="9c584-105">Отправленный объект из [**NavigateFocus**](../webview.md#navigatefocus) / [**DepartingFocus**](../webview.md#departingfocus) , содержащего [**NavigationReason**](#navigationreason) и Location.</span><span class="sxs-lookup"><span data-stu-id="9c584-105">The dispatched object from [**NavigateFocus**](../webview.md#navigatefocus)/[**DepartingFocus**](../webview.md#departingfocus) containing the [**NavigationReason**](#navigationreason) and location.</span></span>  

## <span data-ttu-id="9c584-106">Методы</span><span class="sxs-lookup"><span data-stu-id="9c584-106">Methods</span></span>  

### <span data-ttu-id="9c584-107">requestFocus</span><span class="sxs-lookup"><span data-stu-id="9c584-107">requestFocus</span></span>  

<span data-ttu-id="9c584-108">Вызывается для перемещения фокуса из приложения в WebView.</span><span class="sxs-lookup"><span data-stu-id="9c584-108">Called to move focus from the app to the webview.</span></span>  

### <span data-ttu-id="9c584-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9c584-109">Parameters</span></span>  

<span data-ttu-id="9c584-110">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="9c584-110">This method does not have parameters.</span></span>  

### <span data-ttu-id="9c584-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9c584-111">Return value</span></span>  

<span data-ttu-id="9c584-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="9c584-112">This method does not return a value.</span></span>  

## <span data-ttu-id="9c584-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="9c584-113">Properties</span></span>  

### <span data-ttu-id="9c584-114">navigationReason</span><span class="sxs-lookup"><span data-stu-id="9c584-114">navigationReason</span></span>  

<span data-ttu-id="9c584-115">Перечисляемый тип **NavigationReason**, "Left", "стрелка вверх", "вправо" или "вниз".</span><span class="sxs-lookup"><span data-stu-id="9c584-115">Enumerated type **NavigationReason**, either "left", "up", "right", or "down".</span></span>  

<span data-ttu-id="9c584-116">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9c584-116">This property is read-only.</span></span>  

```javascript
var navigationReason = FocusNavigationEvent.navigationReason;
```  

#### <span data-ttu-id="9c584-117">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9c584-117">Property value</span></span>  

<span data-ttu-id="9c584-118">Type (тип): **NavigationReason**</span><span class="sxs-lookup"><span data-stu-id="9c584-118">Type: **NavigationReason**</span></span>  

### <span data-ttu-id="9c584-119">originHeight</span><span class="sxs-lookup"><span data-stu-id="9c584-119">originHeight</span></span>  

<span data-ttu-id="9c584-120">Положение начальной высоты элемента, на который будет передан фокус.</span><span class="sxs-lookup"><span data-stu-id="9c584-120">The origin height location of the element to be given focus.</span></span>  

<span data-ttu-id="9c584-121">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9c584-121">This property is read-only.</span></span>  

```javascript
var originWoriginHeightidth = FocusNavigationEvent.originHeight;
```  

#### <span data-ttu-id="9c584-122">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9c584-122">Property value</span></span>  

<span data-ttu-id="9c584-123">Тип: с **плавающей точкой**</span><span class="sxs-lookup"><span data-stu-id="9c584-123">Type: **float**</span></span>  

### <span data-ttu-id="9c584-124">originLeft</span><span class="sxs-lookup"><span data-stu-id="9c584-124">originLeft</span></span>  

<span data-ttu-id="9c584-125">Расположение элемента, на котором находится фокус, в исходном расположении слева от него.</span><span class="sxs-lookup"><span data-stu-id="9c584-125">The origin left location of the element to be given focus.</span></span>  

<span data-ttu-id="9c584-126">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9c584-126">This property is read-only.</span></span>  

```javascript
var originLeft = FocusNavigationEvent.originLeft;
```  

#### <span data-ttu-id="9c584-127">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9c584-127">Property value</span></span>  

<span data-ttu-id="9c584-128">Тип: с **плавающей точкой**</span><span class="sxs-lookup"><span data-stu-id="9c584-128">Type: **float**</span></span>  

### <span data-ttu-id="9c584-129">originTop</span><span class="sxs-lookup"><span data-stu-id="9c584-129">originTop</span></span>  

<span data-ttu-id="9c584-130">Верхнее расположение элемента, на который будет наделена фокус.</span><span class="sxs-lookup"><span data-stu-id="9c584-130">The origin top location of the element to be given focus.</span></span>  

<span data-ttu-id="9c584-131">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9c584-131">This property is read-only.</span></span>  

```javascript
var originTop = FocusNavigationEvent.originTop;
```  

#### <span data-ttu-id="9c584-132">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9c584-132">Property value</span></span>  

<span data-ttu-id="9c584-133">Тип: с **плавающей точкой**</span><span class="sxs-lookup"><span data-stu-id="9c584-133">Type: **float**</span></span>  

### <span data-ttu-id="9c584-134">originWidth</span><span class="sxs-lookup"><span data-stu-id="9c584-134">originWidth</span></span>  

<span data-ttu-id="9c584-135">Положение начальной ширины элемента, на который будет передан фокус.</span><span class="sxs-lookup"><span data-stu-id="9c584-135">The origin width location of the element to be given focus.</span></span>  

<span data-ttu-id="9c584-136">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9c584-136">This property is read-only.</span></span>  

```javascript
var originWidth = FocusNavigationEvent.originWidth;
```  

#### <span data-ttu-id="9c584-137">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="9c584-137">Property value</span></span>  

<span data-ttu-id="9c584-138">Тип: с **плавающей точкой**</span><span class="sxs-lookup"><span data-stu-id="9c584-138">Type: **float**</span></span>  
