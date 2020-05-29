---
description: Протокол Microsoft Edge DevTools версии 0,1 поддерживает следующие конечные точки HTTP.
title: Конечные точки HTTP протокола DevTools версии 0,1
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 5b1cf0d347fec5bfe20b2574afcd635ee569c92d
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571684"
---
# <span data-ttu-id="5e00c-103">Конечные точки HTTP протокола DevTools</span><span class="sxs-lookup"><span data-stu-id="5e00c-103">DevTools Protocol HTTP Endpoints</span></span>

> [!NOTE]
> <span data-ttu-id="5e00c-104">Протокол Microsoft Edge DevTools работает только на [Windows 10 2018 апрельского обновления](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) и более поздних сборок для предварительной [оценки Windows](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="5e00c-104">The Microsoft Edge DevTools Protocol works only on [Windows 10 April 2018 Update](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>

<span data-ttu-id="5e00c-105">**Протокол DevTools 0,1** поддерживает следующие конечные точки HTTP.</span><span class="sxs-lookup"><span data-stu-id="5e00c-105">**DevTools Protocol 0.1** supports the following HTTP endpoints.</span></span> <span data-ttu-id="5e00c-106">Дополнительные сведения о том, как подключаться к процессу содержимого браузера и по [доменам](domains/index.md) для всех API-интерфейсов Devtools, можно найти в разделе [использование протокола](../index.md#using-the-protocol) .</span><span class="sxs-lookup"><span data-stu-id="5e00c-106">See [using the protocol](../index.md#using-the-protocol) for more on connecting to a browser content process and the [Domains](domains/index.md) documentation for the full web sockets-based devtools protocol API.</span></span>

## <span data-ttu-id="5e00c-107">/json/version</span><span class="sxs-lookup"><span data-stu-id="5e00c-107">/json/version</span></span>
<span data-ttu-id="5e00c-108">Сведения о браузере хост-компьютера и версии поддерживаемого им протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="5e00c-108">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="5e00c-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e00c-109">Parameters</span></span>**

*<span data-ttu-id="5e00c-110">Нет</span><span class="sxs-lookup"><span data-stu-id="5e00c-110">None</span></span>*

**<span data-ttu-id="5e00c-111">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="5e00c-111">Return object</span></span>**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
}
```

## <span data-ttu-id="5e00c-112">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="5e00c-112">/json/protocol</span></span>

<span data-ttu-id="5e00c-113">Обеспечивает весь интерфейс API протокола, сериализованный как JSON.</span><span class="sxs-lookup"><span data-stu-id="5e00c-113">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="5e00c-114">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e00c-114">Parameters</span></span>**

*<span data-ttu-id="5e00c-115">Нет</span><span class="sxs-lookup"><span data-stu-id="5e00c-115">None</span></span>*

**<span data-ttu-id="5e00c-116">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="5e00c-116">Return object</span></span>**

<span data-ttu-id="5e00c-117">Объект JSON, который представляет доступную поверхность API для текущей версии протокола.</span><span class="sxs-lookup"><span data-stu-id="5e00c-117">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="5e00c-118">/json/list</span><span class="sxs-lookup"><span data-stu-id="5e00c-118">/json/list</span></span>

<span data-ttu-id="5e00c-119">Список кандидатов на странице для отладки.</span><span class="sxs-lookup"><span data-stu-id="5e00c-119">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="5e00c-120">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e00c-120">Parameters</span></span>**

*<span data-ttu-id="5e00c-121">Нет</span><span class="sxs-lookup"><span data-stu-id="5e00c-121">None</span></span>*

**<span data-ttu-id="5e00c-122">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="5e00c-122">Return object</span></span>**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## <span data-ttu-id="5e00c-123">/json/close</span><span class="sxs-lookup"><span data-stu-id="5e00c-123">/json/close</span></span>

<span data-ttu-id="5e00c-124">Закрывает целевой процесс (например, в Microsoft EDGE, закрывает вкладку страницы.)</span><span class="sxs-lookup"><span data-stu-id="5e00c-124">Closes down the target process (e.g., in Microsoft Edge, closes the page tab.)</span></span>

**<span data-ttu-id="5e00c-125">Параметры</span><span class="sxs-lookup"><span data-stu-id="5e00c-125">Parameters</span></span>**

<span data-ttu-id="5e00c-126">Идентификатор целевого объекта</span><span class="sxs-lookup"><span data-stu-id="5e00c-126">Target ID</span></span> 

**<span data-ttu-id="5e00c-127">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="5e00c-127">Return object</span></span>**

```
String("Target is closing")
```
