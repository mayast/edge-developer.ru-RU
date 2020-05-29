---
description: Представляет процесс WebView.
title: Объект MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 7581f6da3a23295180c50f6d41cc282ce998b64e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571303"
---
# <span data-ttu-id="d0668-104">Объект MSWebViewProcess</span><span class="sxs-lookup"><span data-stu-id="d0668-104">MSWebViewProcess object</span></span>

<span data-ttu-id="d0668-105">Представляет процесс [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="d0668-105">Represents a [webview](../webview.md) process.</span></span>

```js
var wvprocess = new MSWebViewProcess();
```

## <span data-ttu-id="d0668-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="d0668-106">Properties</span></span>

### <span data-ttu-id="d0668-107">enterpriseId</span><span class="sxs-lookup"><span data-stu-id="d0668-107">enterpriseId</span></span>

<span data-ttu-id="d0668-108">Корпоративный идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="d0668-108">The enterprise ID of the process.</span></span>

```js
var enterpriseId = wvprocess.enterpriseId;
```

<span data-ttu-id="d0668-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d0668-109">This property is read-only.</span></span>

#### <span data-ttu-id="d0668-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d0668-110">Property value</span></span>
<span data-ttu-id="d0668-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="d0668-111">Type: **DOMString**</span></span>

### <span data-ttu-id="d0668-112">isPrivateNetworkClientServerCapabilityEnabled</span><span class="sxs-lookup"><span data-stu-id="d0668-112">isPrivateNetworkClientServerCapabilityEnabled</span></span>

<span data-ttu-id="d0668-113">Возвращает значение, показывающее, разрешено ли процессу [WebView](../webview.md) в манифесте приложения *частные сети (клиент & сервер)* [объявление возможностей](/windows/uwp/packaging/app-capability-declarations) универсального приложения для Windows.</span><span class="sxs-lookup"><span data-stu-id="d0668-113">Gets a value indicating whether the [webview](../webview.md) process has the *Private Networks (Client & Server)* Universal Windows [App capability declaration](/windows/uwp/packaging/app-capability-declarations) enabled in the app manifest.</span></span>

```js
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```

<span data-ttu-id="d0668-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d0668-114">This property is read-only.</span></span>

#### <span data-ttu-id="d0668-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d0668-115">Property value</span></span>
<span data-ttu-id="d0668-116">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="d0668-116">Type: **Boolean**</span></span>

## <span data-ttu-id="d0668-117">Методы</span><span class="sxs-lookup"><span data-stu-id="d0668-117">Methods</span></span>

### <span data-ttu-id="d0668-118">CreateWebViewAsync</span><span class="sxs-lookup"><span data-stu-id="d0668-118">CreateWebViewAsync</span></span>

<span data-ttu-id="d0668-119">Создает [WebView](../webview.md) в определенном процессе.</span><span class="sxs-lookup"><span data-stu-id="d0668-119">Creates a [webview](../webview.md) in a specific process.</span></span>

```js
wvprocess.createWebviewAsync();
```

#### <span data-ttu-id="d0668-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0668-120">Return value</span></span>

<span data-ttu-id="d0668-121">Команду**`Promise<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="d0668-121">Type: **`Promise<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="d0668-122">GetWebViews</span><span class="sxs-lookup"><span data-stu-id="d0668-122">GetWebViews</span></span>

<span data-ttu-id="d0668-123">Возвращает последовательность объектов **MSWebViewProcess** , размещенных в процессе.</span><span class="sxs-lookup"><span data-stu-id="d0668-123">Returns a sequence of **MSWebViewProcess** objects hosted within the process.</span></span>

#### <span data-ttu-id="d0668-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0668-124">Return value</span></span>

<span data-ttu-id="d0668-125">Команду**`sequence<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="d0668-125">Type: **`sequence<MSHTMLWebViewElement>`**</span></span>

### <span data-ttu-id="d0668-126">Разорван</span><span class="sxs-lookup"><span data-stu-id="d0668-126">Terminate</span></span>

<span data-ttu-id="d0668-127">Завершает процесс.</span><span class="sxs-lookup"><span data-stu-id="d0668-127">Terminates the process.</span></span>

```js
wvprocess.terminate();
```

#### <span data-ttu-id="d0668-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d0668-128">Return value</span></span>

<span data-ttu-id="d0668-129">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="d0668-129">This method does not return a value.</span></span>
