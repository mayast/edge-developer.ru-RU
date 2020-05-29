---
title: Устранение проблем с памятью
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 738ef5fe682633f3100345c922ff12c3c27a7166
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611764"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# <span data-ttu-id="fd3d0-103">Устранение проблем с памятью</span><span class="sxs-lookup"><span data-stu-id="fd3d0-103">Fix Memory Problems</span></span>   



<span data-ttu-id="fd3d0-104">Узнайте, как использовать Microsoft EDGE и DevTools для обнаружения проблем с памятью, в том числе утечек памяти, чрезмерного объема памяти и частых сборок мусора.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-104">Learn how to use Microsoft Edge and DevTools to find memory issues that affect page performance, including memory leaks, memory bloat, and frequent garbage collections.</span></span>  

### <span data-ttu-id="fd3d0-105">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fd3d0-105">Summary</span></span>  

*   <span data-ttu-id="fd3d0-106">Сведения о том, сколько памяти использует ваша страница в диспетчере задач браузера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-106">Find out how much memory your page is currently using with the Microsoft Edge Browser Task Manager.</span></span>  
*   <span data-ttu-id="fd3d0-107">Визуализировать использование памяти по времени с помощью панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="fd3d0-107">Visualize memory usage over time with the **Memory** panel.</span></span>  
*   <span data-ttu-id="fd3d0-108">Определите отсоединенные деревья DOM \ (распространенная причина утечек памяти \) с помощью **моментального снимка кучи**.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-108">Identify detached DOM trees \(a common cause of memory leaks\) with **Heap snapshot**.</span></span>  
*   <span data-ttu-id="fd3d0-109">Узнайте о том, когда новая память выделяется в куче JavaScript \ (JS-приложение \) с **инструментированием выделения на временной шкале**.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-109">Find out when new memory is being allocated in your JavaScript heap \(JS heap\) with **Allocation instrumentation on timeline**.</span></span>  

## <span data-ttu-id="fd3d0-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="fd3d0-110">Overview</span></span>  

<span data-ttu-id="fd3d0-111">В качестве духу модели производительности **салазок** необходимо сосредоточиться на эффективности работы пользователей.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-111">In the spirit of the **RAIL** performance model, the focus of your performance efforts should be your users.</span></span>  

<!--todo: add RAIL section when available  -->  

<span data-ttu-id="fd3d0-112">Проблемы с памятью важны, так как они часто perceivable пользователями.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-112">Memory issues are important because they are often perceivable by users.</span></span>  <span data-ttu-id="fd3d0-113">Пользователи могут воспринимать проблемы с памятью следующими способами:</span><span class="sxs-lookup"><span data-stu-id="fd3d0-113">Users may perceive memory issues in the following ways:</span></span>  

*   <span data-ttu-id="fd3d0-114">**Производительность страницы постепенно восстановится с течением времени**.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-114">**The performance of a page gets progressively worse over time**.</span></span>  <span data-ttu-id="fd3d0-115">Это может быть симптомом утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-115">This is possibly a symptom of a memory leak.</span></span>  <span data-ttu-id="fd3d0-116">Утечка памяти возникает, когда ошибка на странице вызывает последовательное использование страницы больше и больше памяти с течением времени.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-116">A memory leak is when a bug in the page causes the page to progressively use more and more memory over time.</span></span>  
*   <span data-ttu-id="fd3d0-117">**Производительность страницы постоянно неисправна**.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-117">**The performance of a page is consistently bad**.</span></span>  <span data-ttu-id="fd3d0-118">Это может быть симптомом чрезмерного объема памяти.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-118">This is possibly a symptom of memory bloat.</span></span>  <span data-ttu-id="fd3d0-119">Память забывает в том случае, если на странице используется больше памяти, чем требуется для оптимальной скорости страницы.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-119">Memory bloat is when a page uses more memory than is necessary for optimal page speed.</span></span>  
*   <span data-ttu-id="fd3d0-120">**Производительность страницы часто задерживается или приостанавливается**.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-120">**The performance of a page is delayed or appears to pause frequently**.</span></span>  <span data-ttu-id="fd3d0-121">Это может быть симптомом частых сборок мусора.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-121">This is possibly a symptom of frequent garbage collections.</span></span>  <span data-ttu-id="fd3d0-122">Сборка мусора происходит, когда браузер освобождает память.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-122">Garbage collection is when the browser reclaims memory.</span></span>  <span data-ttu-id="fd3d0-123">Браузер определяет, когда это происходит.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-123">The browser decides when this happens.</span></span>  <span data-ttu-id="fd3d0-124">Во время коллекций все выполняемые сценарии приостановлены.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-124">During collections, all script running is paused.</span></span>  <span data-ttu-id="fd3d0-125">Таким образом, если браузер собирают большое количество мусора, среда выполнения сценариев будет приостанавливаться на очень много времени.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-125">So if the browser is garbage collecting a lot, script runtime is going to get paused a lot.</span></span>  

