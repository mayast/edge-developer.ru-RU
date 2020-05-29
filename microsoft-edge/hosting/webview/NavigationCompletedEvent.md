---
description: Содержатся сведения о завершенной навигации WebView
title: Объект NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/26/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 11974f0c66d48569ee63c592bdd3b0153db075b1
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571300"
---
# <span data-ttu-id="92d8f-104">Объект NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="92d8f-104">NavigationCompletedEvent object</span></span>

<span data-ttu-id="92d8f-105">Объект, который представляет событие, которое создается, когда [WebView](../webview.md) закончит загрузку текущего содержимого или переход завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="92d8f-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>

## <span data-ttu-id="92d8f-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="92d8f-106">Properties</span></span>
    
### <span data-ttu-id="92d8f-107">uri</span><span class="sxs-lookup"><span data-stu-id="92d8f-107">uri</span></span>

<span data-ttu-id="92d8f-108">Универсальный код ресурса (URI) структуры навигации.</span><span class="sxs-lookup"><span data-stu-id="92d8f-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>

<span data-ttu-id="92d8f-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="92d8f-109">This property is read-only.</span></span>

```js
var uri = NavigationCompletedEvent.uri;
```

#### <span data-ttu-id="92d8f-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="92d8f-110">Property value</span></span>
<span data-ttu-id="92d8f-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="92d8f-111">Type: **DOMString**</span></span>

### <span data-ttu-id="92d8f-112">Удачи</span><span class="sxs-lookup"><span data-stu-id="92d8f-112">isSuccess</span></span>

<span data-ttu-id="92d8f-113">Возвращает значение, указывающее, успешно ли завершилась Навигация.</span><span class="sxs-lookup"><span data-stu-id="92d8f-113">Gets a value that indicates whether the navigation completed successfully.</span></span>

<span data-ttu-id="92d8f-114">Это свойство доступно только для чтения</span><span class="sxs-lookup"><span data-stu-id="92d8f-114">This property is read-only</span></span>

```js
var isSuccess = NavigationCompletedEvent.isSuccess;
```

#### <span data-ttu-id="92d8f-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="92d8f-115">Property value</span></span>
<span data-ttu-id="92d8f-116">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="92d8f-116">Type: **Boolean**</span></span>

### <span data-ttu-id="92d8f-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="92d8f-117">webErrorStatus</span></span>

<span data-ttu-id="92d8f-118">Если навигация завершилась неудачей, получает значение, указывающее, почему.</span><span class="sxs-lookup"><span data-stu-id="92d8f-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>

<span data-ttu-id="92d8f-119">Это свойство доступно только для чтения</span><span class="sxs-lookup"><span data-stu-id="92d8f-119">This property is read-only</span></span>

```js
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```

#### <span data-ttu-id="92d8f-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="92d8f-120">Property value</span></span>
<span data-ttu-id="92d8f-121">Тип: **Long без знака**</span><span class="sxs-lookup"><span data-stu-id="92d8f-121">Type: **unsigned long**</span></span>
