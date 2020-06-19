---
description: Сведения о навигации по WebView
title: Объект NavigationEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 785e9646ff400e7ad229046c7030b51420b1d9ad
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752173"
---
# <span data-ttu-id="5871d-104">Объект NavigationEvent</span><span class="sxs-lookup"><span data-stu-id="5871d-104">NavigationEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="5871d-105">Объект, представляющий событие, которое создается, когда инициируется Навигация.</span><span class="sxs-lookup"><span data-stu-id="5871d-105">An object that represents an event fired when navigation is initiated.</span></span>  

## <span data-ttu-id="5871d-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="5871d-106">Properties</span></span>  

### <span data-ttu-id="5871d-107">uri</span><span class="sxs-lookup"><span data-stu-id="5871d-107">uri</span></span>  

<span data-ttu-id="5871d-108">Универсальный код ресурса (URI) целевого объекта.</span><span class="sxs-lookup"><span data-stu-id="5871d-108">The Uniform Resource Identifier (URI) of the target.</span></span>  

<span data-ttu-id="5871d-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="5871d-109">This property is read-only.</span></span>  

```javascript
var uri = NavigationEvent.uri;
```  

#### <span data-ttu-id="5871d-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="5871d-110">Property value</span></span>  

<span data-ttu-id="5871d-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="5871d-111">Type: **DOMString**</span></span>  
