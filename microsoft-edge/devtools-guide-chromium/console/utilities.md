---
title: Справочник по API для консольных программ
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: efa03e02813d718514f73445bc0dceb3a1a83f39
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708878"
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

# <span data-ttu-id="48a06-103">Справочник по API для консольных программ</span><span class="sxs-lookup"><span data-stu-id="48a06-103">Console Utilities API Reference</span></span>  

<span data-ttu-id="48a06-104">API консоли содержат набор удобных команд для выполнения распространенных задач: выбор и анализ элементов DOM, отображение данных в удобочитаемом формате, остановка и запуск профилировщика, а также наблюдение за событиями DOM.</span><span class="sxs-lookup"><span data-stu-id="48a06-104">The Console Utilities API contains a collection of convenience commands for performing common tasks:  selecting and inspecting DOM elements, displaying data in readable format, stopping and starting the profiler, and monitoring DOM events.</span></span>  

> [!WARNING]
> <span data-ttu-id="48a06-105">Следующие команды работают только на консоли Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="48a06-105">The following commands only work in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="48a06-106">Команды не работают при запуске из ваших сценариев.</span><span class="sxs-lookup"><span data-stu-id="48a06-106">The commands do not work if run from your scripts.</span></span>  

<span data-ttu-id="48a06-107">Ищете `console.log()` `console.error()` и другие `console.*` методы?</span><span class="sxs-lookup"><span data-stu-id="48a06-107">Looking for `console.log()`, `console.error()`, and the rest of the `console.*` methods?</span></span>  <span data-ttu-id="48a06-108">См.: [Справочник по API для консольных интерфейсов][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="48a06-108">See [Console API Reference][DevToolsConsoleApi].</span></span>  

## <span data-ttu-id="48a06-109">Последнее вычисленное выражение</span><span class="sxs-lookup"><span data-stu-id="48a06-109">Recently Evaluated Expression</span></span>  

```console
$_
```  

<span data-ttu-id="48a06-110">Возвращает значение последнего вычисленного выражения.</span><span class="sxs-lookup"><span data-stu-id="48a06-110">Returns the value of the most recently evaluated expression.</span></span>  

<span data-ttu-id="48a06-111">На приведенном ниже рисунке вычисляется простое выражение \ ( `2 + 2` \).</span><span class="sxs-lookup"><span data-stu-id="48a06-111">In the following figure, a simple expression \(`2 + 2`\) is evaluated.</span></span>  <span data-ttu-id="48a06-112">`$_`Затем вычисляется свойство, которое содержит одно и то же значение.</span><span class="sxs-lookup"><span data-stu-id="48a06-112">The `$_` property is then evaluated, which contains the same value.</span></span>  

:::image type="complex" source="../media/console-arithmatic.msft.png" alt-text="$ _ — это последнее вычисленное выражение" lightbox="../media/console-arithmatic.msft.png":::
   <span data-ttu-id="48a06-114">Рисунок 1: `$_` это последнее вычисленное выражение.</span><span class="sxs-lookup"><span data-stu-id="48a06-114">Figure 1:  `$_` is the most recently evaluated expression</span></span>  
:::image-end:::  

<span data-ttu-id="48a06-115">На приведенном ниже рисунке вычисленное выражение изначально включает массив имен.</span><span class="sxs-lookup"><span data-stu-id="48a06-115">In the following figure, the evaluated expression initially contains an array of names.</span></span>  <span data-ttu-id="48a06-116">Вычисление `$_.length` для определения длины массива, значение, хранящееся в `$_` изменениях, становится последним вычисленным выражением `4` .</span><span class="sxs-lookup"><span data-stu-id="48a06-116">Evaluating `$_.length` to find the length of the array, the value stored in `$_` changes to become the latest evaluated expression, `4`.</span></span>  

:::image type="complex" source="../media/console-array-length.msft.png" alt-text="$ _ изменения при вычислении новых команд" lightbox="../media/console-array-length.msft.png":::
   <span data-ttu-id="48a06-118">Рисунок 2: `$_` изменения при вычислении новых команд</span><span class="sxs-lookup"><span data-stu-id="48a06-118">Figure 2:  `$_` changes when new commands are evaluated</span></span>  
:::image-end:::  

## <span data-ttu-id="48a06-119">Недавно выбранный элемент или объект JavaScript</span><span class="sxs-lookup"><span data-stu-id="48a06-119">Recently Selected Element Or JavaScript Object</span></span>  

```console
$0
```  

<span data-ttu-id="48a06-120">Возвращает последний выбранный элемент или объект JavaScript.</span><span class="sxs-lookup"><span data-stu-id="48a06-120">Returns the most recently selected element or JavaScript object.</span></span>  `$1` <span data-ttu-id="48a06-121">Возвращает второй, последний выбранный элемент и т. д.</span><span class="sxs-lookup"><span data-stu-id="48a06-121">returns the second most recently selected one, and so on.</span></span>  <span data-ttu-id="48a06-122">Команды,,, и, Кроме того, `$0` `$1` работают в `$2` `$3` `$4` виде исторических ссылок на последние пять элементов DOM, проверенных на панели **элементов** , или последние пять объектов кучи JavaScript, выбранных на панели " **память** ".</span><span class="sxs-lookup"><span data-stu-id="48a06-122">The `$0`, `$1`, `$2`, `$3`, and `$4` commands work as a historical reference to the last five DOM elements inspected within the **Elements** panel or the last five JavaScript heap objects selected in the **Memory** panel.</span></span>  

:::row:::
   :::column span="1":::
      ```console
      $0
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $1
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $2
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      ```console
      $3
      ```  
   :::column-end:::
   :::column span="1":::
      ```console
      $4
      ```  
   :::column-end:::
   :::column span="1":::
   :::column-end:::
:::row-end:::  

<span data-ttu-id="48a06-123">На рисунке ниже показан элемент, `img` выбранный на панели **элементы** .</span><span class="sxs-lookup"><span data-stu-id="48a06-123">In the following figure, an `img` element is selected in the **Elements** panel.</span></span>  <span data-ttu-id="48a06-124">В ящике **консоли** `$0` вычисляется и отображается один и тот же элемент.</span><span class="sxs-lookup"><span data-stu-id="48a06-124">In the **Console** drawer, `$0` has been evaluated and displays the same element.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$0.msft.png" alt-text="$0" lightbox="../media/console-image-highlighted-$0.msft.png":::
   <span data-ttu-id="48a06-126">Рис. 3:</span><span class="sxs-lookup"><span data-stu-id="48a06-126">Figure 3:  The</span></span> `$0`  
:::image-end:::  

<span data-ttu-id="48a06-127">На приведенном ниже рисунке показано, как на изображении показан другой элемент, выбранный на той же странице.</span><span class="sxs-lookup"><span data-stu-id="48a06-127">In the following figure, the image shows a different element selected in the same page.</span></span>  <span data-ttu-id="48a06-128">`$0`Теперь он ссылается на только что выбранный элемент, то `$1` есть возвращает ранее выбранное.</span><span class="sxs-lookup"><span data-stu-id="48a06-128">The `$0` now refers to the newly selected element, while `$1` returns the previously selected one.</span></span>  

:::image type="complex" source="../media/console-image-highlighted-$1.msft.png" alt-text="$1" lightbox="../media/console-image-highlighted-$1.msft.png":::
   <span data-ttu-id="48a06-130">На рисунке 4:</span><span class="sxs-lookup"><span data-stu-id="48a06-130">Figure 4:  The</span></span> `$1`  
:::image-end:::  

## <span data-ttu-id="48a06-131">Область выбора запроса</span><span class="sxs-lookup"><span data-stu-id="48a06-131">Query Selector</span></span>  

```console
$(selector, [startNode])
```  

<span data-ttu-id="48a06-132">Возвращает ссылку на первый элемент DOM с указанным селектором CSS.</span><span class="sxs-lookup"><span data-stu-id="48a06-132">Returns the reference to the first DOM element with the specified CSS selector.</span></span>  <span data-ttu-id="48a06-133">Этот метод является псевдонимом метода [Document. querySelector ()][MDNDocumentQuerySelector] .</span><span class="sxs-lookup"><span data-stu-id="48a06-133">This method is an alias for the [document.querySelector()][MDNDocumentQuerySelector] method.</span></span>  

<span data-ttu-id="48a06-134">На приведенном ниже рисунке возвращается ссылка на первый `<img>` элемент в документе.</span><span class="sxs-lookup"><span data-stu-id="48a06-134">In the following figure, a reference to the first `<img>` element in the document is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image.msft.png" alt-text="$ ("Img")" lightbox="../media/console-element-selector-image.msft.png":::
   <span data-ttu-id="48a06-136">На рисунке 5:</span><span class="sxs-lookup"><span data-stu-id="48a06-136">Figure 5:  The</span></span> `$('img')`  
:::image-end:::  

<span data-ttu-id="48a06-137">Наведите указатель мыши на полученный результат, откройте контекстное меню, а затем выберите пункт **Показать на панели элементов** , чтобы найти его в модели DOM, или **прокрутите** страницу, чтобы отобразить ее на странице.</span><span class="sxs-lookup"><span data-stu-id="48a06-137">Hover on the returned result, open the contextual menu \(right-click\), and select **Reveal in Elements Panel** to find it in the DOM or **Scroll in to View** to show it on the page.</span></span>  

<span data-ttu-id="48a06-138">На приведенном ниже рисунке возвращается ссылка на элемент, выбранный в данный момент, и отображается свойство src.</span><span class="sxs-lookup"><span data-stu-id="48a06-138">In the following figure, a reference to the currently selected element is returned and the src property is displayed.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-source.msft.png" alt-text="$ ("Img"). src" lightbox="../media/console-element-selector-image-source.msft.png":::
   <span data-ttu-id="48a06-140">На рисунке 6:</span><span class="sxs-lookup"><span data-stu-id="48a06-140">Figure 6:  The</span></span> `$('img').src`  
:::image-end:::  

<span data-ttu-id="48a06-141">Этот метод также поддерживает второй параметр, startNode, задающий "элемент" или узел, из которого следует искать элементы.</span><span class="sxs-lookup"><span data-stu-id="48a06-141">This method also supports a second parameter, startNode, that specifies an "element" or Node from which to search for elements.</span></span>  <span data-ttu-id="48a06-142">Значением по умолчанию для параметра является `document` .</span><span class="sxs-lookup"><span data-stu-id="48a06-142">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="48a06-143">На приведенном ниже рисунке первый `img` элемент найден после элемента `title--image` и отображается `src` правильно.</span><span class="sxs-lookup"><span data-stu-id="48a06-143">In the following figure, the first `img` element is found after the `title--image` and displays the `src` properly is returned.</span></span>  

:::image type="complex" source="../media/console-element-selector-image-filter-source.msft.png" alt-text="$ ("Img", Document. querySelector ("Title--Image")). src" lightbox="../media/console-element-selector-image-filter-source.msft.png":::
   <span data-ttu-id="48a06-145">На рисунке 7:</span><span class="sxs-lookup"><span data-stu-id="48a06-145">Figure 7:  The</span></span> `$('img', document.querySelector('title--image')).src`  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="48a06-146">Если вы используете библиотеку (например, jQuery, которая использует `$` , эта функция перезаписывается и `$` соответствует реализации из этой библиотеки).</span><span class="sxs-lookup"><span data-stu-id="48a06-146">If you are using a library such as jQuery that uses `$`, the functionality is overwritten, and `$` corresponds to the implementation from that library.</span></span>  

## <span data-ttu-id="48a06-147">Выбор запроса</span><span class="sxs-lookup"><span data-stu-id="48a06-147">Query Selector All</span></span>  

```console
$$(selector, [startNode])
```  

<span data-ttu-id="48a06-148">Возвращает массив элементов, которые соответствуют указанному селектору CSS.</span><span class="sxs-lookup"><span data-stu-id="48a06-148">Returns an array of elements that match the specified CSS selector.</span></span>  <span data-ttu-id="48a06-149">Этот метод эквивалентен вызову метода [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .</span><span class="sxs-lookup"><span data-stu-id="48a06-149">This method is equivalent to calling the [document.querySelectorAll()][MDNDocumentQuerySelectorAll] method.</span></span>  

<span data-ttu-id="48a06-150">В приведенном ниже примере кода и рисунке используется `$$()` для создания массива всех `<img>` элементов в текущем документе и отображения значения `src` свойства для каждого элемента.</span><span class="sxs-lookup"><span data-stu-id="48a06-150">In the following code sample and figure, use `$$()` to create an array of all `<img>` elements in the current document and display the value of the `src` property for each element.</span></span>  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-all.msft.png" alt-text="Использование $ $ () для выбора всех изображений в документе и отображения источников" lightbox="../media/console-element-selector-image-all.msft.png":::
   <span data-ttu-id="48a06-152">Рисунок 8: использование `$$()` для выделения всех изображений в документе и отображения источников</span><span class="sxs-lookup"><span data-stu-id="48a06-152">Figure 8:  Using `$$()` to select all images in the document and display the sources</span></span>  
:::image-end:::  

<span data-ttu-id="48a06-153">Этот метод также поддерживает второй параметр, startNode, указывающий элемент или узел, из которого нужно выполнить поиск элементов.</span><span class="sxs-lookup"><span data-stu-id="48a06-153">This method also supports a second parameter, startNode, that specifies an element or Node from which to search for elements.</span></span>  <span data-ttu-id="48a06-154">Значением по умолчанию для параметра является `document` .</span><span class="sxs-lookup"><span data-stu-id="48a06-154">The default value of the parameter is `document`.</span></span>  

<span data-ttu-id="48a06-155">В следующем примере кода и рисунке измененная версия предыдущего примера кода и на рисунке используются `$$()` для создания массива всех `<img>` элементов, которые отображаются в текущем документе после выбранного узла.</span><span class="sxs-lookup"><span data-stu-id="48a06-155">In the following code sample and figure, a modified version of the previous code sample and figure uses `$$()` to create an array of all `<img>` elements that appear in the current document after the selected Node.</span></span>  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

:::image type="complex" source="../media/console-element-selector-image-filter-all.msft.png" alt-text="Использование $ $ () для выбора всех изображений, которые отображаются после указанного <div> элемента в документе и отображения источников" lightbox="../media/console-element-selector-image-filter-all.msft.png":::
   <span data-ttu-id="48a06-157">Рисунок 9: использование `$$()` для выбора всех изображений, которые отображаются после указанного `<div>` элемента в документе, и отображения источников</span><span class="sxs-lookup"><span data-stu-id="48a06-157">Figure 9:  Using `$$()` to select all images that appear after the specified `<div>` element in the document and display the sources</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="48a06-158">Нажмите клавишу `Shift` + `Enter` консоль, чтобы начать новую строку, не выполняя сценарий.</span><span class="sxs-lookup"><span data-stu-id="48a06-158">Press `Shift`+`Enter` in the console to start a new line without running the script.</span></span>  

## <span data-ttu-id="48a06-159">Выражения</span><span class="sxs-lookup"><span data-stu-id="48a06-159">XPath</span></span>  

```console
$x(path, [startNode])
```  

<span data-ttu-id="48a06-160">Возвращает массив элементов DOM, соответствующих указанному выражению XPath.</span><span class="sxs-lookup"><span data-stu-id="48a06-160">Returns an array of DOM elements that match the specified XPath expression.</span></span>  

<span data-ttu-id="48a06-161">В приведенном ниже примере кода `<p>` возвращаются все элементы на странице.</span><span class="sxs-lookup"><span data-stu-id="48a06-161">In the following code sample and figure, all of the `<p>` elements on the page are returned.</span></span>  

```console
$x("//p")
```  

:::image type="complex" source="../media/console-array-xpath.msft.png" alt-text="Использование селектора XPath" lightbox="../media/console-array-xpath.msft.png":::
   <span data-ttu-id="48a06-163">Рисунок 10: использование селектора XPath</span><span class="sxs-lookup"><span data-stu-id="48a06-163">Figure 10:  Using an XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="48a06-164">В приведенном ниже примере кода и рисунке `<p>` возвращаются все элементы, содержащие `<a>` элементы.</span><span class="sxs-lookup"><span data-stu-id="48a06-164">In the following code sample and figure, all of the `<p>` elements that contain `<a>` elements are returned.</span></span>  

```console
$x("//p[a]")
```  

:::image type="complex" source="../media/console-array-xpath-sub-element.msft.png" alt-text="Использование более сложного селектора XPath" lightbox="../media/console-array-xpath-sub-element.msft.png":::
   <span data-ttu-id="48a06-166">Рисунок 11: использование более сложного селектора XPath</span><span class="sxs-lookup"><span data-stu-id="48a06-166">Figure 11:  Using a more complicated XPath selector</span></span>  
:::image-end:::  

<span data-ttu-id="48a06-167">Как и другие команды Selector, `$x(path)` имеет дополнительный второй параметр, `startNode` указывающий на элемент или узел, из которого нужно выполнить поиск элементов.</span><span class="sxs-lookup"><span data-stu-id="48a06-167">Similar to the other selector commands, `$x(path)` has an optional second parameter, `startNode`, that specifies an element or Node from which to search for elements.</span></span>  

:::image type="complex" source="../media/console-array-xpath-startnode.msft.png" alt-text="Использование селектора XPath с startNode" lightbox="../media/console-array-xpath-startnode.msft.png":::
   <span data-ttu-id="48a06-169">Рисунок 12: использование селектора XPath с</span><span class="sxs-lookup"><span data-stu-id="48a06-169">Figure 12:  Using an XPath selector with</span></span> `startNode`  
:::image-end:::  

## <span data-ttu-id="48a06-170">Сброс</span><span class="sxs-lookup"><span data-stu-id="48a06-170">clear</span></span>  

```console
clear()
```  

<span data-ttu-id="48a06-171">Очищает консоль журнала.</span><span class="sxs-lookup"><span data-stu-id="48a06-171">Clears the console of the history.</span></span>  

```console
clear()
```  

## <span data-ttu-id="48a06-172">copy</span><span class="sxs-lookup"><span data-stu-id="48a06-172">copy</span></span>  

```console
copy(object)
```  

<span data-ttu-id="48a06-173">`copy(object)`Метод копирует строковое представление указанного объекта в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="48a06-173">The `copy(object)` method copies a string representation of the specified object to the clipboard.</span></span>  

```console
copy($0)
```  

## <span data-ttu-id="48a06-174">отладка</span><span class="sxs-lookup"><span data-stu-id="48a06-174">debug</span></span>  

```console
debug(method)
```  

>[!NOTE]
> <span data-ttu-id="48a06-175">[#1050237 проблема с Chromium][MonorailIssue1050237] отслеживает ошибку с `debug()` функцией.</span><span class="sxs-lookup"><span data-stu-id="48a06-175">The [Chromium issue #1050237][MonorailIssue1050237] is tracking a bug with the `debug()` function.</span></span>  <span data-ttu-id="48a06-176">Если вы столкнулись с проблемой, попробуйте использовать вместо нее [точки останова][DevtoolsJavascriptBreakpoints] .</span><span class="sxs-lookup"><span data-stu-id="48a06-176">If you encounter the issue, try [using breakpoints][DevtoolsJavascriptBreakpoints] instead.</span></span>  

<span data-ttu-id="48a06-177">Когда вы запрашиваете указанный метод, отладчик вызывается и останавливается внутри метода на панели « **источники** », что позволяет пошагово пройти этот код и выполнить его отладку.</span><span class="sxs-lookup"><span data-stu-id="48a06-177">When you request the specified method, the debugger is invoked and breaks inside the method on the **Sources** panel allowing you to step through the code and debug it.</span></span>  

```console
debug("debug");
```  

:::image type="complex" source="../media/console-debug-text.msft.png" alt-text="Прерывание в методе с помощью Debug ()" lightbox="../media/console-debug-text.msft.png":::
   <span data-ttu-id="48a06-179">Рисунок 13: прерывание внутри метода с</span><span class="sxs-lookup"><span data-stu-id="48a06-179">Figure 13:  Breaking inside a method with</span></span> `debug()`  
:::image-end:::  

<span data-ttu-id="48a06-180">Используйте `undebug(method)` для прекращения прерывания на методе или с помощью пользовательского интерфейса, чтобы отключить все точки останова.</span><span class="sxs-lookup"><span data-stu-id="48a06-180">Use `undebug(method)` to stop breaking on the method, or use the UI to disable all breakpoints.</span></span>  

<span data-ttu-id="48a06-181">Дополнительные сведения о точках останова можно найти в разделе [приостановка кода с точки останова][DevToolsJavascriptBreakpoints].</span><span class="sxs-lookup"><span data-stu-id="48a06-181">For more information on breakpoints, see [Pause Your Code With Breakpoints][DevToolsJavascriptBreakpoints].</span></span>  

## <span data-ttu-id="48a06-182">dir</span><span class="sxs-lookup"><span data-stu-id="48a06-182">dir</span></span>  

```console
dir(object)
```  

<span data-ttu-id="48a06-183">Отображает список всех свойств указанного объекта в стиле объекта.</span><span class="sxs-lookup"><span data-stu-id="48a06-183">Displays an object-style listing of all of the properties for the specified object.</span></span>  <span data-ttu-id="48a06-184">Этот метод является псевдонимом для метода [Console. dir ()][MDNConsoleDir] .</span><span class="sxs-lookup"><span data-stu-id="48a06-184">This method is an alias for the [console.dir()][MDNConsoleDir] method.</span></span>  

<span data-ttu-id="48a06-185">Вычислите `document.head` текст на консоли, чтобы отобразить HTML `<head>` между `</head>` тегами и.</span><span class="sxs-lookup"><span data-stu-id="48a06-185">Evaluate `document.head` in the Console to display the HTML between the `<head>` and `</head>` tags.</span></span>  <span data-ttu-id="48a06-186">В приведенном ниже примере кода и рисунке после использования на консоли отображается вхождение стиля объекта `console.dir()` .</span><span class="sxs-lookup"><span data-stu-id="48a06-186">In the following code sample and figure, an object-style listing is displayed after using `console.dir()` in the Console.</span></span>  

```console
document.head;
dir(document.head);
```  

:::image type="complex" source="../media/console-dir-document-head-expanded.msft.png" alt-text="Ведение журнала. Head с помощью метода dir ()" lightbox="../media/console-dir-document-head-expanded.msft.png":::
   <span data-ttu-id="48a06-188">Рисунок 14: ведение журнала `document.head` с помощью `dir()` метода</span><span class="sxs-lookup"><span data-stu-id="48a06-188">Figure 14:  Logging `document.head` with `dir()` method</span></span>  
:::image-end:::  

<span data-ttu-id="48a06-189">Дополнительные сведения можно найти в описании [`console.dir()`][DevToolsConsoleApiConsoleDirObject] записи в API-интерфейсе консоли.</span><span class="sxs-lookup"><span data-stu-id="48a06-189">For more information, see the [`console.dir()`][DevToolsConsoleApiConsoleDirObject] entry in the Console API.</span></span>  

## <span data-ttu-id="48a06-190">dirxml</span><span class="sxs-lookup"><span data-stu-id="48a06-190">dirxml</span></span>  

```console
dirxml(object)
```  

<span data-ttu-id="48a06-191">Печатает XML-представление указанного объекта, как показано на вкладке **элементы** .  Этот метод эквивалентен методу [Console. DirXML ()][MDNConsoleDirxml] .</span><span class="sxs-lookup"><span data-stu-id="48a06-191">Prints an XML representation of the specified object, as seen in the **Elements** tab.  This method is equivalent to the [console.dirxml()][MDNConsoleDirxml] method.</span></span>  

## <span data-ttu-id="48a06-192">Проверка</span><span class="sxs-lookup"><span data-stu-id="48a06-192">inspect</span></span>  

```console
inspect(object/method)
```  

<span data-ttu-id="48a06-193">Открывает и выбирает определенный элемент или объект на соответствующей панели: либо панель **элементов** для элементов DOM, либо панель **памяти** для объектов кучи JavaScript.</span><span class="sxs-lookup"><span data-stu-id="48a06-193">Opens and selects the specified element or object in the appropriate panel:  either the **Elements** panel for DOM elements or the **Memory** panel for JavaScript heap objects.</span></span>  

<span data-ttu-id="48a06-194">В приведенном ниже примере и рисунке кода `document.body` откроется панель " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="48a06-194">In the following code sample and figure, the `document.body` opens in the **Elements** panel.</span></span>  

```console
inspect(document.body);
```  

:::image type="complex" source="../media/console-inspect-document-body.msft.png" alt-text="Проверка элемента с помощью проверки ()" lightbox="../media/console-inspect-document-body.msft.png":::
   <span data-ttu-id="48a06-196">Рис. 15: Проверка элемента с помощью</span><span class="sxs-lookup"><span data-stu-id="48a06-196">Figure 15:  Inspecting an element with</span></span> `inspect()`  
:::image-end:::  

<span data-ttu-id="48a06-197">При передаче метода для проверки этот метод открывает документ на панели « **источники** » для проверки.</span><span class="sxs-lookup"><span data-stu-id="48a06-197">When passing a method to inspect, the method opens the document in the **Sources** panel for you to inspect.</span></span>  

## <span data-ttu-id="48a06-198">getEventListeners</span><span class="sxs-lookup"><span data-stu-id="48a06-198">getEventListeners</span></span>  

```console
getEventListeners(object)
```  

<span data-ttu-id="48a06-199">Возвращает прослушиватели событий, зарегистрированные для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="48a06-199">Returns the event listeners registered on the specified object.</span></span>  <span data-ttu-id="48a06-200">Возвращаемое значение — это объект, который содержит массив для всех зарегистрированных типов событий \ (например, `click` или `keydown` \).</span><span class="sxs-lookup"><span data-stu-id="48a06-200">The return value is an object that contains an array for each registered event type \(such as `click` or `keydown`\).</span></span>  <span data-ttu-id="48a06-201">Каждый из этих массивов — это объекты, которые описывают прослушиватель, зарегистрированный для каждого типа.</span><span class="sxs-lookup"><span data-stu-id="48a06-201">The members of each array are objects that describe the listener registered for each type.</span></span>  <span data-ttu-id="48a06-202">В следующем примере кода показано, как перечисляются все прослушиватели событий, зарегистрированные в объекте Document.</span><span class="sxs-lookup"><span data-stu-id="48a06-202">In the following code sample figure, all of the event listeners registered on the document object are listed.</span></span>  

```console
getEventListeners(document);
```  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png" alt-text="Вывод на печать с использованием getEventListeners (документ)" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document.msft.png":::
   <span data-ttu-id="48a06-204">Рисунок 16: результат использования</span><span class="sxs-lookup"><span data-stu-id="48a06-204">Figure 16:  The result of using</span></span> `getEventListeners(document)`  
:::image-end:::  

<span data-ttu-id="48a06-205">Если в указанном объекте зарегистрировано более одного прослушивателя, то массив содержит элемент для каждого прослушивателя.</span><span class="sxs-lookup"><span data-stu-id="48a06-205">If more than one listener is registered on the specified object, then the array contains a member for each listener.</span></span>  <span data-ttu-id="48a06-206">На рисунке ниже показано, как в элементе Document для события зарегистрированы два прослушивателя событий `click` .</span><span class="sxs-lookup"><span data-stu-id="48a06-206">In the following figure, there are two event listeners registered on the document element for the `click` event.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png" alt-text="Несколько прослушивателей" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-expanded-1.msft.png":::
   <span data-ttu-id="48a06-208">Рисунок 17: несколько прослушивателей</span><span class="sxs-lookup"><span data-stu-id="48a06-208">Figure 17:  Multiple listeners</span></span>  
:::image-end:::  

<span data-ttu-id="48a06-209">Вы можете расширить каждый из указанных ниже объектов, чтобы просмотреть свойства.</span><span class="sxs-lookup"><span data-stu-id="48a06-209">You may further expand each of the following objects to explore the properties.</span></span>  

:::image type="complex" source="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png" alt-text="Развернутое представление объекта прослушивателя" lightbox="../media/console-elements-event-listeners-console-get-event-listeners-document-2.msft.png":::
   <span data-ttu-id="48a06-211">Рисунок 18: развернутое представление объекта прослушивателя</span><span class="sxs-lookup"><span data-stu-id="48a06-211">Figure 18:  Expanded view of listener object</span></span>  
:::image-end:::  

## <span data-ttu-id="48a06-212">клавиши</span><span class="sxs-lookup"><span data-stu-id="48a06-212">keys</span></span>  

```console
keys(object)
```  

<span data-ttu-id="48a06-213">Возвращает массив, содержащий имена свойств, принадлежащих указанному объекту.</span><span class="sxs-lookup"><span data-stu-id="48a06-213">Returns an array containing the names of the properties belonging to the specified object.</span></span>  <span data-ttu-id="48a06-214">Чтобы получить связанные значения одинаковых свойств, используйте `values()` .</span><span class="sxs-lookup"><span data-stu-id="48a06-214">To get the associated values of the same properties, use `values()`.</span></span>  

<span data-ttu-id="48a06-215">Например, предположим, что приложение определило следующий объект.</span><span class="sxs-lookup"><span data-stu-id="48a06-215">For example, suppose your application defined the following object.</span></span>  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

<span data-ttu-id="48a06-216">В приведенных ниже примерах кода предполагается, что результат `player1` определен в глобальном пространстве имен \ (для простоты) перед вводом `keys(player1)` и `values(player1)` на консоли.</span><span class="sxs-lookup"><span data-stu-id="48a06-216">In the following code samples and figure, the result assumes `player1` was defined in the global namespace \(for simplicity\) prior to typing `keys(player1)` and `values(player1)` in the console.</span></span>  

```console
keys(player1)

values(player1)
```  

:::image type="complex" source="../media/console-keys-values.msft.png" alt-text="Команды Keys () и Values ()" lightbox="../media/console-keys-values.msft.png":::
   <span data-ttu-id="48a06-218">На рисунке 19: `keys()` `values()` команды и</span><span class="sxs-lookup"><span data-stu-id="48a06-218">Figure 19:  The `keys()` and `values()` commands</span></span>  
:::image-end:::  

## <span data-ttu-id="48a06-219">монитор</span><span class="sxs-lookup"><span data-stu-id="48a06-219">monitor</span></span>  

```console
monitor(method)
```  

<span data-ttu-id="48a06-220">Заносит в консоль сообщение, которое указывает имя метода вместе с аргументами, передаваемыми методу при его вызове.</span><span class="sxs-lookup"><span data-stu-id="48a06-220">Logs a message to the console that indicates the method name along with the arguments that are passed to the method when it was called.</span></span>  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

:::image type="complex" source="../media/console-function-monitor-sum.msft.png" alt-text="Метод Monitor ()" lightbox="../media/console-function-monitor-sum.msft.png":::
   <span data-ttu-id="48a06-222">Рис. 20: `monitor()` метод</span><span class="sxs-lookup"><span data-stu-id="48a06-222">Figure 20:  The `monitor()` method</span></span>  
:::image-end:::  

<span data-ttu-id="48a06-223">Используется `unmonitor(method)` для прекращения наблюдения.</span><span class="sxs-lookup"><span data-stu-id="48a06-223">Use `unmonitor(method)` to cease monitoring.</span></span>  

## <span data-ttu-id="48a06-224">monitorEvents</span><span class="sxs-lookup"><span data-stu-id="48a06-224">monitorEvents</span></span>  

```console
monitorEvents(object[, events])
```  

<span data-ttu-id="48a06-225">Когда в указанном объекте происходит одно из указанных событий, объект события регистрируется в консоли.</span><span class="sxs-lookup"><span data-stu-id="48a06-225">When one of the specified events occurs on the specified object, the event object is logged to the console.</span></span>  <span data-ttu-id="48a06-226">Вы можете указать одно событие для отслеживания, массив событий или один из типов универсальных событий, сопоставленных с предопределенной коллекцией событий.</span><span class="sxs-lookup"><span data-stu-id="48a06-226">You may specify a single event to monitor, an array of events, or one of the generic events types that are mapped to a predefined collection of events.</span></span>  <span data-ttu-id="48a06-227">Ниже приведен пример кода и рисунок.</span><span class="sxs-lookup"><span data-stu-id="48a06-227">See the following code sample and figure.</span></span>  

<span data-ttu-id="48a06-228">Ниже приведено наблюдение за всеми событиями изменения размера объекта Window.</span><span class="sxs-lookup"><span data-stu-id="48a06-228">The following monitors all resize events on the window object.</span></span>  

```console
monitorEvents(window, "resize");
```  

:::image type="complex" source="../media/console-monitor-events-resize-window.msft.png" alt-text="Наблюдение за событиями изменения размера окна" lightbox="../media/console-monitor-events-resize-window.msft.png":::
   <span data-ttu-id="48a06-230">Рисунок 21: наблюдение за событиями изменения размера окна</span><span class="sxs-lookup"><span data-stu-id="48a06-230">Figure 21:  Monitoring window resize events</span></span>  
:::image-end:::  

<span data-ttu-id="48a06-231">В следующем примере определяется массив для мониторинга обоих `resize` и `scroll` событий в объекте Window.</span><span class="sxs-lookup"><span data-stu-id="48a06-231">The following defines an array to monitor both `resize` and `scroll` events on the window object.</span></span>  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

<span data-ttu-id="48a06-232">Вы также можете указать один из доступных типов событий — строки, которые сопоставляются с предопределенными наборами событий.</span><span class="sxs-lookup"><span data-stu-id="48a06-232">You may also specify one of the available types of events, strings that map to predefined sets of events.</span></span>  <span data-ttu-id="48a06-233">В приведенной ниже таблице показаны типы доступных событий и сопоставлений связанных событий.</span><span class="sxs-lookup"><span data-stu-id="48a06-233">The table below displays the available event types and the associated event mappings.</span></span>  

| <span data-ttu-id="48a06-234">Тип события</span><span class="sxs-lookup"><span data-stu-id="48a06-234">Event type</span></span> | <span data-ttu-id="48a06-235">Соответствующие сопоставленные события</span><span class="sxs-lookup"><span data-stu-id="48a06-235">Corresponding mapped events</span></span> |  
|:--- |:--- |  
| `mouse` | <span data-ttu-id="48a06-236">"Click", "DblClick", "MouseDown", "MouseMove", "указатель мыши", "onmouseover", "MouseUp", "MouseWheel"</span><span class="sxs-lookup"><span data-stu-id="48a06-236">"click", "dblclick", "mousedown", "mousemove", "mouseout", "mouseover", "mouseup", "mousewheel"</span></span> |  
| `key` | <span data-ttu-id="48a06-237">"KeyDown", "нажатие клавиши", "KeyUp", "textInput"</span><span class="sxs-lookup"><span data-stu-id="48a06-237">"keydown", "keypress", "keyup", "textInput"</span></span> |  
| `touch` | <span data-ttu-id="48a06-238">"touchcancel", "touchend", "touchmove", "touchstart"</span><span class="sxs-lookup"><span data-stu-id="48a06-238">"touchcancel", "touchend", "touchmove", "touchstart"</span></span> |  
| `control` | <span data-ttu-id="48a06-239">"Размытие", "Изменить", "фокусировку", "прокрутка", "выделить", "Отправить", "выбрать", "Отправить", "с масштабом"</span><span class="sxs-lookup"><span data-stu-id="48a06-239">"blur", "change", "focus", "reset", "resize", "scroll", "select", "submit", "zoom"</span></span> |  

<span data-ttu-id="48a06-240">В следующем примере кода `key` Тип события, соответствующий `key` событиям текстового поля ввода, в данный момент выделены на панели **элементы** .</span><span class="sxs-lookup"><span data-stu-id="48a06-240">In the following code sample, the `key` event type corresponding to `key` events on an input text field are currently selected in the **Elements** panel.</span></span>  

```console
monitorEvents($0, "key");
```  

<span data-ttu-id="48a06-241">На приведенном ниже рисунке показан пример выходных данных после ввода символа в текстовом поле.</span><span class="sxs-lookup"><span data-stu-id="48a06-241">In the following figure the sample output after typing a character in the text field is displayed.</span></span>  

:::image type="complex" source="../media/console-monitor-events-type-t-y.msft.png" alt-text="Контроль событий ключа" lightbox="../media/console-monitor-events-type-t-y.msft.png":::
   <span data-ttu-id="48a06-243">Рис. 22: Отслеживание ключевых событий</span><span class="sxs-lookup"><span data-stu-id="48a06-243">Figure 22:  Monitoring key events</span></span>  
:::image-end:::  

## <span data-ttu-id="48a06-244">профиль</span><span class="sxs-lookup"><span data-stu-id="48a06-244">profile</span></span>  

```console
profile([name])
```  

<span data-ttu-id="48a06-245">Запускает сеанс профилирования ЦП JavaScript с необязательным именем.</span><span class="sxs-lookup"><span data-stu-id="48a06-245">Starts a JavaScript CPU profiling session with an optional name.</span></span>  <span data-ttu-id="48a06-246">Метод [profileEnd ()](#profileend) завершает профиль и отображает результаты на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="48a06-246">The [profileEnd()](#profileend) method completes the profile and displays the results in the **Memory** panel.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="48a06-247">Запустите `profile()` метод, чтобы начать профилирование.</span><span class="sxs-lookup"><span data-stu-id="48a06-247">Run the `profile()` method to start profiling.</span></span>  
    
    ```console
    profile("My profile")
    ```  
    
1.  <span data-ttu-id="48a06-248">Запустите метод [profileEnd ()](#profileend) , чтобы остановить профилирование и отобразить результаты на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="48a06-248">Run the [profileEnd()](#profileend) method to stop profiling and display the results in the **Memory** panel.</span></span>  

<span data-ttu-id="48a06-249">Профили также могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="48a06-249">Profiles may also be nested.</span></span>  <span data-ttu-id="48a06-250">В приведенных ниже примерах кода результат одинаков вне зависимости от порядка.</span><span class="sxs-lookup"><span data-stu-id="48a06-250">In the following code samples and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> <span data-ttu-id="48a06-251">Несколько профилей ЦП могут работать одновременно, и вы не обязаны закрывать каждый из них в заказе на создание.</span><span class="sxs-lookup"><span data-stu-id="48a06-251">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="48a06-252">profileEnd</span><span class="sxs-lookup"><span data-stu-id="48a06-252">profileEnd</span></span>  

```console
profileEnd([name])
```  

<span data-ttu-id="48a06-253">Завершает сеанс профилирования ЦП JavaScript и отображает результаты на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="48a06-253">Completes a JavaScript CPU profiling session and displays the results in the **Memory** panel.</span></span>  <span data-ttu-id="48a06-254">Необходимо запустить метод [Profile ()](#profile) .</span><span class="sxs-lookup"><span data-stu-id="48a06-254">You must be running the [profile()](#profile) method.</span></span>  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  <span data-ttu-id="48a06-255">Запустите метод [Profile ()](#profile) , чтобы начать профилирование.</span><span class="sxs-lookup"><span data-stu-id="48a06-255">Run the [profile()](#profile) method to start profiling.</span></span>  
1.  <span data-ttu-id="48a06-256">Запустите `profileEnd()` метод, чтобы остановить профилирование и отобразить результаты на панели **памяти** .</span><span class="sxs-lookup"><span data-stu-id="48a06-256">Run the `profileEnd()` method to stop profiling and display the results in the **Memory** panel.</span></span>  
    
    ```console
    profileEnd("My profile")
    ```  

<span data-ttu-id="48a06-257">Профили также могут быть вложенными.</span><span class="sxs-lookup"><span data-stu-id="48a06-257">Profiles may also be nested.</span></span>  <span data-ttu-id="48a06-258">В приведенном ниже примере кода результат одинаков вне зависимости от порядка.</span><span class="sxs-lookup"><span data-stu-id="48a06-258">In the following code sample and figure the result is the same regardless of the order.</span></span>  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

<span data-ttu-id="48a06-259">Результат появится в виде снимка кучи на панели " **память** ".</span><span class="sxs-lookup"><span data-stu-id="48a06-259">The result appears as a Heap Snapshot in the **Memory** panel.</span></span>  

:::image type="complex" source="../media/console-memory-multiple-cpu-profiles.msft.png" alt-text="Сгруппированные профили" lightbox="../media/console-memory-multiple-cpu-profiles.msft.png":::
   <span data-ttu-id="48a06-261">Рисунок 23: сгруппированные профили</span><span class="sxs-lookup"><span data-stu-id="48a06-261">Figure 23:  Grouped profiles</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="48a06-262">Несколько профилей ЦП могут работать одновременно, и вы не обязаны закрывать каждый из них в заказе на создание.</span><span class="sxs-lookup"><span data-stu-id="48a06-262">Multiple CPU profiles may operate at the same time and you are not required to close-out each one in creation order.</span></span>  

## <span data-ttu-id="48a06-263">queryObjects</span><span class="sxs-lookup"><span data-stu-id="48a06-263">queryObjects</span></span>  

```console
queryObjects(Constructor)
```  

<span data-ttu-id="48a06-264">Возвращают массив объектов, созданных с помощью указанного конструктора.</span><span class="sxs-lookup"><span data-stu-id="48a06-264">Return an array of objects created with the specified constructor.</span></span>  <span data-ttu-id="48a06-265">Область `queryObjects()` — это выбранный в данный момент контекст среды выполнения на консоли.</span><span class="sxs-lookup"><span data-stu-id="48a06-265">The scope of `queryObjects()` is the currently-selected runtime context in the console.</span></span>

:::row:::
   :::column span="1":::
      ```console
      queryObjects(promise)
      ```  
      
      <span data-ttu-id="48a06-266">Возвращает все `Promises` .</span><span class="sxs-lookup"><span data-stu-id="48a06-266">Returns all `Promises`.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(HTMLElement)
      ```  
      
      <span data-ttu-id="48a06-267">Возвращает все элементы HTML.</span><span class="sxs-lookup"><span data-stu-id="48a06-267">Returns all HTML elements.</span></span>  
   :::column-end:::
   :::column span="1":::
      ```console
      queryObjects(functionName)
      ```  
      
      <span data-ttu-id="48a06-268">Возвращает все объекты, экземпляры которых были созданы с помощью `new functionName()` .</span><span class="sxs-lookup"><span data-stu-id="48a06-268">Returns all objects that were instantiated using `new functionName()`.</span></span>  
   :::column-end:::
:::row-end:::  

---  

## <span data-ttu-id="48a06-269">таблич</span><span class="sxs-lookup"><span data-stu-id="48a06-269">table</span></span>  

```console
table(data[, columns])
```  

<span data-ttu-id="48a06-270">Заносит в журнал объектные данные с форматированием таблицы, основанным на объекте данных, с помощью необязательных заголовков столбцов.</span><span class="sxs-lookup"><span data-stu-id="48a06-270">Logs object data with table formatting based upon the data object in with optional column headings.</span></span>  <span data-ttu-id="48a06-271">В приведенном ниже примере кода и рисунке показано, как отображается список имен, использующих таблицу на консоли.</span><span class="sxs-lookup"><span data-stu-id="48a06-271">In the following code sample and figure, a list of names using a table in the console is displayed.</span></span>  

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

:::image type="complex" source="../media/console-table-display.msft.png" alt-text="Результат выполнения метода Table ()" lightbox="../media/console-table-display.msft.png":::
   <span data-ttu-id="48a06-273">Рисунок 24: результат выполнения `table()` метода</span><span class="sxs-lookup"><span data-stu-id="48a06-273">Figure 24:  The result of the `table()` method</span></span>  
:::image-end:::  

## <span data-ttu-id="48a06-274">Отладка</span><span class="sxs-lookup"><span data-stu-id="48a06-274">undebug</span></span>  

```console
undebug(method)
```  

<span data-ttu-id="48a06-275">Прекращает отладку указанного метода, поэтому при вызове метода отладчик больше не вызывается.</span><span class="sxs-lookup"><span data-stu-id="48a06-275">Stops the debugging of the specified method so that when the method is called, the debugger is no longer invoked.</span></span>  

```console
undebug(getData);
```  

## <span data-ttu-id="48a06-276">отследить</span><span class="sxs-lookup"><span data-stu-id="48a06-276">unmonitor</span></span>  

```console
unmonitor(method)
```  

<span data-ttu-id="48a06-277">Останавливает мониторинг указанного метода.</span><span class="sxs-lookup"><span data-stu-id="48a06-277">Stops the monitoring of the specified method.</span></span>  <span data-ttu-id="48a06-278">Этот метод используется совместно с методом [Monitor ()](#monitor) .</span><span class="sxs-lookup"><span data-stu-id="48a06-278">This method is used in concert with the [monitor()](#monitor) method.</span></span>  

```console
unmonitor(getData);
```  

## <span data-ttu-id="48a06-279">unmonitorEvents</span><span class="sxs-lookup"><span data-stu-id="48a06-279">unmonitorEvents</span></span>  

```console
unmonitorEvents(object[, events])
```  

<span data-ttu-id="48a06-280">Прекращает наблюдение за событиями для указанного объекта и событий.</span><span class="sxs-lookup"><span data-stu-id="48a06-280">Stops monitoring events for the specified object and events.</span></span>  <span data-ttu-id="48a06-281">Например, в приведенном ниже примере останавливается отслеживание всех событий в объекте Window.</span><span class="sxs-lookup"><span data-stu-id="48a06-281">For example, the following stops all event monitoring on the window object.</span></span>  

```console
unmonitorEvents(window);
```  

<span data-ttu-id="48a06-282">Вы также можете отключить наблюдение за определенными событиями для объекта.</span><span class="sxs-lookup"><span data-stu-id="48a06-282">You may also selectively stop monitoring specific events on an object.</span></span>  <span data-ttu-id="48a06-283">Например, следующий код начинает наблюдать за всеми `mouse` событиями выбранного в данный момент элемента, а затем останавливает наблюдение за `mousemove` событиями (возможно, чтобы уменьшить шум в выходных данных консоли \).</span><span class="sxs-lookup"><span data-stu-id="48a06-283">For example, the following code starts monitoring all `mouse` events on the currently selected element, and then stops monitoring `mousemove` events \(perhaps to reduce noise in the console output\).</span></span>  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## <span data-ttu-id="48a06-284">данные</span><span class="sxs-lookup"><span data-stu-id="48a06-284">values</span></span>  

```console
values(object)
```  

<span data-ttu-id="48a06-285">Возвращает массив, содержащий значения всех свойств, принадлежащих указанному объекту.</span><span class="sxs-lookup"><span data-stu-id="48a06-285">Returns an array containing the values of all properties belonging to the specified object.</span></span>  

```console
values(object);
```  

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
> <span data-ttu-id="48a06-295">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48a06-295">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="48a06-296">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/utilities) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="48a06-296">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/utilities) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="48a06-298">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="48a06-298">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
