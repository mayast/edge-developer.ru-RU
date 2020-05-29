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







# Начало работы с JavaScript на консоли   



В этом интерактивном учебнике показано, как запустить JavaScript на консоли Microsoft Edge DevTools.  Сведения о том, как вести журнал сообщений на консоли, можно найти в разделе [Начало работы с сообщениями журнала][DevToolsConsoleLoggingMessages] .  Сведения о том, как приостанавливать код JavaScript и переходить по одной строке за один раз, можно найти в статье [Начало работы с отладкой JavaScript][DevToolsJavascriptIndex] .  

> ##### Рис. 1  
> На **консоли**  
> ![На консоли][ImageConsole]  

## Обзор   

**Консоль** — это [REPL][WikiReadEvalPrintLoop], который означает чтение, оценку, печать и зацикливание.  Она считывает JavaScript, который вы вводите в него, оценивает код, выводит результат [выражения][2alityExpressionsVersusStatements]и осуществляет переход к первому шагу.  

## Настройка DevTools   

Этот учебник предназначен для того, чтобы открыть демонстрацию и попробовать все рабочие процессы самостоятельно.  После того как вы будете физически подписаться на нее, вы, наверное, захотите запомнить рабочие процессы позже.

1.  `Control` + `Shift` + `J` Чтобы открыть консоль, нажмите клавиши \ (Windows \) или `Command` + `Option` + `J` \ (macOS **Console**\).  
1.  Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **пример на консоли JavaScript** , чтобы открыть его в новом окне.  
    
    [Пример сценария на консоли][GlitchConsoleJavascriptExample]  
    
    > ##### Рисунок 2  
    > Страница примера JavaScript на консоли в левой части экрана и DevTools справа  
    > ![Страница примера JavaScript на консоли в левой части экрана и DevTools справа][ImageTutorialDevToolsJs]  

## Просмотр и изменение JavaScript или DOM страницы   

При сборке или отладке страницы часто бывает полезно запускать инструкции на **консоли** , чтобы изменить внешний вид или выполнение страницы.  
    
1.  Обратите внимание на текст на кнопке.  
1.  Введите текст `document.getElementById('hello').textContent = 'Hello, Console!'` в **консоли** и нажмите клавишу `Enter` , чтобы вычислить выражение.  Обратите внимание на то, как изменится текст внутри кнопки.  
    
    > ##### Рисунок3  
    > Внешний вид консоли после вычисления выражения  
    > ![Внешний вид консоли после вычисления выражения][ImageConsoleAfterEvaluating]  
    
    Под кодом, который вы проверили `"Hello, Console!"` .  Отзывайте 4 шага REPL: чтение, оценка, печать, цикл.  После оценки кода программа REPL выводит результат выражения.  Это `"Hello, Console!"` должно быть результатом вычисления `document.getElementById('hello').textContent = 'Hello, Console!'` .  
    
## Запуск произвольного кода JavaScript, не связанного со страницей   

Иногда требуется, чтобы код Песочница в том месте, где вы можете протестировать какой-либо код, или опробуйте новые возможности JavaScript, с которыми вы не знакомы.  Консоль — это идеальное место для экспериментов такого рода.  

1.  Введите текст `5 + 15` на консоли и нажмите клавишу `Enter` , чтобы вычислить выражение. Консоль печатает результат выражения под кодом.  **На рисунке 4** ниже показано, как будет выглядеть консоль после оценки этого выражения.  

1.  На **консоли**введите следующий код.  Попробуйте ввести его, а затем построчно, а не скопировав.  
    
    ```javascript
    function add(a, b=20) {
        return a + b;
    }
    ```  
    
    Если вы не знакомы с синтаксисом, ознакомьтесь со страницей [Определение значений по умолчанию для аргументов функции][Esma6DefaultParameterValues] `b=20` .  
    
1.  Теперь вызовите функцию, которая была только что определена.  
    
    ```javascript
    add(25);
    ```  
    
    > ##### Рисунок4  
    > Как выглядит консоль после вычисления приведенных выше выражений  
    > ![Как выглядит консоль после вычисления приведенных выше выражений][ImagePlayground]  
    
    `add(25)` вычисляется `45` , так как при `add` вызове функции без второго аргумента `b` равным ему присваивается значение по умолчанию `20` .  

## Дальнейшие действия   

<!--See [Run JavaScript][DevToolsConsoleReference] to explore more features related to running JavaScript in the Console.  -->  

<!--todo: add console reference (run javascript) section when available  -->  

DevTools позволяет приостановить выполнение сценария в центре выполнения.  Во время приостановки вы можете использовать **консоль** для просмотра и изменения `window` `DOM` страницы в данный момент времени.  Это обеспечивает мощный рабочий процесс отладки.  В разделе [Начало работы с отладкой JavaScript][DevToolsJavascriptIndex] для интерактивного учебника.  

Кроме того, **консоль** имеет набор удобных функций, которые облегчают взаимодействие с страницей.  Пример  

*   Вместо того `document.querySelector()` чтобы выделять элемент, введите `$()` .  Этот синтаксис имеет тот факт, что jQuery, но он не является jQuery.  Это просто псевдоним `document.querySelector()` .  
*   `debug(function)` фактически задает точку останова в первой строке этой функции.  
*   `keys(object)` Возвращает массив с ключами указанного объекта.  

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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/javascript) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
