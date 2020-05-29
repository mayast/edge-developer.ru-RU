---
description: Представляет строку уведомления, переданную из содержимого WebView в приложение.
title: Объект ScriptNotifyEvent
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/12/2018
ms.topic: reference
ms.prod: microsoft-edge
keywords: WebView, приложения для Windows 10, UWP, EDGE
ms.openlocfilehash: 22313f2d96ca2c5d4d3554ca40589b9a583c89cd
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570827"
---
# <span data-ttu-id="d7c28-104">Объект ScriptNotifyEvent</span><span class="sxs-lookup"><span data-stu-id="d7c28-104">ScriptNotifyEvent object</span></span>

<span data-ttu-id="d7c28-105">Объект, представляющий событие, которое создается, когда содержимое, содержащееся в [WebView](../webview.md) , передает строку приложению с помощью JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d7c28-105">An object that represents an event fired when content contained in the [webview](../webview.md) passes a string to the application by using JavaScript.</span></span>

## <span data-ttu-id="d7c28-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="d7c28-106">Properties</span></span>
    
### <span data-ttu-id="d7c28-107">callingUri</span><span class="sxs-lookup"><span data-stu-id="d7c28-107">callingUri</span></span>

<span data-ttu-id="d7c28-108">Возвращает универсальный код ресурса (URI) страницы, содержащей сценарий, сгенерировавший **ScriptNotifyEvent**.</span><span class="sxs-lookup"><span data-stu-id="d7c28-108">Gets the Uniform Resource Identifier (URI) of the page containing the script that raised the **ScriptNotifyEvent**.</span></span>

<span data-ttu-id="d7c28-109">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d7c28-109">This property is read-only.</span></span>

```js
var callingUri = ScriptNotifyEvent.callingUri;
```

#### <span data-ttu-id="d7c28-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d7c28-110">Property value</span></span>
<span data-ttu-id="d7c28-111">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="d7c28-111">Type: **DOMString**</span></span>

### <span data-ttu-id="d7c28-112">value</span><span class="sxs-lookup"><span data-stu-id="d7c28-112">value</span></span>

<span data-ttu-id="d7c28-113">Имя метода, переданное приложению.</span><span class="sxs-lookup"><span data-stu-id="d7c28-113">The method name as passed to the application.</span></span>

<span data-ttu-id="d7c28-114">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="d7c28-114">This property is read-only.</span></span>

```js
var value = ScriptNotifyEvent.value;
```

#### <span data-ttu-id="d7c28-115">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d7c28-115">Property value</span></span>
<span data-ttu-id="d7c28-116">Type (тип): **DOMString**</span><span class="sxs-lookup"><span data-stu-id="d7c28-116">Type: **DOMString**</span></span>