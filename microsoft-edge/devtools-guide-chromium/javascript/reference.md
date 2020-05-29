---
title: Справочник по отладке JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 1d361bb39523e9b039500f46da54e60b82adbda6
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581742"
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







# Справочник по отладке JavaScript   



Вы узнаете о новых рабочих процессах отладки с полным справочником по функциям отладки Microsoft Edge DevTools.  

Подробнее об отладке можно найти [в статье Начало работы с отладкой JavaScript в Microsoft Edge DevTools][DevToolsJavascriptGetStarted] .  

## Приостановка кода с точки останова   

Установите точку останова, чтобы можно было приостановить выполнение кода в середине среды выполнения.  

Сведения о том, как задавать точки останова, можно найти в разделе [приостановка кода с точки останова][DevToolsJavascriptBreakpoints] .  

[DevToolsJavascriptBreakpoints]: breakpoints.md "Приостановка кода с точки останова в Microsoft Edge DevTools"  

## Пошаговое руководство по коду   

Когда код приостанавливается, проведите по одной строке за раз, изменяя поток управления и значения свойств по своему пути.  

### Шаг с заходом в строке кода   

При приостановке на строке, содержащей функцию, не относящуюся к проблеме, которую вы отлаживается, щелкните значок " **шаг за** ![ шагом", ][ImageStepOverIcon] чтобы запустить функцию без пошаговой отладки.  

> ##### Рис. 1  
> Выбор **пункта "шаг за шагом** "  
> ![Выбор пункта "шаг за шагом"][ImageSelectingStepOver]  

Например, предположим, что выполняется отладка следующего кода:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name); // D
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name; // C
}
```  

Вы приостанавливаете `A` .  Нажимая клавишу " **шаг за шагом**", DevTools запускает весь код в функции, для которой выполняется пошаговое выполнение, `B` а именно `C` .  Затем DevTools приостанавливает `D` .  

### Шаг с заходом в строку кода   

При приостановке в строке кода, содержащей вызов функции, связанный с проблемой, в которой выполняется отладка, щелкните значок **шаг** с заходом, ![ ][ImageStepIntoIcon] чтобы более подробно изучить эту функцию.  

> ##### Рисунок 2  
> Выбор **шага**  
> ![Выбор шага][ImageSelectingStepInto]  

Например, предположим, что выполняется отладка следующего кода:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName(); // A
    updateName(name);
}
function getName() {
    var name = app.first + ' ' + app.last; // B
    return name;
}
```  

Вы приостанавливаете `A` .  Нажимая кнопку " **Шаг с заходом**", DevTools запускает эту строку кода, а затем приостанавливает выполнение `B` .  

### Пошаговое руководство из строки кода   

При приостановке внутри функции, которая не связана с проблемой, которую вы выполняете Отладка, щелкните значок **шаг** с выходом, ![ ][ImageStepOutIcon] чтобы выполнить оставшуюся часть кода функции.  

> ##### Рисунок3  
> Выбор **пункта "шаг с выходом** "  
> ![Выбор пункта "шаг с выходом"][ImageSelectingStepOut]  

Например, предположим, что выполняется отладка следующего кода:  

```javascript
function updateHeader() {
    var day = new Date().getDay();
    var name = getName();
    updateName(name); // C
}
function getName() {
    var name = app.first + ' ' + app.last; // A
    return name; // B
}
```  

Вы приостанавливаете `A` .  Нажимая кнопку " **Шаг с выходом**", DevTools запускает оставшуюся часть кода в `getName()` `B` этом примере, а затем приостанавливает выполнение `C` .  

### Выполнение всего кода до определенной строки   

При отладке длительных функций может возникнуть большой объем кода, не относящегося к той проблеме, которую вы размещаете в отладке.  

Вы можете пошагово пройти все строки, но это утомительно.  Вы можете указать точку останова для строки кода в строке, в которой вы заинтересованы, и нажать на значок возобновления сценария "возобновить **выполнение** скрипта" ![ ][ImageResumeScriptExecutionIcon] , но это быстрее.  

Щелкните правой кнопкой мыши строку кода, в которой вы хотите заинтересовать, и выберите команду **продолжить**.  DevTools запускает весь код до этого момента, а затем приостанавливает выполнение на этой линии.  

> ##### Рисунок4  
> Выбор варианта **"перейти сюда"**  
> ![Выбор варианта "перейти сюда"][ImageSelectingContinueToHere]  

