---
title: Начало работы с JavaScript на консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 724d0e3c7c8439551538383e68a5fc4465eade94
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601728"
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







# <span data-ttu-id="56836-103">Начало работы с JavaScript на консоли</span><span class="sxs-lookup"><span data-stu-id="56836-103">Get Started With Running JavaScript In The Console</span></span>   



<span data-ttu-id="56836-104">В этом интерактивном учебнике показано, как запустить JavaScript на консоли Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="56836-104">This interactive tutorial shows you how to run JavaScript in the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="56836-105">Сведения о том, как вести журнал сообщений на консоли, можно найти в разделе [Начало работы с сообщениями журнала][DevToolsConsoleLoggingMessages] .</span><span class="sxs-lookup"><span data-stu-id="56836-105">See [Get Started With Logging Messages][DevToolsConsoleLoggingMessages] to learn how to log messages to the Console.</span></span>  <span data-ttu-id="56836-106">Сведения о том, как приостанавливать код JavaScript и переходить по одной строке за один раз, можно найти в статье [Начало работы с отладкой JavaScript][DevToolsJavascriptIndex] .</span><span class="sxs-lookup"><span data-stu-id="56836-106">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] to learn how to pause JavaScript code and step through it one line at a time.</span></span>  

> ##### <span data-ttu-id="56836-107">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="56836-107">Figure 1</span></span>  
> <span data-ttu-id="56836-108">На **консоли**</span><span class="sxs-lookup"><span data-stu-id="56836-108">The **Console**</span></span>  
> ![На консоли][ImageConsole]  

## <span data-ttu-id="56836-110">Обзор</span><span class="sxs-lookup"><span data-stu-id="56836-110">Overview</span></span>   

<span data-ttu-id="56836-111">**Консоль** — это [REPL][WikiReadEvalPrintLoop], который означает чтение, оценку, печать и зацикливание.</span><span class="sxs-lookup"><span data-stu-id="56836-111">The **Console** is a [REPL][WikiReadEvalPrintLoop], which stands for Read, Evaluate, Print, and Loop.</span></span>  <span data-ttu-id="56836-112">Она считывает JavaScript, который вы вводите в него, оценивает код, выводит результат [выражения][2alityExpressionsVersusStatements]и осуществляет переход к первому шагу.</span><span class="sxs-lookup"><span data-stu-id="56836-112">It reads the JavaScript that you type into it, evaluates your code, prints out the result of your [expression][2alityExpressionsVersusStatements], and then loops back to the first step.</span></span>  

## <span data-ttu-id="56836-113">Настройка DevTools</span><span class="sxs-lookup"><span data-stu-id="56836-113">Set up DevTools</span></span>   

<span data-ttu-id="56836-114">Этот учебник предназначен для того, чтобы открыть демонстрацию и попробовать все рабочие процессы самостоятельно.</span><span class="sxs-lookup"><span data-stu-id="56836-114">This tutorial is designed for you to open up the demo and try all the workflows yourself.</span></span>  <span data-ttu-id="56836-115">После того как вы будете физически подписаться на нее, вы, наверное, захотите запомнить рабочие процессы позже.</span><span class="sxs-lookup"><span data-stu-id="56836-115">When you physically follow along, you are more likely to remember the workflows later.</span></span>

1.  <span data-ttu-id="56836-116">`Control` + `Shift` + `J` Чтобы открыть консоль, нажмите клавиши \ (Windows \) или `Command` + `Option` + `J` \ (macOS **Console**\).</span><span class="sxs-lookup"><span data-stu-id="56836-116">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\) to open the **Console**.</span></span>  
1.  <span data-ttu-id="56836-117">Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **пример на консоли JavaScript** , чтобы открыть его в новом окне.</span><span class="sxs-lookup"><span data-stu-id="56836-117">Hold `Control` \(Windows\) or `Command` \(macOS\) and click **Console Javascript Example** to open in a new window.</span></span>  
    
    [<span data-ttu-id="56836-118">Пример сценария на консоли</span><span class="sxs-lookup"><span data-stu-id="56836-118">Console Javascript Example</span></span>][GlitchConsoleJavascriptExample]  
    
    > ##### <span data-ttu-id="56836-119">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="56836-119">Figure 2</span></span>  
    > <span data-ttu-id="56836-120">Страница примера JavaScript на консоли в левой части экрана и DevTools справа</span><span class="sxs-lookup"><span data-stu-id="56836-120">The Console JavaScript Example page on the left, and DevTools on the right</span></span>  
    > ![Страница примера JavaScript на консоли в левой части экрана и DevTools справа][ImageTutorialDevToolsJs]  

