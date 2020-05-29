---
title: Проверка анимации
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 6466c7f0e1f8680a2429b565e8022d152d05d733
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572411"
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





# Проверка анимации   



Просмотрите и измените анимацию с помощью инспектора анимации Microsoft Edge DevTools.  

> ##### Рис. 1  
> Инспектор анимации  
> ![Инспектор анимации][ImageAnimationInspector]  

### Краткий обзор  

*   Запишите анимацию, открыв инспектор анимации.  Инспектор анимации автоматически определяет и сортирует анимации в группах.  
*   Изучите анимацию, заменив каждую из них, воспроизводить каждую из них или просматривая исходный код.  
*   Изменяйте анимацию, изменяя время, задержку, продолжительность или смещение опорных кадров.  

## Обзор   

Инспектор анимации Microsoft Edge DevTools имеет два основных назначения.  

*   Проверка анимации.  Вы хотите замедлить, воспроизвести или проверить исходный код для группы анимации.  
*   Изменение анимаций.  Вы хотите изменить время, задержку, длительность или смещение кадров в группе анимации.  Редактирование Безье и изменение опорных кадров в настоящее время не поддерживается.  

Инспектор анимации поддерживает анимацию CSS, переходы CSS и веб-анимации.  `requestAnimationFrame` анимации в настоящее время не поддерживаются.  

### Что такое группа анимации?  

Группа анимации — это группа анимаций, которые могут быть связаны друг с другом.  В настоящее время в веб-браузере отсутствует фактическая Концепция групповых анимаций, поэтому разработчики движений и разработчиков должны создавать и обрабатывать отдельные анимации, чтобы анимация отображалась как один и тот же визуальный эффект.  Инспектор анимации прогнозирует, какие анимации связаны с учетом времени начала, (за исключением задержек и т. д.).  Инспектор анимации также группирует анимацию рядом друг с другом.  
Другими словами, набор анимаций, которые вызываются в одном блоке сценария, группируются вместе.  Если анимация является асинхронной, она помещается в отдельную группу.  

## Начало работы  

Открыть инспектор анимации можно двумя способами:  

*   Открытие меню " **Настройка и управление DevTools** "  
    1.  Перейдите к вложенному меню **другие инструменты** .  
    1.  Выберите **анимации**:  
        
        > ##### Рисунок 2  
        > Анимация с помощью главного меню  
        > ![Анимация с помощью главного меню][ImageAnimationsViaMainMenu]  
        
*   Открытие **меню команд**  
    1.  Введите `Drawer: Show Animations`.  

Инспектор анимации открывается в виде вкладки рядом с лотком консоли.  Поскольку инспектор анимаций является вкладкой ящика, вы можете использовать инспектор анимации на любой DevTools панели.  

> ##### Рисунок3  
> Пустой инспектор анимации  
> ![Пустой инспектор анимации][ImageEmptyAnimationInspector]  

Инспектор анимации сгруппирован в четыре основных раздела \ (или области).  Это руководство относится к каждой области, как описано ниже.  

| | Панель | Описание |  
| --- |:--- |:--- |  
| 1,1 | **Элементы управления** | Здесь вы можете очистить все текущие группы анимации или изменить скорость выбранной в данный момент группы анимации. |  
| 2 | **Обзор** | Выберите группу анимации, чтобы проверить ее и изменить ее в области **сведений** . |  
| Трехконтактный | **Информация о сроках** | Задержите и начните анимацию отсюда или переходите к определенной точке анимации. |  
| четырехпроцессорном | **Сведения** | Проверка и изменение выбранной в данный момент группы эффектов анимации. |  

> ##### Рисунок4  
> Инспектор анимации с заметками  
> ![Инспектор анимации с заметками][ImageAnnotatedAnimationInspector]  

Чтобы зафиксировать анимацию, просто выполните взаимодействие, которое запускает анимацию, когда открыт Инспектор анимации.  Если анимация запускается при загрузке страницы, перезагрузите страницу с помощью инспектора анимации, чтобы определить анимацию.  

<!--  old link: <video src="animations/capture-animations.mp4" autoplay loop muted controls></video>  -->  

<!--  import the video to ACOM using https://review.docs.microsoft.com/en-us/help/contribute/contribute-video-publish?branch=master  -->  

<!--  > [!VIDEO animations/capture-animations.mp4]  -->  

## Проверка анимации   

После захвата анимации есть несколько способов воспроизведения.  

*   Наведите указатель мыши на эскиз в области " **Обзор** ", чтобы просмотреть его в предварительной версии.  
*   В области " **Обзор** " выберите группу анимации \ (чтобы она отображалась в области **сведений** ) и нажмите значок **воспроизведения** ![ ][ImageReplayButtonIcon] .  Анимация воспроизводится в окне просмотра.  **animation speed** ![ ][ImageAnimationSpeedButtonsIcon] Чтобы изменить скорость просмотра в выбранной группе эффектов анимации, щелкните значки скорость анимации анимации.  Вы можете изменить текущее расположение с помощью красной вертикальной черты.  
*   Щелкните и перетащите красную вертикальную полосу, чтобы проочистки анимации просмотра.  