### Перезапустить функцию TOP в стеке вызовов   

Наведя указатель на строку кода, щелкните правой кнопкой мыши в любом месте области **стека звонков** и выберите команду **перезапустить кадр** , чтобы приостановить работу на первой строке функции Top в стеке вызовов.  Функция Top — это последняя вызываемая функция.  

Например, предположим, что выполняется пошаговое выполнение следующего кода:  

```javascript
function factorial(n) {
    var product = 0; // B
    for (var i = 1; i <= n; i++) {
      product += i;
    }
    return product; // A
}
```  

Вы приостанавливаете `A` .  После нажатия кнопки **перезапустить**вы должны быть приостановлены `B` , пока не задана точка останова или нажата клавиша **возобновления выполнения сценария**.  

> ##### Рисунок 5  
> Выбор **перезапуска кадра**  
> ![Выбор перезапуска кадра][ImageSelectingRestartFrame]  

### Среда выполнения сценария возобновления   

Чтобы продолжить выполнение после паузы в сценарии, щелкните значок "возобновить **сценарий запуска сценария** " ![ ][ImageResumeScriptExecutionIcon] .  DevTools запускает сценарий до следующей точки останова (при наличии).  

> ##### Рисунок6  
> Выбор **выполнения скрипта возобновления**  
> ![Выбор выполнения скрипта возобновления][ImageSelectingResumeScriptExecution]  

#### Выполнение принудительного выполнения сценария   

Чтобы пропустить все точки останова и принудительно возобновить выполнение сценария, нажмите и удерживайте значок возобновления **сценария "возобновить выполнение** скрипта", ![ ][ImageResumeScriptExecutionIcon] а затем выберите команду **принудительное** ![ выполнение сценария принудительной обработки ][ImageForceScriptExecutionIcon] .  

> ##### Рисунок7  
> Выбор **принудительного выполнения сценария**  
> ![Выбор принудительного выполнения сценария][ImageSelectingForceScriptExecution]  

### Изменить контекст потока   

При работе с веб-сотрудниками или сотрудниками служб щелкните контекст, указанный в области **потоки** , чтобы переключиться на этот контекст.  Синий значок стрелки соответствует контексту, выбранному в данный момент.  

> ##### Рисунок8  
> Область « **потоки** »  
> ![Область «потоки»][ImageThreadsPane]  

Например, предположим, что вы придерживаетесь точки останова как в основном, так и на рабочем скрипте службы.  Вы хотите просмотреть локальные и глобальные свойства для контекста рабочего процесса службы, но на панели **источники** отображается контекст основного сценария.  Нажимая кнопку "сервисный рабочий процесс" на панели " **потоки** ", вы сможете перейти в этот контекст.  

## Просмотр и изменение локальных, закрытых и глобальных свойств   

При приостановке в строке кода используйте область **область** для просмотра и изменения значений свойств и переменных в локальных, закрытых и глобальных областях.  

*   Дважды щелкните значение свойства, чтобы изменить его.  
*   Неперечислимые свойства затенены.  

> ##### Рисунок9  
> Область " **область** "  
> ![Область "область"][ImageScopePane]  

## Просмотр текущего стека вызовов   

При приостановке на строке кода используйте область **Стек вызовов** для просмотра стека вызовов, в котором вы набрались этим моментом.  

<!--If you are working with async code, check the **Async** checkbox to enable async call stacks.  -->  

Щелкните запись, чтобы перейти к строке кода, в которой была вызвана эта функция.  Синий значок стрелки показывает, какая функция DevTools выделяется в данный момент.  

> ##### Рисунок 10  
> Область « **Стек вызовов** »  
> ![Область «стек вызовов»][ImageCallStackPane]  

> [!NOTE]
> Если в строке кода не присвоена значение, область **стека вызовов** пуста.  

### Копирование трассировки стека   

<!--
This should be moved to an "Export debug data" H2 section when there is enough content for that, but there is not right now, so it is here.
-->

Щелкните правой кнопкой мыши в любом месте области **стека звонков** и выберите команду **Копировать трассировку стека** , чтобы скопировать текущий стек вызовов в буфер обмена.  

> ##### Рисунок11  
> Выбор пункта « **Копировать трассировку стека** »  
> ![Выбор пункта «Копировать трассировку стека»][ImageSelectingCopyStackTrace]  