## <span data-ttu-id="56836-122">Просмотр и изменение JavaScript или DOM страницы</span><span class="sxs-lookup"><span data-stu-id="56836-122">View and change the JavaScript or DOM of the page</span></span>   

<span data-ttu-id="56836-123">При сборке или отладке страницы часто бывает полезно запускать инструкции на **консоли** , чтобы изменить внешний вид или выполнение страницы.</span><span class="sxs-lookup"><span data-stu-id="56836-123">When building or debugging a page, it is often useful to run statements in the **Console** in order to change how the page looks or runs.</span></span>  
    
1.  <span data-ttu-id="56836-124">Обратите внимание на текст на кнопке.</span><span class="sxs-lookup"><span data-stu-id="56836-124">Notice the text in the button.</span></span>  
1.  <span data-ttu-id="56836-125">Введите текст `document.getElementById('hello').textContent = 'Hello, Console!'` в **консоли** и нажмите клавишу `Enter` , чтобы вычислить выражение.</span><span class="sxs-lookup"><span data-stu-id="56836-125">Type `document.getElementById('hello').textContent = 'Hello, Console!'` in the **Console** and then press `Enter` to evaluate the expression.</span></span>  <span data-ttu-id="56836-126">Обратите внимание на то, как изменится текст внутри кнопки.</span><span class="sxs-lookup"><span data-stu-id="56836-126">Notice how the text inside the button changes.</span></span>  
    
    > ##### <span data-ttu-id="56836-127">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="56836-127">Figure 3</span></span>  
    > <span data-ttu-id="56836-128">Внешний вид консоли после вычисления выражения</span><span class="sxs-lookup"><span data-stu-id="56836-128">How the Console looks after evaluating the expression</span></span>  
    > ![Внешний вид консоли после вычисления выражения][ImageConsoleAfterEvaluating]  
    
    <span data-ttu-id="56836-130">Под кодом, который вы проверили `"Hello, Console!"` .</span><span class="sxs-lookup"><span data-stu-id="56836-130">Below the code that you evaluated you see `"Hello, Console!"`.</span></span>  <span data-ttu-id="56836-131">Отзывайте 4 шага REPL: чтение, оценка, печать, цикл.</span><span class="sxs-lookup"><span data-stu-id="56836-131">Recall the 4 steps of REPL: read, evaluate, print, loop.</span></span>  <span data-ttu-id="56836-132">После оценки кода программа REPL выводит результат выражения.</span><span class="sxs-lookup"><span data-stu-id="56836-132">After evaluating your code, a REPL prints the result of the expression.</span></span>  <span data-ttu-id="56836-133">Это `"Hello, Console!"` должно быть результатом вычисления `document.getElementById('hello').textContent = 'Hello, Console!'` .</span><span class="sxs-lookup"><span data-stu-id="56836-133">So `"Hello, Console!"` must be the result of evaluating `document.getElementById('hello').textContent = 'Hello, Console!'`.</span></span>  
    
## <span data-ttu-id="56836-134">Запуск произвольного кода JavaScript, не связанного со страницей</span><span class="sxs-lookup"><span data-stu-id="56836-134">Run arbitrary JavaScript that is not related to the page</span></span>   

