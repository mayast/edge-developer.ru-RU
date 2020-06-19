---
description: Представляет процесс WebView.
title: Объект MSWebViewProcess
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: bb70b0e8eb12c7a7c23d71f01ea24e9084caa156
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752158"
---
# <span data-ttu-id="dde2a-104">Объект MSWebViewProcess</span><span class="sxs-lookup"><span data-stu-id="dde2a-104">MSWebViewProcess object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="dde2a-105">Представляет процесс [WebView](../webview.md) .</span><span class="sxs-lookup"><span data-stu-id="dde2a-105">Represents a [webview](../webview.md) process.</span></span>  

```javascript
var wvprocess = new MSWebViewProcess();
```  

## <span data-ttu-id="dde2a-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="dde2a-106">Properties</span></span>  

### <span data-ttu-id="dde2a-107">enterpriseId</span><span class="sxs-lookup"><span data-stu-id="dde2a-107">enterpriseId</span></span>  

<span data-ttu-id="dde2a-108">Корпоративный идентификатор процесса.</span><span class="sxs-lookup"><span data-stu-id="dde2a-108">The enterprise ID of the process.</span></span>  

```js
var enterpriseId = wvprocess.enterpriseId;
```  

<span data-ttu-id="dde2a-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dde2a-109">This property is read-only.</span></span>  

#### <span data-ttu-id="dde2a-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dde2a-110">Property value</span></span>  

<span data-ttu-id="dde2a-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="dde2a-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="dde2a-112">isPrivateNetworkClientServerCapabilityEnabled</span><span class="sxs-lookup"><span data-stu-id="dde2a-112">isPrivateNetworkClientServerCapabilityEnabled</span></span>  

<span data-ttu-id="dde2a-113">Возвращает значение, показывающее, разрешено ли процессу [WebView](../webview.md) в манифесте приложения *частные сети (клиент & сервер)* [объявление возможностей](/windows/uwp/packaging/app-capability-declarations) универсального приложения для Windows.</span><span class="sxs-lookup"><span data-stu-id="dde2a-113">Gets a value indicating whether the [webview](../webview.md) process has the *Private Networks (Client & Server)* Universal Windows [App capability declaration](/windows/uwp/packaging/app-capability-declarations) enabled in the app manifest.</span></span>  

```javascript
var privateNetwork = wvprocess.isPrivateNetworkClientServerCapabilityEnabled;
```  

<span data-ttu-id="dde2a-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="dde2a-114">This property is read-only.</span></span>  

#### <span data-ttu-id="dde2a-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="dde2a-115">Property value</span></span>  

<span data-ttu-id="dde2a-116">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="dde2a-116">Type: **Boolean**</span></span>  

## <span data-ttu-id="dde2a-117">Методы</span><span class="sxs-lookup"><span data-stu-id="dde2a-117">Methods</span></span>  

### <span data-ttu-id="dde2a-118">CreateWebViewAsync</span><span class="sxs-lookup"><span data-stu-id="dde2a-118">CreateWebViewAsync</span></span>  

<span data-ttu-id="dde2a-119">Создает [WebView](../webview.md) в определенном процессе.</span><span class="sxs-lookup"><span data-stu-id="dde2a-119">Creates a [webview](../webview.md) in a specific process.</span></span>  

```javascript
wvprocess.createWebviewAsync();
```  

#### <span data-ttu-id="dde2a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dde2a-120">Return value</span></span>  

<span data-ttu-id="dde2a-121">Команду**`Promise<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="dde2a-121">Type: **`Promise<MSHTMLWebViewElement>`**</span></span>  

### <span data-ttu-id="dde2a-122">GetWebViews</span><span class="sxs-lookup"><span data-stu-id="dde2a-122">GetWebViews</span></span>  

<span data-ttu-id="dde2a-123">Возвращает последовательность объектов **MSWebViewProcess** , размещенных в процессе.</span><span class="sxs-lookup"><span data-stu-id="dde2a-123">Returns a sequence of **MSWebViewProcess** objects hosted within the process.</span></span>  

#### <span data-ttu-id="dde2a-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dde2a-124">Return value</span></span>  

<span data-ttu-id="dde2a-125">Команду**`sequence<MSHTMLWebViewElement>`**</span><span class="sxs-lookup"><span data-stu-id="dde2a-125">Type: **`sequence<MSHTMLWebViewElement>`**</span></span>  

### <span data-ttu-id="dde2a-126">Разорван</span><span class="sxs-lookup"><span data-stu-id="dde2a-126">Terminate</span></span>  

<span data-ttu-id="dde2a-127">Завершает процесс.</span><span class="sxs-lookup"><span data-stu-id="dde2a-127">Terminates the process.</span></span>  

```javascript
wvprocess.terminate();
```  

#### <span data-ttu-id="dde2a-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dde2a-128">Return value</span></span>  

<span data-ttu-id="dde2a-129">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="dde2a-129">This method does not return a value.</span></span>  
