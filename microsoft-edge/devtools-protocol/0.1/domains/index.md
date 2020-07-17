---
description: Список ссылок на поддерживаемые домены в Microsoft Edge DevTools Protocol версии 0,1.
title: Домены протоколов DevTools — протокол DevTools версии 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: de816e2b07838ba1b6151967ff7b8751789c60ea
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882949"
---
# <span data-ttu-id="19695-103">Домены протоколов DevTools — протокол DevTools версии 0,1 (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="19695-103">DevTools Protocol Domains - DevTools Protocol Version 0.1 (EdgeHTML)</span></span>  

## [<span data-ttu-id="19695-104">Отладчик</span><span class="sxs-lookup"><span data-stu-id="19695-104">Debugger</span></span>](debugger.md)  

<span data-ttu-id="19695-105">Домен отладчика предоставляет возможности отладки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="19695-105">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="19695-106">Он позволяет устанавливать и удалять точки останова, пошаговое выполнение, изменяя трассировку стека и т. д.</span><span class="sxs-lookup"><span data-stu-id="19695-106">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>
## [<span data-ttu-id="19695-107">Page</span><span class="sxs-lookup"><span data-stu-id="19695-107">Page</span></span>](page.md)
<span data-ttu-id="19695-108">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="19695-108">Actions and events related to the inspected page belong to the page domain.</span></span>
## [<span data-ttu-id="19695-109">Время выполнения</span><span class="sxs-lookup"><span data-stu-id="19695-109">Runtime</span></span>](runtime.md)
<span data-ttu-id="19695-110">Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="19695-110">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="19695-111">Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="19695-111">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="19695-112">Исходные объекты сохраняются в памяти, если они не были явно освобождены.</span><span class="sxs-lookup"><span data-stu-id="19695-112">Original objects are maintained in memory unless they are either explicitly released.</span></span>
## [<span data-ttu-id="19695-113">Схема</span><span class="sxs-lookup"><span data-stu-id="19695-113">Schema</span></span>](schema.md)
<span data-ttu-id="19695-114">Предоставляет сведения о схеме протоколов.</span><span class="sxs-lookup"><span data-stu-id="19695-114">Provides information about the protocol schema.</span></span>