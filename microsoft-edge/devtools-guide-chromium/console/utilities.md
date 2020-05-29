---
title: Справочник по API для консольных программ
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 28b40f3f79928725d3d49418e01cf02247224370
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601798"
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





# <span data-ttu-id="5d0e6-103">Справочник по API для консольных программ</span><span class="sxs-lookup"><span data-stu-id="5d0e6-103">Console Utilities API Reference</span></span>   



<span data-ttu-id="5d0e6-104">API консоли содержат набор удобных команд для выполнения распространенных задач: выбор и анализ элементов DOM, отображение данных в удобочитаемом формате, остановка и запуск профилировщика, а также наблюдение за событиями DOM.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-104">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="5d0e6-105">Следующие команды работают только на консоли Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-105">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="5d0e6-106">Команды не работают при запуске из ваших сценариев.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-106">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="5d0e6-107">Ищете `console.log()` `console.error()` и другие `console.*` методы?</span><span class="sxs-lookup"><span data-stu-id="5d0e6-107">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="5d0e6-108">См.: [Справочник по API для консольных интерфейсов][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="5d0e6-108">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="5d0e6-109">Последнее вычисленное выражение</span><span class="sxs-lookup"><span data-stu-id="5d0e6-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="5d0e6-110">Возвращает значение последнего вычисленного выражения.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="5d0e6-111">На [рисунке 1](#figure-1)вычисляется простое выражение \ ( `2 + 2` \).</span><span class="sxs-lookup"><span data-stu-id="5d0e6-111">In [Figure 1](#figure-1), a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="5d0e6-112">`$_`Затем вычисляется свойство, которое содержит одно и то же значение.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

> ##### <span data-ttu-id="5d0e6-113">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="5d0e6-113">Figure 1</span></span>  
> `$_` <span data-ttu-id="5d0e6-114">— Это последнее вычисленное выражение</span><span class="sxs-lookup"><span data-stu-id="5d0e6-114">is the most recently evaluated expression</span></span>  
> ![$ _ — это последнее вычисленное выражение][ImageRecentExpression]  

<span data-ttu-id="5d0e6-116">На [рисунке 2](#figure-2)вычисленное выражение изначально включает массив имен.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-116">In [Figure 2](#figure-2), the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="5d0e6-117">Вычисление `$_.length` для определения длины массива, значение, хранящееся в `$_` изменениях, становится последним вычисленным выражением `4` .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-117">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

> ##### <span data-ttu-id="5d0e6-118">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="5d0e6-118">Figure 2</span></span>  
> `$_` <span data-ttu-id="5d0e6-119">изменения при вычислении новых команд</span><span class="sxs-lookup"><span data-stu-id="5d0e6-119">changes when new commands are evaluated</span></span>  
> ![$ _ изменения при вычислении новых команд][ImageChangedRecentExpression]  

## <span data-ttu-id="5d0e6-121">Недавно выбранный элемент или объект JavaScript</span><span class="sxs-lookup"><span data-stu-id="5d0e6-121">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="5d0e6-122">Возвращает последний выбранный элемент или объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-122">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="5d0e6-123">Возвращает второй, последний выбранный элемент и т. д.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-123">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="5d0e6-124">Команды,,, и, Кроме того, `$0` `$1` работают в `$2` `$3` `$4` виде исторических ссылок на последние пять элементов DOM, проверенных на панели **элементов** , или последние пять объектов кучи JavaScript, выбранных на панели " **память** ".</span><span class="sxs-lookup"><span data-stu-id="5d0e6-124">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

```console
$1
```  

```console
$2
```  

```console
$3
```  

```console
$4
```  

<span data-ttu-id="5d0e6-125">На [рисунке 3](#figure-3) `img` выделен элемент на панели **элементы** .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-125">In [Figure 3](#figure-3), an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="5d0e6-126">В ящике **консоли** `$0` вычисляется и отображается один и тот же элемент.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-126">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

> ##### <span data-ttu-id="5d0e6-127">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="5d0e6-127">Figure 3</span></span>  
> <span data-ttu-id="5d0e6-128">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d0e6-128">The</span></span> `$0`  
> ![$0][ImageElement0]  

<span data-ttu-id="5d0e6-130">На [рисунке 4](#figure-4)показан другой элемент, выбранный на той же странице.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-130">In [Figure 4](#figure-4), the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="5d0e6-131">`$0`Теперь он ссылается на только что выбранный элемент, то `$1` есть возвращает ранее выбранное.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-131">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

> ##### <span data-ttu-id="5d0e6-132">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="5d0e6-132">Figure 4</span></span>  
> <span data-ttu-id="5d0e6-133">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d0e6-133">The</span></span> `$1`  
> ![$1][ImageElement1]  

## <span data-ttu-id="5d0e6-135">Область выбора запроса</span><span class="sxs-lookup"><span data-stu-id="5d0e6-135">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="5d0e6-136">Возвращает ссылку на первый элемент DOM с указанным селектором CSS.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-136">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="5d0e6-137">Этот метод является псевдонимом метода [Document. querySelector ()][MDNDocumentQuerySelector] .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-137">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="5d0e6-138">На [рисунке 5](#figure-5)возвращается ссылка на первый `<img>` элемент в документе.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-138">In [Figure 5](#figure-5), a reference to the first `<img>` element in the document is returned.</span></span>  

> ##### <span data-ttu-id="5d0e6-139">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="5d0e6-139">Figure 5</span></span>  
> <span data-ttu-id="5d0e6-140">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d0e6-140">The</span></span> `$('img')`  
> ![$ ("Img")][ImageElementImg]  

<span data-ttu-id="5d0e6-142">Щелкните возвращенный результат правой кнопкой мыши и выберите пункт **Показать на панели элементов** , чтобы найти его в DOM, или **прокрутите** страницу, чтобы отобразить ее на странице.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-142">Right-click on the returned result and select **Reveal in Elements Panel** to find it in the DOM, or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="5d0e6-143">На [рисунке 6](#figure-6)возвращается ссылка на текущий выбранный элемент, и отображается свойство src.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-143">In [Figure 6](#figure-6), a reference to the currently selected element is returned and the src property is displayed.</span></span>  

> ##### <span data-ttu-id="5d0e6-144">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="5d0e6-144">Figure 6</span></span>  
> <span data-ttu-id="5d0e6-145">Параметр</span><span class="sxs-lookup"><span data-stu-id="5d0e6-145">The</span></span> `$('img').src`  
> ![$ ("Img"). src][ImageElementImgSource]  

<span data-ttu-id="5d0e6-147">Этот метод также поддерживает второй параметр, startNode, задающий "элемент" или узел, из которого следует искать элементы.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-147">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="5d0e6-148">Значение этого параметра по умолчанию — `document` .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-148">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="5d0e6-149">На [рисунке 7](#figure-7)первый `img` элемент найден после элемента `title--image` и отображается `src` правильно.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-149">In [Figure 7](#figure-7), the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

> ##### <span data-ttu-id="5d0e6-150">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="5d0e6-150">Figure 7</span></span>  
> <span data-ttu-id="5d0e6-151">$ ("Img", Document. querySelector ("Title--Image")). src</span><span class="sxs-lookup"><span data-stu-id="5d0e6-151">The $('img', document.querySelector('title--image')).src</span></span>  
> ![$ ("Img", Document. querySelector ("Title--Image")). src][ImageElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="5d0e6-153">Если вы используете библиотеку, например jQuery, которая используется `$` , эта функция перезаписывается и `$` соответствует реализации из этой библиотеки.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-153">If you are using a library such as jQuery that uses `$`, this functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="5d0e6-154">Выбор запроса</span><span class="sxs-lookup"><span data-stu-id="5d0e6-154">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="5d0e6-155">Возвращает массив элементов, которые соответствуют указанному селектору CSS.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-155">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="5d0e6-156">Этот метод эквивалентен вызову метода [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-156">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="5d0e6-157">На [рисунке 8](#figure-8)используйте `$$()` для создания массива всех `<img>` элементов в текущем документе и отображения значения `src` свойства для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-157">In [Figure 8](#figure-8), use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="5d0e6-158">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="5d0e6-158">Figure 8</span></span>  
> <span data-ttu-id="5d0e6-159">Использование `$$()` для выбора всех изображений в документе и отображения источников</span><span class="sxs-lookup"><span data-stu-id="5d0e6-159">Using `$$()` to select all images in the document and display the sources</span></span>  
> ![Использование $ $ () для выбора всех изображений в документе и отображения источников][ImageArrayElementImgSource]  

<span data-ttu-id="5d0e6-161">Этот метод также поддерживает второй параметр, startNode, указывающий элемент или узел, из которого нужно выполнить поиск элементов.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-161">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="5d0e6-162">Значение этого параметра по умолчанию — `document` .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-162">The default value of this parameter is `document`.</span></span>  

<span data-ttu-id="5d0e6-163">На [рисунке 9](#figure-9)измененная версия [рисунка 8](#figure-8) используется `$$()` для создания массива всех `<img>` элементов, которые отображаются в текущем документе после выбранного узла.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-163">In [Figure 9](#figure-9), a modified version of [Figure 8](#figure-8) uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### <span data-ttu-id="5d0e6-164">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="5d0e6-164">Figure 9</span></span>  
> <span data-ttu-id="5d0e6-165">Использование `$$()` для выбора всех изображений, которые отображаются после указанного `<div>` элемента в документе, и отображения источников</span><span class="sxs-lookup"><span data-stu-id="5d0e6-165">Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
> ![Использование $ $ () для выбора всех изображений, которые отображаются после указанного <div> элемента в документе и отображения источников][ImageArrayElementImgNodeSource]  

> [!NOTE]
> <span data-ttu-id="5d0e6-167">Нажмите клавишу `Shift` + `Enter` консоль, чтобы начать новую строку, не выполняя сценарий.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-167">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="5d0e6-168">Выражения</span><span class="sxs-lookup"><span data-stu-id="5d0e6-168">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="5d0e6-169">Возвращает массив элементов DOM, соответствующих указанному выражению XPath.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-169">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="5d0e6-170">На [рис. 10](#figure-10) `<p>` возвращаются все элементы на странице.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-170">In [Figure 10](#figure-10), all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

> ##### <span data-ttu-id="5d0e6-171">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="5d0e6-171">Figure 10</span></span>  
> <span data-ttu-id="5d0e6-172">Использование селектора XPath</span><span class="sxs-lookup"><span data-stu-id="5d0e6-172">Using an XPath selector</span></span>  
> ![Использование селектора XPath][ImageArrayXpath]  

<span data-ttu-id="5d0e6-174">На [рисунке 11](#figure-11) `<p>` возвращаются все элементы, содержащие `<a>` элементы.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-174">In [Figure 11](#figure-11), all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

> ##### <span data-ttu-id="5d0e6-175">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="5d0e6-175">Figure 11</span></span>  
> <span data-ttu-id="5d0e6-176">Использование более сложного селектора XPath</span><span class="sxs-lookup"><span data-stu-id="5d0e6-176">Using a more complicated XPath selector</span></span>  
> ![Использование более сложного селектора XPath][ImageArrayXpathChild]  

<span data-ttu-id="5d0e6-178">Как и другие команды Selector, `$x(path)` имеет дополнительный второй параметр, `startNode` указывающий на элемент или узел, из которого нужно выполнить поиск элементов.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-178">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

> ##### <span data-ttu-id="5d0e6-179">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="5d0e6-179">Figure 12</span></span>  
> <span data-ttu-id="5d0e6-180">Использование селектора XPath с</span><span class="sxs-lookup"><span data-stu-id="5d0e6-180">Using an XPath selector with</span></span> `startNode`  
> ![Использование селектора XPath с startNode][ImageArrayXpathNode]  

## <span data-ttu-id="5d0e6-182">Сброс</span><span class="sxs-lookup"><span data-stu-id="5d0e6-182">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="5d0e6-183">Очищает консоль журнала.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-183">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="5d0e6-184">copy</span><span class="sxs-lookup"><span data-stu-id="5d0e6-184">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="5d0e6-185">`copy(object)`Метод копирует строковое представление указанного объекта в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-185">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="5d0e6-186">отладка</span><span class="sxs-lookup"><span data-stu-id="5d0e6-186">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="5d0e6-187">[#1050237 проблема с Chromium][MonorailIssue1050237] отслеживает ошибку с `debug()` функцией.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-187">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="5d0e6-188">Если вы столкнулись с этой проблемой, попробуйте использовать вместо нее [точки останова][DevtoolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-188">If you encounter this issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="5d0e6-189">Когда вы запрашиваете указанный метод, отладчик вызывается и останавливается внутри метода на панели « **источники** », что позволяет пошагово пройти этот код и выполнить его отладку.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-189">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

> ##### <span data-ttu-id="5d0e6-190">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="5d0e6-190">Figure 13</span></span>  
> <span data-ttu-id="5d0e6-191">Прерывание внутри метода с</span><span class="sxs-lookup"><span data-stu-id="5d0e6-191">Breaking inside a method with</span></span> `debug()`  
> ![Прерывание в методе с помощью Debug ()][ImageDebugMethod]  

<span data-ttu-id="5d0e6-193">Используйте `undebug(method)` для прекращения прерывания на методе или с помощью пользовательского интерфейса, чтобы отключить все точки останова.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-193">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="5d0e6-194">Дополнительные сведения о точках останова можно найти в разделе [приостановка кода с точки останова][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="5d0e6-194">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="5d0e6-195">dir</span><span class="sxs-lookup"><span data-stu-id="5d0e6-195">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="5d0e6-196">Отображает список всех свойств указанного объекта в стиле объекта.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-196">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="5d0e6-197">Этот метод является псевдонимом для метода [Console. dir ()][MDNConsoleDir] .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-197">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="5d0e6-198">Вычислите `document.head` текст на консоли, чтобы отобразить HTML `<head>` между `</head>` тегами и.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-198">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="5d0e6-199">На [рисунке 14](#figure-14)после использования на консоли отображается вхождение стиля объекта `console.dir()` .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-199">In [Figure 14](#figure-14), an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

> ##### <span data-ttu-id="5d0e6-200">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="5d0e6-200">Figure 14</span></span>  
> <span data-ttu-id="5d0e6-201">Ведение журнала `document.head` с помощью `dir()` метода</span><span class="sxs-lookup"><span data-stu-id="5d0e6-201">Logging `document.head` with `dir()` method</span></span>  
> ![Ведение журнала. Head с помощью метода dir ()][ImageLogObject]  

<span data-ttu-id="5d0e6-203">Дополнительные сведения можно найти в описании [`console.dir()`][DevToolsConsoleApiConsoleDirObject] записи в API-интерфейсе консоли.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-203">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="5d0e6-204">dirxml</span><span class="sxs-lookup"><span data-stu-id="5d0e6-204">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="5d0e6-205">Печатает XML-представление указанного объекта, как показано на вкладке **элементы** .  Этот метод эквивалентен методу [Console. DirXML ()][MDNConsoleDirxml] .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-205">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="5d0e6-206">Проверка</span><span class="sxs-lookup"><span data-stu-id="5d0e6-206">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="5d0e6-207">Открывает и выбирает определенный элемент или объект на соответствующей панели: либо панель **элементов** для элементов DOM, либо панель **памяти** для объектов кучи JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-207">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="5d0e6-208">На [рис. 15](#figure-15) `document.body` откроется панель **элементы** .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-208">In [Figure 15](#figure-15), the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

> ##### <span data-ttu-id="5d0e6-209">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="5d0e6-209">Figure 15</span></span>  
> <span data-ttu-id="5d0e6-210">Проверка элемента с помощью</span><span class="sxs-lookup"><span data-stu-id="5d0e6-210">Inspecting an element with</span></span> `inspect()`  
> ![Проверка элемента с помощью проверки ()][ImageInspectElement]  

<span data-ttu-id="5d0e6-212">При передаче метода для проверки метод открывает документ, находящийся на панели « **источники** », для проверки.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-212">When passing a method to inspect, the method opens the document up in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="5d0e6-213">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="5d0e6-213">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="5d0e6-214">Возвращает прослушиватели событий, зарегистрированные для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-214">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="5d0e6-215">Возвращаемое значение — это объект, который содержит массив для всех зарегистрированных типов событий \ (например, `click` или `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="5d0e6-215">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="5d0e6-216">Каждый из этих массивов — это объекты, которые описывают прослушиватель, зарегистрированный для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-216">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="5d0e6-217">На [рисунке 16](#figure-16)перечислены все прослушиватели событий, зарегистрированные на объекте Document.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-217">In [Figure 16](#figure-16), all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

> ##### <span data-ttu-id="5d0e6-218">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="5d0e6-218">Figure 16</span></span>  
> <span data-ttu-id="5d0e6-219">Вывод на печать</span><span class="sxs-lookup"><span data-stu-id="5d0e6-219">Output of using</span></span> `getEventListeners(document)`  
> ![Вывод на печать с использованием getEventListeners (документ)][ImageGetListeners]  

<span data-ttu-id="5d0e6-221">Если в указанном объекте зарегистрировано более одного прослушивателя, то массив содержит элемент для каждого прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-221">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="5d0e6-222">На [рисунке 16](#figure-16)в элементе Document для события зарегистрированы два прослушивателя событий `click` .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-222">In [Figure 16](#figure-16), there are two event listeners registered on the document element for the `click` event.</span></span>  

> ##### <span data-ttu-id="5d0e6-223">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="5d0e6-223">Figure 17</span></span>  
> <span data-ttu-id="5d0e6-224">Несколько прослушивателей</span><span class="sxs-lookup"><span data-stu-id="5d0e6-224">Multiple listeners</span></span>  
> ![Несколько прослушивателей][ImageMultipleListeners]  

<span data-ttu-id="5d0e6-226">Вы можете расширить каждый из указанных ниже объектов, чтобы просмотреть свойства.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-226">You may further expand each of the following objects to explore the properties.</span></span>  

> ##### <span data-ttu-id="5d0e6-227">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="5d0e6-227">Figure 18</span></span>  
> <span data-ttu-id="5d0e6-228">Развернутое представление объекта прослушивателя</span><span class="sxs-lookup"><span data-stu-id="5d0e6-228">Expanded view of listener object</span></span>  
> ![Развернутое представление объекта прослушивателя][ImageListenersExpanded]  

## <span data-ttu-id="5d0e6-230">клавиши</span><span class="sxs-lookup"><span data-stu-id="5d0e6-230">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="5d0e6-231">Возвращает массив, содержащий имена свойств, принадлежащих указанному объекту.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-231">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="5d0e6-232">Чтобы получить связанные значения одинаковых свойств, используйте `values()` .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-232">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="5d0e6-233">Например, предположим, что приложение определило следующий объект.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-233">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="5d0e6-234">На [рис. 19](#figure-19)результат `player1` определен в глобальном пространстве имен \ (для простоты) перед вводом `keys(player1)` и `values(player1)` на консоли.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-234">In [Figure 19](#figure-19), the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### <span data-ttu-id="5d0e6-235">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="5d0e6-235">Figure 19</span></span>  
> <span data-ttu-id="5d0e6-236">`keys()`Команды и `values()`</span><span class="sxs-lookup"><span data-stu-id="5d0e6-236">The `keys()` and `values()` commands</span></span>  
> ![Команды Keys () и Values ()][ImageConsoleKeysValues]  

## <span data-ttu-id="5d0e6-238">монитор</span><span class="sxs-lookup"><span data-stu-id="5d0e6-238">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="5d0e6-239">Заносит в консоль сообщение, которое указывает имя метода вместе с аргументами, передаваемыми методу при его вызове.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-239">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

> ##### <span data-ttu-id="5d0e6-240">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="5d0e6-240">Figure 20</span></span>  
> <span data-ttu-id="5d0e6-241">`monitor()`Метод</span><span class="sxs-lookup"><span data-stu-id="5d0e6-241">The `monitor()` method</span></span>  
> ![Метод Monitor ()][ImageConsoleMonitorSum]  

<span data-ttu-id="5d0e6-243">Используется `unmonitor(method)` для прекращения наблюдения.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-243">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="5d0e6-244">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="5d0e6-244">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="5d0e6-245">Когда в указанном объекте происходит одно из указанных событий, объект события регистрируется в консоли.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-245">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="5d0e6-246">Вы можете указать одно событие для отслеживания, массив событий или один из типов универсальных событий, сопоставленных с предопределенной коллекцией событий.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-246">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="5d0e6-247">Посмотрите [Рисунок 21](#figure-21).</span><span class="sxs-lookup"><span data-stu-id="5d0e6-247">See [Figure 21](#figure-21).</span></span>  

<span data-ttu-id="5d0e6-248">Ниже приведено наблюдение за всеми событиями изменения размера объекта Window.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-248">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

> ##### <span data-ttu-id="5d0e6-249">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="5d0e6-249">Figure 21</span></span>  
> <span data-ttu-id="5d0e6-250">Наблюдение за событиями изменения размера окна</span><span class="sxs-lookup"><span data-stu-id="5d0e6-250">Monitoring window resize events</span></span>  
> ![Наблюдение за событиями изменения размера окна][ImageMonitorResize]  

<span data-ttu-id="5d0e6-252">В следующем примере определяется массив для мониторинга обоих `resize` и `scroll` событий в объекте Window.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-252">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="5d0e6-253">Вы также можете указать один из доступных типов событий — строки, которые сопоставляются с предопределенными наборами событий.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-253">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="5d0e6-254">В приведенной ниже таблице показаны типы доступных событий и сопоставлений связанных событий.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-254">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="5d0e6-255">Тип события</span><span class="sxs-lookup"><span data-stu-id="5d0e6-255">Event type</span></span> | <span data-ttu-id="5d0e6-256">Соответствующие сопоставленные события</span><span class="sxs-lookup"><span data-stu-id="5d0e6-256">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="5d0e6-257">"Click", "DblClick", "MouseDown", "MouseMove", "указатель мыши", "onmouseover", "MouseUp", "MouseWheel"</span><span class="sxs-lookup"><span data-stu-id="5d0e6-257">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="5d0e6-258">"KeyDown", "нажатие клавиши", "KeyUp", "textInput"</span><span class="sxs-lookup"><span data-stu-id="5d0e6-258">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="5d0e6-259">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="5d0e6-259">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="5d0e6-260">"Размытие", "Изменить", "фокусировку", "прокрутка", "выделить", "Отправить", "выбрать", "Отправить", "с масштабом"</span><span class="sxs-lookup"><span data-stu-id="5d0e6-260">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="5d0e6-261">На [рисунке 22](#figure-22)на `key` `key` панели **элементы** выделены типы событий, соответствующие событиям текстового поля ввода.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-261">In [Figure 22](#figure-22), the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="5d0e6-262">На [рисунке 22](#figure-22) показан пример выходных данных после ввода символа в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-262">In [Figure 22](#figure-22) the sample output after typing a character in the text field is displayed.</span></span>  

> ##### <span data-ttu-id="5d0e6-263">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="5d0e6-263">Figure 22</span></span>  
> <span data-ttu-id="5d0e6-264">Контроль событий ключа</span><span class="sxs-lookup"><span data-stu-id="5d0e6-264">Monitoring key events</span></span>  
> ![Контроль событий ключа][ImageMonitorKey]  

## <span data-ttu-id="5d0e6-266">профиль</span><span class="sxs-lookup"><span data-stu-id="5d0e6-266">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="5d0e6-267">Запускает сеанс профилирования ЦП JavaScript с необязательным именем.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-267">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="5d0e6-268">Метод [profileEnd ()](#profileend) завершает профиль и отображает результаты на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-268">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="5d0e6-269">Запустите `profile()` метод, чтобы начать профилирование.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-269">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="5d0e6-270">Запустите метод [profileEnd ()](#profileend) , чтобы остановить профилирование и отобразить результаты на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-270">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="5d0e6-271">Профили также могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-271">Profiles may also be nested.</span></span>  <span data-ttu-id="5d0e6-272">На [рисунке 23](#figure-23) результат одинаков, независимо от того, где находится заказ.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-272">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="5d0e6-273">Несколько профилей ЦП могут работать одновременно, и вы не обязаны закрывать каждый из них в заказе на создание.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-273">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="5d0e6-274">profileEnd</span><span class="sxs-lookup"><span data-stu-id="5d0e6-274">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="5d0e6-275">Завершает сеанс профилирования ЦП JavaScript и отображает результаты на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-275">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="5d0e6-276">Необходимо запустить метод [Profile ()](#profile) .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-276">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="5d0e6-277">Запустите метод [Profile ()](#profile) , чтобы начать профилирование.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-277">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="5d0e6-278">Запустите `profileEnd()` метод, чтобы остановить профилирование и отобразить результаты на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-278">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="5d0e6-279">Профили также могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-279">Profiles may also be nested.</span></span>  <span data-ttu-id="5d0e6-280">На [рисунке 23](#figure-23) результат одинаков, независимо от того, где находится заказ.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-280">In [Figure 23](#figure-23) the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="5d0e6-281">Результат появится в виде снимка кучи на панели " **память** ".</span><span class="sxs-lookup"><span data-stu-id="5d0e6-281">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

> ##### <span data-ttu-id="5d0e6-282">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="5d0e6-282">Figure 23</span></span>  
> <span data-ttu-id="5d0e6-283">Сгруппированные профили</span><span class="sxs-lookup"><span data-stu-id="5d0e6-283">Grouped profiles</span></span>  
> ![Сгруппированные профили][ImageGroupedProfiles]  

> [!NOTE]
> <span data-ttu-id="5d0e6-285">Несколько профилей ЦП могут работать одновременно, и вы не обязаны закрывать каждый из них в заказе на создание.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-285">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="5d0e6-286">таблич</span><span class="sxs-lookup"><span data-stu-id="5d0e6-286">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="5d0e6-287">Заносит в журнал объектные данные с форматированием таблицы, основанным на объекте данных, с помощью необязательных заголовков столбцов.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-287">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="5d0e6-288">На [рисунке 24](#figure-24)показан список имен, использующих таблицу на консоли.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-288">In [Figure 24](#figure-24), a list of names using a table in the console is displayed.</span></span>  

```console
var names = {
    0:  {
        firstName:  "John",
        lastName:  "Smith"
    },
    1:  {
        firstName:  "Jane",
        lastName:  "Doe"
    }
};
table(names);
```  

> ##### <span data-ttu-id="5d0e6-289">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="5d0e6-289">Figure 24</span></span>  
> <span data-ttu-id="5d0e6-290">`table()`Метод</span><span class="sxs-lookup"><span data-stu-id="5d0e6-290">The `table()` method</span></span>  
> ![Метод Table ()][ImageConsoleTable]  

## <span data-ttu-id="5d0e6-292">Отладка</span><span class="sxs-lookup"><span data-stu-id="5d0e6-292">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="5d0e6-293">Прекращает отладку указанного метода, поэтому при вызове метода отладчик больше не вызывается.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-293">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="5d0e6-294">отследить</span><span class="sxs-lookup"><span data-stu-id="5d0e6-294">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="5d0e6-295">Останавливает мониторинг указанного метода.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-295">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="5d0e6-296">Используется совместно с методом [Monitor ()](#monitor) .</span><span class="sxs-lookup"><span data-stu-id="5d0e6-296">This is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="5d0e6-297">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="5d0e6-297">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="5d0e6-298">Прекращает наблюдение за событиями для указанного объекта и событий.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-298">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="5d0e6-299">Например, в приведенном ниже примере останавливается отслеживание всех событий в объекте Window.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-299">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="5d0e6-300">Вы также можете отключить наблюдение за определенными событиями для объекта.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-300">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="5d0e6-301">Например, следующий код начинает наблюдать за всеми `mouse` событиями выбранного в данный момент элемента, а затем останавливает наблюдение за `mousemove` событиями (возможно, чтобы уменьшить шум в выходных данных консоли \).</span><span class="sxs-lookup"><span data-stu-id="5d0e6-301">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="5d0e6-302">данные</span><span class="sxs-lookup"><span data-stu-id="5d0e6-302">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="5d0e6-303">Возвращает массив, содержащий значения всех свойств, принадлежащих указанному объекту.</span><span class="sxs-lookup"><span data-stu-id="5d0e6-303">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

<!--   -->  



<!-- image links -->  

[ImageRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-arithmatic.msft.png "Рисунок 1: $ _ — это последнее вычисленное выражение"  
[ImageChangedRecentExpression]: /microsoft-edge/devtools-guide-chromium/media/console-array-length.msft.png "Рисунок 2: $ _ изменения при вычислении новых команд"  
[ImageElement0]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$0.msft.png "Рис. 3: $0"  
[ImageElement1]: /microsoft-edge/devtools-guide-chromium/media/console-image-highlighted-$1.msft.png "Рисунок 4: $1"  
[ImageElementImg]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image.msft.png "Рисунок 5: $ ("img")"  
[ImageElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-source.msft.png "Рисунок 6: $ ("img"). src"  
[ImageElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-source.msft.png "Рисунок 7: $ ("img", Document. querySelector ("Title--Image")). src"  
[ImageArrayElementImgSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-all.msft.png "Рисунок 8: использование $ $ () для выбора всех изображений в документе и отображения источников"  
[ImageArrayElementImgNodeSource]: /microsoft-edge/devtools-guide-chromium/media/console-element-selector-image-filter-all.msft.png "На рисунке 9: использование $ $ () для выбора всех изображений, которые отображаются после указанного <div> элемента в документе и отображения источников"  
[ImageArrayXpath]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath.msft.png "Рисунок 10: использование селектора XPath"  
[ImageArrayXpathChild]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-sub-element.msft.png "Рисунок 11: использование более сложного селектора XPath"  
[ImageArrayXpathNode]: /microsoft-edge/devtools-guide-chromium/media/console-array-xpath-startnode.msft.png "Рисунок 12: использование селектора XPath с startNode"  
[ImageDebugMethod]: /microsoft-edge/devtools-guide-chromium/media/console-debug-text.msft.png "Рисунок 13: прерывание внутри метода с помощью Debug ()"  
[ImageLogObject]: /microsoft-edge/devtools-guide-chromium/media/console-dir-document-head-expanded.msft.png "Рисунок 14: ведение журнала "документ. тело" с помощью метода dir ()"  
[ImageInspectElement]: /microsoft-edge/devtools-guide-chromium/media/console-inspect-document-body.msft.png "Рис. 15: Проверка элемента с помощью проверки ()"  
[ImageGetListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document.msft.png "Рисунок 16: вывод на печать с использованием getEventListeners (документ)"  
[ImageMultipleListeners]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png "Рисунок 17: несколько прослушивателей"  
[ImageListenersExpanded]: /microsoft-edge/devtools-guide-chromium/media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png "Рисунок 18: развернутое представление объекта прослушивателя"  
[ImageConsoleKeysValues]: /microsoft-edge/devtools-guide-chromium/media/console-keys-values.msft.png "Рис. 19: команды Keys () и Values ()"  
[ImageConsoleMonitorSum]: /microsoft-edge/devtools-guide-chromium/media/console-function-monitor-sum.msft.png "Рисунок 20: метод Monitor ()"  
[ImageMonitorResize]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-resize-window.msft.png "Рисунок 21: наблюдение за событиями изменения размера окна"  
[ImageMonitorKey]: /microsoft-edge/devtools-guide-chromium/media/console-monitor-events-type-t-y.msft.png "Рис. 22: Отслеживание ключевых событий"  
[ImageGroupedProfiles]: /microsoft-edge/devtools-guide-chromium/media/console-memory-multiple-cpu-profiles.msft.png "Рисунок 23: сгруппированные профили"  
[ImageConsoleTable]: /microsoft-edge/devtools-guide-chromium/media/console-table-display.msft.png "Рисунок 24: метод Table ()"  

<!-- links -->  

[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Справочник по API консоли"  
[DevToolsConsoleApiConsoleDirObject]: /microsoft-edge/devtools-guide-chromium/console/api#dir "Справочник по API dir-Console"  
[DevToolsJavascriptBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints "Приостановка кода с точки останова в Microsoft Edge DevTools"  
[DevToolsRenderingToolsJSRuntime]: /microsoft-edge/devtools-guide-chromium/rendering-tools/js-runtime "Ускорение выполнения JavaScript"  

[MDNConsoleDir]: https://developer.mozilla.org/docs/Web/API/Console/dir "Console. dir () | MDN"  
[MDNConsoleDirxml]: https://developer.mozilla.org/docs/Web/API/Console/dirxml "Console. DirXML () | MDN"  
[MDNDocumentQuerySelector]: https://developer.mozilla.org/docs/Web/API/Document/querySelector "Document. querySelector () | MDN"  
[MDNDocumentQuerySelectorAll]: https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll "Document. querySelectorAll () | MDN"  

[MonorailIssue1050237]: https://bugs.chromium.org/p/chromium/issues/detail?id=1050237 "Ошибка 1050237: Отладка (функция) не работает | Monorail"  

> [!NOTE]
> <span data-ttu-id="5d0e6-337">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d0e6-337">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5d0e6-338">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/utilities) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5d0e6-338">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5d0e6-340">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5d0e6-340">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
