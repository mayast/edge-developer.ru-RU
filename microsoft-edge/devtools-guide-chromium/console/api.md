---
title: Справочник по API консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: e54bae7c7c61584ccd39568f1bb54312cc2082c0
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601756"
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





# <span data-ttu-id="726a6-103">Справочник по API консоли</span><span class="sxs-lookup"><span data-stu-id="726a6-103">Console API Reference</span></span>   

  

<span data-ttu-id="726a6-104">Используйте методы API консоли для записи сообщений на консоль из JavaScript.</span><span class="sxs-lookup"><span data-stu-id="726a6-104">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="726a6-105">В разделе Начало [работы с сообщениями журнала на консоли можно][DevtoolsConsoleLog] ознакомиться с интерактивным введением в раздел.</span><span class="sxs-lookup"><span data-stu-id="726a6-105">See [Get Started With Logging Messages To The Console][DevtoolsConsoleLog] for an interactive introduction to the topic.</span></span>  <span data-ttu-id="726a6-106">Ознакомьтесь со [справочными материалами API для консольных программ] [DevtoolConsoleUtilities] , если вы ищете удобные методы, такие как `debug()` или `monitorEvents()` доступные только на консоли.</span><span class="sxs-lookup"><span data-stu-id="726a6-106">See [Console Utilities API Reference] [DevtoolConsoleUtilities] if you are looking for the convenience methods like `debug()` or `monitorEvents()` which are only available from the Console.</span></span>  

## <span data-ttu-id="726a6-107">затребованного</span><span class="sxs-lookup"><span data-stu-id="726a6-107">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="726a6-108">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-108">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="726a6-109">При вычислении выводит на консоль [сообщение об ошибке](#error) `expression` `false` .</span><span class="sxs-lookup"><span data-stu-id="726a6-109">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

> ##### <span data-ttu-id="726a6-110">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="726a6-110">Figure 1</span></span>  
> <span data-ttu-id="726a6-111">Результат `console.assert()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-111">The result of the `console.assert()` example</span></span>  
> ![Результат примера Console. Assert ()][ImageAssert]  

## <span data-ttu-id="726a6-113">Сброс</span><span class="sxs-lookup"><span data-stu-id="726a6-113">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="726a6-114">Очищает консоль.</span><span class="sxs-lookup"><span data-stu-id="726a6-114">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="726a6-115">Если включен [протокол Preserve][DevtoolsConsoleReferenceLevel] , метод [clear](#clear) отключен.</span><span class="sxs-lookup"><span data-stu-id="726a6-115">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

<span data-ttu-id="726a6-116">Дополнительные сведения: [Очистка консоли][DevtoolsConsoleReferenceClear]</span><span class="sxs-lookup"><span data-stu-id="726a6-116">See also: [Clear the Console][DevtoolsConsoleReferenceClear]</span></span>  

## <span data-ttu-id="726a6-117">счет</span><span class="sxs-lookup"><span data-stu-id="726a6-117">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="726a6-118">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-118">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="726a6-119">Записывает количество вызовов метода [Count](#count) в той же строке и с тем же `label` .</span><span class="sxs-lookup"><span data-stu-id="726a6-119">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="726a6-120">Для сброса счетчика используйте метод [countReset](#countreset) .</span><span class="sxs-lookup"><span data-stu-id="726a6-120">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

> ##### <span data-ttu-id="726a6-121">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="726a6-121">Figure 2</span></span>  
> <span data-ttu-id="726a6-122">Результат `console.count()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-122">The result of the `console.count()` example</span></span>  
> ![Результат примера Console. Count ()][ImageCount]  

## <span data-ttu-id="726a6-124">countReset</span><span class="sxs-lookup"><span data-stu-id="726a6-124">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="726a6-125">Сбрасывает число.</span><span class="sxs-lookup"><span data-stu-id="726a6-125">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

## <span data-ttu-id="726a6-126">отладка</span><span class="sxs-lookup"><span data-stu-id="726a6-126">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="726a6-127">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-127">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="726a6-128">Идентичен методу [log](#log) .</span><span class="sxs-lookup"><span data-stu-id="726a6-128">Identical to the [log](#log) method.</span></span>  

```javascript
console.debug('debug');  
```  

> ##### <span data-ttu-id="726a6-129">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="726a6-129">Figure 3</span></span>  
> <span data-ttu-id="726a6-130">Результат `console.debug()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-130">The result of the `console.debug()` example</span></span>  
> ![Результат примера Console. Debug ()][ImageDebug]  

## <span data-ttu-id="726a6-132">dir</span><span class="sxs-lookup"><span data-stu-id="726a6-132">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="726a6-133">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-133">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="726a6-134">Печатает представление JSON указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="726a6-134">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

> ##### <span data-ttu-id="726a6-135">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="726a6-135">Figure 4</span></span>  
> <span data-ttu-id="726a6-136">Результат `console.dir()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-136">The result of the `console.dir()` example</span></span>  
> ![Результат примера Console. dir ()][ImageDir]  

