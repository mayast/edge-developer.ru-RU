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





# Справочник по API для консольных программ   



API консоли содержат набор удобных команд для выполнения распространенных задач: выбор и анализ элементов DOM, отображение данных в удобочитаемом формате, остановка и запуск профилировщика, а также наблюдение за событиями DOM.  

> [!WARNING]
> Следующие команды работают только на консоли Microsoft Edge DevTools.  Команды не работают при запуске из ваших сценариев.  

Ищете `console.log()` `console.error()` и другие `console.*` методы?  См.: [Справочник по API для консольных интерфейсов][DevToolsConsoleApi].  

## Последнее вычисленное выражение  

```console
$_
```  

Возвращает значение последнего вычисленного выражения.  

На [рисунке 1](#figure-1)вычисляется простое выражение \ ( `2 + 2` \).  `$_`Затем вычисляется свойство, которое содержит одно и то же значение.  

> ##### Рис. 1  
> `$_` — Это последнее вычисленное выражение  
> ![$ _ — это последнее вычисленное выражение][ImageRecentExpression]  

На [рисунке 2](#figure-2)вычисленное выражение изначально включает массив имен.  Вычисление `$_.length` для определения длины массива, значение, хранящееся в `$_` изменениях, становится последним вычисленным выражением `4` .  

> ##### Рисунок 2  
> `$_` изменения при вычислении новых команд  
> ![$ _ изменения при вычислении новых команд][ImageChangedRecentExpression]  

## Недавно выбранный элемент или объект JavaScript  

```console
$0
```  

Возвращает последний выбранный элемент или объект JavaScript.  `$1` Возвращает второй, последний выбранный элемент и т. д.  Команды,,, и, Кроме того, `$0` `$1` работают в `$2` `$3` `$4` виде исторических ссылок на последние пять элементов DOM, проверенных на панели **элементов** , или последние пять объектов кучи JavaScript, выбранных на панели " **память** ".  

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

На [рисунке 3](#figure-3) `img` выделен элемент на панели **элементы** .  В ящике **консоли** `$0` вычисляется и отображается один и тот же элемент.  

> ##### Рисунок3  
> Параметр `$0`  
> ![$0][ImageElement0]  

На [рисунке 4](#figure-4)показан другой элемент, выбранный на той же странице.  `$0`Теперь он ссылается на только что выбранный элемент, то `$1` есть возвращает ранее выбранное.  

> ##### Рисунок4  
> Параметр `$1`  
> ![$1][ImageElement1]  

## Область выбора запроса  

```console
$(selector, [startNode])
```  

Возвращает ссылку на первый элемент DOM с указанным селектором CSS.  Этот метод является псевдонимом метода [Document. querySelector ()][MDNDocumentQuerySelector] .  

На [рисунке 5](#figure-5)возвращается ссылка на первый `<img>` элемент в документе.  

> ##### Рисунок 5  
> Параметр `$('img')`  
> ![$ ("Img")][ImageElementImg]  

Щелкните возвращенный результат правой кнопкой мыши и выберите пункт **Показать на панели элементов** , чтобы найти его в DOM, или **прокрутите** страницу, чтобы отобразить ее на странице.  

На [рисунке 6](#figure-6)возвращается ссылка на текущий выбранный элемент, и отображается свойство src.  

> ##### Рисунок6  
> Параметр `$('img').src`  
> ![$ ("Img"). src][ImageElementImgSource]  

Этот метод также поддерживает второй параметр, startNode, задающий "элемент" или узел, из которого следует искать элементы.  Значение этого параметра по умолчанию — `document` .  

На [рисунке 7](#figure-7)первый `img` элемент найден после элемента `title--image` и отображается `src` правильно.  

> ##### Рисунок7  
> $ ("Img", Document. querySelector ("Title--Image")). src  
> ![$ ("Img", Document. querySelector ("Title--Image")). src][ImageElementImgNodeSource]  

> [!NOTE]
> Если вы используете библиотеку, например jQuery, которая используется `$` , эта функция перезаписывается и `$` соответствует реализации из этой библиотеки.  

## Выбор запроса  

```console
$$(selector, [startNode])
```  

Возвращает массив элементов, которые соответствуют указанному селектору CSS.  Этот метод эквивалентен вызову метода [Document. querySelectorAll ()][MDNDocumentQuerySelectorAll] .  

На [рисунке 8](#figure-8)используйте `$$()` для создания массива всех `<img>` элементов в текущем документе и отображения значения `src` свойства для каждого элемента.  

```console
var images = $$('img');
for (each in images) {
    console.log(images[each].src);
}
```  

> ##### Рисунок8  
> Использование `$$()` для выбора всех изображений в документе и отображения источников  
> ![Использование $ $ () для выбора всех изображений в документе и отображения источников][ImageArrayElementImgSource]  

Этот метод также поддерживает второй параметр, startNode, указывающий элемент или узел, из которого нужно выполнить поиск элементов.  Значение этого параметра по умолчанию — `document` .  

На [рисунке 9](#figure-9)измененная версия [рисунка 8](#figure-8) используется `$$()` для создания массива всех `<img>` элементов, которые отображаются в текущем документе после выбранного узла.  

```console
var images = $$('img', document.querySelector(`title--image`));
for (each in images) {
   console.log(images[each].src);
}
```  

> ##### Рисунок9  
> Использование `$$()` для выбора всех изображений, которые отображаются после указанного `<div>` элемента в документе, и отображения источников  
> ![Использование $ $ () для выбора всех изображений, которые отображаются после указанного <div> элемента в документе и отображения источников][ImageArrayElementImgNodeSource]  

> [!NOTE]
> Нажмите клавишу `Shift` + `Enter` консоль, чтобы начать новую строку, не выполняя сценарий.  

## Выражения  

```console
$x(path, [startNode])
```  

Возвращает массив элементов DOM, соответствующих указанному выражению XPath.  

На [рис. 10](#figure-10) `<p>` возвращаются все элементы на странице.  

```console
$x("//p")
```  

> ##### Рисунок 10  
> Использование селектора XPath  
> ![Использование селектора XPath][ImageArrayXpath]  

На [рисунке 11](#figure-11) `<p>` возвращаются все элементы, содержащие `<a>` элементы.  

```console
$x("//p[a]")
```  

> ##### Рисунок11  
> Использование более сложного селектора XPath  
> ![Использование более сложного селектора XPath][ImageArrayXpathChild]  

Как и другие команды Selector, `$x(path)` имеет дополнительный второй параметр, `startNode` указывающий на элемент или узел, из которого нужно выполнить поиск элементов.  

> ##### Рисунок12  
> Использование селектора XPath с `startNode`  
> ![Использование селектора XPath с startNode][ImageArrayXpathNode]  

## Сброс  

```console
clear()
```  

Очищает консоль журнала.  

```console
clear()
```  

## copy  

```console
copy(object)
```  

`copy(object)`Метод копирует строковое представление указанного объекта в буфер обмена.  

```console
copy($0)
```  

## отладка  

```console
debug(method)
```  

>[!NOTE]
> [#1050237 проблема с Chromium][MonorailIssue1050237] отслеживает ошибку с `debug()` функцией.  Если вы столкнулись с этой проблемой, попробуйте использовать вместо нее [точки останова][DevtoolsJavascriptBreakpoints] .  

Когда вы запрашиваете указанный метод, отладчик вызывается и останавливается внутри метода на панели « **источники** », что позволяет пошагово пройти этот код и выполнить его отладку.  

```console
debug("debug");
```  

> ##### Рисунок13  
> Прерывание внутри метода с `debug()`  
> ![Прерывание в методе с помощью Debug ()][ImageDebugMethod]  

Используйте `undebug(method)` для прекращения прерывания на методе или с помощью пользовательского интерфейса, чтобы отключить все точки останова.  

Дополнительные сведения о точках останова можно найти в разделе [приостановка кода с точки останова][DevToolsJavascriptBreakpoints].  

## dir  

```console
dir(object)
```  

Отображает список всех свойств указанного объекта в стиле объекта.  Этот метод является псевдонимом для метода [Console. dir ()][MDNConsoleDir] .  

Вычислите `document.head` текст на консоли, чтобы отобразить HTML `<head>` между `</head>` тегами и.  На [рисунке 14](#figure-14)после использования на консоли отображается вхождение стиля объекта `console.dir()` .  

```console
document.head;
dir(document.head);
```  

> ##### Рисунок14  
> Ведение журнала `document.head` с помощью `dir()` метода  
> ![Ведение журнала. Head с помощью метода dir ()][ImageLogObject]  

Дополнительные сведения можно найти в описании [`console.dir()`][DevToolsConsoleApiConsoleDirObject] записи в API-интерфейсе консоли.  

## dirxml  

```console
dirxml(object)
```  

Печатает XML-представление указанного объекта, как показано на вкладке **элементы** .  Этот метод эквивалентен методу [Console. DirXML ()][MDNConsoleDirxml] .  

## Проверка  

```console
inspect(object/method)
```  

Открывает и выбирает определенный элемент или объект на соответствующей панели: либо панель **элементов** для элементов DOM, либо панель **памяти** для объектов кучи JavaScript.  

На [рис. 15](#figure-15) `document.body` откроется панель **элементы** .  

```console
inspect(document.body);
```  

> ##### Рисунок15  
> Проверка элемента с помощью `inspect()`  
> ![Проверка элемента с помощью проверки ()][ImageInspectElement]  

При передаче метода для проверки метод открывает документ, находящийся на панели « **источники** », для проверки.  

## getEventListeners  

```console
getEventListeners(object)
```  

Возвращает прослушиватели событий, зарегистрированные для указанного объекта.  Возвращаемое значение — это объект, который содержит массив для всех зарегистрированных типов событий \ (например, `click` или `keydown` \).  Каждый из этих массивов — это объекты, которые описывают прослушиватель, зарегистрированный для каждого типа.  На [рисунке 16](#figure-16)перечислены все прослушиватели событий, зарегистрированные на объекте Document.  

```console
getEventListeners(document);
```  

> ##### Рисунок16  
> Вывод на печать `getEventListeners(document)`  
> ![Вывод на печать с использованием getEventListeners (документ)][ImageGetListeners]  

Если в указанном объекте зарегистрировано более одного прослушивателя, то массив содержит элемент для каждого прослушивателя.  На [рисунке 16](#figure-16)в элементе Document для события зарегистрированы два прослушивателя событий `click` .  

> ##### Рисунок17  
> Несколько прослушивателей  
> ![Несколько прослушивателей][ImageMultipleListeners]  

Вы можете расширить каждый из указанных ниже объектов, чтобы просмотреть свойства.  

> ##### Рис. 18  
> Развернутое представление объекта прослушивателя  
> ![Развернутое представление объекта прослушивателя][ImageListenersExpanded]  

## клавиши  

```console
keys(object)
```  

Возвращает массив, содержащий имена свойств, принадлежащих указанному объекту.  Чтобы получить связанные значения одинаковых свойств, используйте `values()` .  

Например, предположим, что приложение определило следующий объект.  

```console
var player1 = { "name":  "Ted", "level": 42 }
```  

На [рис. 19](#figure-19)результат `player1` определен в глобальном пространстве имен \ (для простоты) перед вводом `keys(player1)` и `values(player1)` на консоли.  

```console
keys(player1)
```  

```console
values(player1)
```  

> ##### На рисунке 19  
> `keys()`Команды и `values()`  
> ![Команды Keys () и Values ()][ImageConsoleKeysValues]  

## монитор  

```console
monitor(method)
```  

Заносит в консоль сообщение, которое указывает имя метода вместе с аргументами, передаваемыми методу при его вызове.  

```console
function sum(x, y) {
    return x + y;
}
monitor(sum);
```  

> ##### Рис. 20  
> `monitor()`Метод  
> ![Метод Monitor ()][ImageConsoleMonitorSum]  

Используется `unmonitor(method)` для прекращения наблюдения.  

## monitorEvents  

```console
monitorEvents(object[, events])
```  

Когда в указанном объекте происходит одно из указанных событий, объект события регистрируется в консоли.  Вы можете указать одно событие для отслеживания, массив событий или один из типов универсальных событий, сопоставленных с предопределенной коллекцией событий.  Посмотрите [Рисунок 21](#figure-21).  

Ниже приведено наблюдение за всеми событиями изменения размера объекта Window.  

```console
monitorEvents(window, "resize");
```  

> ##### Рисунок 21  
> Наблюдение за событиями изменения размера окна  
> ![Наблюдение за событиями изменения размера окна][ImageMonitorResize]  

В следующем примере определяется массив для мониторинга обоих `resize` и `scroll` событий в объекте Window.  

```console
monitorEvents(window, ["resize", "scroll"]);
```  

Вы также можете указать один из доступных типов событий — строки, которые сопоставляются с предопределенными наборами событий.  В приведенной ниже таблице показаны типы доступных событий и сопоставлений связанных событий.  

| Тип события | Соответствующие сопоставленные события |  
|:--- |:--- |  
| `mouse` | "Click", "DblClick", "MouseDown", "MouseMove", "указатель мыши", "onmouseover", "MouseUp", "MouseWheel" |  
| `key` | "KeyDown", "нажатие клавиши", "KeyUp", "textInput" |  
| `touch` | "touchcancel", "touchend", "touchmove", "touchstart" |  
| `control` | "Размытие", "Изменить", "фокусировку", "прокрутка", "выделить", "Отправить", "выбрать", "Отправить", "с масштабом" |  

На [рисунке 22](#figure-22)на `key` `key` панели **элементы** выделены типы событий, соответствующие событиям текстового поля ввода.  

```console
monitorEvents($0, "key");
```  

На [рисунке 22](#figure-22) показан пример выходных данных после ввода символа в текстовом поле.  

> ##### Рис. 22  
> Контроль событий ключа  
> ![Контроль событий ключа][ImageMonitorKey]  

## профиль  

```console
profile([name])
```  

Запускает сеанс профилирования ЦП JavaScript с необязательным именем.  Метод [profileEnd ()](#profileend) завершает профиль и отображает результаты на панели **памяти** .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Запустите `profile()` метод, чтобы начать профилирование.  
    
    ```console
    profile("My profile")
    ```  
    
1.  Запустите метод [profileEnd ()](#profileend) , чтобы остановить профилирование и отобразить результаты на панели **памяти** .  

Профили также могут быть вложенными.  На [рисунке 23](#figure-23) результат одинаков, независимо от того, где находится заказ.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

> [!NOTE]
> Несколько профилей ЦП могут работать одновременно, и вы не обязаны закрывать каждый из них в заказе на создание.  

## profileEnd  

```console
profileEnd([name])
```  

Завершает сеанс профилирования ЦП JavaScript и отображает результаты на панели **памяти** .  Необходимо запустить метод [Profile ()](#profile) .  <!--See also [Speed Up JavaScript Runtime][DevToolsRenderingToolsJSRuntime].  -->  

1.  Запустите метод [Profile ()](#profile) , чтобы начать профилирование.  
1.  Запустите `profileEnd()` метод, чтобы остановить профилирование и отобразить результаты на панели **памяти** .  
    
    ```console
    profileEnd("My profile")
    ```  

Профили также могут быть вложенными.  На [рисунке 23](#figure-23) результат одинаков, независимо от того, где находится заказ.  

```console
profile('A');
profile('B');
profileEnd('A');
profileEnd('B');
```  

Результат появится в виде снимка кучи на панели " **память** ".  

> ##### Рис. 23  
> Сгруппированные профили  
> ![Сгруппированные профили][ImageGroupedProfiles]  

> [!NOTE]
> Несколько профилей ЦП могут работать одновременно, и вы не обязаны закрывать каждый из них в заказе на создание.  

## таблич  

```console
table(data[, columns])
```  

Заносит в журнал объектные данные с форматированием таблицы, основанным на объекте данных, с помощью необязательных заголовков столбцов.  На [рисунке 24](#figure-24)показан список имен, использующих таблицу на консоли.  

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

> ##### Рисунок 24  
> `table()`Метод  
> ![Метод Table ()][ImageConsoleTable]  

## Отладка  

```console
undebug(method)
```  

Прекращает отладку указанного метода, поэтому при вызове метода отладчик больше не вызывается.  

```console
undebug(getData);
```  

## отследить  

```console
unmonitor(method)
```  

Останавливает мониторинг указанного метода.  Используется совместно с методом [Monitor ()](#monitor) .  

```console
unmonitor(getData);
```  

## unmonitorEvents  

```console
unmonitorEvents(object[, events])
```  

Прекращает наблюдение за событиями для указанного объекта и событий.  Например, в приведенном ниже примере останавливается отслеживание всех событий в объекте Window.  

```console
unmonitorEvents(window);
```  

Вы также можете отключить наблюдение за определенными событиями для объекта.  Например, следующий код начинает наблюдать за всеми `mouse` событиями выбранного в данный момент элемента, а затем останавливает наблюдение за `mousemove` событиями (возможно, чтобы уменьшить шум в выходных данных консоли \).  

```console
monitorEvents($0, "mouse");
unmonitorEvents($0, "mousemove");
```  

## данные  

```console
values(object)
```  

Возвращает массив, содержащий значения всех свойств, принадлежащих указанному объекту.  

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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/utilities) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