<span data-ttu-id="56836-135">Иногда требуется, чтобы код Песочница в том месте, где вы можете протестировать какой-либо код, или опробуйте новые возможности JavaScript, с которыми вы не знакомы.</span><span class="sxs-lookup"><span data-stu-id="56836-135">Sometimes, you just want a code playground where you are able to test some code, or try out new JavaScript features you are not familiar with.</span></span>  <span data-ttu-id="56836-136">Консоль — это идеальное место для экспериментов такого рода.</span><span class="sxs-lookup"><span data-stu-id="56836-136">The Console is a perfect place for these kinds of experiments.</span></span>  

1.  <span data-ttu-id="56836-137">Введите текст `5 + 15` на консоли и нажмите клавишу `Enter` , чтобы вычислить выражение.</span><span class="sxs-lookup"><span data-stu-id="56836-137">Type `5 + 15` in the Console and press `Enter` to evaluate the expression.</span></span> <span data-ttu-id="56836-138">Консоль печатает результат выражения под кодом.</span><span class="sxs-lookup"><span data-stu-id="56836-138">The Console prints out the result of the expression below your code.</span></span>  <span data-ttu-id="56836-139">**На рисунке 4** ниже показано, как будет выглядеть консоль после оценки этого выражения.</span><span class="sxs-lookup"><span data-stu-id="56836-139">**Figure 4** below shows how your Console should look after evaluating this expression.</span></span>  

1.  <span data-ttu-id="56836-140">На **консоли**введите следующий код.</span><span class="sxs-lookup"><span data-stu-id="56836-140">Type the following code into the **Console**.</span></span>  <span data-ttu-id="56836-141">Попробуйте ввести его, а затем построчно, а не скопировав.</span><span class="sxs-lookup"><span data-stu-id="56836-141">Try typing it out, character-by-character, rather than copy-pasting it.</span></span>  
    
    ```javascript
    function add(a, b=20) {
        return a + b;
    }
    ```  
    
    <span data-ttu-id="56836-142">Если вы не знакомы с синтаксисом, ознакомьтесь со страницей [Определение значений по умолчанию для аргументов функции][Esma6DefaultParameterValues] `b=20` .</span><span class="sxs-lookup"><span data-stu-id="56836-142">See [define default values for function arguments][Esma6DefaultParameterValues] if you are unfamiliar with the `b=20` syntax.</span></span>  
    
1.  <span data-ttu-id="56836-143">Теперь вызовите функцию, которая была только что определена.</span><span class="sxs-lookup"><span data-stu-id="56836-143">Now, call the function that you just defined.</span></span>  
    
    ```javascript
    add(25);
    ```  
    
    > ##### <span data-ttu-id="56836-144">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="56836-144">Figure 4</span></span>  
    > <span data-ttu-id="56836-145">Как выглядит консоль после вычисления приведенных выше выражений</span><span class="sxs-lookup"><span data-stu-id="56836-145">How the Console looks after evaluating the expressions above</span></span>  
    > ![Как выглядит консоль после вычисления приведенных выше выражений][ImagePlayground]  
    
    `add(25)` <span data-ttu-id="56836-147">вычисляется `45` , так как при `add` вызове функции без второго аргумента `b` равным ему присваивается значение по умолчанию `20` .</span><span class="sxs-lookup"><span data-stu-id="56836-147">evaluates to `45` because when the `add` function is called without a second argument, `b` defaults to `20`.</span></span>  

## <span data-ttu-id="56836-148">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="56836-148">Next steps</span></span>   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

<span data-ttu-id="56836-149">DevTools позволяет приостановить выполнение сценария в центре выполнения.</span><span class="sxs-lookup"><span data-stu-id="56836-149">DevTools lets you pause a script in the middle of running.</span></span>  <span data-ttu-id="56836-150">Во время приостановки вы можете использовать **консоль** для просмотра и изменения `window` `DOM` страницы в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="56836-150">While you are paused, you may use the **Console** to view and change the `window` or `DOM` of the page at that moment in time.</span></span>  <span data-ttu-id="56836-151">Это обеспечивает мощный рабочий процесс отладки.</span><span class="sxs-lookup"><span data-stu-id="56836-151">This makes for a powerful debugging workflow.</span></span>  <span data-ttu-id="56836-152">В разделе [Начало работы с отладкой JavaScript][DevToolsJavascriptIndex] для интерактивного учебника.</span><span class="sxs-lookup"><span data-stu-id="56836-152">See [Get Started With Debugging JavaScript][DevToolsJavascriptIndex] for an interactive tutorial.</span></span>  

