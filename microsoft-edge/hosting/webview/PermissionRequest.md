---
description: Предоставляет сведения о запросе разрешения
title: Объект PermissionRequest
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/15/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 023f19170e7b5cdb52a1de9d5d4d7c755c89edbe
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571290"
---
# <span data-ttu-id="4b174-104">Объект PermissionRequest</span><span class="sxs-lookup"><span data-stu-id="4b174-104">PermissionRequest object</span></span>

<span data-ttu-id="4b174-105">Предоставляет сведения о запросе разрешений.</span><span class="sxs-lookup"><span data-stu-id="4b174-105">Provides information about a permission request.</span></span> <span data-ttu-id="4b174-106">Этот объект доступен из свойства permissionRequest аргументов события из события [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) WebView.</span><span class="sxs-lookup"><span data-stu-id="4b174-106">This object is available from the permissionRequest property of the event args from the [MSWebViewPermissionRequested](../webview.md#mswebviewpermissionrequested) webview event.</span></span>

```js
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

## <span data-ttu-id="4b174-107">Методы</span><span class="sxs-lookup"><span data-stu-id="4b174-107">Methods</span></span>

### <span data-ttu-id="4b174-108">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b174-108">allow</span></span>

<span data-ttu-id="4b174-109">Разрешает запрос на разрешение.</span><span class="sxs-lookup"><span data-stu-id="4b174-109">Allows the request for permission.</span></span>

#### <span data-ttu-id="4b174-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b174-110">Parameters</span></span>

<span data-ttu-id="4b174-111">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="4b174-111">This method has no parameters.</span></span>

#### <span data-ttu-id="4b174-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b174-112">Return value</span></span>

<span data-ttu-id="4b174-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4b174-113">This method does not return a value.</span></span>

### <span data-ttu-id="4b174-114">отложить</span><span class="sxs-lookup"><span data-stu-id="4b174-114">defer</span></span>

<span data-ttu-id="4b174-115">Если вместо синхронно разрешенных или запрещенных PermissionRequest, вам требуется время для взаимодействия с пользователем или выполнения какого-либо другого асинхронного действия, вызовите функцию отсрочки () в PermissionRequest.</span><span class="sxs-lookup"><span data-stu-id="4b174-115">If instead of synchronously allowing or disallowing a PermissionRequest, you require time to interact with the user or take some other asynchronous action, call defer() on the PermissionRequest.</span></span> <span data-ttu-id="4b174-116">PermissionRequest теперь будет доступен как DeferredPermissionRequest из getDeferredPermissionRequests и getDeferredPermissionRequestById.</span><span class="sxs-lookup"><span data-stu-id="4b174-116">The PermissionRequest will now be available as a DeferredPermissionRequest from getDeferredPermissionRequests and getDeferredPermissionRequestById.</span></span> <span data-ttu-id="4b174-117">Вы можете сопоставить текущую PermissionRequest с соответствующей DeferredPermissionRequest с помощью свойства Match ID.</span><span class="sxs-lookup"><span data-stu-id="4b174-117">You can correlate the current PermissionRequest with the corresponding DeferredPermissionRequest via the matching id property.</span></span>

#### <span data-ttu-id="4b174-118">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b174-118">Parameters</span></span>

<span data-ttu-id="4b174-119">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="4b174-119">This method has no parameters.</span></span>

#### <span data-ttu-id="4b174-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b174-120">Return value</span></span>

<span data-ttu-id="4b174-121">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4b174-121">This method does not return a value.</span></span>

### <span data-ttu-id="4b174-122">запретить</span><span class="sxs-lookup"><span data-stu-id="4b174-122">deny</span></span>

<span data-ttu-id="4b174-123">Отклоняет запрос на разрешение.</span><span class="sxs-lookup"><span data-stu-id="4b174-123">Denies the request for permission.</span></span>

#### <span data-ttu-id="4b174-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b174-124">Parameters</span></span>

<span data-ttu-id="4b174-125">У этого метода нет параметров.</span><span class="sxs-lookup"><span data-stu-id="4b174-125">This method has no parameters.</span></span>

#### <span data-ttu-id="4b174-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b174-126">Return value</span></span>

<span data-ttu-id="4b174-127">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="4b174-127">This method does not return a value.</span></span>

## <span data-ttu-id="4b174-128">Свойства</span><span class="sxs-lookup"><span data-stu-id="4b174-128">Properties</span></span>

### <span data-ttu-id="4b174-129">id</span><span class="sxs-lookup"><span data-stu-id="4b174-129">id</span></span>

<span data-ttu-id="4b174-130">Уникальный идентификатор, который можно использовать для сопоставления текущего PermissionRequest с соответствующим DeferredPermissionRequest при использовании метода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="4b174-130">A unique ID that can be used to correlate the current PermissionRequest with a corresponding DeferredPermissionRequest if the defer method is used.</span></span> <span data-ttu-id="4b174-131">Просмотрите метод "отложить".</span><span class="sxs-lookup"><span data-stu-id="4b174-131">See the defer method.</span></span>

<span data-ttu-id="4b174-132">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4b174-132">This property is read-only.</span></span>

##### <span data-ttu-id="4b174-133">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4b174-133">Property value</span></span>

<span data-ttu-id="4b174-134">Тип: **Long без знака**</span><span class="sxs-lookup"><span data-stu-id="4b174-134">Type: **Unsigned long**</span></span>

### <span data-ttu-id="4b174-135">состояни</span><span class="sxs-lookup"><span data-stu-id="4b174-135">state</span></span>

<span data-ttu-id="4b174-136">Возвращает значение "неизвестно", "отложить", "разрешить" или "запретить", чтобы показать текущее состояние запроса разрешения.</span><span class="sxs-lookup"><span data-stu-id="4b174-136">Returns "unknown", "defer", "allow", or "deny" to indicate the current state of permission request.</span></span> <span data-ttu-id="4b174-137">Строка состояния будет соответствовать тому, какой метод допускает, запрещает или задерживается (Последнее или неизвестное), если ни один из методов не был вызван.</span><span class="sxs-lookup"><span data-stu-id="4b174-137">The state string will correspond to whichever method allow, deny, or defer was called last or "unknown" if none of the methods have been called.</span></span>

<span data-ttu-id="4b174-138">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4b174-138">This property is read-only.</span></span>

#### <span data-ttu-id="4b174-139">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4b174-139">Property value</span></span>

<span data-ttu-id="4b174-140">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="4b174-140">Type: **String**</span></span>

### <span data-ttu-id="4b174-141">Тип</span><span class="sxs-lookup"><span data-stu-id="4b174-141">type</span></span>

<span data-ttu-id="4b174-142">Тип запрашиваемого разрешения.</span><span class="sxs-lookup"><span data-stu-id="4b174-142">The type of permission being requested.</span></span> <span data-ttu-id="4b174-143">Это может быть одно из следующих строковых значений:</span><span class="sxs-lookup"><span data-stu-id="4b174-143">This may be one of the following string values:</span></span>

- <span data-ttu-id="4b174-144">**географическое расположение**: доступ к данным о расположении с помощью навигатора. Географическое положение.</span><span class="sxs-lookup"><span data-stu-id="4b174-144">**geolocation**: access to location data via navigator.geolocation.</span></span>
- <span data-ttu-id="4b174-145">**unlimitedIndexedDBQuota**: позволяет IndexedDB API игнорировать обычное ограничение на размер сохраненных данных.</span><span class="sxs-lookup"><span data-stu-id="4b174-145">**unlimitedIndexedDBQuota**: allow IndexedDB APIs to ignore the usual stored data size limit.</span></span>
- <span data-ttu-id="4b174-146">**носители**: доступ к микрофону и камере с помощью навигатора. getUserMedia.</span><span class="sxs-lookup"><span data-stu-id="4b174-146">**media**: access to the microphone and camera via navigator.getUserMedia.</span></span>
- <span data-ttu-id="4b174-147">**pointerlock**: возможность блокировки и управления указателем мыши с помощью элемента. requestPointerLock.</span><span class="sxs-lookup"><span data-stu-id="4b174-147">**pointerlock**: ability to lock and control the mouse pointer via Element.requestPointerLock.</span></span>
- <span data-ttu-id="4b174-148">**уведомления**: возможность отображения уведомлений на рабочем столе через окно. Извещен.</span><span class="sxs-lookup"><span data-stu-id="4b174-148">**webnotifications**: ability to show desktop notifications via window.Notification.</span></span>
- <span data-ttu-id="4b174-149">**экран**: возможность делать снимки экрана с помощью API захвата мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="4b174-149">**screen**: ability to take screen shots via the Media Capture API.</span></span>
- <span data-ttu-id="4b174-150">**immersiveview**: возможность управления выводом на экран в VR.</span><span class="sxs-lookup"><span data-stu-id="4b174-150">**immersiveview**: ability to control a VR display.</span></span>

<span data-ttu-id="4b174-151">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4b174-151">This property is read-only.</span></span>

#### <span data-ttu-id="4b174-152">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4b174-152">Property value</span></span>

<span data-ttu-id="4b174-153">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="4b174-153">Type: **String**</span></span>

### <span data-ttu-id="4b174-154">uri</span><span class="sxs-lookup"><span data-stu-id="4b174-154">uri</span></span>

<span data-ttu-id="4b174-155">Универсальный код ресурса (URI) документа, запросившего разрешение.</span><span class="sxs-lookup"><span data-stu-id="4b174-155">The Uniform Resource Identifier (URI) of the document requesting permission.</span></span>

<span data-ttu-id="4b174-156">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4b174-156">This property is read-only.</span></span>

#### <span data-ttu-id="4b174-157">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="4b174-157">Property value</span></span>

<span data-ttu-id="4b174-158">Тип: **строка**</span><span class="sxs-lookup"><span data-stu-id="4b174-158">Type: **String**</span></span>
