---
description: Содержатся сведения об источнике ссылки для навигации
title: Объект NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 72c8a213f632e9e74145de9c34b949adf074cd22
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752130"
---
# <span data-ttu-id="8c52f-104">Объект NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="8c52f-104">NavigationEventWithReferrer object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="8c52f-105">Объект, представляющий событие, которое создается, когда инициируется Навигация, и навигация содержит ссылку.</span><span class="sxs-lookup"><span data-stu-id="8c52f-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>  

## <span data-ttu-id="8c52f-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="8c52f-106">Properties</span></span>  

### <span data-ttu-id="8c52f-107">раздел</span><span class="sxs-lookup"><span data-stu-id="8c52f-107">referer</span></span>

<span data-ttu-id="8c52f-108">Универсальный код ресурса (URI) страницы в [WebView](../webview.md) , запрашивающей навигацию.</span><span class="sxs-lookup"><span data-stu-id="8c52f-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="8c52f-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8c52f-109">This property is read-only.</span></span>  

#### <span data-ttu-id="8c52f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8c52f-110">Property value</span></span>  

<span data-ttu-id="8c52f-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="8c52f-111">Type: **DOMString**</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

### <span data-ttu-id="8c52f-112">uri</span><span class="sxs-lookup"><span data-stu-id="8c52f-112">uri</span></span>  

<span data-ttu-id="8c52f-113">Универсальный код ресурса (URI) целевого объекта навигации.</span><span class="sxs-lookup"><span data-stu-id="8c52f-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="8c52f-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="8c52f-114">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="8c52f-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="8c52f-115">Property value</span></span>  

<span data-ttu-id="8c52f-116">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="8c52f-116">Type: **DOMString**</span></span>  
