---
description: Представляет отложенный запрос на разрешение пользователя на доступ к функциям устройства.
title: Объект DeferredPermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: dc1f0753f879f511fdc380c806eb88b6be358016
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752144"
---
# <span data-ttu-id="bf5f7-104">Объект DeferredPermissionRequest</span><span class="sxs-lookup"><span data-stu-id="bf5f7-104">DeferredPermissionRequest object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="bf5f7-105">Представляет отложенный запрос содержимого [WebView](../webview.md) для разрешения конечным пользователем на доступ к специализированной функциональности устройства (например, географическое расположение или блокировку указателя).</span><span class="sxs-lookup"><span data-stu-id="bf5f7-105">Represents a deferred request by the content of the [webview](../webview.md) for end-user permission to access specialized device functionality (such as geolocation, or pointer lock).</span></span>  

```javascript
// In this sample, when we receive a permission request we construct some basic UI to ask the
// user if they want to give permission.
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    const requestContainer = document.createElement("div");

    // We use this function as the handler for the allow and deny buttons.
    function completeDeferredPermissionRequest(allow) {
        // Find the DeferredPermissionRequest using the id of the PermissionRequest we deferred.
        const deferredPermissionRequest = webview.getDeferredPermissionRequestById(permissionRequest.id);
        if (allow) {
            deferredPermissionRequest.allow();
        }
        else {
            deferredPermissionRequest.deny();
        }
        requestContainer.parentElement.removeChild(requestContainer);
    }

    // Construct some simple UI to tell the user about the permission request and get their
    // feedback via the allow and deny buttons
    const description = document.createElement("span");
    description.textContent = "Allow " + uri + " to access " + type + "?";

    const allow = document.createElement("button");
    allow.textContent = "Allow";
    allow.addEventListener("click", () => completeDeferredPermissionRequest(true));

    const deny = document.createElement("button");
    deny.textContent = "Deny";
    deny.addEventListener("click", () => completeDeferredPermissionRequest(false));

    requestContainer.appendChild(description);
    requestContainer.appendChild(allow);
    requestContainer.appendChild(deny);
    document.body.appendChild(requestContainer);

    permissionRequest.defer();
});
```  

## <span data-ttu-id="bf5f7-106">Методы</span><span class="sxs-lookup"><span data-stu-id="bf5f7-106">Methods</span></span>  

### <span data-ttu-id="bf5f7-107">Пуск</span><span class="sxs-lookup"><span data-stu-id="bf5f7-107">allow</span></span>  

<span data-ttu-id="bf5f7-108">Разрешает запрос на разрешение.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-108">Allows the request for permission.</span></span>  

```javascript
deferredPermissionRequest.allow();
```  

#### <span data-ttu-id="bf5f7-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf5f7-109">Parameters</span></span>  

<span data-ttu-id="bf5f7-110">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-110">This method has no parameters.</span></span>  

#### <span data-ttu-id="bf5f7-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf5f7-111">Return value</span></span>  

<span data-ttu-id="bf5f7-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-112">This method does not return a value.</span></span>  

### <span data-ttu-id="bf5f7-113">запретить</span><span class="sxs-lookup"><span data-stu-id="bf5f7-113">deny</span></span>  

<span data-ttu-id="bf5f7-114">Отклоняет запрос на разрешение.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-114">Denies the request for permission.</span></span>  

```javascript
deferredPermissionRequest.deny();
```  

#### <span data-ttu-id="bf5f7-115">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf5f7-115">Parameters</span></span>  

<span data-ttu-id="bf5f7-116">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-116">This method has no parameters.</span></span>  

#### <span data-ttu-id="bf5f7-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="bf5f7-117">Return value</span></span>  

<span data-ttu-id="bf5f7-118">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-118">This method does not return a value.</span></span>  

## <span data-ttu-id="bf5f7-119">Свойства</span><span class="sxs-lookup"><span data-stu-id="bf5f7-119">Properties</span></span>  

### <span data-ttu-id="bf5f7-120">id</span><span class="sxs-lookup"><span data-stu-id="bf5f7-120">id</span></span>  

<span data-ttu-id="bf5f7-121">Уникальный идентификатор, который можно использовать для сопоставления текущего DeferredPermissionRequest с объектом PermissionRequest из предыдущего события MSWebViewPermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-121">A unique ID that can be used to correlate the current DeferredPermissionRequest with a PermissionRequest object from a previous MSWebViewPermissionRequested event.</span></span> <span data-ttu-id="bf5f7-122">Просмотрите метод **PermissionRequested. отсрочки** .</span><span class="sxs-lookup"><span data-stu-id="bf5f7-122">See the **PermissionRequested.defer** method.</span></span>  