### <span data-ttu-id="fd3d0-126">Чрезмерное использование памяти: насколько это "слишком много"?</span><span class="sxs-lookup"><span data-stu-id="fd3d0-126">Memory bloat: how much is "too much"?</span></span>  

<span data-ttu-id="fd3d0-127">Определение утечек памяти очень просто.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-127">A memory leak is easy to define.</span></span>  <span data-ttu-id="fd3d0-128">Если на сайте используется больше и больше памяти, это значит, что у вас есть утечка.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-128">If a site is progressively using more and more memory, then you have a leak.</span></span>  <span data-ttu-id="fd3d0-129">Но закрепление памяти немного сложнее.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-129">But memory bloat is a bit harder to pin down.</span></span>  <span data-ttu-id="fd3d0-130">Что такое "использование слишком большого объема памяти"?</span><span class="sxs-lookup"><span data-stu-id="fd3d0-130">What qualifies as "using too much memory"?</span></span>  

<span data-ttu-id="fd3d0-131">Здесь нет жестких номеров, так как различные устройства и браузеры имеют различные возможности.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-131">There are no hard numbers here, because different devices and browsers have different capabilities.</span></span>  <span data-ttu-id="fd3d0-132">Одна и та же страница, работающая на высококачественном смартфоне, может аварийно завершить работу на смартфоне.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-132">The same page that runs smoothly on a high-end smartphone may crash on a low-end smartphone.</span></span>  

<span data-ttu-id="fd3d0-133">Основной способ — использовать модель САЛАЗОК и сосредоточиться на ваших пользователях.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-133">The key here is to use the RAIL model and focus on your users.</span></span>  <span data-ttu-id="fd3d0-134">Узнайте, какие устройства будут популярными для ваших пользователей, а затем протестируйте свою страницу на этих устройствах.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-134">Find out what devices are popular with your users, and then test out your page on those devices.</span></span>  <span data-ttu-id="fd3d0-135">Если вы постоянно восстановитсяе, страница может превысить возможности памяти для этих устройств.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-135">If the experience is consistently bad, the page may be exceeding the memory capabilities of those devices.</span></span>  

## <span data-ttu-id="fd3d0-136">Наблюдение за использованием памяти в режиме реального времени с помощью диспетчера задач браузера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fd3d0-136">Monitor memory use in realtime with the Microsoft Edge Browser Task Manager</span></span>  

<span data-ttu-id="fd3d0-137">Используйте диспетчер задач браузера Microsoft EDGE в качестве отправной точки для исследования проблем с памятью.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-137">Use the Microsoft Edge Browser Task Manager as a starting point to your memory issue investigation.</span></span>  <span data-ttu-id="fd3d0-138">Диспетчер задач браузера Microsoft Edge — это монитор реального времени, в котором сообщается, сколько памяти использует страница в данный момент.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-138">The Microsoft Edge Browser Task Manager is a realtime monitor that tells you how much memory a page is currently using.</span></span>  

1.  <span data-ttu-id="fd3d0-139">Нажмите `Shift` + `Esc` или перейдите в главное меню Microsoft EDGE и выберите пункт **другие инструменты**  >  **Диспетчер задач браузера** , чтобы открыть диспетчер задач браузера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-139">Press `Shift`+`Esc` or go to the Microsoft Edge main menu and select **More tools** > **Browser Task Manager** to open the Microsoft Edge Browser Task Manager.</span></span>  
    
    > ##### <span data-ttu-id="fd3d0-140">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="fd3d0-140">Figure 1</span></span>  
    > <span data-ttu-id="fd3d0-141">Открытие диспетчера задач браузера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="fd3d0-141">Opening the Microsoft Edge Browser Task Manager</span></span>  
    > ![Открытие диспетчера задач браузера Microsoft Edge][ImageTaskManager]  
    
1.  <span data-ttu-id="fd3d0-143">Щелкните правой кнопкой мыши заголовок таблицы в диспетчере задач браузера Microsoft EDGE и включите **память JavaScript**.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-143">Right-click on the table header of the Microsoft Edge Browser Task Manager and enable **JavaScript memory**.</span></span>  
    
    > ##### <span data-ttu-id="fd3d0-144">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="fd3d0-144">Figure 2</span></span>  
    > <span data-ttu-id="fd3d0-145">Включите память JavaScript</span><span class="sxs-lookup"><span data-stu-id="fd3d0-145">Enable JavaScript memory</span></span>  
    > ![Включите память JavaScript][ImageJavascriptMemory]  
    
