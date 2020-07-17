---
description: Протокол Microsoft Edge DevTools версии 0,2 поддерживает следующие конечные точки HTTP.
title: Конечные точки HTTP для протокола Microsoft Edge DevTools версии 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: eb5b29e4d8149f511d8a7cbca3da72391a13e449
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882860"
---
# <span data-ttu-id="8457b-103">Конечные точки HTTP для протокола Microsoft Edge DevTools версии 0,2 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="8457b-103">Microsoft Edge DevTools Protocol Version 0.2 HTTP Endpoints (EdgeHTML)</span></span>  

> [!NOTE]
> <span data-ttu-id="8457b-104">Версия 0,2 протокола Microsoft Edge DevTools работает только на [обновлениях для Windows 10 октября 2018]() и более поздних сборок для [предварительной оценки Windows](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="8457b-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update]() and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="8457b-105">**Протокол DevTools 0,2** поддерживает следующие конечные точки HTTP.</span><span class="sxs-lookup"><span data-stu-id="8457b-105">**DevTools Protocol 0.2** supports the following HTTP endpoints.</span></span> <span data-ttu-id="8457b-106">Дополнительные сведения о том, как подключаться к процессу содержимого браузера и по [доменам](domains/index.md) для всех API-интерфейсов Devtools, можно найти в разделе [использование протокола](../index.md#using-the-protocol) .</span><span class="sxs-lookup"><span data-stu-id="8457b-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="8457b-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="8457b-107">/json/version</span></span>
<span data-ttu-id="8457b-108">Сведения о браузере хост-компьютера и версии поддерживаемого им протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="8457b-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="8457b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="8457b-109">Parameters</span></span>**

*<span data-ttu-id="8457b-110">Нет</span><span class="sxs-lookup"><span data-stu-id="8457b-110">None</span></span>*

**<span data-ttu-id="8457b-111">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="8457b-111">Return object</span></span>**

```json
{
    "Browser":"Edge/18.17763",
    "Protocol-Version":"0.2",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/18.17763"
}
```

## <span data-ttu-id="8457b-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="8457b-112">/json/protocol</span></span>

<span data-ttu-id="8457b-113">Обеспечивает весь интерфейс API протокола, сериализованный как JSON.</span><span class="sxs-lookup"><span data-stu-id="8457b-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="8457b-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="8457b-114">Parameters</span></span>**

*<span data-ttu-id="8457b-115">Нет</span><span class="sxs-lookup"><span data-stu-id="8457b-115">None</span></span>*

**<span data-ttu-id="8457b-116">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="8457b-116">Return object</span></span>**

<span data-ttu-id="8457b-117">Объект JSON, который представляет доступную поверхность API для текущей версии протокола.</span><span class="sxs-lookup"><span data-stu-id="8457b-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="8457b-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="8457b-118">/json/list</span></span>

<span data-ttu-id="8457b-119">Список кандидатов на странице для отладки.</span><span class="sxs-lookup"><span data-stu-id="8457b-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="8457b-120">Параметры</span><span class="sxs-lookup"><span data-stu-id="8457b-120">Parameters</span></span>**

*<span data-ttu-id="8457b-121">Нет</span><span class="sxs-lookup"><span data-stu-id="8457b-121">None</span></span>*

**<span data-ttu-id="8457b-122">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="8457b-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="8457b-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="8457b-123">/json/close</span></span>

<span data-ttu-id="8457b-124">Закрывает целевой процесс (например, в Microsoft EDGE, закрывает вкладку страницы.)</span><span class="sxs-lookup"><span data-stu-id="8457b-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="8457b-125">Параметры</span><span class="sxs-lookup"><span data-stu-id="8457b-125">Parameters</span></span>**

<span data-ttu-id="8457b-126">Идентификатор целевого объекта</span><span class="sxs-lookup"><span data-stu-id="8457b-126">Target ID</span></span> 

**<span data-ttu-id="8457b-127">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="8457b-127">Return object</span></span>**

```
String("Target is closing")
```
