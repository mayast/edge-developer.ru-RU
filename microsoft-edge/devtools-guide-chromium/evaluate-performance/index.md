---
title: Приступая к анализу производительности среды выполнения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: bff2d2fb0ff8424303289183ca8c5935ef477381
ms.sourcegitcommit: 50991a04c18283a8890ae33fcc3491c0476c7684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611743"
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







# Приступая к анализу производительности среды выполнения   



> [!NOTE]
> Сведения о том, как ускорить загрузку страниц, можно найти в разделе [Оптимизация веб-сайта][DevtoolsSpeedGetStarted] .  

Производительность во время выполнения — это то, как страница выполняется при ее запуске, а не в виде загрузки.  В этом учебнике объясняется, как использовать панель производительности Microsoft Edge DevTools для анализа производительности среды выполнения.  В плане модели **салазок** уровни опыта, описанные в этом учебнике, полезны для анализа отклика, анимации и этапов простоя страницы.  

<!--todo: add rail link when section is ready -->  

## Начало работы   

В этом учебнике вы откроете DevTools на реальной странице и с помощью панели Performance (производительность) найдите узкие места в производительности на странице.  

1.  Откройте Microsoft EDGE в **режиме InPrivate**.  Режим InPrivate обеспечивает выполнение Microsoft EDGE в чистом состоянии.  Например, если на вашем компьютере установлено большое количество расширений, это может привести к снижению производительности с помощью этих расширений.  
    
    <!--TODO: replace section when updated for new Edge  -->
    
1.  Загрузите следующую страницу в окне InPrivate.  Это демонстрационный ролик, для которого вы собираетесь профилировать.  На странице показан ряд маленьких значков, перемещаясь вверх и вниз.  
    
    ```https
    https://microsoft-edge-chromium-devtools.glitch.me/jank/
    ```  
    
1.  `Control` + `Shift` + `I` Чтобы открыть DevTools, нажмите клавиши \ (Windows \) или `Command` + `Option` + `I` \ (macOS \).  
    
    > ###### Рис. 1  
    > Демонстрация слева и DevTools справа  
    > ![Демонстрация слева и DevTools справа][ImageGetStarted]  
    
    > [!NOTE]
    > Для остальных снимков DevTools [отсоединяется в отдельном окне][DevtoolsCustomizePlacement] , и вы сможете лучше видеть содержимое.  
    
### Имитация мобильного ЦП  

На мобильных устройствах больше энергии ЦП, чем на настольных компьютерах и ноутбуках.  Каждый раз, когда вы профилем страницы, используйте метод регулирования ЦП для моделирования того, как страница работает на мобильных устройствах.  

1.  В DevTools откройте вкладку **производительность** .  
1.  Убедитесь, что флажок **снимки экрана** включен.  
1.  Нажмите кнопку Параметры захвата **параметров** ![ ][ImageCaptureSettingsIcon] .  DevTools показывает параметры, связанные с тем, как они захватывают метрики производительности.  
1.  На вкладке **ЦП**выберите пункт **замедление 4X**.  DevTools загружает ЦП так, чтобы он был 4 медленнее, чем обычно.  
    
    > ###### Рисунок 2  
    > Регулировка скорости ЦП  
    > ![Регулировка скорости ЦП][ImageCPUThrottling]  
    
    > [!NOTE]
    > При тестировании других страниц, чтобы убедиться в том, что они работают на мобильных устройствах с низким энергопотреблением, настройте для ускорения ЦП **6X замедление**.  Эта демонстрация не подходит для 6xного замедления, поэтому она просто использует 4X замедления для целей обучения.  
    
### Настройка ролика  

Очень сложно создать демонстрацию производительности во время выполнения, который постоянно подходит всем читателям этого веб-сайта.  Этот раздел позволяет настроить демонстрацию, чтобы убедиться в том, что взаимодействие с изображениями и описаниями, которые вы видите в этом учебнике, не зависит от настройки.

