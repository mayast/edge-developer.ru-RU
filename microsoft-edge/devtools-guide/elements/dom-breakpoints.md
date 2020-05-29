---
description: Использование точек останова DOM для наглядной отладки макета на странице
title: DevTools — элементы точки останова для DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, элементы, точки останова DOM, изменения DOM
ms.custom: seodec18
ms.openlocfilehash: 4e9eab4727cf1c3ef74b69495dd972838985e589
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572548"
---
# <span data-ttu-id="9d2b0-104">Точки останова DOM</span><span class="sxs-lookup"><span data-stu-id="9d2b0-104">DOM breakpoints</span></span>

<span data-ttu-id="9d2b0-105">Управление контрольными точками на основе изменений DOM из этой области, в том числе отключения, удаления и повторной привязки.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-105">Manage your DOM mutation breakpoints from this pane, including disabling, deleting and rebinding them.</span></span>

<span data-ttu-id="9d2b0-106">Контрольные точки изменений DOM можно использовать для перехода в отладчик при каждом изменении выбранного узла элемента.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-106">You can use DOM mutation breakpoints to break into the debugger whenever a selected element node changes.</span></span> <span data-ttu-id="9d2b0-107">Это полезно для отслеживания кода, который несет ответственность за выявление визуальных сбоев с помощью пользовательского интерфейса, без необходимости устанавливать отдельные точки останова на каждом API 450 + DOM в *EdgeHTML* , который может инициировать такие изменения.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-107">This is helpful for tracking down the code responsible for causing visual glitches with your UI without having to set individual breakpoints on each of the 450+ DOM APIs in *EdgeHTML* that can trigger such changes.</span></span> 

<span data-ttu-id="9d2b0-108">Для настройки точки останова DOM щелкните правой кнопкой мыши любой элемент в *представлении дерева HTML* панели **элементы** , чтобы открыть контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-108">To set a DOM breakpoint, right-click on any element in the **Elements** panel *HTML tree view* to open the context menu.</span></span>

![Контекстное меню точек останова DOM](../media/elements_dom_breakpoints_contextmenu.png)

<span data-ttu-id="9d2b0-110">Вы можете настроить любую из указанных ниже точек останова.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-110">You can set any of the following breakpoints:</span></span>

 - <span data-ttu-id="9d2b0-111">**Разрыв на удаленном узле**: переход в отладчик при удалении выбранного элемента из документа (дерево DOM).</span><span class="sxs-lookup"><span data-stu-id="9d2b0-111">**Break on Node removed**: Break into the debugger when the selected element is removed from the document (DOM tree).</span></span>

 - <span data-ttu-id="9d2b0-112">**Прерывать на поддереве изменено**: разрывать в отладчике, когда все потомки выбранного элемента изменяются (добавляются, удаляются или их поддеревья изменяются).</span><span class="sxs-lookup"><span data-stu-id="9d2b0-112">**Break on Subtree modified**: Break into the debugger when any of the descendants of the selected element are changed (added, removed, or their subtrees are modified).</span></span> <span data-ttu-id="9d2b0-113">Это не будет прерываться при изменении атрибутов (это можно узнать ниже).</span><span class="sxs-lookup"><span data-stu-id="9d2b0-113">This will not break when attributes are modified (see the next option for that).</span></span>

 - <span data-ttu-id="9d2b0-114">**Прерывать на измененном атрибуте**: переход в отладчик при добавлении, удалении или изменении атрибута выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-114">**Break on Attribute modified**: Break into the debugger when an attribute of the selected element is added, removed or changed in value.</span></span>

<span data-ttu-id="9d2b0-115">В области **точки останова DOM** будет указан выбранный элемент (путем создания элемента Selector, описывающего его расположение в DOM) и указаны типы точек останова (*Удаление узла, изменение поддерева, изменение атрибута*).</span><span class="sxs-lookup"><span data-stu-id="9d2b0-115">The **DOM breakpoints** pane will then list the selected element (by generating a selector describing its location in the DOM) and the types of breakpoints you have set (*Node removed, Subtree modified, Attribute modified*).</span></span> <span data-ttu-id="9d2b0-116">Отсюда вы также можете *повторно привязать*, *Отключить*или *Удалить* точки останова (в контекстном меню "RT-щелчок") или все вместе (с помощью кнопок).</span><span class="sxs-lookup"><span data-stu-id="9d2b0-116">From here, you can also *rebind*, *disable*, or *delete* your breakpoints, individually (from the rt-click context menu) or all at once (using the buttons).</span></span>

![Область точек останова DOM](../media/elements_dom_breakpoints.png)

## <span data-ttu-id="9d2b0-118">Сохранение состояния точки останова</span><span class="sxs-lookup"><span data-stu-id="9d2b0-118">Breakpoint persistence</span></span>