<span data-ttu-id="fd3d0-147">В этих двух столбцах указываются различные способы использования памяти на странице.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-147">These two columns tell you different things about how your page is using memory:</span></span>  

*   <span data-ttu-id="fd3d0-148">Столбец **Memory** представляет встроенную память.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-148">The **Memory** column represents native memory.</span></span>  <span data-ttu-id="fd3d0-149">Узлы DOM хранятся в собственной памяти.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-149">DOM nodes are stored in native memory.</span></span>  <span data-ttu-id="fd3d0-150">Если это значение возрастает, узлы DOM создаются.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-150">If this value is increasing, DOM nodes are getting created.</span></span>  
*   <span data-ttu-id="fd3d0-151">Столбец " **память" JavaScript** представляет кучу JS.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-151">The **JavaScript Memory** column represents the JS heap.</span></span>  <span data-ttu-id="fd3d0-152">Этот столбец состоит из двух значений.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-152">This column contains two values.</span></span>  <span data-ttu-id="fd3d0-153">Интересующее вас значение — номер Live (число в круглых скобках).</span><span class="sxs-lookup"><span data-stu-id="fd3d0-153">The value you are interested in is the live number \(the number in parentheses\).</span></span>  <span data-ttu-id="fd3d0-154">Номер "в сети" показывает, сколько памяти используется достижимыми объектами на странице.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-154">The live number represents how much memory the reachable objects on your page are using.</span></span>  <span data-ttu-id="fd3d0-155">Если это число будет увеличиваться, создаются либо новые объекты, либо все существующие объекты.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-155">If this number is increasing, either new objects are being created, or the existing objects are growing.</span></span>  

<!--*   live number reference: https://groups.google.com/d/msg/google-chrome-developer-tools/aTMVGoNM0VY/bLmf3l2CpJ8J  -->  

## <span data-ttu-id="fd3d0-156">Визуализация утечек памяти с помощью панели "производительность"</span><span class="sxs-lookup"><span data-stu-id="fd3d0-156">Visualize memory leaks with Performance panel</span></span>  

<span data-ttu-id="fd3d0-157">Кроме того, вы можете использовать панель производительности как другую отправную точку расследования.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-157">You may also use the Performance panel as another starting point in your investigation.</span></span>  <span data-ttu-id="fd3d0-158">С помощью панели Performance можно визуализировать использование памяти страницы с течением времени.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-158">The Performance panel helps you visualize the memory use of a page over time.</span></span>  

1.  <span data-ttu-id="fd3d0-159">Откройте панель " **производительность** " на DevTools.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-159">Open the **Performance** panel on DevTools.</span></span>  
1.  <span data-ttu-id="fd3d0-160">Включите флажок " **память** ".</span><span class="sxs-lookup"><span data-stu-id="fd3d0-160">Enable the **Memory** checkbox.</span></span>  
1.  <span data-ttu-id="fd3d0-161">[Создание записи][DevtoolsEvaluatePerformanceReferenceRecord].</span><span class="sxs-lookup"><span data-stu-id="fd3d0-161">[Make a recording][DevtoolsEvaluatePerformanceReferenceRecord].</span></span>  

> [!TIP]
> <span data-ttu-id="fd3d0-162">Рекомендуется запускать и завершать запись с помощью принудительной сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-162">It is a good practice to start and end your recording with a forced garbage collection.</span></span>  <span data-ttu-id="fd3d0-163">Нажмите кнопку **собирать** мусорную сборку ![ мусора ][ImageForceGarbageCollectionIcon] при записи для принудительного сбора мусора.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-163">Click the **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button while recording to force garbage collection.</span></span>  

<span data-ttu-id="fd3d0-164">Чтобы продемонстрировать записи в памяти, Взгляните на приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-164">To demonstrate memory recordings, consider the code below:</span></span>  

