---
title: Справочник по API консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/09/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 19545759ede4252f2e7ba21329d482f4eb96f0c6
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708518"
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

# <span data-ttu-id="83e36-103">Справочник по API консоли</span><span class="sxs-lookup"><span data-stu-id="83e36-103">Console API Reference</span></span>  

<span data-ttu-id="83e36-104">Используйте методы API консоли для записи сообщений на консоль из JavaScript.</span><span class="sxs-lookup"><span data-stu-id="83e36-104">Use the Console API methods to write messages to the Console from your JavaScript.</span></span>  <span data-ttu-id="83e36-105">Чтобы ознакомиться с интерактивным введением в раздел, ознакомьтесь с разделом начало [работы с сообщениями журнала на консоли][DevtoolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="83e36-105">For an interactive introduction to the topic, see [Get Started With Logging Messages To The Console][DevtoolsConsoleLog].</span></span>  <span data-ttu-id="83e36-106">Удобные методы, такие как `debug()` или `monitorEvents()` доступные только в области **консоли** , приведены в [справочнике API для консольных утилит][DevtoolConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="83e36-106">For the convenience methods like `debug()` or `monitorEvents()` which are only available from the **Console** pane, see [Console Utilities API Reference][DevtoolConsoleUtilities].</span></span>  

---  

## <span data-ttu-id="83e36-107">затребованного</span><span class="sxs-lookup"><span data-stu-id="83e36-107">assert</span></span>  

```javascript
console.assert(expression, object)
```

<span data-ttu-id="83e36-108">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-108">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<!--todo: add reference level (reference#persist-messages-across-page-loads) when available -->  

<span data-ttu-id="83e36-109">При вычислении выводит на консоль [сообщение об ошибке](#error) `expression` `false` .</span><span class="sxs-lookup"><span data-stu-id="83e36-109">Writes an [error](#error) to the console when `expression` evaluates to `false`.</span></span>  

```javascript
const x = 5;
const y = 3;
const reason = 'x is expected to be less than y';
console.assert(x < y, {x, y, reason});
```  

:::image type="complex" source="../media/console-demo-assert-button.msft.png" alt-text="Результат примера Console. Assert ()" lightbox="../media/console-demo-assert-button.msft.png":::
   <span data-ttu-id="83e36-111">Рисунок 1: результат `console.assert()` примера</span><span class="sxs-lookup"><span data-stu-id="83e36-111">Figure 1:  The result of the `console.assert()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-112">Сброс</span><span class="sxs-lookup"><span data-stu-id="83e36-112">clear</span></span>  

```javascript
console.clear()
```

<span data-ttu-id="83e36-113">Очищает консоль.</span><span class="sxs-lookup"><span data-stu-id="83e36-113">Clears the console.</span></span>  

```javascript
console.clear();  
```  

<span data-ttu-id="83e36-114">Если включен [протокол Preserve][DevtoolsConsoleReferenceLevel] , метод [clear](#clear) отключен.</span><span class="sxs-lookup"><span data-stu-id="83e36-114">If [Preserve Log][DevtoolsConsoleReferenceLevel] is enabled, the [clear](#clear) method is disabled.</span></span>  

### <span data-ttu-id="83e36-115">См. также</span><span class="sxs-lookup"><span data-stu-id="83e36-115">See also</span></span>  

*   [<span data-ttu-id="83e36-116">Очистка консоли</span><span class="sxs-lookup"><span data-stu-id="83e36-116">Clear the Console</span></span>][DevtoolsConsoleReferenceClear]  

---  

## <span data-ttu-id="83e36-117">счет</span><span class="sxs-lookup"><span data-stu-id="83e36-117">count</span></span>  

```javascript
console.count([label])
```  

<span data-ttu-id="83e36-118">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-118">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="83e36-119">Записывает количество вызовов метода [Count](#count) в той же строке и с тем же `label` .</span><span class="sxs-lookup"><span data-stu-id="83e36-119">Writes the number of times that the [count](#count) method has been invoked at the same line and with the same `label`.</span></span>  <span data-ttu-id="83e36-120">Для сброса счетчика используйте метод [countReset](#countreset) .</span><span class="sxs-lookup"><span data-stu-id="83e36-120">Use the [countReset](#countreset) method to reset the count.</span></span>  

```javascript
console.count();
console.count('coffee');
console.count();
console.count();
```  

:::image type="complex" source="../media/console-demo-count-button.msft.png" alt-text="Результат примера Console. Count ()" lightbox="../media/console-demo-count-button.msft.png":::
   <span data-ttu-id="83e36-122">Рисунок 2: результат `console.count()` примера</span><span class="sxs-lookup"><span data-stu-id="83e36-122">Figure 2:  The result of the `console.count()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-123">countReset</span><span class="sxs-lookup"><span data-stu-id="83e36-123">countReset</span></span>  

```javascript
console.countReset([label])
```  

<span data-ttu-id="83e36-124">Сбрасывает число.</span><span class="sxs-lookup"><span data-stu-id="83e36-124">Resets a count.</span></span>  

```javascript
console.countReset();
console.countReset('coffee');
```  

---  

## <span data-ttu-id="83e36-125">отладка</span><span class="sxs-lookup"><span data-stu-id="83e36-125">debug</span></span>  

```javascript
console.debug(object [, object, ...])
```  

<span data-ttu-id="83e36-126">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-126">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Verbose`

<span data-ttu-id="83e36-127">Совпадает с [журналом](#log) , кроме разных уровней ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="83e36-127">Identical to [log](#log) except different log level.</span></span>  

```javascript
console.debug('debug');  
```  

:::image type="complex" source="../media/console-demo-debug-button.msft.png" alt-text="Результат примера Console. Debug ()" lightbox="../media/console-demo-debug-button.msft.png":::
   <span data-ttu-id="83e36-129">Рисунок 3: результат `console.debug()` примера</span><span class="sxs-lookup"><span data-stu-id="83e36-129">Figure 3:  The result of the `console.debug()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-130">dir</span><span class="sxs-lookup"><span data-stu-id="83e36-130">dir</span></span>  

```javascript
console.dir(object)
```  

<span data-ttu-id="83e36-131">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-131">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="83e36-132">Печатает представление JSON указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="83e36-132">Prints a JSON representation of the specified object.</span></span>  

```javascript
console.dir(document.head);
```  

:::image type="complex" source="../media/console-demo-dir-button.msft.png" alt-text="Результат примера Console. dir ()" lightbox="../media/console-demo-dir-button.msft.png":::
   <span data-ttu-id="83e36-134">Рисунок 4: результат `console.dir()` примера</span><span class="sxs-lookup"><span data-stu-id="83e36-134">Figure 4:  The result of the `console.dir()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-135">dirxml</span><span class="sxs-lookup"><span data-stu-id="83e36-135">dirxml</span></span>  

```javascript
console.dirxml(node)
```  

<span data-ttu-id="83e36-136">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-136">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="83e36-137">Печатает XML-представление потомков `node` .</span><span class="sxs-lookup"><span data-stu-id="83e36-137">Prints an XML representation of the descendants of `node`.</span></span>  

```javascript
console.dirxml(document);
```  

:::image type="complex" source="../media/console-demo-dirxml-button.msft.png" alt-text="Результат примера Console. DirXML ()" lightbox="../media/console-demo-dirxml-button.msft.png":::
   <span data-ttu-id="83e36-139">На рисунке 5 показан результат примера. `console.dirxml()`</span><span class="sxs-lookup"><span data-stu-id="83e36-139">Figure 5:  The result of the `console.dirxml()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-140">ошибка</span><span class="sxs-lookup"><span data-stu-id="83e36-140">error</span></span>  

```javascript
console.error(object [, object, ...])
```  

<span data-ttu-id="83e36-141">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-141">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Error`  

<span data-ttu-id="83e36-142">Выводит на `object` консоль сообщение об ошибке, форматирует его как ошибку и включает трассировку стека.</span><span class="sxs-lookup"><span data-stu-id="83e36-142">Prints the `object` to the Console, formats it as an error, and includes a stack trace.</span></span>  

```javascript
console.error("I'm sorry, Dave.  I'm afraid I can't do that.");
```  

:::image type="complex" source="../media/console-demo-error-button.msft.png" alt-text="Результат примера Console. Error ()" lightbox="../media/console-demo-error-button.msft.png":::
   <span data-ttu-id="83e36-144">Рисунок 6: результат `console.error()` примера</span><span class="sxs-lookup"><span data-stu-id="83e36-144">Figure 6:  The result of the `console.error()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-145">группа</span><span class="sxs-lookup"><span data-stu-id="83e36-145">group</span></span>  

```javascript
console.group(label)
```  

<span data-ttu-id="83e36-146">Визуально группирует сообщения, пока не будет использован метод [groupEnd](#groupend) .</span><span class="sxs-lookup"><span data-stu-id="83e36-146">Visually groups messages together until the [groupEnd](#groupend) method is used.</span></span>  <span data-ttu-id="83e36-147">Используйте метод [groupCollapsed](#groupcollapsed) , чтобы свернуть группу при первом входе в систему на консоли.</span><span class="sxs-lookup"><span data-stu-id="83e36-147">Use the [groupCollapsed](#groupcollapsed) method to collapse the group when it is initially logged to the Console.</span></span>  

```javascript
const label = 'Adolescent Irradiated Espionage Tortoises';
console.group(label);
console.info('Leo');
console.info('Mike');
console.info('Don');
console.info('Raph');
console.groupEnd(label);
```  

:::image type="complex" source="../media/console-demo-group-button.msft.png" alt-text="Результат примера Console. Group ()" lightbox="../media/console-demo-group-button.msft.png":::
   <span data-ttu-id="83e36-149">На рисунке 7 показан результат примера. `console.group()`</span><span class="sxs-lookup"><span data-stu-id="83e36-149">Figure 7:  The result of the `console.group()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-150">groupCollapsed</span><span class="sxs-lookup"><span data-stu-id="83e36-150">groupCollapsed</span></span>  

```javascript
console.groupCollapsed(label)
```  

<span data-ttu-id="83e36-151">То же, что и в методе [log](#log) , за исключением того, что группа изначально свернута при входе в систему на консоли.</span><span class="sxs-lookup"><span data-stu-id="83e36-151">Same as the [log](#log) method, except the group is initially collapsed when it is logged to the Console.</span></span>  

---  

## <span data-ttu-id="83e36-152">groupEnd</span><span class="sxs-lookup"><span data-stu-id="83e36-152">groupEnd</span></span>  

```javascript
console.groupEnd(label)
```  

<span data-ttu-id="83e36-153">Прекращение визуальной группировки сообщений.</span><span class="sxs-lookup"><span data-stu-id="83e36-153">Stops visually grouping messages.</span></span>  <span data-ttu-id="83e36-154">Просмотрите метод [группировки](#group) .</span><span class="sxs-lookup"><span data-stu-id="83e36-154">See the [group](#group) method.</span></span>  

---  

## <span data-ttu-id="83e36-155">"Сведения"</span><span class="sxs-lookup"><span data-stu-id="83e36-155">info</span></span>  

```javascript
console.info(object [, object, ...])
```  

<span data-ttu-id="83e36-156">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-156">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="83e36-157">Идентичен методу [log](#log) .</span><span class="sxs-lookup"><span data-stu-id="83e36-157">Identical to the [log](#log) method.</span></span>  

```javascript
console.info('info');
```  

:::image type="complex" source="../media/console-demo-info-button.msft.png" alt-text="Результат примера console.info ()" lightbox="../media/console-demo-info-button.msft.png":::
   <span data-ttu-id="83e36-159">Рисунок 8: результат `console.info()` примера</span><span class="sxs-lookup"><span data-stu-id="83e36-159">Figure 8:  The result of the `console.info()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-160">выходе</span><span class="sxs-lookup"><span data-stu-id="83e36-160">log</span></span>  

```javascript
console.log(object [, object, ...])
```  

<span data-ttu-id="83e36-161">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-161">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="83e36-162">Вывод на консоль сообщения.</span><span class="sxs-lookup"><span data-stu-id="83e36-162">Prints a message to the Console.</span></span>  

```javascript
console.log('log');
```  

:::image type="complex" source="../media/console-demo-log-button.msft.png" alt-text="Результат примера Console. log ()" lightbox="../media/console-demo-log-button.msft.png":::
   <span data-ttu-id="83e36-164">На рисунке 9 показан результат примера. `console.log()`</span><span class="sxs-lookup"><span data-stu-id="83e36-164">Figure 9:  The result of the `console.log()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-165">таблич</span><span class="sxs-lookup"><span data-stu-id="83e36-165">table</span></span>  

```javascript
console.table(array)
```  

<span data-ttu-id="83e36-166">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-166">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="83e36-167">Заносит в журнал массив объектов в виде таблицы.</span><span class="sxs-lookup"><span data-stu-id="83e36-167">Logs an array of objects as a table.</span></span>  

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

:::image type="complex" source="../media/console-demo-table-button.msft.png" alt-text="Пример использования Console. Table ()" lightbox="../media/console-demo-table-button.msft.png":::
   <span data-ttu-id="83e36-169">Рисунок 10: результат `console.table()` примера</span><span class="sxs-lookup"><span data-stu-id="83e36-169">Figure 10:  The result of the `console.table()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-170">time</span><span class="sxs-lookup"><span data-stu-id="83e36-170">time</span></span>  

```javascript
console.time([label])
```  

<span data-ttu-id="83e36-171">Запуск нового таймера.</span><span class="sxs-lookup"><span data-stu-id="83e36-171">Starts a new timer.</span></span>  <span data-ttu-id="83e36-172">Используйте метод [timeEnd](#timeend) , чтобы остановить таймер и напечатать время, затраченное на консоль.</span><span class="sxs-lookup"><span data-stu-id="83e36-172">Use the [timeEnd](#timeend) method to stop the timer and print the elapsed time to the Console.</span></span>  

```javascript
console.time();
for (var i = 0; i < 100000; i++) {
    let square = i ** 2;
}
console.timeEnd();
```  

:::image type="complex" source="../media/console-demo-time-button.msft.png" alt-text="Результат примера Console. Time ()" lightbox="../media/console-demo-time-button.msft.png":::
   <span data-ttu-id="83e36-174">На рисунке 11 показан результат примера. `console.time()`</span><span class="sxs-lookup"><span data-stu-id="83e36-174">Figure 11:  The result of the `console.time()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-175">timeEnd</span><span class="sxs-lookup"><span data-stu-id="83e36-175">timeEnd</span></span>  

```javascript
console.timeEnd([label])
```  

<span data-ttu-id="83e36-176">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-176">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="83e36-177">Останавливает таймер.</span><span class="sxs-lookup"><span data-stu-id="83e36-177">Stops a timer.</span></span>  <span data-ttu-id="83e36-178">Просмотрите метод [time (время](#time) ).</span><span class="sxs-lookup"><span data-stu-id="83e36-178">See the [time](#time) method.</span></span>  

---  

## <span data-ttu-id="83e36-179">событий</span><span class="sxs-lookup"><span data-stu-id="83e36-179">trace</span></span>  

```javascript
console.trace()
```  

<span data-ttu-id="83e36-180">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-180">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Info`  

<span data-ttu-id="83e36-181">Выводит на консоль трассировку стека.</span><span class="sxs-lookup"><span data-stu-id="83e36-181">Prints a stack trace to the Console.</span></span>  

```javascript
const first = () => { second(); };
const second = () => { third(); };
const third = () => { fourth(); };
const fourth = () => { console.trace(); };
first();
```  

:::image type="complex" source="../media/console-demo-trace-button.msft.png" alt-text="Результат примера Console. Trace ()" lightbox="../media/console-demo-trace-button.msft.png":::
   <span data-ttu-id="83e36-183">Рис. 12: результат `console.trace()` примера</span><span class="sxs-lookup"><span data-stu-id="83e36-183">Figure 12:  The result of the `console.trace()` example</span></span>  
:::image-end:::  

---  

## <span data-ttu-id="83e36-184">оповещает</span><span class="sxs-lookup"><span data-stu-id="83e36-184">warn</span></span>  

```javascript
console.warn(object [, object, ...])
```  

<span data-ttu-id="83e36-185">[Уровень журнала][DevtoolsConsoleReferencePersist]:</span><span class="sxs-lookup"><span data-stu-id="83e36-185">[Log level][DevtoolsConsoleReferencePersist]:</span></span> `Warning`  

<span data-ttu-id="83e36-186">Вывод на консоль предупреждения.</span><span class="sxs-lookup"><span data-stu-id="83e36-186">Prints a warning to the Console.</span></span>  

```javascript
console.warn('warn');
```  

:::image type="complex" source="../media/console-demo-warn-button.msft.png" alt-text="Результат примера Console. warn ()" lightbox="../media/console-demo-warn-button.msft.png":::
   <span data-ttu-id="83e36-188">Рисунок 13: результат `console.warn()` примера</span><span class="sxs-lookup"><span data-stu-id="83e36-188">Figure 13:  The result of the `console.warn()` example</span></span>  
:::image-end:::  

<!-- links -->  

[DevtoolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с сообщениями журнала на консоли"  
[DevtoolConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Справочник по API для консольных программ"  
[DevtoolsConsoleReferenceClear]: /microsoft-edge/devtools-guide-chromium/console/reference#clear-the-console "Удаление ссылки на консоль консоли"  
[DevtoolsConsoleReferencePersist]: /microsoft-edge/devtools-guide-chromium/console/reference#persist-messages-across-page-loads "Сохранение сообщений на странице с загрузкой на консоли"  
[DevtoolsConsoleReferenceLevel]: /microsoft-edge/devtools-guide-chromium/console/reference#filter-by-log-level "Фильтрация по уровню журнала — Справочник по консоли"  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

> [!NOTE]
> <span data-ttu-id="83e36-195">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83e36-195">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="83e36-196">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/api) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="83e36-196">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/api) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="83e36-198">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="83e36-198">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