### Просмотр подробных сведений о анимации  

После захвата группы анимации щелкните ее в области " **Обзор** ", чтобы просмотреть подробные сведения.  В области **сведений** каждая из анимаций назначается отдельной строке.  

> ##### Рисунок 5  
> Сведения о группе эффектов анимации  
> ![Сведения о группе эффектов анимации][ImageAnimationGroupDetails]  

Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра.  Щелкните анимацию, чтобы выделить ее на панели " **элементы** ".  

> ##### Рисунок6  
> Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра  
> ![Наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра][ImageHoverOverAnimationHighlightViewport]  

Самым левым и темным разделом анимации является определение.  Справа, более размытые части представляют собой итерации.  Например, на [рисунке 7](#figure-7)разделы 2 и 3 представляют собой итерации раздела One.  

> ##### Рисунок7  
> Схема итераций анимации  
> ![Схема итераций анимации][ImageDiagramAnimationIterations]  

Если к двум элементам применена одинаковая анимация, инспектор анимации назначает элементам один и тот же цвет.  Цвет является произвольным и не имеет значимости.  Например, на [рисунке 8](#figure-8) используются два элемента с `div.cwccw.earlier` `div.cwccw.later` одинаковой анимацией \ ( `spinrightleft` \), как `div.ccwcw.earlier` и `div.ccwcw.later` элементы.  

> ##### Рисунок8  
> Анимация с цветовым кодированием  
> ![Анимация с цветовым кодированием][ImageColorCodedAnimations]  

## Изменение анимации   

Вы можете изменить анимацию с помощью инспектора анимации тремя способами:  

*   Длительность анимации.  
*   Временные интервалы для ключевых кадров.  
*   Время начала задержки.  

В этом разделе показано, что [на рисунке 9](#figure-9) представлена исходная анимация.  

> ##### Рисунок9  
> Исходная анимация перед изменением  
> ![Исходная анимация перед изменением][ImageOriginalAnimationBeforeModification]  

Чтобы изменить длительность анимации, щелкните и перетащите первый или последний круг.  

> ##### Рисунок 10  
> Измененная длительность  
> ![Измененная длительность][ImageModifiedDuration]  

Если анимация определяет любые правила для ключевого кадра, они будут представлены как белые внутренние круги.  Щелкните и перетащите один из них, чтобы изменить временные показатели для ключевого кадра.  

> ##### Рисунок11  
> Измененный ключевой кадр  
> ![Измененный ключевой кадр][ImageModifiedKeyframe]  

Чтобы добавить задержку для анимации, щелкните и перетащите ее в любое место за исключением кругов.  

> ##### Рисунок12  
> Измененная задержка  
> ![Измененная задержка][ImageModifiedDelay]  

<!--   -->  



<!-- image links -->  

[ImageAnimationSpeedButtonsIcon]: /microsoft-edge/devtools-guide-chromium/media/animation-speed-buttons-icon.msft.png  
[ImageReplayButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/replay-button-icon.msft.png  

[ImageAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-completed.msft.png "Рисунок 1: инспектор анимации"  
[ImageAnimationsViaMainMenu]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-more-tools-animations.msft.png "Рисунок 2: анимация с помощью главного меню"  
[ImageEmptyAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations.msft.png "Рисунок 3: пустой инспектор анимации"  
[ImageAnnotatedAnimationInspector]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-paused.msft.png "Рисунок 4: инспектор анимации с примечаниями"  
[ImageAnimationGroupDetails]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-elements-styles-drawer-animations-selected-completed.msft.png "Рисунок 5: сведения о группе эффектов анимации"  
[ImageHoverOverAnimationHighlightViewport]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-split-elements-styles-drawer-animations-selected-completed.msft.png "Рисунок 6: наведите указатель мыши на анимацию, чтобы выделить ее в окне просмотра"  
[ImageDiagramAnimationIterations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations-highlight.msft.png "Рисунок 7: схема итераций анимации"  
[ImageColorCodedAnimations]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-display-animations.msft.png "Рисунок 8: анимация с цветовым кодированием"  
[ImageOriginalAnimationBeforeModification]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations.msft.png "Рисунок 9: исходная анимация перед изменением"  
[ImageModifiedDuration]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-shorter.msft.png "Рисунок 10: изменена длительность"  
[ImageModifiedKeyframe]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-keyframe-modification.msft.png "Рисунок 11: изменен ключевой кадр"  
[ImageModifiedDelay]: /microsoft-edge/devtools-guide-chromium/media/inspect-styles-glitch-spin-animations-console-animations-delay.msft.png "Рисунок 12: измененная задержка"  

<!-- links -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/inspect-styles/animations) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
