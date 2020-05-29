---
description: Узнайте о новых возможностях Microsoft Edge DevTools в обновлении для Windows 10 от 2018 октября
title: Новые возможности Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, edgehtml 18
ms.custom: RS5, seodec18
ms.openlocfilehash: 604419f4c77ccaaf2dfd3179273be803cde86fc8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571708"
---
# <span data-ttu-id="6ad27-104">DevTools в новейшем обновлении для Windows 10 (EdgeHTML 18)</span><span class="sxs-lookup"><span data-stu-id="6ad27-104">DevTools in the latest Windows 10 update (EdgeHTML 18)</span></span>

<span data-ttu-id="6ad27-105">Последнее обновление Microsoft Edge DevTools позволяет получить ряд специальных возможностей в пользовательском интерфейсе и, в частности, новые специальные панели для [*рабочих процессов*](#service-workers-panel) и [*хранения*](#storage-panel), средства [поиска файлов](#source-file-search-tools) исходного кода в отладчике и новые [домены протоколов пограничного DevTools](#edge-devtools-protocol-updates) для отладки стиля и макета и API консоли.</span><span class="sxs-lookup"><span data-stu-id="6ad27-105">The latest update to Microsoft Edge DevTools adds a number of conveniences both to the UI and under the hood, including new dedicated panels for [*Service Workers*](#service-workers-panel) and [*Storage*](#storage-panel), source [file search](#source-file-search-tools) tools in the Debugger, and new [Edge DevTools Protocol domains](#edge-devtools-protocol-updates) for style/layout debugging and console APIs.</span></span>

<span data-ttu-id="6ad27-106">Ниже приведены последние компоненты Microsoft Edge DevTools, доступные в обновлении для [Windows 10 от 2018 октября](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span><span class="sxs-lookup"><span data-stu-id="6ad27-106">Here are the latest Microsoft Edge DevTools features available now in the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)).</span></span> <span data-ttu-id="6ad27-107">Кроме того, мы также исправлены некоторые ошибки, связанные со специальными возможностями, надежностью и производительностью, для улучшения основ!</span><span class="sxs-lookup"><span data-stu-id="6ad27-107">In addition to all this, we’ve also fixed a number of accessibility, reliability, and performance bugs to improve fundamentals!</span></span>

## <span data-ttu-id="6ad27-108">Приложение DevTools</span><span class="sxs-lookup"><span data-stu-id="6ad27-108">DevTools app</span></span>