## <span data-ttu-id="726a6-138">dirxml</span><span class="sxs-lookup"><span data-stu-id="726a6-138">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="726a6-139">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-139">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="726a6-140">Печатает XML-представление потомков `node` .</span><span class="sxs-lookup"><span data-stu-id="726a6-140">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

> ##### <span data-ttu-id="726a6-141">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="726a6-141">Figure 5</span></span>  
> <span data-ttu-id="726a6-142">Результат `console.dirxml()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-142">The result of the `console.dirxml()` example</span></span>  
> ![Результат примера Console. DirXML ()][ImageDirXml]  

## <span data-ttu-id="726a6-144">ошибка</span><span class="sxs-lookup"><span data-stu-id="726a6-144">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="726a6-145">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-145">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="726a6-146">Выводит на `object` консоль сообщение об ошибке, форматирует его как ошибку и включает трассировку стека.</span><span class="sxs-lookup"><span data-stu-id="726a6-146">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

> ##### <span data-ttu-id="726a6-147">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="726a6-147">Figure 6</span></span>  
> <span data-ttu-id="726a6-148">Результат `console.error()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-148">The result of the `console.error()` example</span></span>  
> ![Результат примера Console. Error ()][ImageError]  

## <span data-ttu-id="726a6-150">группа</span><span class="sxs-lookup"><span data-stu-id="726a6-150">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="726a6-151">Визуально группирует сообщения, пока не будет использован метод [groupEnd](#groupend) .</span><span class="sxs-lookup"><span data-stu-id="726a6-151">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="726a6-152">Используйте метод [groupCollapsed](#groupcollapsed) , чтобы свернуть группу при первом входе в систему на консоли.</span><span class="sxs-lookup"><span data-stu-id="726a6-152">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

> ##### <span data-ttu-id="726a6-153">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="726a6-153">Figure 7</span></span>  
> <span data-ttu-id="726a6-154">Результат `console.group()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-154">The result of the `console.group()` example</span></span>  
> ![Результат примера Console. Group ()][ImageGroup]  

## <span data-ttu-id="726a6-156">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="726a6-156">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="726a6-157">То же, что и в методе [log](#log) , за исключением того, что группа изначально свернута при входе в систему на консоли.</span><span class="sxs-lookup"><span data-stu-id="726a6-157">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

## <span data-ttu-id="726a6-158">groupEnd</span><span class="sxs-lookup"><span data-stu-id="726a6-158">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="726a6-159">Прекращение визуальной группировки сообщений.</span><span class="sxs-lookup"><span data-stu-id="726a6-159">Stops visually grouping messages.</span></span>  <span data-ttu-id="726a6-160">Просмотрите метод [группировки](#group) .</span><span class="sxs-lookup"><span data-stu-id="726a6-160">See the [group](#group) method.</span></span>  

## <span data-ttu-id="726a6-161">"Сведения"</span><span class="sxs-lookup"><span data-stu-id="726a6-161">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="726a6-162">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-162">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="726a6-163">Идентичен методу [log](#log) .</span><span class="sxs-lookup"><span data-stu-id="726a6-163">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

> ##### <span data-ttu-id="726a6-164">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="726a6-164">Figure 8</span></span>  
> <span data-ttu-id="726a6-165">Результат `console.info()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-165">The result of the `console.info()` example</span></span>  
> ![Результат примера console.info ()][ImageInfo]  

## <span data-ttu-id="726a6-167">выходе</span><span class="sxs-lookup"><span data-stu-id="726a6-167">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="726a6-168">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-168">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="726a6-169">Вывод на консоль сообщения.</span><span class="sxs-lookup"><span data-stu-id="726a6-169">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

> ##### <span data-ttu-id="726a6-170">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="726a6-170">Figure 9</span></span>  
> <span data-ttu-id="726a6-171">Результат `console.log()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-171">The result of the `console.log()` example</span></span>  
> ![Результат примера Console. log ()][ImageLog]  

## <span data-ttu-id="726a6-173">таблич</span><span class="sxs-lookup"><span data-stu-id="726a6-173">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="726a6-174">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-174">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="726a6-175">Заносит в журнал массив объектов в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="726a6-175">Logs an array of objects as a table.</span></span>  

```javascript
console.table([
    {
        first: 'René',
        last: 'Magritte',
    },
    {
        first: 'Chaim',
        last: 'Soutine',
        birthday: '18930113',
    },
    {
        first: 'Henri',
        last: 'Matisse',
    }
]);
```  

> ##### <span data-ttu-id="726a6-176">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="726a6-176">Figure 10</span></span>  
> <span data-ttu-id="726a6-177">Результат `console.table()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-177">The result of the `console.table()` example</span></span>  
> ![Пример использования Console. Table ()][ImageTable]  