Ниже приведен пример выходных данных.  

```javascript
getNumber1 (get-started.js:35)
inputsAreEmpty (get-started.js:22)
onClick (get-started.js:15)
```  

## Игнорировать сценарий или шаблон сценариев  

Помечайте сценарий как код библиотеки, если вы хотите пропустить этот сценарий во время отладки.  При пометке в виде кода библиотеки сценарий скрывается в области **стека вызовов** , и вы никогда не просматриваете функции сценария при пошаговом выполнении кода.  

Например, предположим, что выполняется пошаговое выполнение следующего кода:  

```javascript
function animate() {
    prepare();
    lib.doFancyStuff(); // A
    render();
}
```  

`A` — это библиотека стороннего поставщика, которой вы доверяете.  Если вы уверены, что проблема, выполняемая при отладке, не связана с библиотекой стороннего поставщика, имеет смысл помечать сценарий как **код библиотеки**.  

### Пометка сценария как кода библиотеки в области "редактор"  

Чтобы помечать сценарий как **код библиотеки** на панели " **Редактор** ", выполните указанные ниже действия.  

1.  Откройте файл.  
1.  Щелкните правой кнопкой мыши в любом месте.  
1.  Нажмите кнопку **помечать как код библиотеки**.  

> ##### Рисунок12  
> Пометка сценария как **кода библиотеки** в области " **Редактор** "  
> ![Пометка сценария как кода библиотеки в области "редактор"][ImageMarkEditorPane]  

### Пометка сценария как кода библиотеки на панели «стек вызовов»  

Чтобы помечать сценарий как **код библиотеки** на панели « **стек звонков** », выполните указанные ниже действия.  

1.  Щелкните правой кнопкой мыши функцию в сценарии.  
1.  Нажмите кнопку **помечать как код библиотеки**.  

> ##### Рисунок13  
> Пометка сценария как **кода библиотеки** на панели « **Стек вызовов** »  
> ![Пометка сценария как кода библиотеки на панели «стек вызовов»][ImageMarkCallStackPane]  

### Пометка сценария как кода библиотеки из параметров  

Чтобы помечать один сценарий или шаблон сценариев из параметров, выполните указанные ниже действия.  

1.  Откройте [Параметры][DevToolsCustomize].  
1.  Перейдите на вкладку **код библиотеки** .  
1.  Нажмите кнопку **Добавить узор**.  
1.  Введите имя сценария или шаблон регулярного выражения для имен сценариев, чтобы помечать его как **код библиотеки**.  
1.  Щелкните **Добавить**.  

> ##### Рисунок14  
> Пометка сценария как **кода библиотеки** из параметров  
> ![Пометка сценария как кода библиотеки из параметров][ImageMarkScriptSettings]  

## Выполнение фрагментов кода отладки на любой странице   

Если вы обнаружите, что вы используете один и тот же код отладки в консоли, рассматривайте фрагменты кода.  Фрагменты — это сценарии среды выполнения, созданные, сохраняемые и выполняемые в DevTools.  

Дополнительные сведения можно найти в разделе [выполнение фрагментов кода на любой странице][DevToolsJavascriptSnippets] .  

## Просмотр значений настраиваемых выражений JavaScript   

Используйте область **контрольных** значений для просмотра значений настраиваемых выражений.  Вы можете просмотреть любое допустимое выражение JavaScript.  

> ##### Рисунок15  
> Область **контрольных значений**  
> ![Область контрольных значений][ImageWatchPane]  

*   Щелкните значок Добавить **выражение** ![ Добавить выражение ][ImageAddExpressionIcon] , чтобы создать новое выражение контрольного значения.  
*   Щелкните значок **обновления** обновления ![ ][ImageRefreshIcon] , чтобы обновить значения всех существующих выражений.  Значения автоматически обновляются при пошаговом выполнении кода.  
*   Наведите указатель мыши на выражение и щелкните значок **Удалить** выражение удаления выражения, ![ ][ImageDeleteExpressionIcon] чтобы удалить его.  

## Создание читаемого файла minified   

Щелкните значок формата **формата** ![ ][ImageFormatIcon] , чтобы сделать файл minified удобным для чтения.  

> ##### Рисунок16  
> Кнопка " **Формат** "  
> ![Кнопка "формат"][ImageFormat]  

