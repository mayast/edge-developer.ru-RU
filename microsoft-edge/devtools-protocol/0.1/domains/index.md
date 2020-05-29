---
description: Список ссылок на поддерживаемые домены в Microsoft Edge DevTools Protocol версии 0,1.
title: Домены — протокол DevTools версии 0,1
author: pelavall
ms.author: pelavall
ms.date: 12/15/2017
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: b3cf3411a8402b7407012eb789f8bf267b4997a8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571688"
---
# <span data-ttu-id="a9a35-103">Домены протоколов DevTools</span><span class="sxs-lookup"><span data-stu-id="a9a35-103">DevTools Protocol Domains</span></span>
## [<span data-ttu-id="a9a35-104">Отладчика</span><span class="sxs-lookup"><span data-stu-id="a9a35-104">Debugger</span></span>](debugger.md)
<span data-ttu-id="a9a35-105">Домен отладчика предоставляет возможности отладки JavaScript.</span><span class="sxs-lookup"><span data-stu-id="a9a35-105">Debugger domain exposes JavaScript debugging capabilities.</span></span> <span data-ttu-id="a9a35-106">Он позволяет устанавливать и удалять точки останова, пошаговое выполнение, изменяя трассировку стека и т. д.</span><span class="sxs-lookup"><span data-stu-id="a9a35-106">It allows setting and removing breakpoints, stepping through execution, exploring stack traces, etc.</span></span>
## [<span data-ttu-id="a9a35-107">Page</span><span class="sxs-lookup"><span data-stu-id="a9a35-107">Page</span></span>](page.md)
<span data-ttu-id="a9a35-108">Действия и события, связанные с проверенной страницей, относятся к домену страницы.</span><span class="sxs-lookup"><span data-stu-id="a9a35-108">Actions and events related to the inspected page belong to the page domain.</span></span>
## [<span data-ttu-id="a9a35-109">Язык</span><span class="sxs-lookup"><span data-stu-id="a9a35-109">Runtime</span></span>](runtime.md)
<span data-ttu-id="a9a35-110">Домен среды выполнения предоставляет среду выполнения JavaScript с помощью удаленных и зеркальных объектов.</span><span class="sxs-lookup"><span data-stu-id="a9a35-110">Runtime domain exposes JavaScript runtime by means of remote evaluation and mirror objects.</span></span> <span data-ttu-id="a9a35-111">Результаты вычислений возвращаются как зеркальный объект, который предоставляет тип объекта, строковое представление и уникальный идентификатор, который можно использовать для дальнейшей ссылки на объект.</span><span class="sxs-lookup"><span data-stu-id="a9a35-111">Evaluation results are returned as mirror object that expose object type, string representation and unique identifier that can be used for further object reference.</span></span> <span data-ttu-id="a9a35-112">Исходные объекты сохраняются в памяти, если они не были явно освобождены.</span><span class="sxs-lookup"><span data-stu-id="a9a35-112">Original objects are maintained in memory unless they are either explicitly released.</span></span>
## [<span data-ttu-id="a9a35-113">Схема</span><span class="sxs-lookup"><span data-stu-id="a9a35-113">Schema</span></span>](schema.md)
<span data-ttu-id="a9a35-114">Предоставляет сведения о схеме протоколов.</span><span class="sxs-lookup"><span data-stu-id="a9a35-114">Provides information about the protocol schema.</span></span>