<span data-ttu-id="9d2b0-119">Точки останова сохраняются (и определяются по URL-адресу страницы, в которой они находятся) в составе параметров DevTools.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-119">Breakpoints are stored (and scoped to the URL of the page they're set within) as part of your DevTools settings.</span></span> <span data-ttu-id="9d2b0-120">При повторной загрузке страницы или закрытии и повторном открытии средств DevTools пытается повторно привязать точки останова к связанным элементам.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-120">When the page is reloaded or the tools are closed and reopened, DevTools will attempt to rebind your breakpoints to their associated elements.</span></span>

<span data-ttu-id="9d2b0-121">Точки останова, которые не удалось автоматически повторно привязать, обозначается значком предупреждения в круговой точке останова.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-121">Breakpoints that couldn't be automatically rebinded are indicated with a warning icon on the breakpoint circle.</span></span> <span data-ttu-id="9d2b0-122">Для этого вы можете дождаться повторной привязки элемента вручную (с помощью кнопки **повторной привязки** и/или пункта контекстного меню) после того, как соответствующий элемент появится в DOM (и значок точки останова больше не отображается) или полностью **Удалить** точку останова.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-122">For these, you can wait to rebind the element manually (using the **Rebind breakpoint** button and/or context menu option) once a corresponding element appears in the DOM (and the breakpoint icon no longer shows the warning indicator), or **Delete** the breakpoint altogether.</span></span>

![Индикатор несвязанной точки останова](../media/elements_dom_breakpoint_unbound.png)

<span data-ttu-id="9d2b0-124">В дополнение к этой области " *точки останова DOM* " вы также можете управлять [точками останова DOM](../debugger.md#dom-breakpoints) в **отладчике**.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-124">In addition to this *DOM breakpoints* pane, you can also manage your [DOM breakpoints](../debugger.md#dom-breakpoints) from within the **Debugger**.</span></span>

## <span data-ttu-id="9d2b0-125">Текущие ограничения</span><span class="sxs-lookup"><span data-stu-id="9d2b0-125">Current limitations</span></span>

<span data-ttu-id="9d2b0-126">Обратите внимание на перечисленные ниже ограничения на отладку точки останова DOM в EDGE DevTools:</span><span class="sxs-lookup"><span data-stu-id="9d2b0-126">Please be aware of the following limitations of DOM breakpoint debugging in Edge DevTools:</span></span>

- <span data-ttu-id="9d2b0-127">Edge DevTools в настоящее время не поддерживает повторное связывание точек останова внутри [ `<iframe>` s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe).</span><span class="sxs-lookup"><span data-stu-id="9d2b0-127">Edge DevTools don't currently support rebinding breakpoints inside of [`<iframe>`s](https://developer.mozilla.org/docs/Web/HTML/Element/iframe).</span></span> <span data-ttu-id="9d2b0-128">Если вы установили точку останова в Интернет-кадре и закроете Edge DevTools или обновите страницу, точка останова будет потеряна.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-128">If you set a breakpoint in an iframe and close Edge DevTools or refresh the page, the breakpoint will be lost.</span></span>

- <span data-ttu-id="9d2b0-129">Если ваш сценарий встречает синхронно выполняемую точку останова перед [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) завершением DOM, вы не сможете установить точку останова DOM, пока отладчик не будет приостановлен.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-129">If your script encounters a synchronously-executed breakpoint before the DOM [`readyState`](https://developer.mozilla.org/docs/Web/API/Document/readyState) is completed, you won't be able to set a DOM breakpoint while the debugger is paused.</span></span> <span data-ttu-id="9d2b0-130">Вы обычно можете устранить эту ситуацию, задав [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) атрибуты или [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) атрибут сценария.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-130">You can typically remedy this situation by setting the [`defer`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) or [`async`](https://developer.mozilla.org/docs/Web/HTML/Element/script#Attributes) script attributes.</span></span>

- <span data-ttu-id="9d2b0-131">Для синхронных скриптов мы активируем функцию автоматического повторной привязки точек останова при [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) вызове события.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-131">For synchronous scripts, we trigger automatic rebinding of breakpoints when the [`window.onload`](https://developer.mozilla.org/docs/Web/API/GlobalEventHandlers/onload) event is called.</span></span> <span data-ttu-id="9d2b0-132">В этом случае мы можем пропустить точки останова, которые инициируются во время первоначальной сборки DOM, управляемой сценарием.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-132">In this case, we may miss binding breakpoints that would trigger during initial script-driven build-up of the DOM.</span></span> <span data-ttu-id="9d2b0-133">Для асинхронных скриптов мы активируем попытку повторной привязки перед выполнением первого сценария, поэтому точки останова могут быть повторно привязаны и срабатывать нужным образом.</span><span class="sxs-lookup"><span data-stu-id="9d2b0-133">For asynchronous scripts, we trigger a rebind attempt before the first script executes, so your breakpoints may rebind and trigger as desired.</span></span>