1.  Продолжайте нажимать кнопку " **Добавить 10** ", пока синие значки не перемещаются заметно ниже.  На высоком уровне компьютера может потребоваться около 20 щелчков мыши.  
1.  Нажмите кнопку **оптимизировать**.  Синие значки должны двигаться быстрее и более гладко.  

    > [!NOTE]
    > Если вы не видите заметную разницу между оптимизированными и неоптимизированными версиями, попробуйте выбрать команду **вычесть 10** несколько раз и повторить попытку.  
    > Если вы добавите слишком много синих значков, вы просто сможете максимально использовать ЦП, и вы не будете видеть существенные различия в результатах двух версий.  

1.  Нажмите **Отмена оптимизации**.  Синие значки перемещаются медленнее и более Jank еще раз.  

### Запись производительности среды выполнения   

Когда вы запустили оптимизированную версию страницы, синие значки перемещаются быстрее.  
Почему так?  Обе версии предназначены для того, чтобы переместить значки в одинаковые промежутки времени.  Чтобы выяснить, как выявить узкие места производительности в неоптимизированной версии, сделайте запись на панели производительности.  

1.  В **DevTools нажмите запись Record (запись)** ![ ][ImageRecordIcon] .  
    DevTools захватывает метрики производительности по мере выполнения страницы.  
    
    > ###### Рисунок3 
    > Профилирование страницы  
    > ![Профилирование страницы][ImagePageProfiling]  
    
1.  Подождите несколько секунд.  
1.  Нажмите кнопку **остановить**.  DevTools останавливает запись, обрабатывает данные, а затем отображает результаты на панели Performance.  
    
    > ###### Рисунок4  
    > Результаты профиля  
    > ![Результаты профиля][ImageProfileResults]  

Wow, это является большим объемом данных.  Не беспокойтесь, это будет очень полезно в скором времени.  

## Анализ результатов   

После того как вы загрузили производительность страницы, вы можете оценить, насколько низкая производительность страницы, и найти причины.  

### Анализ кадров в секунду  

Основная метрика для измерения производительности любой анимации — число кадров в секунду с повтором (кадр/с).  Пользователи будут рады, что анимации работают в 60 кадр/с.  

1.  Посмотрите на диаграмму в **кадре** .  Если вы видите красную полосу над **кадром кадров**, это означает, что частота кадров, отброшенных таким образом, что она может повредить взаимодействие с пользователем.  Как правило, чем больше зеленая полоса, тем выше кадр кадров.  
    
    > ###### Рисунок 5  
    > Диаграмма кадр/с  
    > ![Диаграмма кадр/с][ImageFPSChart]  

1.  Под диаграммой с **кадром кадров** вы видите диаграмму **ЦП** .  Цвета на диаграмме **ЦП** соответствуют цветам на вкладке " **Сводка** " в нижней части панели "производительность".  Тот факт, что диаграмма **ЦП** заполнена цветом, означает, что ЦП был maxed во время записи.  Всякий раз, когда вы видите maxed ЦП в течение длительного времени, это подсказка для поиска способов уменьшения объема работы.  
    
    > ###### Рисунок6  
    > Вкладка "Диаграмма ЦП" и "Сводка"  
    > ![Вкладка "Диаграмма ЦП" и "Сводка"][ImageCPUSummary]  

1.  Наведите указатель мыши на диаграммы **кадров**, **ЦП**и **сети** .  В DevTools показан снимок страницы на данный момент времени.  Чтобы воспроизвести запись, передвиньте указатель влево и вправо.  Это называется чисткум, и его можно использовать для анализа хода анимации вручную.  
    
    > ###### Рисунок7  
    > Просмотр снимка страницы в 2500ms отметке записи  
    > ![Просмотр снимка страницы в 2500ms отметке записи][ImageViewingScreenshot]  

1.  В разделе **кадры** наведите указатель мыши на один из зеленых квадратиков.  DevTools показывает, что этот конкретный кадр находится в кадре/сек.  Скорее всего, каждый кадр расположен ниже целевого числа 60 кадр/с.  
    
    > ###### Рисунок8  
    > Наведение указателя мыши на рамку  
    > ![Наведение указателя мыши на рамку][ImageFrameHover]  

