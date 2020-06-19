---
description: Предоставляет сведения о запросе разрешения
title: Объект PermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: c769bf122c3ca116d5783b73d0ff4f183d2cd52d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752118"
---
# <span data-ttu-id="877ed-104">Объект PermissionRequest</span><span class="sxs-lookup"><span data-stu-id="877ed-104">PermissionRequest object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="877ed-105">Предоставляет сведения о запросе разрешений.</span><span class="sxs-lookup"><span data-stu-id="877ed-105">Provides information about a permission request.</span></span> <span data-ttu-id="877ed-106">Этот объект доступен из свойства permissionRequest аргументов события из события [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) WebView.</span><span class="sxs-lookup"><span data-stu-id="877ed-106">This object is available from the permissionRequest property of the event args from the [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) webview event.</span></span>  

```javascript
webview.addEventListener("MSWebViewPermissionRequested", permissionRequestedEventArgs => {
    const permissionRequest = permissionRequestedEventArgs.permissionRequest;
    switch (permissionRequest.type) {
        case "geolocation":
        case "media":
        case "pointerlock":
        case "webnotifications":
        case "screen":
        case "immersiveview":
            if (permissionRequest.uri.startsWith("https://www.example.com/")) {
                // Implicitly trust particular URI
                permissionRequest.allow();
            }
            else if (permissionRequest.uri.startsWith("https://")) {
                // Defer the request so we can ask the user to allow or deny the request
                permissionRequest.defer();
                // Later we'll need to use webview.getDeferredPermissionRequestById for this
                // request and call allow or deny.
                promptUserForDeferredPermissionRequest(
                    permissionRequest.id,
                    permissionRequest.uri,
                    permissionRequest.type);
            }
            else {
                // Implicitly deny non-https URIs
                permissionRequest.deny();
            }
            break;

        case "unlimitedIndexedDBQuota":
        default:
            permissionRequest.deny();
            break;
    }
});
```  

## <span data-ttu-id="877ed-107">Методы</span><span class="sxs-lookup"><span data-stu-id="877ed-107">Methods</span></span>  

### <span data-ttu-id="877ed-108">Пуск</span><span class="sxs-lookup"><span data-stu-id="877ed-108">allow</span></span>  

<span data-ttu-id="877ed-109">Разрешает запрос на разрешение.</span><span class="sxs-lookup"><span data-stu-id="877ed-109">Allows the request for permission.</span></span>  

#### <span data-ttu-id="877ed-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="877ed-110">Parameters</span></span>  

<span data-ttu-id="877ed-111">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="877ed-111">This method has no parameters.</span></span>  

#### <span data-ttu-id="877ed-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="877ed-112">Return value</span></span>  

<span data-ttu-id="877ed-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="877ed-113">This method does not return a value.</span></span>  

### <span data-ttu-id="877ed-114">отложить</span><span class="sxs-lookup"><span data-stu-id="877ed-114">defer</span></span>  

<span data-ttu-id="877ed-115">Если вместо синхронно разрешенных или запрещенных PermissionRequest, вам требуется время для взаимодействия с пользователем или выполнения какого-либо другого асинхронного действия, вызовите функцию отсрочки () в PermissionRequest.</span><span class="sxs-lookup"><span data-stu-id="877ed-115">If instead of synchronously allowing or disallowing a PermissionRequest, you require time to interact with the user or take some other asynchronous action, call defer() on the PermissionRequest.</span></span>  <span data-ttu-id="877ed-116">PermissionRequest теперь будет доступен как DeferredPermissionRequest из getDeferredPermissionRequests и getDeferredPermissionRequestById.</span><span class="sxs-lookup"><span data-stu-id="877ed-116">The PermissionRequest will now be available as a DeferredPermissionRequest from getDeferredPermissionRequests and getDeferredPermissionRequestById.</span></span>  <span data-ttu-id="877ed-117">Вы можете сопоставить текущую PermissionRequest с соответствующей DeferredPermissionRequest с помощью свойства Match ID.</span><span class="sxs-lookup"><span data-stu-id="877ed-117">You can correlate the current PermissionRequest with the corresponding DeferredPermissionRequest via the matching id property.</span></span>  

#### <span data-ttu-id="877ed-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="877ed-118">Parameters</span></span>  

<span data-ttu-id="877ed-119">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="877ed-119">This method has no parameters.</span></span>  

#### <span data-ttu-id="877ed-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="877ed-120">Return value</span></span>  

<span data-ttu-id="877ed-121">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="877ed-121">This method does not return a value.</span></span>  

### <span data-ttu-id="877ed-122">запретить</span><span class="sxs-lookup"><span data-stu-id="877ed-122">deny</span></span>  

<span data-ttu-id="877ed-123">Отклоняет запрос на разрешение.</span><span class="sxs-lookup"><span data-stu-id="877ed-123">Denies the request for permission.</span></span>  

#### <span data-ttu-id="877ed-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="877ed-124">Parameters</span></span>  

<span data-ttu-id="877ed-125">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="877ed-125">This method has no parameters.</span></span>  