<span data-ttu-id="56836-153">Кроме того, **консоль** имеет набор удобных функций, которые облегчают взаимодействие с страницей.</span><span class="sxs-lookup"><span data-stu-id="56836-153">The **Console** also has a set of convenience functions that make it easier to interact with a page.</span></span>  <span data-ttu-id="56836-154">Пример</span><span class="sxs-lookup"><span data-stu-id="56836-154">For example:</span></span>  

*   <span data-ttu-id="56836-155">Вместо того `document.querySelector()` чтобы выделять элемент, введите `$()` .</span><span class="sxs-lookup"><span data-stu-id="56836-155">Rather than typing `document.querySelector()` to select an element, type `$()`.</span></span>  <span data-ttu-id="56836-156">Этот синтаксис имеет тот факт, что jQuery, но он не является jQuery.</span><span class="sxs-lookup"><span data-stu-id="56836-156">This syntax is inspired by jQuery, but it is not actually jQuery.</span></span>  <span data-ttu-id="56836-157">Это просто псевдоним `document.querySelector()` .</span><span class="sxs-lookup"><span data-stu-id="56836-157">It is just an alias for `document.querySelector()`.</span></span>  
*   `debug(function)` <span data-ttu-id="56836-158">фактически задает точку останова в первой строке этой функции.</span><span class="sxs-lookup"><span data-stu-id="56836-158">effectively sets a breakpoint on the first line of that function.</span></span>  
*   `keys(object)` <span data-ttu-id="56836-159">Возвращает массив с ключами указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="56836-159">returns an array containing the keys of the specified object.</span></span>  

<!--See [Console Utilities API Reference][DevToolsConsoleUtilities] to explore all the convenience functions.  -->  

<!--todo: add console utilities api reference section when available  -->  

 



<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "Рисунок 1: консоль"  
[ImageTutorialDevToolsJs]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-empty.msft.png "Рис. 2: страница примера JavaScript на консоли слева и DevTools справа"  
[ImageConsoleAfterEvaluating]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-change-button-text.msft.png "Рисунок 3: внешний вид консоли после вычисления выражения"  
[ImagePlayground]: /microsoft-edge/devtools-guide-chromium/media/console-javascript-example-console-playground.msft.png "На рисунке 4 показано, как выглядит консоль после вычисления приведенных выше выражений."  

<!-- links -->  

[DevToolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с сообщениями журнала на консоли"  
[DevToolsConsoleReference]: /microsoft-edge/devtools-guide-chromium/console/reference#run-javascript "Справочник по консоли"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium//console/utilities "Справочник по API для консольных программ"  

[DevToolsJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  

[2alityExpressionsVersusStatements]: https://2ality.com/2012/09/expressions-vs-statements.html "Выражения и операторы в JavaScript"  

[Esma6DefaultParameterValues]: https://es6-features.org/index#DefaultParameterValues "Значения параметров по умолчанию — обработка расширенных параметров-ECMAScript 6 — новые возможности: Общие сведения о сравнении &"  

[GlitchConsoleJavascriptExample]: https://microsoft-edge-chromium-devtools.glitch.me/static/console/javascript/index.html "Пример кода JavaScript на консоли | Цепь"  

[WikiReadEvalPrintLoop]: https://en.wikipedia.org/wiki/Read–eval–print_loop "Read – eval — цикл печати — Википедии"  

> [!NOTE]
> <span data-ttu-id="56836-172">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="56836-172">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="56836-173">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/javascript) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="56836-173">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/javascript) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="56836-175">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="56836-175">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
