---
description: Предоставляет сведения о текущем запросе разрешения
title: Объект PermissionRequestedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/04/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 07fccebc9e061d4ee7a85e48271aaf9c0574e1ef
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572727"
---
# <span data-ttu-id="8f689-104">Объект PermissionRequestedEvent</span><span class="sxs-lookup"><span data-stu-id="8f689-104">PermissionRequestedEvent object</span></span>

<span data-ttu-id="8f689-105">Предоставляет сведения о текущем запросе разрешения.</span><span class="sxs-lookup"><span data-stu-id="8f689-105">Provides event information about the current permission request.</span></span>

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

## <span data-ttu-id="8f689-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f689-106">Properties</span></span>

### <span data-ttu-id="8f689-107">permissionRequest</span><span class="sxs-lookup"><span data-stu-id="8f689-107">permissionRequest</span></span>

<span data-ttu-id="8f689-108">Возвращает объект **[PermissionRequest](permissionrequest.md)** , который представляет запрос на разрешение конечного пользователя, сделанный содержимым [WebView](../webview.md).</span><span class="sxs-lookup"><span data-stu-id="8f689-108">Returns a **[PermissionRequest](permissionrequest.md)** object that represents the end-user permission request made by content of the [webview](../webview.md).</span></span>

<span data-ttu-id="8f689-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8f689-109">This property is read-only.</span></span>