<span data-ttu-id="bf5f7-123">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-123">This property is read-only.</span></span>  

```javascript
var id = deferredPermissionRequest.id;
```  

##### <span data-ttu-id="bf5f7-124">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bf5f7-124">Property value</span></span>  

<span data-ttu-id="bf5f7-125">Тип: **Long без знака**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-125">Type: **Unsigned long**</span></span>  

### <span data-ttu-id="bf5f7-126">Тип</span><span class="sxs-lookup"><span data-stu-id="bf5f7-126">type</span></span>  

<span data-ttu-id="bf5f7-127">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-127">The type of permission being requested.</span></span> <span data-ttu-id="bf5f7-128">Это может быть одно из следующих строковых значений:</span><span class="sxs-lookup"><span data-stu-id="bf5f7-128">This may be one of the following string values:</span></span>  

*   <span data-ttu-id="bf5f7-129">**географическое расположение**: доступ к данным о расположении с помощью навигатора. Географическое положение.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-129">**geolocation**: access to location data via navigator.geolocation.</span></span>  
*   <span data-ttu-id="bf5f7-130">**unlimitedIndexedDBQuota**: позволяет IndexedDB API игнорировать обычное ограничение на размер сохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-130">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>  
*   <span data-ttu-id="bf5f7-131">**носители**: доступ к микрофону и камере с помощью навигатора. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-131">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>  
*   <span data-ttu-id="bf5f7-132">**pointerlock**: возможность блокировки и управления указателем мыши с помощью элемента. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-132">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>  
*   <span data-ttu-id="bf5f7-133">**уведомления**: возможность отображения уведомлений на рабочем столе через окно. Извещен.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-133">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>  
*   <span data-ttu-id="bf5f7-134">**экран**: возможность делать снимки экрана с помощью API захвата мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-134">**screen**: ability to take screen shots via the Media Capture API.</span></span>  
*   <span data-ttu-id="bf5f7-135">**immersiveview**: возможность управления выводом на экран в VR.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-135">**immersiveview**: ability to control a VR display.</span></span>  

<span data-ttu-id="bf5f7-136">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-136">This property is read-only.</span></span>  

```javascript
var type = deferredPermissionRequest.type;
```  

#### <span data-ttu-id="bf5f7-137">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bf5f7-137">Property value</span></span>  

<span data-ttu-id="bf5f7-138">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-138">Type: **String**</span></span>  

### <span data-ttu-id="bf5f7-139">uri</span><span class="sxs-lookup"><span data-stu-id="bf5f7-139">uri</span></span>  

<span data-ttu-id="bf5f7-140">Универсальный код ресурса (URI) документа, запросившего разрешение.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-140">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>  

<span data-ttu-id="bf5f7-141">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-141">This property is read-only.</span></span>  

```javascript
var uri = deferredPermissionRequest.uri;
```  

##### <span data-ttu-id="bf5f7-142">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="bf5f7-142">Property value</span></span>  

<span data-ttu-id="bf5f7-143">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="bf5f7-143">Type: **String**</span></span>  

## <span data-ttu-id="bf5f7-144">Требования</span><span class="sxs-lookup"><span data-stu-id="bf5f7-144">Requirements</span></span>  

|  |  |  
|:--- |:--- |  
| **<span data-ttu-id="bf5f7-145">Минимальный поддерживаемый клиент</span><span class="sxs-lookup"><span data-stu-id="bf5f7-145">Minimum supported client</span></span>** | <span data-ttu-id="bf5f7-146">Windows 10 [только приложения Магазина Windows]</span><span class="sxs-lookup"><span data-stu-id="bf5f7-146">Windows 10 [Windows Store apps only]</span></span> |  
| **<span data-ttu-id="bf5f7-147">Минимальный поддерживаемый сервер</span><span class="sxs-lookup"><span data-stu-id="bf5f7-147">Minimum supported server</span></span>** | <span data-ttu-id="bf5f7-148">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-148">Not supported</span></span> |  
| **<span data-ttu-id="bf5f7-149">Минимальный поддерживаемый телефон</span><span class="sxs-lookup"><span data-stu-id="bf5f7-149">Minimum supported phone</span></span>** | <span data-ttu-id="bf5f7-150">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="bf5f7-150">Not supported</span></span> |  