<span data-ttu-id="6ad27-109">Мы обновили отдельное [приложение Microsoft Edge DevTools Preview](../devtools-guide.md#microsoft-store-app).</span><span class="sxs-lookup"><span data-stu-id="6ad27-109">We've updated the standalone [Microsoft Edge DevTools Preview app](../devtools-guide.md#microsoft-store-app).</span></span> <span data-ttu-id="6ad27-110">Последний выпуск включает в себя доступ для удаленной отладки к основным funtionality в [**отладчике**](./debugger.md), [**элементах**](./elements.md) (для операций только для чтения) и на панелях [**консоли**](./console.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad27-110">The latest release includes remote debugging access to core funtionality in the [**Debugger**](./debugger.md), [**Elements**](./elements.md) (for read-only operations), and [**Console**](./console.md) panels.</span></span>

## <span data-ttu-id="6ad27-111">Панель "работники обслуживания"</span><span class="sxs-lookup"><span data-stu-id="6ad27-111">Service Workers panel</span></span>

<span data-ttu-id="6ad27-112">Теперь на экране выделена область [**сотрудников службы**](./service-workers.md) для проверки, управления и отладки рабочих процессов сайта.</span><span class="sxs-lookup"><span data-stu-id="6ad27-112">There's now a dedicated [**Service Workers**](./service-workers.md) panel for inspecting, managing, and debugging your site's service workers.</span></span> <span data-ttu-id="6ad27-113">Это обеспечивает те же функциональные возможности, что и ранее в панели *отладчика* (теперь с меньшим пределами пользовательского интерфейса!).</span><span class="sxs-lookup"><span data-stu-id="6ad27-113">This provides the same functionality as was previously in the *Debugger* panel (now with a less-crowded UI!).</span></span>

![Панель "работники обслуживания"](./media/service_worker.png)

## <span data-ttu-id="6ad27-115">Панель "хранилище"</span><span class="sxs-lookup"><span data-stu-id="6ad27-115">Storage panel</span></span>

<span data-ttu-id="6ad27-116">Мы также переместили все локальные инспекторы хранилища (*локальные и Sesion хранилище, IndexedDB, cookie-файлы*), которые ранее находятся в *отладчике* , на собственную выделенную панель [**хранилища**](./storage.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad27-116">We've also moved all the local storage inspectors (*Local and Sesion Storage, IndexedDB, Cookies, Cache*) previously in the *Debugger* to their own dedicated [**Storage**](./storage.md) panel.</span></span>

![Панель "хранилище"](./media/storage_cache.png)

## <span data-ttu-id="6ad27-118">Средства поиска файлов исходного кода</span><span class="sxs-lookup"><span data-stu-id="6ad27-118">Source file search tools</span></span>

<span data-ttu-id="6ad27-119">В [**отладчике**](./debugger.md) теперь есть область [поиска файлов исходного кода](./debugger.md#file-search) .</span><span class="sxs-lookup"><span data-stu-id="6ad27-119">The [**Debugger**](./debugger.md) now has a [source file search](./debugger.md#file-search) pane.</span></span> <span data-ttu-id="6ad27-120">Откройте файл с помощью команды *найти в файлах* ( `Ctrl` + `Shift` + `F` ), если вы пытаетесь найти в исходном коде определенную строку.</span><span class="sxs-lookup"><span data-stu-id="6ad27-120">Open it with the *Find in files* command (`Ctrl`+`Shift`+`F`) when you have a specific string of code you're trying to find in the source.</span></span> <span data-ttu-id="6ad27-121">На панели инструментов находятся различные параметры поиска, в том числе регулярные выражения.</span><span class="sxs-lookup"><span data-stu-id="6ad27-121">The toolbar provides different search options, including regular expressions.</span></span> 

![Поиск файлов отладчика](./media/debugger_file_search.png)

<span data-ttu-id="6ad27-123">Кроме того, вы можете быстро открыть любой загруженный исходный файл с помощью команды *Открыть файл* ( `Ctrl` + `P` ).</span><span class="sxs-lookup"><span data-stu-id="6ad27-123">You can also quickly open any loaded source file with the *Open file* (`Ctrl`+`P`) command.</span></span>

![Открытие файла отладчика](./media/debugger_open_file.png)

## <span data-ttu-id="6ad27-125">Обновления протокола DevTools Edge</span><span class="sxs-lookup"><span data-stu-id="6ad27-125">Edge DevTools Protocol updates</span></span>

<span data-ttu-id="6ad27-126">[Версия 0,2](../devtools-protocol/0.2/index.md) протокола DevTools предоставляет новые домены для работы со стилями и разметкой (только для чтения) и консольными API в дополнение к основным функциям отладки скриптов, представленным в [версии 0,1](../devtools-protocol/0.1/index.md).</span><span class="sxs-lookup"><span data-stu-id="6ad27-126">[Version 0.2](../devtools-protocol/0.2/index.md) of the DevTools Protocol provides new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in [Version 0.1](../devtools-protocol/0.1/index.md).</span></span> <span data-ttu-id="6ad27-127">В пользовательском интерфейсе Edge DevTools это преобразуется в функции, доступные в [**элементах**](../devtools-guide/elements.md) (для операций только на чтение), [**консоли**](../devtools-guide/console.md) и панели [**отладчика**](../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="6ad27-127">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../devtools-guide/elements.md) (for read-only operations), [**Console**](../devtools-guide/console.md) and [**Debugger**](../devtools-guide/debugger.md) panels.</span></span>