Разумеется, в этом ролике очень очевидно, что страница не работает хорошо.  Но в реальных сценариях это может быть не так, поэтому все эти средства помогут вам сделать измерения весьма удобными.  

#### Премия: открытие индикатора кадров  

Еще одним удобным инструментом является индикатор между КАДРами, который обеспечивает оценки в реальном времени при выполнении страницы.  

1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).  
1.  Начните вводить текст `Rendering` в меню команд и выберите пункт **Показать отрисовку**.  
1.  На вкладке " **рендеринг** " Включите **индикатор кадров**.  В правом верхнем углу окна просмотра появится новая наложение.  
    
    > ###### Рисунок9  
    > Индикатор кадров в кадре  
    > ![Индикатор кадров в кадре][ImageFPSMeter]  

1.  Отключите **индикатор кадров** , а затем нажмите `Escape` , чтобы закрыть вкладку **рендеринг** .  Вы не будете использовать его в этом учебнике.  

### Определение узкого места  

Теперь, когда вы проверили, что анимация не работает, следующий вопрос для ответа: почему?  

1.  Обратите внимание на вкладку Сводка.  Если не выбрано ни одного события, на этой вкладке показана разбивка действий.  Страница потратила большую часть ее отображения времени.  Так как производительность — это изображение, которое уменьшает трудозатраты, цель состоит в том, чтобы уменьшить время, затраченное на обработку результатов.  
    
    > ###### Рисунок 10  
    > Вкладка "Сводка"  
    > ![Вкладка "Сводка"][ImageSummaryTab]  

1.  Разверните раздел **основной** .  DevTools показывает flameную диаграмму активности в главном потоке с течением времени.  С течением времени ось x представляет запись.  Каждая строка представляет событие.  Более широкий отрезок означает, что событие занимает больше времени.  Ось y представляет стек вызова.  Если вы видите события, наложенные друг на друга, это означает, что события верхнего уровня приводили к появлению младших событий.  
    
    > ##### Рисунок11  
    > Основной раздел  
    > ![Основной раздел][ImageMainSection]  

1.  В записи много данных.  Увеличить одно событие можно, нажав и удерживая указатель мыши над **обзором**, который включает в себя раздел с диаграммами в **кадрах**, **ЦП**и **сети** .  В **главном** разделе и на вкладке " **Сводка** " отображаются только сведения о выбранной части записи.  
    
    > ###### Рисунок12  
    > Увеличено на одном событии  
    > ![Увеличено на событии][ImageZoomedAnimation]  
    
    > [!NOTE]
    > Еще один способ увеличить масштаб — сосредоточиться на **основном** разделе, щелкнув его фон или выбрав событие, а затем нажать клавиши,, и, удерживая нажатой клавишу `W` `A` `S` `D` .  
    
    1.  Обратите внимание на красный треугольник в правой верхней части события **анимации Frame, инициированной анимацией** .  Если вы видите красный треугольник, это предупреждение может быть связано с проблемой, связанной с этим событием.  
    
    > [!NOTE]
    > Событие **анимации Frame срабатывает** при каждом запуске [ `requestAnimationFrame()` обратного вызова][MDNWebRequestAnimationFrame] .  
    
1.  Щелкните событие **кадр анимации, которое активировалось** .  На вкладке **Сводка** теперь отображаются сведения об этом событии.  Обратите внимание на ссылку " **Показать** ".  Щелчок приводит к тому, что DevTools выделит событие, которое инициировало событие Frame, инициированной **анимацией** .  Также обратите внимание на ссылку **app. js: 95** .  При нажатии этой кнопки осуществляется переход к нужной строке исходного кода.
    
    > ##### Рисунок13  
    > Дополнительные сведения о событии анимации запускаемого кадра  
    > ![Дополнительные сведения о событии анимации запускаемого кадра][ImageAnimationFrameFired]  
    
    > [!NOTE]
    > После выбора события с помощью клавиш со стрелками выберите события рядом с ним.  