## Изменение сценария   

При исправлении ошибки часто требуется протестировать некоторые изменения в коде JavaScript.  Вам не нужно вносить изменения в внешний редактор или интегрированную среду разработки и повторно загрузить страницу.  Вы можете редактировать сценарий в DevTools.  

Чтобы изменить сценарий, выполните указанные ниже действия.  

1.  Откройте файл в области " **Редактор** " на панели " **источники** ".  
1.  Внесите изменения в область " **Редактор** ".  
1.  Чтобы сохранить, нажмите клавиши `Ctrl` + `S` \ (Windows \) или `Command` + `S` \ (macOS \).  DevTools заменяет весь JS – файл в механизме JavaScript Microsoft Edge.  

> ##### Рисунок17  
> Область " **Редактор** "  
> ![Область "редактор"][ImageEditorPane]  

## Отключение JavaScript   

[В разделе Отключение JavaScript с Microsoft Edge DevTools][DevToolsJavascriptDisable].  

<!--## Feedback   -->  



<!-- image links -->  

[ImageStepOverIcon]: /microsoft-edge/devtools-guide-chromium/media/step-over-icon.msft.png  
[ImageStepIntoIcon]: /microsoft-edge/devtools-guide-chromium/media/step-into-icon.msft.png  
[ImageStepOutIcon]: /microsoft-edge/devtools-guide-chromium/media/step-out-icon.msft.png  
[ImageResumeScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-run-icon.msft.png  
[ImageForceScriptExecutionIcon]: /microsoft-edge/devtools-guide-chromium/media/force-script-run-icon.msft.png  
[ImageAddExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/add-expression-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageDeleteExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-expression-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  

[ImageSelectingStepOver]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-over-next-function-call.msft.png "Рисунок 1: выбор пункта "шаг за шагом""  
[ImageSelectingStepInto]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-into-next-function-call.msft.png "Рисунок 2: выбор пункта "шаг""  
[ImageSelectingStepOut]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-step-out-of-current-function.msft.png "Рисунок 3: выбор пункта "шаг с выходом""  
[ImageSelectingContinueToHere]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-continue-to-here.msft.png "Рисунок 4: выбор варианта перейти сюда"  
[ImageSelectingRestartFrame]: /microsoft-edge/devtools-guide-chromium/media/javascript-source-page-debugger-restart-frame.msft.png "Рисунок 5: выбор перезапуска кадра"  
[ImageSelectingResumeScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-resume-script-runtime.msft.png "Рисунок 6: выбор выполнения сценария возобновления"  
[ImageSelectingForceScriptExecution]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-force-script-runtime.msft.png "Рисунок 7: выбор принудительного выполнения сценария"  
[ImageThreadsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-main-min-js-threads.msft.png "Рисунок 8: область "потоки""  
[ImageScopePane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-scope.msft.png "Рисунок 9: область "область""  
[ImageCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty.msft.png "Рисунок 10: область стека звонков"  
[ImageSelectingCopyStackTrace]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-copy-stack-trace.msft.png "Рисунок 11: выбор пункта "Копировать трассировку стека""  
[ImageMarkEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-editor-mark-as-library-code.msft.png "Рисунок 12: Пометка сценария как кода библиотеки в области "редактор""  
[ImageMarkCallStackPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-glitch-debug-js-sources-get-started-inputs-are-empty-call-stack-mark-as-library-code.msft.png "Рис. 13: Пометка сценария как кода библиотеки в области стека вызовов"  
[ImageMarkScriptSettings]: /microsoft-edge/devtools-guide-chromium/media/javascript-framework-library-code.msft.png "Рисунок 14: Пометка сценария как кода библиотеки из параметров"  
[ImageWatchPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-get-started-js-watch.msft.png "Рисунок 15: область контрольных значений"  
[ImageFormat]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-non-minified.msft.png "Рисунок 16: кнопка "формат""  
[ImageEditorPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-html-minified.msft.png "Рисунок 17: область "редактор""  

<!-- links -->  

[DevToolsJavascriptDisable]: disable.md "Отключение JavaScript с помощью Microsoft Edge DevTools"  
[DevToolsJavascriptGetStarted]: index.md "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  
[DevToolsJavascriptSnippets]: snippets.md "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools"  

[DevToolsCustomize]: ../customize/index.md "Настройка Microsoft Edge DevTools"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
