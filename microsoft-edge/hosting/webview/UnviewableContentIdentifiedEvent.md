---
description: Указывает, что WebView пытается загрузить неподдерживаемый файл.
title: Объект UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/25/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: cec85ca2d5458a05cfd88210907523f25fb4af95
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570826"
---
# <span data-ttu-id="f8693-104">Объект UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="f8693-104">UnviewableContentIdentifiedEvent object</span></span>

<span data-ttu-id="f8693-105">Указывает, что [WebView](../webview.md) пытается перейти к файлу неподдерживаемого типа контента.</span><span class="sxs-lookup"><span data-stu-id="f8693-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span> 

## <span data-ttu-id="f8693-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="f8693-106">Properties</span></span>

### <span data-ttu-id="f8693-107">Носителя</span><span class="sxs-lookup"><span data-stu-id="f8693-107">mediaType</span></span>

<span data-ttu-id="f8693-108">Возвращает тип контента для непредставленного содержимого.</span><span class="sxs-lookup"><span data-stu-id="f8693-108">Gets the content type of the unviewable content.</span></span>

<span data-ttu-id="f8693-109">Это свойство доступно только для чтения</span><span class="sxs-lookup"><span data-stu-id="f8693-109">This property is read-only</span></span>

```js
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```

#### <span data-ttu-id="f8693-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f8693-110">Property value</span></span>
<span data-ttu-id="f8693-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="f8693-111">Type: **DOMString**</span></span>

### <span data-ttu-id="f8693-112">раздел</span><span class="sxs-lookup"><span data-stu-id="f8693-112">referer</span></span>

<span data-ttu-id="f8693-113">Универсальный код ресурса (URI) страницы в [WebView](../webview.md) , запрашивающей навигацию.</span><span class="sxs-lookup"><span data-stu-id="f8693-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>

<span data-ttu-id="f8693-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f8693-114">This property is read-only.</span></span>


```js
var referer = NavigationEventWithReferrer.referer;
```

#### <span data-ttu-id="f8693-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f8693-115">Property value</span></span>
<span data-ttu-id="f8693-116">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="f8693-116">Type: **DOMString**</span></span>

### <span data-ttu-id="f8693-117">uri</span><span class="sxs-lookup"><span data-stu-id="f8693-117">uri</span></span>

<span data-ttu-id="f8693-118">Универсальный код ресурса (URI) целевого объекта навигации.</span><span class="sxs-lookup"><span data-stu-id="f8693-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>

<span data-ttu-id="f8693-119">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f8693-119">This property is read-only.</span></span>

```js
var uri = NavigationEventWithReferrer.uri;
```

#### <span data-ttu-id="f8693-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f8693-120">Property value</span></span>
<span data-ttu-id="f8693-121">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="f8693-121">Type: **DOMString**</span></span>
