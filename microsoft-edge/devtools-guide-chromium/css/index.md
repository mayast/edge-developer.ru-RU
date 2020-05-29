---
title: Приступая к просмотру и изменению каскадных таблиц стилей
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 85fceaa44b0143a82ca8f66ef8c63e1a9275dcd8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601819"
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





# Приступая к просмотру и изменению каскадных таблиц стилей   



Эти интерактивные учебники помогут вам ознакомиться с основными принципами просмотра и изменения CSS для страниц с помощью Microsoft Edge DevTools.  

## Открытие примеров CSS  

1.  Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **примеры CSS** , чтобы открыть их в новом окне.  
    
    [Примеры CSS][GlitchDevToolsCssExamples]  

> [!NOTE]
> Если вы хотите [закрепить окно DevTools][DevToolsCustomizePlacement] справа от окна просмотра \ (на [рис. 1](#figure-1)\), нажмите кнопку **Настройка и управление DevTools** `...` .  В раскрывающемся меню **Настройка и управление DevTools** в разделе **закрепляемая на стороне** экрана выберите пункт **закрепить по правому**краю.  
    
## Просмотр CSS для элемента   

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Щелкните текст правой кнопкой мыши `Inspect Me!` и выберите команду **проверить**.  
    1.  В DevTools на панели " **элементы** " на вкладке " **дерево DOM** " `Inspect Me!` выделена кнопка "элемент".  
        
        > ##### Рис. 1  
        > Проверяемый элемент выделен в **дереве DOM**  
        > ![Проверяемый элемент выделен в дереве DOM][ImageInspect]  
        
    1.  `Inspect Me!`Найдите значение атрибута в элементе `data-message` и скопируйте его.  
1.  На странице в поле **значение `data-message` :** введите значение.  
1.  Щелкните текст правой кнопкой мыши `Inspect Me!` и выберите команду **проверить**.  
    
    1.  В DevTools на панели **элементы** откройте вкладку **стили** .  
    1.  На вкладке **стили** `Inspect Me!` элемент выделен.  
    1.  В `Inspect Me!` элементе найдите `aloha` правило класса.  
        
        > [!NOTE]
        > Вы видите это правило, так как оно применяется к `Inspect Me!` элементу.  
        
    1.  В `aloha` классе найдите значение для `padding` стиля и скопируйте его.  
        
        > ##### Рисунок 2  
        > Классы CSS, примененные к выбранному элементу, такие как `aloha` , отображаются на вкладке " **стили** "  
        > ![Классы CSS, примененные к проверяемому элементу, выделяются на вкладке "стили"][ImageAloha]  
        
1.  На странице в поле **значение `padding` :** введите значение.  

## Добавление объявления CSS в элемент   

Используйте вкладку **стили** , если вы хотите изменить или добавить объявления CSS к элементу.  

> [!NOTE]
> Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Щелкните текст правой кнопкой мыши `Add A Background Color To Me!` и выберите команду **проверить**.  
1.  Нажмите кнопку в `element.style` верхней части вкладки **стили** .  
1.  Введите текст `background-color` и нажмите клавишу `Enter` .  
1.  Введите текст `honeydew` и нажмите клавишу `Enter` .  В **дереве DOM** вы увидите, что к элементу применено объявление встроенного стиля.  

> ##### Рисунок3  
> `background-color:honeydew`Объявление применено к элементу с помощью `element.style` раздела вкладки " **стили** "  
> ![Добавление объявления CSS к элементу с помощью вкладки "стили"][ImageDeclaration]  

## Добавление класса CSS в элемент   

С помощью вкладки " **стили** " можно увидеть, как выглядит элемент, когда класс CSS применяется к элементу или удаляется из него.  

> [!NOTE]
> Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Щелкните элемент правой кнопкой мыши `Add A Class To Me!` и выберите команду **проверить**.  
1.  Щелкните **. CLS**.  DevTools открывает текстовое поле, в котором можно добавлять классы к выбранному элементу.  
1.  Введите `color_me` текст в текстовом поле **Добавить новый класс** и нажмите клавишу `Enter` .  Флажок отображается под текстовым полем " **Добавить новый класс** ", в котором можно включить или отключить класс.  Если `Add A Class To Me!` к элементу применены другие классы, вы также можете переключаться между ними.  

> ##### Рисунок4  
> `color_me`Класс применен к элементу с помощью раздела **. CLS** на вкладке " **стили** ".  
> ![Применение класса color_me к элементу][ImageApplyClass]  

## Добавление PseudoState в класс   

С помощью вкладки **стили** вы можете навсегда применить CSS-PseudoState к элементу.  DevTools поддерживает `:active` , `:focus` , `:hover` , и `:visited` .  

> [!NOTE]
> Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Наведите указатель мыши на `Hover Over Me!` текст.  Цвет фона изменится.  
1.  Щелкните текст правой кнопкой мыши `Hover Over Me!` и выберите команду **проверить**.  
1.  На вкладке **стили** щелкните **: Hov**.  
1.  Установите флажок **: наведение указателя мыши** .  Цвет фона изменится так же, как и раньше, несмотря на то, что вы не наводите указатель мыши на элемент.  

> ##### Рисунок 5  
> Переключение `:hover` PseudoState для элемента  
> ![Переключение наведения указателя на PseudoState элемента][ImageSetHover]  

## Изменение размеров элемента   

С помощью интерактивной схемы **"модель Box** " на вкладке " **стили** " можно изменить ширину, высоту, заполнение, границу или длину границы элемента.  

> [!NOTE]
> Завершите [Просмотр CSS для](#view-the-css-for-an-element) учебника по элементу, прежде чем сделать это.  

1.  [Откройте примеры CSS](#open-css-examples).  
1.  Щелкните элемент правой кнопкой мыши `Change My Margin!` и выберите команду **проверить**.  
1.  На схеме **модель Box** на вкладке **стили** наведите указатель мыши на **Заполнение**.  Заполнение элемента выделено в окне просмотра.  

    > [!NOTE]
    > В зависимости от размера окна DevTools, возможно, потребуется прокрутить в нижнюю часть вкладки **стили** , чтобы увидеть **модель Box**.  

1.  Дважды щелкните левое поле в **модели Box**, которое в настоящее время имеет значение `-` , означающее, что у элемента нет левого поля.  
1.  Введите текст `100px` и нажмите клавишу `Enter` .  **Модель Box** по умолчанию имеет значения пикселей, но также принимает другие значения, например `25%` или `10vw` .  

> ##### Рисунок6  
> Наведение указателя мыши на заполнение элемента  
> ![Наведение указателя мыши на заполнение элемента][ImageShowPadding]  

> ##### Рисунок7  
> Изменение левого поля элемента  
> ![Изменение левого поля элемента][ImageChangeMargin]  

 



<!-- image links -->  

[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me.msft.png "Рисунок 1: в дереве DOM выделено проверенный элемент"  
[ImageAloha]: /microsoft-edge/devtools-guide-chromium/media/css-elements-inspect-me-styles.msft.png "Рисунок 2: классы CSS, примененные к проверяемому элементу, выделяются на вкладке "стили""  
[ImageDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-background-color-to-me-styles-p.msft.png "Рисунок 3: Добавление объявления CSS к элементу с помощью вкладки "стили""  
[ImageApplyClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-add-a-class-to-me-styles-cls.msft.png "Рисунок 4: применение класса color_me к элементу"  
[ImageSetHover]: /microsoft-edge/devtools-guide-chromium/media/css-elements-hover-over-me-styles-hov-hover.msft.png "Рис. 5: переключение наведения указателя на элемент PseudoState"  
[ImageShowPadding]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-padding.msft.png "Рисунок 6: наведение указателя мыши на заполнение элемента"  
[ImageChangeMargin]: /microsoft-edge/devtools-guide-chromium/media/css-elements-change-my-margin-styles-margin-edit.msft.png "Рисунок 7: изменение левого поля элемента"  

<!-- links -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  

[GlitchDevToolsCssExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/css/examples/ecma.html "Примеры CSS — Microsoft EDGE (Chromium) DevTools | Цепь"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