#### <span data-ttu-id="877ed-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="877ed-126">Return value</span></span>  

<span data-ttu-id="877ed-127">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="877ed-127">This method does not return a value.</span></span>  

## <span data-ttu-id="877ed-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="877ed-128">Properties</span></span>  

### <span data-ttu-id="877ed-129">id</span><span class="sxs-lookup"><span data-stu-id="877ed-129">id</span></span>  

<span data-ttu-id="877ed-130">Уникальный идентификатор, который можно использовать для сопоставления текущего PermissionRequest с соответствующим DeferredPermissionRequest при использовании метода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="877ed-130">A unique ID that can be used to correlate the current PermissionRequest with a corresponding DeferredPermissionRequest if the defer method is used.</span></span>  <span data-ttu-id="877ed-131">Просмотрите метод "отложить".</span><span class="sxs-lookup"><span data-stu-id="877ed-131">See the defer method.</span></span>  

<span data-ttu-id="877ed-132">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="877ed-132">This property is read-only.</span></span>  

##### <span data-ttu-id="877ed-133">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="877ed-133">Property value</span></span>  

<span data-ttu-id="877ed-134">Тип: **Long без знака**</span><span class="sxs-lookup"><span data-stu-id="877ed-134">Type: **Unsigned long**</span></span>  

### <span data-ttu-id="877ed-135">состояни</span><span class="sxs-lookup"><span data-stu-id="877ed-135">state</span></span>  

<span data-ttu-id="877ed-136">Возвращает значение "неизвестно", "отложить", "разрешить" или "запретить", чтобы показать текущее состояние запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="877ed-136">Returns "unknown", "defer", "allow", or "deny" to indicate the current state of permission request.</span></span>  <span data-ttu-id="877ed-137">Строка состояния будет соответствовать тому, какой метод допускает, запрещает или задерживается (Последнее или неизвестное), если ни один из методов не был вызван.</span><span class="sxs-lookup"><span data-stu-id="877ed-137">The state string will correspond to whichever method allow, deny, or defer was called last or "unknown" if none of the methods have been called.</span></span>  

<span data-ttu-id="877ed-138">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="877ed-138">This property is read-only.</span></span>  

#### <span data-ttu-id="877ed-139">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="877ed-139">Property value</span></span>  

<span data-ttu-id="877ed-140">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="877ed-140">Type: **String**</span></span>  

### <span data-ttu-id="877ed-141">Тип</span><span class="sxs-lookup"><span data-stu-id="877ed-141">type</span></span>  

<span data-ttu-id="877ed-142">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="877ed-142">The type of permission being requested.</span></span> <span data-ttu-id="877ed-143">Это может быть одно из следующих строковых значений:</span><span class="sxs-lookup"><span data-stu-id="877ed-143">This may be one of the following string values:</span></span>  

*   <span data-ttu-id="877ed-144">**географическое расположение**: доступ к данным о расположении с помощью навигатора. Географическое положение.</span><span class="sxs-lookup"><span data-stu-id="877ed-144">**geolocation**: access to location data via navigator.geolocation.</span></span>  
*   <span data-ttu-id="877ed-145">**unlimitedIndexedDBQuota**: позволяет IndexedDB API игнорировать обычное ограничение на размер сохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="877ed-145">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>  
*   <span data-ttu-id="877ed-146">**носители**: доступ к микрофону и камере с помощью навигатора. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="877ed-146">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>  
*   <span data-ttu-id="877ed-147">**pointerlock**: возможность блокировки и управления указателем мыши с помощью элемента. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="877ed-147">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>  
*   <span data-ttu-id="877ed-148">**уведомления**: возможность отображения уведомлений на рабочем столе через окно. Извещен.</span><span class="sxs-lookup"><span data-stu-id="877ed-148">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>  
*   <span data-ttu-id="877ed-149">**экран**: возможность делать снимки экрана с помощью API захвата мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="877ed-149">**screen**: ability to take screen shots via the Media Capture API.</span></span>  
*   <span data-ttu-id="877ed-150">**immersiveview**: возможность управления выводом на экран в VR.</span><span class="sxs-lookup"><span data-stu-id="877ed-150">**immersiveview**: ability to control a VR display.</span></span>  

<span data-ttu-id="877ed-151">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="877ed-151">This property is read-only.</span></span>  

#### <span data-ttu-id="877ed-152">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="877ed-152">Property value</span></span>  

<span data-ttu-id="877ed-153">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="877ed-153">Type: **String**</span></span>  

### <span data-ttu-id="877ed-154">uri</span><span class="sxs-lookup"><span data-stu-id="877ed-154">uri</span></span>  

<span data-ttu-id="877ed-155">Универсальный код ресурса (URI) документа, запросившего разрешение.</span><span class="sxs-lookup"><span data-stu-id="877ed-155">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>  

<span data-ttu-id="877ed-156">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="877ed-156">This property is read-only.</span></span>  

#### <span data-ttu-id="877ed-157">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="877ed-157">Property value</span></span>  

<span data-ttu-id="877ed-158">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="877ed-158">Type: **String**</span></span>  