## <span data-ttu-id="726a6-179">time</span><span class="sxs-lookup"><span data-stu-id="726a6-179">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="726a6-180">Запуск нового таймера.</span><span class="sxs-lookup"><span data-stu-id="726a6-180">Starts a new timer.</span></span>  <span data-ttu-id="726a6-181">Используйте метод [timeEnd](#timeend) , чтобы остановить таймер и напечатать время, затраченное на консоль.</span><span class="sxs-lookup"><span data-stu-id="726a6-181">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

> ##### <span data-ttu-id="726a6-182">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="726a6-182">Figure 11</span></span>  
> <span data-ttu-id="726a6-183">Результат `console.time()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-183">The result of the `console.time()` example</span></span>  
> ![Результат примера Console. Time ()][ImageTime]  

## <span data-ttu-id="726a6-185">timeEnd</span><span class="sxs-lookup"><span data-stu-id="726a6-185">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="726a6-186">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-186">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="726a6-187">Останавливает таймер.</span><span class="sxs-lookup"><span data-stu-id="726a6-187">Stops a timer.</span></span>  <span data-ttu-id="726a6-188">Просмотрите метод [time (время](#time) ).</span><span class="sxs-lookup"><span data-stu-id="726a6-188">See the [time](#time) method.</span></span>  

## <span data-ttu-id="726a6-189">событий</span><span class="sxs-lookup"><span data-stu-id="726a6-189">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="726a6-190">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-190">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="726a6-191">Выводит на консоль трассировку стека.</span><span class="sxs-lookup"><span data-stu-id="726a6-191">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

> ##### <span data-ttu-id="726a6-192">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="726a6-192">Figure 12</span></span>  
> <span data-ttu-id="726a6-193">Результат `console.trace()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-193">The result of the `console.trace()` example</span></span>  
> ![Результат примера Console. Trace ()][ImageTrace]  

## <span data-ttu-id="726a6-195">оповещает</span><span class="sxs-lookup"><span data-stu-id="726a6-195">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="726a6-196">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="726a6-196">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="726a6-197">Вывод на консоль предупреждения.</span><span class="sxs-lookup"><span data-stu-id="726a6-197">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

> ##### <span data-ttu-id="726a6-198">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="726a6-198">Figure 13</span></span>  
> <span data-ttu-id="726a6-199">Результат `console.warn()` примера</span><span class="sxs-lookup"><span data-stu-id="726a6-199">The result of the `console.warn()` example</span></span>  
> ![Результат примера Console. warn ()][ImageWarn]  

   

  

<!-- image links -->  

[ImageAssert]: /microsoft-edge/devtools-guide-chromium/media/console-demo-assert-button.msft.png "Рисунок 1: результат примера Console. Assert ()"  
[ImageCount]: /microsoft-edge/devtools-guide-chromium/media/console-demo-count-button.msft.png "Рисунок 2: результат примера Console. Count ()"  
[ImageDebug]: /microsoft-edge/devtools-guide-chromium/media/console-demo-debug-button.msft.png "Рисунок 3: результат примера Console. Debug ()"  
[ImageDir]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dir-button.msft.png "Рисунок 4: результат примера Console. dir ()"  
[ImageDirXml]: /microsoft-edge/devtools-guide-chromium/media/console-demo-dirxml-button.msft.png "Рисунок 5: результат примера Console. DirXML ()"  
[ImageError]: /microsoft-edge/devtools-guide-chromium/media/console-demo-error-button.msft.png "Рисунок 6: результат примера Console. Error ()"  
[ImageGroup]: /microsoft-edge/devtools-guide-chromium/media/console-demo-group-button.msft.png "Рисунок 7: результат примера Console. Group ()"  
[ImageInfo]: /microsoft-edge/devtools-guide-chromium/media/console-demo-info-button.msft.png "Рисунок 8: результат примера console.info ()"  
[ImageLog]: /microsoft-edge/devtools-guide-chromium/media/console-demo-log-button.msft.png "Рисунок 9: результат примера Console. log ()"  
[ImageTable]: /microsoft-edge/devtools-guide-chromium/media/console-demo-table-button.msft.png "Рисунок 10: результат примера Console. Table ()"  
[ImageTime]: /microsoft-edge/devtools-guide-chromium/media/console-demo-time-button.msft.png "Рисунок 11: результат примера Console. Time ()"  
[ImageTrace]: /microsoft-edge/devtools-guide-chromium/media/console-demo-trace-button.msft.png "Рисунок 12: результат примера Console. Trace ()"  
[ImageWarn]: /microsoft-edge/devtools-guide-chromium/media/console-demo-warn-button.msft.png "Рисунок 13: результат примера Console. warn ()"  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с сообщениями журнала на консоли"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Справочник по API для консольных программ"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Удаление ссылки на консоль консоли"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Сохранение сообщений на странице с загрузкой на консоли"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Фильтрация по уровню журнала — Справочник по консоли"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

> [!NOTE]
> <span data-ttu-id="726a6-220">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="726a6-220">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="726a6-221">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/api) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="726a6-221">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="726a6-223">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="726a6-223">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