1.  В рамках события **app. Update** существует множество фиолетовых событий.  Если бы они были шире, они будут выглядеть так, как будто для каждого из них имеется красный треугольник.  Щелкните одно из фиолетовых событий **макета** .  DevTools предоставляет дополнительные сведения о событии на вкладке " **Сводка** ".  В действительности есть предупреждение о принудительном передвижении \ (другое слово для макета \).  

1.  На вкладке **Сводка** щелкните ссылку **app. js: 71** в разделе **Макет принудительно**.  DevTools перенесет вас в строку кода, которая замещает макет.  
    
    > ##### Рисунок14  
    > Строка кода, вызвавшая принудительный макет.  
    > ![Строка кода, вызвавшая принудительный макет.][ImageForcedLayoutSRC]  
    
    > [!NOTE]
    > Проблема с этим кодом состоит в том, что в каждом кадре анимации меняется стиль каждого значка, а затем запрашивается расположение каждого значка на странице.  Поскольку стили изменились, браузер не знает о том, изменилось ли положение каждого значка, поэтому для вычисления его положения необходимо изменить макет значка.  <!--  See [Avoid forced synchronous layouts][RenderingAvoidSynchronousLayouts] to learn more.  -->

<!-- todo: add layouts section when available -->

Phew!  Это было бы очень много, но теперь у вас есть надежная основа базового рабочего процесса для анализа производительности среды выполнения.  Молодец.  

### Премия: анализ оптимизированной версии  

Используй рабочие процессы и инструменты, которые вы только что узнали, нажмите кнопку **оптимизировать** на демонстрационной версии, чтобы включить оптимизированный код, переведите другую запись и проанализируйте результаты.  С улучшенной частотой кадров, направленной на сокращение событий в диаграмме Flame в **главном** разделе, можно увидеть, что оптимизированная версия приложения работает гораздо меньше, что повышает производительность.  

> [!NOTE]
> Несмотря на то, что эта "оптимизированная" версия не подходит, так как она по-прежнему обрабатывает `top` свойство каждого значка.  Лучший подход — придерживаться свойств, которые влияют только на композицию.  
<!--  > See [Use transform and opacity changes for animations][RenderingCompositor] for more information.  -->  

<!--todo: add rendering section when available -->

## Дальнейшие действия

<!--The foundation for understanding performance is the RAIL model.  This model teaches you the performance metrics that are most important to your users.  
See [Measure Performance With The RAIL Model][RAIL] to learn more.  -->  

Для более удобного функционирования с помощью панели "производительность" лучше всего сделать это.  Попробуйте выполнить профилирование на своих страницах и проанализировать результаты.  Если у вас возникли вопросы по поводу ваших результатов, используйте значок **обратной связи** , нажмите `Alt`  +  `Shift`  +  `I` на Windows ( `Option`  +  `Shift`  +  `I` на macOS) или [твит][TwitterEdgeDevtools].  Включите снимки экрана или ссылки на воспроизводимые страницы, если это возможно.

> ##### Рисунок15
> Значок **обратной связи** в Microsoft Edge DevTools  
> ![Значок * * Feedback * * в Microsoft Edge DevTools][ImageFeedbackIcon]

<!-- To really master runtime performance, you've got to learn how the browser translates HTML, CSS, and JS into pixels on a screen.  The best place to start is the [Rendering Performance Overview][RenderingPerformance].  [The Anatomy Of A Frame][FrameAnatomy] dives into even more detail.  -->  

Наконец, существует множество способов улучшить производительность во время выполнения.  В этом учебнике рассмотрены определенные узкие места анимации, направленные на экран с помощью панели производительности, но это только одно из многих узких мест.  <!--  The rest of the Rendering Performance series has a lot of good tips for improving various aspects of runtime performance, such as:  -->

<!--
*   [Optimizing JS Execution][RenderingOptimizeJS]  
*   [Reduce The Scope And Complexity Of Style Calculations][RenderingReduceScope]  
*   [Avoid Large, Complex Layouts And Layout Thrashing][RenderingAvoidThrashing]  
*   [Simplify Paint Complexity And Reduce Paint Areas][RenderingSimplifyPaint]  
*   [Stick To Compositor-Only Properties And Manage Layer Count][RenderingManageLayers]  
*   [Debounce Your Input Handlers][RenderingDebounceInputs]  
-->

