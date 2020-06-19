---
description: Содержатся сведения о завершенной навигации WebView
title: Объект NavigationCompletedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: eb5727ab59dbaf056f05ab4b19450c70f85d595f
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752142"
---
# <span data-ttu-id="1bf92-104">Объект NavigationCompletedEvent</span><span class="sxs-lookup"><span data-stu-id="1bf92-104">NavigationCompletedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="1bf92-105">Объект, который представляет событие, которое создается, когда [WebView](../webview.md) закончит загрузку текущего содержимого или переход завершился сбоем.</span><span class="sxs-lookup"><span data-stu-id="1bf92-105">An object that represents an event fired when the [webview](../webview.md) has finished loading the current content or if navigation has failed.</span></span>  

## <span data-ttu-id="1bf92-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="1bf92-106">Properties</span></span>  

### <span data-ttu-id="1bf92-107">uri</span><span class="sxs-lookup"><span data-stu-id="1bf92-107">uri</span></span>  

<span data-ttu-id="1bf92-108">Универсальный код ресурса (URI) структуры навигации.</span><span class="sxs-lookup"><span data-stu-id="1bf92-108">The Uniform Resource Identifier (URI) of the navigation.</span></span>  

<span data-ttu-id="1bf92-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1bf92-109">This property is read-only.</span></span>  

```javascript
var uri = NavigationCompletedEvent.uri;
```  

#### <span data-ttu-id="1bf92-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1bf92-110">Property value</span></span>  

<span data-ttu-id="1bf92-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="1bf92-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="1bf92-112">Удачи</span><span class="sxs-lookup"><span data-stu-id="1bf92-112">isSuccess</span></span>  

<span data-ttu-id="1bf92-113">Возвращает значение, указывающее, успешно ли завершилась Навигация.</span><span class="sxs-lookup"><span data-stu-id="1bf92-113">Gets a value that indicates whether the navigation completed successfully.</span></span>  

<span data-ttu-id="1bf92-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1bf92-114">This property is read-only.</span></span>  

```javascript
var isSuccess = NavigationCompletedEvent.isSuccess;
```  

#### <span data-ttu-id="1bf92-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1bf92-115">Property value</span></span>  

<span data-ttu-id="1bf92-116">Тип: **логический**</span><span class="sxs-lookup"><span data-stu-id="1bf92-116">Type: **Boolean**</span></span>  

### <span data-ttu-id="1bf92-117">webErrorStatus</span><span class="sxs-lookup"><span data-stu-id="1bf92-117">webErrorStatus</span></span>  

<span data-ttu-id="1bf92-118">Если навигация завершилась неудачей, получает значение, указывающее, почему.</span><span class="sxs-lookup"><span data-stu-id="1bf92-118">If the navigation was unsuccessful, gets a value that indicates why.</span></span>  

<span data-ttu-id="1bf92-119">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="1bf92-119">This property is read-only.</span></span>  

```javascript
var webErrorStatus = NavigationCompletedEvent.webErrorStatus;
```  

#### <span data-ttu-id="1bf92-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1bf92-120">Property value</span></span>  

<span data-ttu-id="1bf92-121">Тип: **Long без знака**</span><span class="sxs-lookup"><span data-stu-id="1bf92-121">Type: **unsigned long**</span></span>  
