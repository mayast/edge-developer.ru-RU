---
description: Указывает, что WebView пытается загрузить неподдерживаемый файл.
title: Объект UnviewableContentIdentifiedEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 0179522f3eaf0813531084eb996ee9d392e8249d
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752015"
---
# <span data-ttu-id="ec784-104">Объект UnviewableContentIdentifiedEvent</span><span class="sxs-lookup"><span data-stu-id="ec784-104">UnviewableContentIdentifiedEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="ec784-105">Указывает, что [WebView](../webview.md) пытается перейти к файлу неподдерживаемого типа контента.</span><span class="sxs-lookup"><span data-stu-id="ec784-105">Indicates the [webview](../webview.md) is attempting to navigate to a file of an unsupported content type.</span></span>  

## <span data-ttu-id="ec784-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="ec784-106">Properties</span></span>  

### <span data-ttu-id="ec784-107">Носителя</span><span class="sxs-lookup"><span data-stu-id="ec784-107">mediaType</span></span>  

<span data-ttu-id="ec784-108">Возвращает тип контента для непредставленного содержимого.</span><span class="sxs-lookup"><span data-stu-id="ec784-108">Gets the content type of the unviewable content.</span></span>  

<span data-ttu-id="ec784-109">Это свойство доступно только для чтения</span><span class="sxs-lookup"><span data-stu-id="ec784-109">This property is read-only</span></span>  

```javascript
var mediaType = UnviewableContentIdentifiedEvent.mediaType;
```  

#### <span data-ttu-id="ec784-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ec784-110">Property value</span></span>  

<span data-ttu-id="ec784-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="ec784-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="ec784-112">раздел</span><span class="sxs-lookup"><span data-stu-id="ec784-112">referer</span></span>  

<span data-ttu-id="ec784-113">Универсальный код ресурса (URI) страницы в [WebView](../webview.md) , запрашивающей навигацию.</span><span class="sxs-lookup"><span data-stu-id="ec784-113">The Uniform Resource Identifier (URI) of the page in the [webview](../webview.md) requesting navigation.</span></span>  

<span data-ttu-id="ec784-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ec784-114">This property is read-only.</span></span>  

```javascript
var referer = NavigationEventWithReferrer.referer;
```  

#### <span data-ttu-id="ec784-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ec784-115">Property value</span></span>  

<span data-ttu-id="ec784-116">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="ec784-116">Type: **DOMString**</span></span>  

### <span data-ttu-id="ec784-117">uri</span><span class="sxs-lookup"><span data-stu-id="ec784-117">uri</span></span>  

<span data-ttu-id="ec784-118">Универсальный код ресурса (URI) целевого объекта навигации.</span><span class="sxs-lookup"><span data-stu-id="ec784-118">The Uniform Resource Identifier (URI) of the destination of the navigation.</span></span>  

<span data-ttu-id="ec784-119">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="ec784-119">This property is read-only.</span></span>  

```javascript
var uri = NavigationEventWithReferrer.uri;
```  

#### <span data-ttu-id="ec784-120">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="ec784-120">Property value</span></span>  

<span data-ttu-id="ec784-121">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="ec784-121">Type: **DOMString**</span></span>  