<!-- image links -->  

[ImageCaptureSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[ImageGetStarted]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-get-started-side-by-side.msft.png "Рисунок 1: демонстрация слева и DevTools справа"  
[ImageCPUThrottling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-settings.msft.png "Рисунок 2: регулирование центрального процессора"  
[ImagePageProfiling]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-profiling.msft.png "Рисунок 3: Профилирование страницы"  
[ImageProfileResults]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-capture-results.msft.png "Рисунок 4: результаты работы с профилем"  
[ImageFPSChart]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-fps-chart.msft.png "Рисунок 5: диаграмма кадр/с"  
[ImageCPUSummary]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-cpu-chart.msft.png "Рисунок 6: вкладка "Диаграмма ЦП" и "Сводка", выделенная синим цветом"  
[ImageViewingScreenshot]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-screenshot-hover.msft.png "Рисунок 7: Просмотр снимка страницы в 2500ms отметке записи"  
[ImageFrameHover]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-frame-hover.msft.png "Рисунок 8: наведение указателя мыши на кадр"  
[ImageFPSMeter]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-fps-meter-overlay.msft.png "Рисунок 9: индикатор кадров в кадре"  
[ImageSummaryTab]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-summary-tab.msft.png "Рисунок 10: вкладка "Сводка""  
[ImageMainSection]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main.msft.png "На рисунке 11: основной раздел"  
[ImageZoomedAnimation]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-main-zoomed.msft.png "Рисунок 12: масштабирование одной анимации кадром, вызванным событием"  
[ImageAnimationFrameFired]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-performance-animation-frame-fired.msft.png "Рисунок 13. Дополнительные сведения о событии анимации Frame активировалось"  
[ImageForcedLayoutSRC]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-sources-app-update.msft.png "Рисунок 14: строка кода, вызвавшая принудительный макет."  
[ImageFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/evaluate-performance-feedback-icon.msft.png "Рисунок 15: значок * * Feedback * * в Microsoft Edge DevTools"

<!-- links -->

[DevtoolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools"  

[TwitterEdgeDevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "EdgeDevTools-опубликовать твит | Контента"  

[MDNWebRequestAnimationFrame]: https://developer.mozilla.org/docs/Web/API/window/requestAnimationFrame "Window. requestAnimationFrame \ (\) | MDN"  

<!--[InPrivate]: https://support.microsoft.com/help/4026200/microsoft-edge-browse-inprivate "Browse InPrivate in Microsoft Edge"  -->

<!--[FrameAnatomy]: https://aerotwist.com/blog/the-anatomy-of-a-frame  -->  

<!--[RAIL]: /web/fundamentals/performance/rail  -->  
<!--[RenderingAvoidSynchronousLayouts]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing#avoid_forced_synchronous_layouts  -->  
<!--[RenderingAvoidThrashing]: /web/fundamentals/performance/rendering/avoid-large-complex-layouts-and-layout-thrashing  -->  
<!--[RenderingCompositor]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count#use_transform_and_opacity_changes_for_animations  -->  
<!--[RenderingDebounceInputs]: /web/fundamentals/performance/rendering/debounce-your-input-handlers  -->
<!--[RenderingManageLayers]: /web/fundamentals/performance/rendering/stick-to-compositor-only-properties-and-manage-layer-count  -->  
<!--[RenderingOptimizeJS]: /web/fundamentals/performance/rendering/optimize-javascript-execution  -->  
<!--[RenderingPerformance]: /web/fundamentals/performance/rendering  -->  
<!--[RenderingReduceScope]: /web/fundamentals/performance/rendering/reduce-the-scope-and-complexity-of-style-calculations  -->  
<!--[RenderingSimplifyPaint]: /web/fundamentals/performance/rendering/simplify-paint-complexity-and-reduce-paint-areas  -->  

<!--[StackOverflowAlphabetBrowserDevtools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser - Stack Overflow"  -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/evaluate-performance/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
