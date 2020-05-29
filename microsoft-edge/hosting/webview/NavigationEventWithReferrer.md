---
description: Содержатся сведения об источнике ссылки для навигации
title: Объект NavigationEventWithReferrer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/22/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: b11f60724387d996d0a730965602b5ead6a84145
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571294"
---
# <span data-ttu-id="fb7cb-104">Объект NavigationEventWithReferrer</span><span class="sxs-lookup"><span data-stu-id="fb7cb-104">NavigationEventWithReferrer object</span></span>

<span data-ttu-id="fb7cb-105">Объект, представляющий событие, которое создается, когда инициируется Навигация, и навигация содержит ссылку.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-105">An object that represents an event fired when navigation is initiated and the navigation contains a referer.</span></span>

## <span data-ttu-id="fb7cb-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="fb7cb-106">Properties</span></span>

### <span data-ttu-id="fb7cb-107">раздел</span><span class="sxs-lookup"><span data-stu-id="fb7cb-107">referer</span></span>

<span data-ttu-id="fb7cb-108">Универсальный код ресурса (URI) страницы в [WebView](../webview.md) , запрашивающей навигацию.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-108">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="fb7cb-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-109">This property is read-only.</span></span>

#### <span data-ttu-id="fb7cb-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fb7cb-110">Property value</span></span>
<span data-ttu-id="fb7cb-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="fb7cb-111">Type: **DOMString**</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

### <span data-ttu-id="fb7cb-112">uri</span><span class="sxs-lookup"><span data-stu-id="fb7cb-112">uri</span></span>

<span data-ttu-id="fb7cb-113">Универсальный код ресурса (URI) целевого объекта навигации.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-113">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="fb7cb-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fb7cb-114">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="fb7cb-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="fb7cb-115">Property value</span></span>
<span data-ttu-id="fb7cb-116">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="fb7cb-116">Type: **DOMString**</span></span>