```javascript
var x = [];
function grow() {
    for (var i = 0; i < 10000; i++) {
        document.body.appendChild(document.createElement('div'));
    }
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="fd3d0-165">Каждый раз, когда была нажата кнопка, на которую ссылается код, 10000 `div` узлы добавляются в тело документа, а в `x` массив помещается строка из 1 000 000 символов `x` .</span><span class="sxs-lookup"><span data-stu-id="fd3d0-165">Every time that the button referenced in the code is pressed, ten thousand `div` nodes are appended to the document body, and a string of one million `x` characters is pushed onto the `x` array.</span></span>  <span data-ttu-id="fd3d0-166">Выполнение этого кода приводит к записи на панели **производительности** , например [на рис. 3](#figure-3).</span><span class="sxs-lookup"><span data-stu-id="fd3d0-166">Running this code produces a recording in the **Performance** panel like [Figure 3](#figure-3).</span></span>  

> ##### <span data-ttu-id="fd3d0-167">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="fd3d0-167">Figure 3</span></span>  
> <span data-ttu-id="fd3d0-168">Простой рост</span><span class="sxs-lookup"><span data-stu-id="fd3d0-168">Simple growth</span></span>  
> ![Простой рост][ImageSimpleGrowth]  

<span data-ttu-id="fd3d0-170">Прежде всего, объясните пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-170">First, an explanation of the user interface.</span></span>  <span data-ttu-id="fd3d0-171">Граф **кучи** в области **обзора** \ (ниже **net**\) представляет кучу JS.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-171">The **HEAP** graph in the **Overview** pane \(below **NET**\) represents the JS heap.</span></span>  <span data-ttu-id="fd3d0-172">Под областью **обзора** находится панель **счетчиков** .</span><span class="sxs-lookup"><span data-stu-id="fd3d0-172">Below the **Overview** pane is the **Counter** pane.</span></span>  <span data-ttu-id="fd3d0-173">Здесь вы можете видеть использование памяти, разбитое на "JS-файлы" \ (то же, что и граф **кучи** в области **обзора** \), документы, узлы DOM, прослушиватели и память GPU.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-173">Here you are able to see memory usage broken down by JS heap \(same as **HEAP** graph in the **Overview** pane\), documents, DOM nodes, listeners, and GPU memory.</span></span>  <span data-ttu-id="fd3d0-174">Отключение CheckBox скрывает его на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-174">Disabling a checkbox hides it from the graph.</span></span>  

<span data-ttu-id="fd3d0-175">Теперь анализ кода по сравнению с [рисунком 3](#figure-3).</span><span class="sxs-lookup"><span data-stu-id="fd3d0-175">Now, an analysis of the code compared with [Figure 3](#figure-3).</span></span>  <span data-ttu-id="fd3d0-176">Если посмотреть на счетчик Nodes \ (зеленая диаграмма \), вы сможете убедиться, что он правильно соответствует коду.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-176">If you look at the node counter \(the green graph\) you are able to see that it matches up cleanly with the code.</span></span>  <span data-ttu-id="fd3d0-177">Количество узлов увеличивается на отдельных этапах.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-177">The node count increases in discrete steps.</span></span>  <span data-ttu-id="fd3d0-178">Возможно, вы предполагаете, что каждый рост количества узлов является вызовом `grow()` .</span><span class="sxs-lookup"><span data-stu-id="fd3d0-178">You may presume that each increase in the node count is a call to `grow()`.</span></span>  <span data-ttu-id="fd3d0-179">Диаграмма кучи JS \ (синяя диаграмма \) не так проста.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-179">The JS heap graph \(the blue graph\) is not as straightforward.</span></span>  <span data-ttu-id="fd3d0-180">В соответствии с лучшими рекомендациями, первый DIP — это принудительная сборка мусора (достигается нажатием **collect garbage** ![ кнопки "собрать мусор" для сборки мусора ][ImageForceGarbageCollectionIcon] ).</span><span class="sxs-lookup"><span data-stu-id="fd3d0-180">In keeping with best practices, the first dip is actually a forced garbage collection \(achieved by pressing the  **collect garbage** ![force garbage collection][ImageForceGarbageCollectionIcon] button\).</span></span>  <span data-ttu-id="fd3d0-181">По мере выполнения записи вы можете видеть, что пики размера кучи JS.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-181">As the recording progresses you are able to see that the JS heap size spikes.</span></span>  <span data-ttu-id="fd3d0-182">Это является естественным и ожидаемым: код JavaScript создает узлы DOM при каждом нажатии кнопки и выполняет большое количество действий при создании строки из 1 000 000 знаков.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-182">This is natural and expected:  the JavaScript code is creating the DOM nodes on every button click and doing a lot of work when it creates the string of one million characters.</span></span>  <span data-ttu-id="fd3d0-183">Ключевое описание — тот факт, что куча JS завершается быстрее, чем начало, ("начало" — это точка после принудительной сборки мусора).</span><span class="sxs-lookup"><span data-stu-id="fd3d0-183">The key thing here is the fact that the JS heap ends higher than it began \(the "beginning" here being the point after the forced garbage collection\).</span></span>  <span data-ttu-id="fd3d0-184">В реальном мире, если вы увидели этот шаблон размера кучи JS или размера узла, возможно, он может определять утечку памяти.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-184">In the real world, if you saw this pattern of increasing JS heap size or node size, it may potentially define a memory leak.</span></span>  

<!--todo: the Heap snapshots and Profiles panel are not found in Edge  -->  

## <span data-ttu-id="fd3d0-185">Обнаружение утечек памяти отключенного дерева DOM с помощью снимков кучи</span><span class="sxs-lookup"><span data-stu-id="fd3d0-185">Discover detached DOM tree memory leaks with Heap Snapshots</span></span>  

<span data-ttu-id="fd3d0-186">Узел DOM обстается сборщиком мусора только в том случае, если на странице нет ссылок на узел либо из дерева DOM, либо из кода JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-186">A DOM node is only garbage collected when there are no references to the node from either the DOM tree or JavaScript code running on the page.</span></span>  <span data-ttu-id="fd3d0-187">Узел считается отсоединенным, когда он удаляется из дерева DOM, но некоторые сценарии JavaScript по-прежнему ссылаются на него.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-187">A node is said to be "detached" when it is removed from the DOM tree but some JavaScript still references it.</span></span>  <span data-ttu-id="fd3d0-188">Отсоединенные узлы DOM являются распространенной причиной утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-188">Detached DOM nodes are a common cause of memory leaks.</span></span>  <span data-ttu-id="fd3d0-189">В этом разделе рассказывается о том, как использовать профилировщики кучи в DevTools для определения отделенных узлов.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-189">This section teaches you how to use the heap profilers in DevTools to identify detached nodes.</span></span>  

<span data-ttu-id="fd3d0-190">Вот простой пример отсоединенных узлов DOM.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-190">Here is a simple example of detached DOM nodes.</span></span>  

```javascript
var detachedNodes;
function create() {
    var ul = document.createElement('ul');
    for (var i = 0; i < 10; i++) {
        var li = document.createElement('li');
        ul.appendChild(li);
    }
    detachedNodes = ul;
}
document.getElementById('create').addEventListener('click', create);
```  

<span data-ttu-id="fd3d0-191">При нажатии на кнопку, на которую ссылается код, создается `ul` узел с десятью `li` потомками.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-191">Clicking the button referenced in the code creates a `ul` node with ten `li` children.</span></span>  <span data-ttu-id="fd3d0-192">На эти узлы ссылается код, но они не существуют в дереве DOM, поэтому каждый из них отсоединен.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-192">These nodes are referenced by the code but do not exist in the DOM tree, so each is detached.</span></span>  

<span data-ttu-id="fd3d0-193">Моментальные снимки кучи — это один из способов идентифицировать отсоединенные узлы.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-193">Heap snapshots are one way to identify detached nodes.</span></span>  <span data-ttu-id="fd3d0-194">Как показано в названии, в снимках кучи показано, как распределяются память между объектами JS и сайтами DOM на странице в момент создания снимка.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-194">As the name implies, heap snapshots show you how memory is distributed among the JS objects and DOM nodes for your page at the point of time of the snapshot.</span></span>  

<span data-ttu-id="fd3d0-195">Чтобы создать снимок, откройте DevTools и перейдите на панель **память** , установите переключатель в положение " **снимок кучи** ", а затем нажмите кнопку " **сделать снимок** ".</span><span class="sxs-lookup"><span data-stu-id="fd3d0-195">To create a snapshot, open DevTools and go to the **Memory** panel, select the **Heap snapshot** radio button, and then press the **Take snapshot** button.</span></span>  

> ##### <span data-ttu-id="fd3d0-196">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="fd3d0-196">Figure 4</span></span>  
> <span data-ttu-id="fd3d0-197">Создание снимка кучи</span><span class="sxs-lookup"><span data-stu-id="fd3d0-197">Take heap snapshot</span></span>  
> ![Создание снимка кучи][ImageTakeHeapSnapshot]  

<span data-ttu-id="fd3d0-199">Для обработки и загрузки снимков может потребоваться некоторое время.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-199">The snapshot may take some time to process and load.</span></span>  <span data-ttu-id="fd3d0-200">После завершения работы выберите ее в левой панели \ (снимки с именами из **кучи**).</span><span class="sxs-lookup"><span data-stu-id="fd3d0-200">After it is finished, select it from the left-hand panel \(named **HEAP SNAPSHOTS**\).</span></span>  

<span data-ttu-id="fd3d0-201">Введите текст `Detached` в поле " **Фильтр класса** " для поиска отсоединенных деревьев DOM.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-201">Type `Detached` in the **Class filter** textbox to search for detached DOM trees.</span></span>  

> ##### <span data-ttu-id="fd3d0-202">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="fd3d0-202">Figure 5</span></span>  
> <span data-ttu-id="fd3d0-203">Фильтрация для отсоединенных узлов</span><span class="sxs-lookup"><span data-stu-id="fd3d0-203">Filtering for detached nodes</span></span>  
> ![Фильтрация для отсоединенных узлов][ImageFilteringForDetachedNodes]  

<span data-ttu-id="fd3d0-205">Разверните CARATS, чтобы разобраться в отсоединенном дереве.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-205">Expand the carats to investigate a detached tree.</span></span>  

> ##### <span data-ttu-id="fd3d0-206">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="fd3d0-206">Figure 6</span></span>  
> <span data-ttu-id="fd3d0-207">Исследование отключенного дерева</span><span class="sxs-lookup"><span data-stu-id="fd3d0-207">Investigating detached tree</span></span>  
> ![Исследование отключенного дерева][ImageInvestigatingDetachedTree]  

<!--Nodes highlighted yellow have direct references to them from the JavaScript code.  Nodes highlighted red do not have direct references.  They are only alive because they are part of the tree for the yellow node.  In general, you want to focus on the yellow nodes.  Fix your code so that the yellow node is not alive for longer than it needs to be, and you also get rid of the red nodes that are part of the tree for the yellow node.  -->

<span data-ttu-id="fd3d0-209">Щелкните узел, чтобы изучить его еще больше.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-209">Click on a node to investigate it further.</span></span>  <span data-ttu-id="fd3d0-210">В области **объектов** вы можете просмотреть дополнительные сведения о коде, который ссылается на него.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-210">In the **Objects** pane you are able to see more information about the code that is referencing it.</span></span>  <span data-ttu-id="fd3d0-211">Например, на [рис. 7](#figure-7) вы видите, что `detachedNodes` переменная ссылается на узел.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-211">For example, in [Figure 7](#figure-7) you are able to see that the `detachedNodes` variable is referencing the node.</span></span>  <span data-ttu-id="fd3d0-212">Чтобы устранить эту проблему, необходимо изучить код, использующий `detachedUNode` переменную, и убедиться, что ссылка на узел удаляется, когда он больше не нужен.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-212">To fix this particular memory leak, you should study the code that uses the `detachedUNode` variable and ensure that the reference to the node is removed when it is no longer needed.</span></span>

> ##### <span data-ttu-id="fd3d0-213">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="fd3d0-213">Figure 7</span></span>  
> <span data-ttu-id="fd3d0-214">Исследование узла</span><span class="sxs-lookup"><span data-stu-id="fd3d0-214">Investigating a node</span></span>  
> ![Исследование узла][ImageInvestigatingNode]  

<!--todo: the allocation timeline does not appear in the DevTools in Edge  -->  

## <span data-ttu-id="fd3d0-216">Определение утечек памяти кучи JS с инструментированием выделения на временной шкале</span><span class="sxs-lookup"><span data-stu-id="fd3d0-216">Identify JS heap memory leaks with Allocation instrumentation on timeline</span></span>  

<span data-ttu-id="fd3d0-217">**Инструментирование выделения на временной шкале** — это еще один инструмент, который может помочь вам отслеживать утечки памяти в куче JS.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-217">**Allocation instrumentation on timeline** is another tool that may help you track down memory leaks in your JS heap.</span></span>  

<span data-ttu-id="fd3d0-218">На временной шкале с помощью следующего кода показано **Инструментирование выделения ресурсов** .</span><span class="sxs-lookup"><span data-stu-id="fd3d0-218">Demonstrate **Allocation instrumentation on timeline**  using the following code.</span></span>  

```javascript
var x = [];
function grow() {
    x.push(new Array(1000000).join('x'));
}
document.getElementById('grow').addEventListener('click', grow);
```  

<span data-ttu-id="fd3d0-219">При каждом нажатии кнопки, на которую ссылается код, в массив добавляется строка из 1 000 000 символов `x` .</span><span class="sxs-lookup"><span data-stu-id="fd3d0-219">Every time that the button referenced in the code is pushed, a string of one million characters is added to the `x` array.</span></span>  

<span data-ttu-id="fd3d0-220">Чтобы записать Инструментарий выделения на временную шкалу, откройте DevTools, перейдите на панель **память** , выберите переключатель **Инструментирование на временной шкале** , нажмите кнопку **Пуск** , выполните действие, которое вы считаете причиной возникновения утечек памяти, и нажмите кнопку Остановить запись **профиля кучи** , ![ ][ImageStopRecordingIcon] когда закончите.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-220">To record an Allocation instrumentation on timeline, open DevTools, go to the **Memory** panel, select the **Allocation instrumentation on timeline** radio button, press the **Start** button, perform the action that you suspect is causing the memory leak, and then press the **Stop recording heap profile** ![stop recording][ImageStopRecordingIcon] button when you are done.</span></span>  

<span data-ttu-id="fd3d0-221">Когда вы записываете элементы, обратите внимание на то, что синие полосы отображаются на инструментальных инструментах выделения на временной шкале, как показано на [рисунке 8](#figure-8).</span><span class="sxs-lookup"><span data-stu-id="fd3d0-221">As you are recording, notice if any blue bars show up on the Allocation instrumentation on timeline, like in [Figure 8](#figure-8).</span></span>  

> ##### <span data-ttu-id="fd3d0-222">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="fd3d0-222">Figure 8</span></span>  
> <span data-ttu-id="fd3d0-223">Новые распределения</span><span class="sxs-lookup"><span data-stu-id="fd3d0-223">New allocations</span></span>  
> ![Новые распределения][ImageNewAllocations]  

<span data-ttu-id="fd3d0-225">Эти синие отрезки представляют новые выделения памяти.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-225">Those blue bars represent new memory allocations.</span></span>  <span data-ttu-id="fd3d0-226">Новые выделения памяти являются кандидатами на утечку памяти.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-226">Those new memory allocations are your candidates for memory leaks.</span></span>  <span data-ttu-id="fd3d0-227">Вы можете изменить масштаб на панели, чтобы отфильтровать область **конструктора** , чтобы отображались только те объекты, которые были выделены в течение указанного периода времени.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-227">You are able to zoom on a bar to filter the **Constructor** pane to only show objects that were allocated during the specified timeframe.</span></span>  

> ##### <span data-ttu-id="fd3d0-228">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="fd3d0-228">Figure 9</span></span>  
> <span data-ttu-id="fd3d0-229">Уменьшенная временная шкала выделения</span><span class="sxs-lookup"><span data-stu-id="fd3d0-229">Zoomed allocation timeline</span></span>  
> ![Уменьшенная временная шкала выделения][ImageZoomedAllocationTimeline]  

<span data-ttu-id="fd3d0-231">Разверните объект и щелкните значение, чтобы просмотреть дополнительные сведения в области **объектов** .</span><span class="sxs-lookup"><span data-stu-id="fd3d0-231">Expand the object and click on the value to view more details in the **Object** pane.</span></span>  <span data-ttu-id="fd3d0-232">Например, на [рис. 10](#figure-10), просмотрев сведения о новом выделенном объекте, вы сможете увидеть, что он был выделен для `x` переменной в `Window` области.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-232">For example, in [Figure 10](#figure-10), by viewing the details of the object that was newly allocated, you should be able to see that it was allocated to the `x` variable in the `Window` scope.</span></span>  

> ##### <span data-ttu-id="fd3d0-233">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="fd3d0-233">Figure 10</span></span> 
> <span data-ttu-id="fd3d0-234">Сведения об объекте</span><span class="sxs-lookup"><span data-stu-id="fd3d0-234">Object details</span></span>  
> ![Сведения об объекте][ImageObjectDetail]  

## <span data-ttu-id="fd3d0-236">Изучение выделения памяти по функциям</span><span class="sxs-lookup"><span data-stu-id="fd3d0-236">Investigate memory allocation by function</span></span>   

<span data-ttu-id="fd3d0-237">Используйте тип профилирования **выборки выделения** для просмотра выделения памяти функцией JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-237">Use the **Allocation sampling** profiling type to view memory allocation by JavaScript function.</span></span>  

> ##### <span data-ttu-id="fd3d0-238">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="fd3d0-238">Figure 11</span></span>  
> <span data-ttu-id="fd3d0-239">Выборка распределения записей</span><span class="sxs-lookup"><span data-stu-id="fd3d0-239">Record Allocation sampling</span></span>  
> ![Выборка распределения записей][ImageRecordAllocationSampling]  

1.  <span data-ttu-id="fd3d0-241">Установите переключатель **выборка распределения** .</span><span class="sxs-lookup"><span data-stu-id="fd3d0-241">Select the **Allocation sampling** radio button.</span></span>  <span data-ttu-id="fd3d0-242">Если на странице есть рабочий процесс, вы можете выбрать его в качестве целевого объекта профилирования с помощью раскрывающегося меню рядом с кнопкой " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="fd3d0-242">If there is a worker on the page, you are able to select that as the profiling target using the dropdown menu next to the **Start** button.</span></span>  
1.  <span data-ttu-id="fd3d0-243">Нажмите кнопку " **Пуск** ".</span><span class="sxs-lookup"><span data-stu-id="fd3d0-243">Press the **Start** button.</span></span>  
1.  <span data-ttu-id="fd3d0-244">Выполните действия, которые нужно изучить на странице.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-244">Perform the actions on the page which you want to investigate.</span></span>  
1.  <span data-ttu-id="fd3d0-245">После завершения всех действий нажмите кнопку " **остановить** ".</span><span class="sxs-lookup"><span data-stu-id="fd3d0-245">Press the **Stop** button when you have finished all of your actions.</span></span>  

<span data-ttu-id="fd3d0-246">DevTools показывает разделение выделения памяти по функциям.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-246">DevTools shows you a breakdown of memory allocation by function.</span></span>  <span data-ttu-id="fd3d0-247">Представление по умолчанию является **большим (снизу вверх)**, в котором отображаются функции, которые выделили наибольшую область памяти сверху.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-247">The default view is **Heavy (Bottom Up)**, which displays the functions that allocated the most memory at the top.</span></span>  

> ##### <span data-ttu-id="fd3d0-248">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="fd3d0-248">Figure 12</span></span>  
> <span data-ttu-id="fd3d0-249">Выборка распределения</span><span class="sxs-lookup"><span data-stu-id="fd3d0-249">Allocation sampling</span></span>  
>![Выборка распределения][ImageAllocationSampling]  

## <span data-ttu-id="fd3d0-251">Точечные часто используемые сборки мусора</span><span class="sxs-lookup"><span data-stu-id="fd3d0-251">Spot frequent garbage collections</span></span>  

<span data-ttu-id="fd3d0-252">Если страница часто задерживается, возможно, у вас возникли проблемы с обсбором мусора.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-252">If your page appears to pause frequently, then you may have garbage collection issues.</span></span>  

<span data-ttu-id="fd3d0-253">Вы можете использовать либо Диспетчер задач браузера Microsoft EDGE, либо записи памяти для выявления частых сборок мусора.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-253">You are able to use either the Microsoft Edge Browser Task Manager or Performance memory recordings to spot frequent garbage collection.</span></span>  <span data-ttu-id="fd3d0-254">В диспетчере задач браузера Microsoft Edge часто растет и падает **память** , а также значения **памяти JavaScript** , которые представляют собой частый процесс сборки мусора.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-254">In the Microsoft Edge Browser Task Manager, frequently rising and falling **Memory** or **JavaScript Memory** values represent frequent garbage collection.</span></span>  <span data-ttu-id="fd3d0-255">В записях производительности частые изменения (рост и отпадает) на графы JS или счетчики узлов указывают на частную сборку мусора.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-255">In Performance recordings, frequent changes (rising and falling) to the JS heap or node count graphs indicate frequent garbage collection.</span></span>  

<span data-ttu-id="fd3d0-256">После того как вы обнаружите проблему, вы можете использовать **инструментарий выделения для записи временной шкалы** , чтобы узнать, где выделяется память, и какая функция вызывает распределение.</span><span class="sxs-lookup"><span data-stu-id="fd3d0-256">After you have identified the problem, you are able to use an **Allocation instrumentation on timeline** recording to find out where memory is being allocated and which functions are causing the allocations.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageForceGarbageCollectionIcon]: /microsoft-edge/devtools-guide-chromium/media/collect-garbage-icon.msft.png  
[ImageStopRecordingIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-recording-icon.msft.png  

[ImageTaskManager]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-settings-more-tools-browser-task-manager.msft.png "Рисунок 1: Открытие диспетчера задач браузера Microsoft Edge"  
[ImageJavascriptMemory]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-bing-browser-task-manager-javascript-memory.msft.png "Рисунок 2: включение памяти JavaScript"  
[ImageSimpleGrowth]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-1-performance-memory.msft.png "Рисунок 3: простое расширение"  
[ImageTakeHeapSnapshot]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot.msft.png "Рисунок 4: создание снимка кучи"  
[ImageFilteringForDetachedNodes]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached.msft.png "Рисунок 5: Фильтрация отсоединенных узлов"  
[ImageInvestigatingDetachedTree]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded.msft.png "Рисунок 6: исследование отсоединенных деревьев"  
[ImageInvestigatingNode]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-12-memory-heap-snapshot-filter-detached-expanded-selected.msft.png "Рисунок 7: исследование узла"  
[ImageNewAllocations]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-all.msft.png "Рисунок 8: новые выделения"  
[ImageZoomedAllocationTimeline]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused.msft.png "Рисунок 9: уменьшенная временная шкала выделения"  
[ImageObjectDetail]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-13-allocation-timeline-snapshot-focused-constructor-expanded.msft.png "Рисунок 10: сведения об объекте"  
[ImageRecordAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling.msft.png "Рисунок 11: выборка для выделения записей"  
[ImageAllocationSampling]: /microsoft-edge/devtools-guide-chromium/media/memory-problems-glitch-example-05-memory-allocation-sampling-heavy-bottom-up.msft.png "Рисунок 12: Выбор распределения"  

<!-- links -->  

[DevtoolsEvaluatePerformanceReferenceRecord]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#record-performance "Сведения о производительности записи: Справочник по анализу производительности"  

<!--[RAIL]: /profile/evaluate-performance/rail  -->
<!--[recording]: /profile/evaluate-performance/timeline-tool#make-a-recording ""  -->  

<!--[hngd]: https://jsfiddle.net/kaycebasques/tmtbw8ef/  -->  

> [!NOTE]
> <span data-ttu-id="fd3d0-270">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fd3d0-270">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fd3d0-271">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="fd3d0-271">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/memory-problems/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fd3d0-273">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fd3d0-273">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  