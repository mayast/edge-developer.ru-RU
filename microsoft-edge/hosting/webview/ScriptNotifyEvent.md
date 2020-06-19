---
description: Представляет строку уведомления, переданную из содержимого WebView в приложение.
title: Объект ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 164bfa7228b1f4ccf9817e4b7231361d090f1394
ms.sourcegitcommit: 037a2d62333691104c9accb4862968f80a3465a2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/18/2020
ms.locfileid: "10752026"
---
# <span data-ttu-id="b9ea6-104">Объект ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="b9ea6-104">ScriptNotifyEvent object</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="b9ea6-105">Объект, представляющий событие, которое создается, когда содержимое, содержащееся в [WebView](../webview.md) , передает строку приложению с помощью JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b9ea6-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>  

## <span data-ttu-id="b9ea6-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="b9ea6-106">Properties</span></span>  

### <span data-ttu-id="b9ea6-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="b9ea6-107">callingUri</span></span>  

<span data-ttu-id="b9ea6-108">Возвращает универсальный код ресурса (URI) страницы, содержащей сценарий, сгенерировавший **ScriptNotifyEvent**.</span><span class="sxs-lookup"><span data-stu-id="b9ea6-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>  

<span data-ttu-id="b9ea6-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b9ea6-109">This property is read-only.</span></span>  

```javascript
var callingUri = ScriptNotifyEvent.callingUri;
```  

#### <span data-ttu-id="b9ea6-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b9ea6-110">Property value</span></span>  

<span data-ttu-id="b9ea6-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="b9ea6-111">Type: **DOMString**</span></span>  

### <span data-ttu-id="b9ea6-112">value</span><span class="sxs-lookup"><span data-stu-id="b9ea6-112">value</span></span>  

<span data-ttu-id="b9ea6-113">Имя метода, переданное приложению.</span><span class="sxs-lookup"><span data-stu-id="b9ea6-113">The method name as passed to the application.</span></span>  

<span data-ttu-id="b9ea6-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b9ea6-114">This property is read-only.</span></span>  

```javascript
var value = ScriptNotifyEvent.value;
```  

#### <span data-ttu-id="b9ea6-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b9ea6-115">Property value</span></span>  

<span data-ttu-id="b9ea6-116">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="b9ea6-116">Type: **DOMString**</span></span>  
