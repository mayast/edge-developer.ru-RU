---
description: Использование API консоли для программной отладки и профилирования кода
title: DevTools — консольный интерфейс API
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, консольный API
ms.custom: seodec18
ms.openlocfilehash: d722934c3694c3c23e367141158ad45f6d03b175
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572596"
---
# <span data-ttu-id="d1a68-104">API консоли</span><span class="sxs-lookup"><span data-stu-id="d1a68-104">Console API</span></span>

<span data-ttu-id="d1a68-105">*API консоли* предоставляет командную строку и программный доступ к консоли DevTools через Глобальный `console` объект, что позволяет:</span><span class="sxs-lookup"><span data-stu-id="d1a68-105">The *Console API* provides command-line and programmatic access to the  DevTools Console through the global `console` object, allowing you to:</span></span>

 - <span data-ttu-id="d1a68-106">[Регистрация настраиваемых сообщений](#logging-custom-messages) из кода</span><span class="sxs-lookup"><span data-stu-id="d1a68-106">[Log custom messages](#logging-custom-messages) from you code</span></span>
 - <span data-ttu-id="d1a68-107">[Проверка объектов и элементов](#inspecting-objects-and-elements) и регистрация их данных</span><span class="sxs-lookup"><span data-stu-id="d1a68-107">[Inspect objects and elements](#inspecting-objects-and-elements) and log their information</span></span>
 - <span data-ttu-id="d1a68-108">[Проверка и измерение кода](#testing-and-measuring) путем настройки утверждений, таймеров и счетчиков</span><span class="sxs-lookup"><span data-stu-id="d1a68-108">[Test and measure your code](#testing-and-measuring) by setting assertions, timers and counters</span></span>
 - <span data-ttu-id="d1a68-109">[Создание снимков кучи](#taking-heap-snapshots) для оценки потребления памяти выполняющегося кода и выявления утечек памяти</span><span class="sxs-lookup"><span data-stu-id="d1a68-109">[Take snapshots of the heap](#taking-heap-snapshots) to assess the memory consumption of your running code and identify memory leaks</span></span>
 - <span data-ttu-id="d1a68-110">[Трассировка callstacks](#tracing-callstacks) для понимания места вызова кода</span><span class="sxs-lookup"><span data-stu-id="d1a68-110">[Trace your callstacks](#tracing-callstacks) to understand where your code is being called from</span></span> 
 - <span data-ttu-id="d1a68-111">[Упорядочение данных журнала](#organizing-log-output) для упрощения отладки</span><span class="sxs-lookup"><span data-stu-id="d1a68-111">[Organize your log output](#organizing-log-output) to streamline your debugging</span></span>

<span data-ttu-id="d1a68-112">Ниже указаны команды и параметры форматирования, которые в настоящее время поддерживаются в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="d1a68-112">The following are the commands and formatting parameters currently supported by Microsoft Edge.</span></span> <span data-ttu-id="d1a68-113">Они работают точно так же, как и в крупных браузерах.</span><span class="sxs-lookup"><span data-stu-id="d1a68-113">They work similarly on major browsers.</span></span>

## <span data-ttu-id="d1a68-114">Ведение журнала настраиваемых сообщений</span><span class="sxs-lookup"><span data-stu-id="d1a68-114">Logging custom messages</span></span>

<span data-ttu-id="d1a68-115">Ваш код может отправлять на консоль различные типы настраиваемых сообщений, в том числе:</span><span class="sxs-lookup"><span data-stu-id="d1a68-115">Your code can send several types of custom messages to the console, including:</span></span>

<span data-ttu-id="d1a68-116">Тип сообщения</span><span class="sxs-lookup"><span data-stu-id="d1a68-116">Message type</span></span>  | &nbsp;   |
:------------------- | :------ |
<span data-ttu-id="d1a68-117">[**Error ()**](https://developer.mozilla.org/docs/Web/API/Console/error) и [ **Exception ()**](https://developer.mozilla.org/docs/Web/API/Console/error)</span><span class="sxs-lookup"><span data-stu-id="d1a68-117">[**error()**](https://developer.mozilla.org/docs/Web/API/Console/error) and [**exception()**](https://developer.mozilla.org/docs/Web/API/Console/error)</span></span>| <span data-ttu-id="d1a68-118">Критические ошибки и сбои</span><span class="sxs-lookup"><span data-stu-id="d1a68-118">Critical errors and failures</span></span>
[**<span data-ttu-id="d1a68-119">warn ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-119">warn()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/warn) | <span data-ttu-id="d1a68-120">Возможные ошибки или неожиданные действия</span><span class="sxs-lookup"><span data-stu-id="d1a68-120">Possible errors or unexpected behavior</span></span> 
[**<span data-ttu-id="d1a68-121">INFO ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-121">info()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/info) | <span data-ttu-id="d1a68-122">Полезные (но не важные) сведения</span><span class="sxs-lookup"><span data-stu-id="d1a68-122">Useful, but non-critical information</span></span>
<span data-ttu-id="d1a68-123">[**log ()**](https://developer.mozilla.org/docs/Web/API/Console/log) и [ **Debug ()**](https://developer.mozilla.org/docs/Web/API/Console/log)</span><span class="sxs-lookup"><span data-stu-id="d1a68-123">[**log()**](https://developer.mozilla.org/docs/Web/API/Console/log) and [**debug()**](https://developer.mozilla.org/docs/Web/API/Console/log)</span></span> | <span data-ttu-id="d1a68-124">Общая Отладка (без создания системного значка оповещения на консоли)</span><span class="sxs-lookup"><span data-stu-id="d1a68-124">General debugging (without generating a system alert icon in the console)</span></span>

   
<span data-ttu-id="d1a68-125">Вы можете сгруппировать и отфильтровать эти данные вместе с другими сообщениями, созданными в Microsoft EDGE, на панели консоли.</span><span class="sxs-lookup"><span data-stu-id="d1a68-125">You can group and filter these along with the other messages generated from Microsoft Edge from the  Console panel.</span></span> <span data-ttu-id="d1a68-126">Для всех настраиваемых методов сообщений требуется параметр String (Message) и параметры подстановки для необязательного формата.</span><span class="sxs-lookup"><span data-stu-id="d1a68-126">All custom message methods require a string (message) parameter and optional format substitution parameters.</span></span> <span data-ttu-id="d1a68-127">Microsoft EDGE поддерживает следующие параметры форматирования:</span><span class="sxs-lookup"><span data-stu-id="d1a68-127">Microsoft Edge supports the following formatting options:</span></span>

<span data-ttu-id="d1a68-128">Параметр Format (формат)</span><span class="sxs-lookup"><span data-stu-id="d1a68-128">Format parameter</span></span> | &nbsp;
:------------------- | :--- |
**<span data-ttu-id="d1a68-129">% b</span><span class="sxs-lookup"><span data-stu-id="d1a68-129">%b</span></span>** | <span data-ttu-id="d1a68-130">Двоичный</span><span class="sxs-lookup"><span data-stu-id="d1a68-130">Binary</span></span>
**<span data-ttu-id="d1a68-131">% c</span><span class="sxs-lookup"><span data-stu-id="d1a68-131">%c</span></span>** | <span data-ttu-id="d1a68-132">Встроенный стиль CSS (см. пример ниже)</span><span class="sxs-lookup"><span data-stu-id="d1a68-132">Inline CSS style (see example below)</span></span>
<span data-ttu-id="d1a68-133">**% d**, **% i**</span><span class="sxs-lookup"><span data-stu-id="d1a68-133">**%d**, **%i**</span></span> | <span data-ttu-id="d1a68-134">целое число</span><span class="sxs-lookup"><span data-stu-id="d1a68-134">Integer</span></span> 
**<span data-ttu-id="d1a68-135">% f</span><span class="sxs-lookup"><span data-stu-id="d1a68-135">%f</span></span>** | <span data-ttu-id="d1a68-136">Плавающий</span><span class="sxs-lookup"><span data-stu-id="d1a68-136">Float</span></span>  
**<span data-ttu-id="d1a68-137">% s</span><span class="sxs-lookup"><span data-stu-id="d1a68-137">%s</span></span>** | <span data-ttu-id="d1a68-138">Строка</span><span class="sxs-lookup"><span data-stu-id="d1a68-138">String</span></span> 
**<span data-ttu-id="d1a68-139">% x</span><span class="sxs-lookup"><span data-stu-id="d1a68-139">%x</span></span>** | <span data-ttu-id="d1a68-140">Чисел</span><span class="sxs-lookup"><span data-stu-id="d1a68-140">Hexadecimal</span></span> 
**<span data-ttu-id="d1a68-141">% e</span><span class="sxs-lookup"><span data-stu-id="d1a68-141">%e</span></span>** | <span data-ttu-id="d1a68-142">Водит</span><span class="sxs-lookup"><span data-stu-id="d1a68-142">Exponent</span></span> 

<span data-ttu-id="d1a68-143">Например, вот как можно включить строковые и целочисленные переменные в сообщение журнала:</span><span class="sxs-lookup"><span data-stu-id="d1a68-143">For example, here's how you would include string and integer variables in your log message:</span></span>

```javascript
var myText = 'pieces';
var myVal = 5;
console.log("The number of %s is %d.", myText, myVal);
```

>`The number of pieces is 5.`

<span data-ttu-id="d1a68-144">Вот как можно добавить зеленый эффект подсветки в сообщение журнала с помощью встроенного CSS ( `%c` ):</span><span class="sxs-lookup"><span data-stu-id="d1a68-144">And here's how you might add a green highlight effect to a log message with inline CSS (`%c`):</span></span>

```javascript
console.log("%cHighlight this log message in green", "background-color: #10ff00; text-transform: uppercase;");
```

![Журнал консоли с встроенными стилями](../media/console_api_css.png)

## <span data-ttu-id="d1a68-146">Проверка объектов и элементов</span><span class="sxs-lookup"><span data-stu-id="d1a68-146">Inspecting objects and elements</span></span>

<span data-ttu-id="d1a68-147">Проверяемые объекты отображаются на консоли в свернутом виде дерева с развернутыми узлами.</span><span class="sxs-lookup"><span data-stu-id="d1a68-147">Inspectable objects appear in the console in a collapsed tree view with expandable nodes.</span></span> <span data-ttu-id="d1a68-148">Консоль определяет, отправляет ли вы узел DOM (например, DIV) или объект JavaScript (например, событие) и автоматически отображает их как обнаруженный тип.</span><span class="sxs-lookup"><span data-stu-id="d1a68-148">The console detects whether you are sending a DOM node (like a div) or a JavaScript object (like an event) and displays them as the detected type automatically.</span></span>

<span data-ttu-id="d1a68-149">Вы также можете принудительно использовать определенные выходные данные:</span><span class="sxs-lookup"><span data-stu-id="d1a68-149">You can also force a specific output:</span></span>

<span data-ttu-id="d1a68-150">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-150">Command</span></span> | &nbsp;
:------------------- | :--- |
[**<span data-ttu-id="d1a68-151">dir ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-151">dir()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/dir) | <span data-ttu-id="d1a68-152">Отображает как объект JavaScript, который вы изучите</span><span class="sxs-lookup"><span data-stu-id="d1a68-152">Displays as inspectable JavaScript object</span></span>
[**<span data-ttu-id="d1a68-153">dirxml()</span><span class="sxs-lookup"><span data-stu-id="d1a68-153">dirxml()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/dirxml) | <span data-ttu-id="d1a68-154">Отображается как узел DOM, который вы проверили</span><span class="sxs-lookup"><span data-stu-id="d1a68-154">Displays as inspectable DOM node</span></span>

<span data-ttu-id="d1a68-155">Например, попробуйте открыть консоль и сравните следующие выходные элементы для `<div id='main'>` элемента на этой странице:</span><span class="sxs-lookup"><span data-stu-id="d1a68-155">For example, try opening the console and compare the following outputs for the `<div id='main'>` element on this page:</span></span>

```javascript
console.dir(document.querySelector('#main'));
console.dirxml(document.querySelector('#main'));
```

![Сравнение выходных данных "Dir" и "DirXML"](../media/console_api_dir.png)

### <span data-ttu-id="d1a68-157">Выбор элемента на панели « **элементы** »</span><span class="sxs-lookup"><span data-stu-id="d1a68-157">Selecting an element in the **Elements** panel</span></span>

<span data-ttu-id="d1a68-158">Вы можете выбрать элемент в контекстном дереве HTML страницы прямо из консоли для немедленной отладки макета и стиля.</span><span class="sxs-lookup"><span data-stu-id="d1a68-158">You can select an element within the HTML tree context of the page directly from the console for immediate layout and style debugging.</span></span>

<span data-ttu-id="d1a68-159">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-159">Command</span></span> | &nbsp;
:------------------- | :--- |
**<span data-ttu-id="d1a68-160">SELECT ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-160">select()</span></span>** | <span data-ttu-id="d1a68-161">Переключение на панель **элементов** и установка фокуса на указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="d1a68-161">Switches to the **Elements** panel and sets focus to the specified element.</span></span>

<span data-ttu-id="d1a68-162">Например, если открыть консоль на этой странице, введите следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d1a68-162">For example, if you open the console on this page and type:</span></span>

```javascript
console.select(document.querySelector("body"));
```

<span data-ttu-id="d1a68-163">DevTools перейдет на панель **элементы** (если она еще не является текущей) и установите фокус в [*представлении в виде дерева HTML*](../elements.md#html-tree-view) на указанный элемент.</span><span class="sxs-lookup"><span data-stu-id="d1a68-163">The DevTools will switch to the **Elements** panel (if its not already the current) and set focus in the [*HTML tree view*](../elements.md#html-tree-view) to the specified element.</span></span>

![Пример метода "Select"](../media/console_api_select.png)

## <span data-ttu-id="d1a68-165">Тестирование и измерение</span><span class="sxs-lookup"><span data-stu-id="d1a68-165">Testing and measuring</span></span>

### <span data-ttu-id="d1a68-166">Тестирование кода</span><span class="sxs-lookup"><span data-stu-id="d1a68-166">Testing your code</span></span>

<span data-ttu-id="d1a68-167">Добавляйте утверждения тестового API-интерфейса для модульного тестирования и отладки кода при его выполнении в браузере.</span><span class="sxs-lookup"><span data-stu-id="d1a68-167">Add Console API test assertions to your code for unit testing and debugging your code as it runs in the browser.</span></span>

<span data-ttu-id="d1a68-168">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-168">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="d1a68-169">Assert ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-169">assert()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/assert) | <span data-ttu-id="d1a68-170">Заносит в журнал сообщение об ошибке консоли, если указанное выражение имеет *значение false*.</span><span class="sxs-lookup"><span data-stu-id="d1a68-170">Logs a console error message if the provided expression evaluates to *false*.</span></span>

<span data-ttu-id="d1a68-171">В дополнение к логическому выражению, которое вы используете для тестируемого утверждения, вы можете добавить дополнительное сообщение и параметры форматирования, как и в случае с другими [настраиваемыми сообщениями консоли](#logging-custom-messages).</span><span class="sxs-lookup"><span data-stu-id="d1a68-171">In addition to the logical expression you supply as the testable assertion, you can add an optional message and formatting parameters as you would use with other [custom console messages](#logging-custom-messages).</span></span> <span data-ttu-id="d1a68-172">Пример</span><span class="sxs-lookup"><span data-stu-id="d1a68-172">For example:</span></span>

```javascript
var x = 26.8;
console.assert(x < 25, 'The value of x is %f (it is NOT less than %i)', x, 25);
```

![Пример метода Assert](../media/console_api_assert.png)

### <span data-ttu-id="d1a68-174">Подсчет выполнения в коде</span><span class="sxs-lookup"><span data-stu-id="d1a68-174">Counting executions in your code</span></span>

<span data-ttu-id="d1a68-175">Вы можете настроить в коде счетчики, чтобы следить за тем, сколько вхождений окружающего кода выполняется.</span><span class="sxs-lookup"><span data-stu-id="d1a68-175">You can set counters in your code to keep track of how many times the surrounding code gets executed.</span></span> <span data-ttu-id="d1a68-176">С помощью счетчиков можно убедиться, что ваш код работает должным образом и поможет диагностировать узкие места производительности.</span><span class="sxs-lookup"><span data-stu-id="d1a68-176">Setting counters can help ensure your code is running as expected and assist you in diagnosing performance bottlenecks.</span></span>

<span data-ttu-id="d1a68-177">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-177">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="d1a68-178">Count ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-178">count()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/count) | <span data-ttu-id="d1a68-179">Увеличивается и записывает количество операций *Count ()* для данной метки.</span><span class="sxs-lookup"><span data-stu-id="d1a68-179">Increments and logs the number of times *count()* for the given label has been executed.</span></span>
[**<span data-ttu-id="d1a68-180">countReset()</span><span class="sxs-lookup"><span data-stu-id="d1a68-180">countReset()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/countReset) | <span data-ttu-id="d1a68-181">Сбрасывает количество на ноль для заданной метки счетчика.</span><span class="sxs-lookup"><span data-stu-id="d1a68-181">Resets the count to zero for the given counter label.</span></span>

<span data-ttu-id="d1a68-182">Например, выполните следующие строки на консоли:</span><span class="sxs-lookup"><span data-stu-id="d1a68-182">For example, executing the following lines in console:</span></span>

```javascript
console.count('My Counter');
console.count('My Counter');
console.countReset('My Counter');
console.count('My Counter');
```

 <span data-ttu-id="d1a68-183">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-183">.</span></span> <span data-ttu-id="d1a68-184">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-184">.</span></span> <span data-ttu-id="d1a68-185">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-185">.</span></span> <span data-ttu-id="d1a68-186">Это приведет к следующим результатам:</span><span class="sxs-lookup"><span data-stu-id="d1a68-186">will result in:</span></span>
> <span data-ttu-id="d1a68-187">Мой счетчик: 1</span><span class="sxs-lookup"><span data-stu-id="d1a68-187">My Counter: 1</span></span>

### <span data-ttu-id="d1a68-188">Синхронизация кода</span><span class="sxs-lookup"><span data-stu-id="d1a68-188">Timing your code</span></span>

<span data-ttu-id="d1a68-189">Инструментировать код с помощью помеченных таймеров, чтобы оценить время, необходимое для выполнения данной операции.</span><span class="sxs-lookup"><span data-stu-id="d1a68-189">Instrument your code with labeled timers to measure how long it takes to complete a given operation.</span></span>

<span data-ttu-id="d1a68-190">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-190">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="d1a68-191">Time ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-191">time()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/time) | <span data-ttu-id="d1a68-192">Запускает таймер с заданной меткой.</span><span class="sxs-lookup"><span data-stu-id="d1a68-192">Starts a timer with the given label.</span></span>
[**<span data-ttu-id="d1a68-193">timeEnd()</span><span class="sxs-lookup"><span data-stu-id="d1a68-193">timeEnd()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/timeEnd) | <span data-ttu-id="d1a68-194">Завершает таймер с заданной меткой и показывает затраченное время (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="d1a68-194">Ends the timer with the given label and reports the time elapsed (in milliseconds).</span></span>
[**<span data-ttu-id="d1a68-195">timeStamp ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-195">timeStamp()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/timeStamp) | <span data-ttu-id="d1a68-196">Показывает текущее системное время (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="d1a68-196">Reports the current system time (in milliseconds).</span></span>

<span data-ttu-id="d1a68-197">Например, попробуйте выполнить следующие строки на консоли:</span><span class="sxs-lookup"><span data-stu-id="d1a68-197">For example, try executing the following lines in console:</span></span>

```javascript
console.time('My Timer');
console.timeEnd('My Timer');
```

### <span data-ttu-id="d1a68-198">Создание снимков кучи</span><span class="sxs-lookup"><span data-stu-id="d1a68-198">Taking heap snapshots</span></span>

<span data-ttu-id="d1a68-199">Создание снимков кучи для оценки потребления памяти запущенного кода и выявления утечек памяти.</span><span class="sxs-lookup"><span data-stu-id="d1a68-199">Take snapshots of the heap to assess the memory consumption of your running code and identify memory leaks.</span></span>

<span data-ttu-id="d1a68-200">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-200">Command</span></span> | &nbsp;
:------------ | :-------------
**<span data-ttu-id="d1a68-201">takeHeapSnapshot()</span><span class="sxs-lookup"><span data-stu-id="d1a68-201">takeHeapSnapshot()</span></span>** | <span data-ttu-id="d1a68-202">Захватывает сведения о текущей куче JavaScript и ее выделенных объектах.</span><span class="sxs-lookup"><span data-stu-id="d1a68-202">Captures details about the current JavaScript heap and its allocated objects.</span></span>

<span data-ttu-id="d1a68-203">Для получения снимков кучи необходимо, чтобы выполнялось приложение DevTools [Memory Profiler](../memory.md#toolbar) .</span><span class="sxs-lookup"><span data-stu-id="d1a68-203">The  DevTools [memory profiler](../memory.md#toolbar) must be running in order to take heap snapshots.</span></span> <span data-ttu-id="d1a68-204">Каждый из них будет отображаться в виде плитки в [*сводке моментальных снимков*](../memory.md#snapshot-summary) панели [**памяти**](../memory.md) для дальнейшей проверки.</span><span class="sxs-lookup"><span data-stu-id="d1a68-204">Each snapshot will appear as a tile in the [*Snapshot summary*](../memory.md#snapshot-summary) of the [**Memory**](../memory.md) panel for further inspection.</span></span>

## <span data-ttu-id="d1a68-205">Трассировка callstacks</span><span class="sxs-lookup"><span data-stu-id="d1a68-205">Tracing callstacks</span></span>

<span data-ttu-id="d1a68-206">Сведения о том, где выполняется вызов вашего кода, о том, что он работает, а также о том, как долго выполнение программы может быть полезно при анализе slowness или неожиданного поведения.</span><span class="sxs-lookup"><span data-stu-id="d1a68-206">Understanding where your code is being called from, what code is running, and how long that execution takes can be useful in analyzing slowness or unexpected behavior.</span></span> <span data-ttu-id="d1a68-207">Трассировка стека показывает путь выполнения, по которому ваш код пройдет за него, из запроса трассировки вверх по пути.</span><span class="sxs-lookup"><span data-stu-id="d1a68-207">A stack trace shows you the execution path your code took to reach it, from the trace request upward through the path.</span></span> 

<span data-ttu-id="d1a68-208">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-208">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="d1a68-209">Trace ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-209">trace()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/trace) | <span data-ttu-id="d1a68-210">Выводит трассировку стека обработки текущего выполнения сценария.</span><span class="sxs-lookup"><span data-stu-id="d1a68-210">Outputs a trace of the current script execution callstack.</span></span>

<span data-ttu-id="d1a68-211">Например, для запуска следующего кода на консоли:</span><span class="sxs-lookup"><span data-stu-id="d1a68-211">For example, running the following code in the console:</span></span>

```javascript
function a(){
  c();
}
function b(){
  c();
}
function c(){
  console.trace()
}
function d(){
  b();
}

a();
d();
```

<span data-ttu-id="d1a68-212">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-212">.</span></span> <span data-ttu-id="d1a68-213">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-213">.</span></span> <span data-ttu-id="d1a68-214">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-214">.</span></span> <span data-ttu-id="d1a68-215">будут выводиться следующие трассировки стека:</span><span class="sxs-lookup"><span data-stu-id="d1a68-215">will output the following stack traces:</span></span>
> <span data-ttu-id="d1a68-216">Console. Trace () на c (код eval: 8:3) на этапе (eval Code: 2:3) на этапе оценки кода (код eval: 14:1)</span><span class="sxs-lookup"><span data-stu-id="d1a68-216">console.trace() at c (eval code:8:3) at a (eval code:2:3) at eval code (eval code:14:1)</span></span>
> 
> <span data-ttu-id="d1a68-217">Console. Trace () в c (eval код: 8:3) на странице b (eval Code: 5:3) на d (eval Code: 11:3) на этапе оценки кода (eval: 15:1)</span><span class="sxs-lookup"><span data-stu-id="d1a68-217">console.trace() at c (eval code:8:3) at b (eval code:5:3) at d (eval code:11:3) at eval code (eval code:15:1)</span></span>

## <span data-ttu-id="d1a68-218">Упорядочение выходных данных журнала</span><span class="sxs-lookup"><span data-stu-id="d1a68-218">Organizing log output</span></span>

<span data-ttu-id="d1a68-219">Для простого удаления всех предыдущих выходных данных на консоли используйте *Console. Clear ()* (или `CTRL + L` ).</span><span class="sxs-lookup"><span data-stu-id="d1a68-219">To simply clear all previous console output, use *console.clear()* (or `CTRL + L`).</span></span> <span data-ttu-id="d1a68-220">Это не очищает историю команд консоли (вы по-прежнему можете обойти ее с помощью клавиш со стрелками вверх и вниз).</span><span class="sxs-lookup"><span data-stu-id="d1a68-220">This does not clear the backstack of your console command history (you can still traverse it with the up and down arrow keys).</span></span>

<span data-ttu-id="d1a68-221">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-221">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="d1a68-222">Clear ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-222">clear()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/clear) | <span data-ttu-id="d1a68-223">Очистка всех предыдущих выходных данных на консоли.</span><span class="sxs-lookup"><span data-stu-id="d1a68-223">Clears all previous console output.</span></span>

<span data-ttu-id="d1a68-224">Если ваш код выводит большое количество сообщений консоли, вы можете визуально упорядочивать их по вложенным блокам с помощью следующих команд:</span><span class="sxs-lookup"><span data-stu-id="d1a68-224">If your code outputs a lot of console messages, you can visually organize them into nested blocks with the following commands:</span></span>

 <span data-ttu-id="d1a68-225">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-225">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="d1a68-226">Group ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-226">group()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/group) | <span data-ttu-id="d1a68-227">Запускает новый уровень вложенности для вывода на консоль с указанной (необязательной) меткой.</span><span class="sxs-lookup"><span data-stu-id="d1a68-227">Starts a new level of nesting for console output with the specified (optional) label.</span></span>
[**<span data-ttu-id="d1a68-228">groupCollapsed()</span><span class="sxs-lookup"><span data-stu-id="d1a68-228">groupCollapsed()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/groupCollapsed) | <span data-ttu-id="d1a68-229">Запускает новый уровень вложенности для вывода на консоль с указанной (необязательной) меткой, но элемент управления группированием по умолчанию свернут и должен быть развернут (с помощью элемента управления стрелками), чтобы отобразить дочерний вывод.</span><span class="sxs-lookup"><span data-stu-id="d1a68-229">Starts a new level of nesting for console output with the specified (optional) label, however the grouping control is collapsed by default and must be expanded (by clicking on the arrow control) to display the child output.</span></span>
[**<span data-ttu-id="d1a68-230">groupEnd()</span><span class="sxs-lookup"><span data-stu-id="d1a68-230">groupEnd()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/groupEnd) | <span data-ttu-id="d1a68-231">Завершает группу вложений для указанной метки.</span><span class="sxs-lookup"><span data-stu-id="d1a68-231">Ends the nesting group for the specified label.</span></span>

<span data-ttu-id="d1a68-232">Например, попробуйте ввести на консоли следующие команды:</span><span class="sxs-lookup"><span data-stu-id="d1a68-232">For example, try entering the following commands in the console:</span></span>

```javascript
console.groupCollapsed('Group 1');
console.log('In Group 1');
console.groupCollapsed('Group 1.1');
console.log('In Group 1.1');
console.groupEnd('Group 1.1');
console.groupEnd('Group 1');
console.log('No longer in a group');
```

<span data-ttu-id="d1a68-233">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-233">.</span></span> <span data-ttu-id="d1a68-234">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-234">.</span></span> <span data-ttu-id="d1a68-235">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-235">.</span></span> <span data-ttu-id="d1a68-236">затем разверните элементы управления *Group 1* и *Group 1,1* , чтобы увидеть, как вложенные комментарии в журнале.</span><span class="sxs-lookup"><span data-stu-id="d1a68-236">and then expand the *Group 1* and *Group 1.1* controls to see how the log comments are nested:</span></span>

![Группировка сообщений на консоли](../media/console_api_group.png)

<span data-ttu-id="d1a68-238">Иногда проще визуализировать объект или массив JavaScript в табличной форме, а не в виде плоского списка.</span><span class="sxs-lookup"><span data-stu-id="d1a68-238">Sometimes its easier to visualize a JavaScript object or array in tabular form, rather than a flat list.</span></span> <span data-ttu-id="d1a68-239">Для этого можно использовать команду *Console. Table ()* :</span><span class="sxs-lookup"><span data-stu-id="d1a68-239">For that, you can use the *console.table()* command:</span></span>

<span data-ttu-id="d1a68-240">Команда</span><span class="sxs-lookup"><span data-stu-id="d1a68-240">Command</span></span> | &nbsp;
:------------ | :-------------
[**<span data-ttu-id="d1a68-241">Table ()</span><span class="sxs-lookup"><span data-stu-id="d1a68-241">table()</span></span>**](https://developer.mozilla.org/docs/Web/API/Console/table) | <span data-ttu-id="d1a68-242">Выводит предоставленный массив или объект на консоль в табличной форме.</span><span class="sxs-lookup"><span data-stu-id="d1a68-242">Outputs the supplied array or object to the console in tabular form.</span></span>

<span data-ttu-id="d1a68-243">Например, в приведенном ниже массиве объектов:</span><span class="sxs-lookup"><span data-stu-id="d1a68-243">For example, the following object array:</span></span>

```javascript
var orders = [{'Size':'XL', 'Quantity':1},{'Size':'M', 'Quantity':3}, {'Size':'L', 'Quantity':2}];
console.table(orders);
```

<span data-ttu-id="d1a68-244">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-244">.</span></span> <span data-ttu-id="d1a68-245">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-245">.</span></span> <span data-ttu-id="d1a68-246">.</span><span class="sxs-lookup"><span data-stu-id="d1a68-246">.</span></span> <span data-ttu-id="d1a68-247">выводится в этой таблице на консоли:</span><span class="sxs-lookup"><span data-stu-id="d1a68-247">will render as this table in the console:</span></span>

![Отображение массива объектов в виде таблицы на консоли](../media/console_api_table.png)
