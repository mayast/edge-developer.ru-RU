---
title: Справочник по CSS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 4f0370b83d8c939476a1ed378dbdf750101c9527
ms.sourcegitcommit: 0048eb692d49eab4755c0c3ef6866e6a9122d579
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10843972"
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







# Справочник по CSS   



Ознакомьтесь с новыми рабочими процессами в этой полной справке Microsoft Edge DevTools функции, относящиеся к просмотру и изменению каскадных таблиц стилей.  

Ознакомьтесь с основными принципами [просмотра и изменения каскадных таблиц стилей][DevToolsCSSGetStarted] .  

## Выбор элемента   

Панель " **элементы** " в DevTools позволяет просматривать или изменять CSS для одного элемента за один раз.  Выбранный элемент выделится в **дереве DOM**.  Стили элемента отображаются на панели " **стили** ".  В разделе [Просмотр CSS для элемента][DevToolsCSSGetStartedTutorial] учебника.  

> [!NOTE]
> На [рисунке 1](#figure-1) `h1` элемент, выделенный в **дереве DOM** , является выбранным элементом.  Справа в области **стили** отображаются стили элемента.  В левой части экрана выделяется элемент в окне просмотра, но только потому, что в данный момент указатель мыши наведен на него в **дереве DOM**.  

> ##### Рис. 1  
> Пример выбранного элемента  
> ![Пример выбранного элемента][ImageSelectedElement]  

Существует множество способов выбора элемента.  

*   В окне просмотра щелкните элемент правой кнопкой мыши и выберите команду **проверить**.  
*   В DevTools щелкните **выбрать элемент** , ![ выберите элемент ][ImageSelectAnElementIcon] или нажмите клавиши `Control` + `Shift` + `C` \ (Windows \) или `Command` + `Shift` + `C` \ (macOS \), а затем щелкните элемент в окне просмотра.  
*   В DevTools щелкните элемент в **дереве DOM**.  
*   В DevTools выполните запрос, как `document.querySelector('p')` на **консоли**, щелкните результат правой кнопкой мыши и выберите пункт **Показать на панели элементов**.  

## Просмотр CSS   

### Просмотр внешней таблицы стилей, в которой определено правило   

В области **стили** щелкните ссылку рядом с правилом CSS, чтобы открыть внешнюю таблицу стилей, которая определяет правило.  

Если таблица стилей minified, ознакомьтесь с тем, [чтобы сделать файл minified читаемым][DevToolsJavascriptReferenceFormat].  

> [!NOTE]
> На [рис. 2](#figure-2), при нажатии кнопки `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css:2` Переход к строке 2 `https://docs.microsoft.com/_themes/docs.theme/master/en-us/_themes/styles/b66bc881.site-ltr.css` , где `.content h1:first-of-type` определено правило CSS.  

> ##### Рисунок 2  
> Просмотр таблицы стилей, в которой определено правило  
> ![Просмотр таблицы стилей, в которой определено правило][ImageViewRuleStylesheet]  

### Просмотр только CSS, которая фактически применяется к элементу   

На вкладке **стили** отображаются все правила, применимые к элементу, включая объявления, которые были переопределены.  Если вы не заинтересованы в переопределенных объявлениях, используйте **вычисляемые** вкладки для просмотра только CSS, которая фактически применяется к элементу.  

1.  [Выберите элемент](#select-an-element).  
1.  Перейдите на вкладку " **вычисляемые** " на панели " **элементы** ".  

> [!NOTE]
> В окне с широкой DevTools **Вычисляемая** вкладка не существует.  Содержимое **вычисляемой** вкладки отображается на вкладке **стили** .  

Унаследованные свойства являются непрозрачными.  Установите флажок **Показать все** , чтобы увидеть все унаследованные значения.  

> [!NOTE]
> На [рисунке 3](#figure-3)на вкладке " **Вычисляемая** вкладка" показаны свойства CSS, применяемые к текущему `h1` элементу.  

> ##### Рисунок3  
> **Вычисляемая** вкладка  
> ![Вычисляемая вкладка][ImageComputedTab]  

### Просмотр свойств CSS в алфавитном порядке   

Используйте **вычисляемую** вкладку.  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Просмотр унаследованных свойств CSS   

Установите флажок **Показать все** на вкладке **вычисляемый** .  Просмотреть [только CSS, фактически примененный к элементу](#view-only-the-css-that-is-actually-applied-to-an-element).  

### Просмотр модели Box для элемента   

Чтобы просмотреть [модель Box][MDNBoxModel] элемента, перейдите на вкладку **стили** .  Если окно DevTools узким, схема **модель Box** находится в нижней части вкладки.  

Чтобы изменить значение, дважды щелкните его.  

> [!NOTE]
> На [рисунке 4](#figure-4)схема **модель Box** на вкладке **стили** показывает модель Box для элемента, выбранного в данный момент `h1` .  

> ##### Рисунок4  
> Схема **модели Box**  
> ![Схема модели Box][ImageBoxModel]  

### Поиск и фильтрация CSS элемента   

С помощью текстового поля **Фильтр** на вкладках **стили** и **вычисляемые** вкладки можно искать определенные свойства или значения CSS.  

Чтобы также искать унаследованные свойства на вкладке **вычисляемые** , установите флажок **Показать все** .  

> [!NOTE]
> На [рисунке 5](#figure-5)вкладка **стили** отфильтрована, чтобы отображались только правила, включающие поисковый запрос `color` .  

> ##### Рисунок 5  
> Фильтрация вкладки " **стили** "  
> ![Фильтрация вкладки "стили"][ImageStylesFilter]  

> [!NOTE]
> На [рисунке 6](#figure-6)с помощью **вычисляемой** вкладки отображаются только объявления, включающие поисковый запрос `100%` .  

> ##### Рисунок6  
> Фильтрация на вкладке " **Вычисляемая** вкладка"  
> ![Фильтрация на вкладке "вычисляемая вкладка"][ImageComputerFilter]  

### Переключение на псевдо-класс   

Чтобы переключить псевдо-класс, например, `:active` `:focus` `:hover` или `:visited` :  

1.  [Выберите элемент](#select-an-element).  
1.  На панели " **элементы** " перейдите на вкладку " **стили** ".  
1.  Щелкните **: Hov**.  
1.  Проверьте псевдо-класс, который вы хотите включить.  

> [!NOTE]
> На [рисунке 7](#figure-7)переключитесь на `:hover` псевдо-класс.  В окне просмотра убедитесь в том, что `background-color: cornflowerblue` объявление применяется к элементу, несмотря на то что элемент фактически не наведен на указатель.  

> ##### Рисунок7  
> Переключение `:hover` псевдо-класса  
> ![Переключение: псевдо-класс для наведения][ImagePseudoClass]  

Дополнительные сведения о том, как [Добавить PseudoState в класс][DevToolsCSSGetStartedAddPseudoState] для интерактивного учебника. 

### Просмотр страницы в режиме печати   

Чтобы просмотреть страницу в режиме печати, выполните указанные ниже действия.  
1.  [Открытие меню команд][DevToolsCommandMenu].  
1.  Начните вводить текст `Rendering` и выберите его `Show Rendering` .  
1.  В раскрывающемся списке **Эмуляция мультимедиа в CSS** нажмите кнопку **Печать**.  

### Просмотр использованной и неиспользуемой CSS с помощью вкладки "покрытие"   

На вкладке Coverage показано, какая страница CSS используется в действительности.  

1.  Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), когда DevTools в фокусе, чтобы открыть меню команд.  
1.  Начните вводить текст `coverage` и выберите **Показать покрытие**.  Откроется вкладка покрытие.  
    
    > ##### Рисунок8  
    > Открытие вкладки "покрытие" в меню команд  
    > ![Открытие вкладки "покрытие" в меню команд][ImageCommandMenu]  
    
    > ##### Рисунок9  
    > Вкладка "покрытие"  
    > ![Вкладка "покрытие"][ImageCoverageEmpty]  
    
1.  Нажмите кнопку **начать покрытие и обновите** страницу, чтобы ![ запустить инструментирование, и обновите ее ][ImageRefreshIcon] .  Обновленная страница и вкладка Coverage предоставляют общие сведения о том, сколько стилей CSS и JavaScript используется для каждого файла, загружаемого браузером.  Зеленый представляет используемые CSS.  Красный — неиспользуемый CSS.  
    
    > ##### Рисунок 10  
    > Общие сведения о том, какая таблица CSS (и JavaScript) используется и неиспользуемая  
    > ![Общие сведения о том, какая таблица CSS (и JavaScript) используется и неиспользуемая][ImageCoverageOverview]  

1.  Щелкните CSS-файл, чтобы просмотреть разбиение по строкам для используемого CSS.  
    
    > [!NOTE]
    > На [рисунке 11](#figure-11)строки 145 в 147 и 149 в 151 из `b66bc881.site-ltr.css` не используются, в то время как используются строки 163 — 166.  
    
    > ##### Рисунок11  
    > Разбиение по строкам для используемых и неиспользуемых CSS  
    > ![Разбиение по строкам для используемых и неиспользуемых CSS][ImageCoverageDetail]  
    
### Принудительная печать в режиме предварительного просмотра   

Просмотрите [DevTools в режиме предварительного просмотра][DevToolsCssPrintPreview].  

## Изменение CSS   

<!-- todo s/CSS declaration/declaration/ -->  

### Добавление объявления CSS в элемент   

Поскольку порядок объявлений влияет на стиль элемента, вы можете добавлять объявления различными способами.  

*   [Добавление встроенного объявления](#add-an-inline-declaration).  Эквивалентно добавлению `style` атрибута в HTML элемента.  
*   [Добавление объявления в правило стиля](#add-a-declaration-to-a-style-rule).  

**Какой рабочий процесс следует использовать?** В большинстве сценариев вы, возможно, захотите использовать рабочий процесс объявления на встроенных элементах.  Встроенные объявления имеют более высокие особенности, чем внешние, поэтому встроенный рабочий процесс гарантирует, что изменения вступают в силу в элементе так, как вы ожидали.  Дополнительные сведения о том, как узнать подробности, приведены в разделе [типы Selector][MDNSelectorTypes] .  

Если при отладке любого стиля элемента требуется специально проверить, что происходит, если объявление определено в разных местах, используйте другой рабочий процесс.  

#### Добавление встроенного объявления   

Чтобы добавить встроенное объявление, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element).  
1.  В области **стили** щелкните между скобками раздела **element. Style** .  Курсор фокусируется на том, что позволяет вводить текст.  
1.  Введите имя свойства и нажмите клавишу `Enter` .  
1.  Введите допустимое значение для этого свойства и нажмите клавишу `Enter` .  Убедитесь, что в **дереве DOM** `style` к элементу добавлен атрибут.  

> [!NOTE]
> На [рисунке 12](#figure-12)к `margin-top` `background-color` выбранному элементу применены свойства и.  В **дереве DOM** убедитесь, что объявления отражены в `style` атрибуте для элемента.  

> ##### Рисунок12  
> Добавление встроенных объявлений  
> ![Добавление встроенных объявлений][ImageInlineDeclarations]  

#### Добавление объявления в правило стиля   

Чтобы добавить объявление к существующему правилу стиля, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element).  
1.  В области **стили** щелкните между скобками правила стиля, к которому вы хотите добавить объявление.  Курсор фокусируется на том, что позволяет вводить текст.  
1.  Введите имя свойства и нажмите клавишу `Enter` .  
1.  Введите допустимое значение для этого свойства и нажмите клавишу `Enter` .  

> ##### Рисунок13  
> Добавление `border-bottom-style:groove` объявления в правило стиля  
> ![Добавление объявления в правило стиля][ImageAddDeclarationExistingRule]  

### Изменение имени или значения объявления   

Дважды щелкните имя или значение объявления, чтобы изменить его.  Сочетания клавиш для быстрого увеличения или уменьшения значения (, или единиц) можно найти [в статье изменение значений объявлений](#change-declaration-values-with-keyboard-shortcuts) `0.1` `1` `10` `100` .  

> ##### Рисунок14  
> Изменение значения `border-bottom-style`  
> ![Изменение значения объявления][ImageAddDeclarationExistingRule2]  

### Изменение значений объявлений с помощью сочетаний клавиш   

При редактировании значения объявления вы можете использовать следующие сочетания клавиш, чтобы увеличить значение на фиксированную величину.  

*   Нажмите клавиши `Alt` + `Up` \ (Windows \) или `Option` + `Up` \ (macOS \), чтобы увеличить значение `0.1` .  
*   Нажмите `Up` , чтобы изменить значение на `1` или, `0.1` Если текущее значение находится в диапазоне от `-1` и `1` .  
*   Нажмите, `Shift` + `Up` чтобы увеличить `10` .  
*   Нажмите клавиши `Shift` + `Page Up` \ (Windows \) или `Shift` + `Command` + `Up` \ (macOS \), чтобы увеличить значение на `100` .  

Кроме того, выполняется уменьшение.  Просто замените каждый из `Up` упомянутых выше экземпляров `Down` .  

### Добавление класса в элемент   

Чтобы добавить класс в элемент, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element) в **дереве DOM**.  
1.  Щелкните **. CLS**.  
1.  Введите имя класса в текстовом поле **Добавить новый класс** .  
1.  Нажмите клавишу `Enter` .  

> ##### Рисунок15  
> Область « **классы элементов** »  
> ![Область «классы элементов»][ImageElementClasses]  

### Переключение класса   

Чтобы включить или отключить класс для элемента, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element) в **дереве DOM**.  
1.  Откройте область **классы элементов** .  Дополнительные сведения о том, [как добавить класс в элемент](#add-a-class-to-an-element).  Под текстовым полем **Добавить новый класс** находятся все классы, которые применяются к этому элементу.  
1.  Установите флажок рядом с классом, который вы хотите включить или отключить.  

### Добавление правила стиля   

Чтобы добавить новое правило стиля, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element).  
1.  Нажмите кнопку **новое** правило стиля ![ ][ImageNewStyleRuleIcon] .  DevTools вставляет новое правило под правилом **element. Style** .  

> [!NOTE]
> На [рисунке 16](#figure-16)DevTools добавляет `h1.devsite-page-title` правило стиля после нажатия кнопки **новое правило стиля**.  

> ##### Рисунок16  
> Добавление нового правила стиля  
> ![Добавление нового правила стиля][ImageStyleRule]  

#### Выберите таблицу стилей, к которой нужно добавить правило.   

При [добавлении нового правила стиля](#add-a-style-rule)щелкните **и удерживайте новое правило стиля,** чтобы ![ ][ImageNewStyleRuleIcon] выбрать таблицу стилей, к которой нужно добавить правило.  

> ##### Рисунок17  
> Выбор таблицы стилей  
> ![Выбор таблицы стилей][ImageChooseStylesheet]  

#### Добавление правила стиля в определенное место   

Чтобы добавить правило стиля в определенное расположение на вкладке " **стили** ", выполните указанные ниже действия.  

1.  Наведите указатель мыши на правило стиля, которое находится в том месте, куда вы хотите добавить новое правило стиля.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Нажмите кнопку **Вставить правило стиля ниже** ![ , чтобы вставить правило стиля ниже ][ImageNewStyleRuleIcon] .  

> ##### Рис. 18  
> **Вставить правило стиля ниже**  
> ![Вставить правило стиля ниже][ImageInsertStyleRuleBelow]  

### Панель инструментов "другие действия"   

Панель инструментов " **другие действия** " позволяет:  

*   Вставка правила стиля прямо ниже того, на котором вы отправили фокус.  
*   Добавьте в `background-color` `color` `box-shadow` правило стиля, которое `text-shadow` вы хотите включить, или объявление.  

Чтобы открыть панель инструментов **Дополнительные действия** , выполните указанные ниже действия.  

1.  На вкладке **стили** наведите указатель мыши на правило стиля.  **Дополнительные действия** `...` находится в правом нижнем углу раздела "правило стиля".  
    
    > [!NOTE]
    > На [рисунке 19](#figure-19)наведите указатель мыши на `.header-holder.has-default-focus` правило стиля, и в правом нижнем углу раздела правила стиля появится элемент **другие действия** .  
    
    > ##### На рисунке 19  
    > Показать **Дополнительные действия**  
    > ![Показать дополнительные действия][ImageRevealMore]  
    
1.  Наведите указатель мыши на элемент **другие действия** `...` , чтобы открыть описанные выше действия.  
    
    > [!NOTE]
    > **Правило стиля вставки, показанное ниже** , выводится при наведении указателя мыши на **другие действия**.  
    
    > ##### Рис. 20  
    > Панель инструментов « **другие действия** »  
    > ![Панель инструментов «другие действия»][ImageInsertStyleRuleBelow2]  
    
### Переключить объявление   

Чтобы включить или отключить одно объявление, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element).  
1.  В области **стили** наведите указатель мыши на правило, которое определяет объявление.  Рядом с каждым объявлением отображаются флажки.  
1.  Установите или снимите флажок рядом с объявлением.  Если вы снимите флажок объявления, DevTools пересекает его, чтобы показать, что он больше не активен.  

> [!NOTE]
> На [рисунке 21](#figure-21) `margin-top` свойство для выбранного в данный момент элемента было отключено.  

> ##### Рисунок 21  
> Переключение объявления  
> ![Переключение объявления][ImageToggleDeclaration]  

### Добавление объявления цвета фона   

Чтобы добавить `background-color` объявление в элемент, выполните указанные ниже действия.  

1.  Наведите указатель мыши на правило стиля, в которое вы хотите добавить `background-color` объявление.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Щелкните **добавить цвет фона** ![ добавить цвет фона ][ImageAddBackgroundColorIcon] .  

> ##### Рис. 22  
> **Добавление цвета фона**  
> ![Добавление цвета фона][ImageAddBackgroundColor]  

### Добавление объявления цвета   

Чтобы добавить `color` объявление в элемент, выполните указанные ниже действия.  

1.  Наведите указатель мыши на правило стиля, в которое вы хотите добавить `color` объявление.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Нажмите кнопку **Добавить** цвет ![ ][ImageAddColorIcon] .  

> ##### Рис. 23  
> **Добавить цвет**  
> ![Добавить цвет][ImageAddColor]  

### Добавление объявления с помощью блочной тени   

Чтобы добавить `box-shadow` объявление в элемент, выполните указанные ниже действия.  

1.  Наведите указатель мыши на правило стиля, в которое вы хотите добавить `box-shadow` объявление.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Нажмите кнопку Добавить тень надписи "добавить рамку **"** ![ ][ImageAddBoxShadowIcon] .  

> ##### Рисунок 24  
> **Добавление тени для поля**  
> ![Добавление тени для поля][ImageAddBoxShadow]  

### Добавление объявления тени для текста   

Чтобы добавить `text-shadow` объявление в элемент, выполните указанные ниже действия.  

1.  Наведите указатель мыши на правило стиля, в которое вы хотите добавить `text-shadow` объявление.  
1.  [Показать панель инструментов " **другие действия** "](#reveal-the-more-actions-toolbar).  
1.  Нажмите кнопку **Добавить** тень текста ![ Добавить тень ][ImageAddTextShadowIcon] .  

> ##### Рис. 25  
> **Добавление тени текста**  
> ![Добавление тени текста][ImageAddTextShadow]  

### Изменение цвета с помощью палитры цветов   

В **средстве выбора цвета** есть графический интерфейс для изменения `color` и `background-color` объявлений.  

Чтобы открыть окно **выбора цвета**, выполните указанные ниже действия.  

1.  [Выберите элемент](#select-an-element).  
1.  На вкладке **стили** найдите и щелкните то `color` `background-color` же объявление, которое вы хотите изменить.  Слева от "," `color` `background-color` или аналогичного значения есть маленький квадрат, который является предварительным просмотром цвета.  
    
    > [!NOTE]
    > На [рисунке 26](#figure-26)в маленьком квадрате слева от него `rgba(0, 0, 0, 0.7)` показана эта цветная область.  
    
    > ##### Рис. 26  
    > Цвет предварительного просмотра  
    > ![Цвет предварительного просмотра][ImageColorPreview]  
    
1.  Нажмите кнопку Предварительный просмотр, чтобы открыть окно **выбора цвета**.  
    
    > ##### На рисунке 27  
    > **Выбор цвета**  
    > ![Выбор цвета][ImageColorPicker]  
    
Ниже приведено описание каждого элемента пользовательского интерфейса в **средстве выбора цвета**.  

> ##### Рис. 28  
> Палитра цветов с заметками  
> ![Палитра цветов с заметками][ImageColorPickerAnnotated]  

1.  **Тени**.  
1.  **Пипетка**.  Посмотрите [образец цвета на странице с помощью пипетки](#sample-a-color-off-the-page-with-the-eyedropper).  
1.  **Копирование в буфер обмена**.  Скопируйте **Отображаемое значение** в буфер обмена.  
1.  **Отображаемое значение**.  Представление RGBA, HSLA или шестнадцатеричного представления цвета.  
1.  **Цветовая палитра**.  Щелкните один из этих квадратов, чтобы изменить цвет на этот квадрат.  
1.  **Оттенок**.  
1.  **Opacity (прозрачность**).  
1.  **Показать переключатель значения**.  Переключение между представлениями "RGBA", "HSLA" и "шестнадцатеричный" текущего цвета.  
1.  **Переключатель цветовой палитры**.  Переключение между [палитрой «дизайн материала][MaterialDesignColorSystem]», настраиваемой палитрой или палитрой цветов страницы.  DevTools создает цветовую палитру страницы на основе цветов, найденных в стилях.  

#### Выбор цвета на странице с помощью пипетки   

Когда вы закроете окно **выбора цвета**, **Eyedropper** ![ Пипетка по ][ImageEyedropperIcon] умолчанию будет включена.  Чтобы изменить выбранный цвет на другой цвет на странице, выполните указанные ниже действия.  

1.  Наведите указатель мыши на целевой цвет в окне просмотра.  
1.  Щелкните, чтобы подтвердить.  
    
    > [!NOTE]
    > На [рисунке 29](#figure-29)в **средстве выбора цвета** отображается текущее цветное значение `rgba(0,0,0,0.7)` , которое близко к черному.  Этот цвет следует изменить на черный, выделенный в окне просмотра, после того как вы щелкните черный.  
    
    > ##### Рис. 29  
    > Использование пипетки  
    > ![Использование пипетки][ImageUsingEyedropper]  
    
 



<!-- image links -->  

[ImageAddBackgroundColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-background-color-icon.msft.png  
[ImageAddBoxShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-box-shadow-icon.msft.png  
[ImageAddColorIcon]: /microsoft-edge/devtools-guide-chromium/media/add-color-icon.msft.png  
[ImageAddTextShadowIcon]: /microsoft-edge/devtools-guide-chromium/media/add-text-shadow-icon.msft.png  
[ImageEyedropperIcon]: /microsoft-edge/devtools-guide-chromium/media/eyedropper-icon.msft.png  
[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageSelectAnElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-an-element-icon.msft.png  

[ImageSelectedElement]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1.msft.png "Рисунок 1: пример выбранного элемента"  
[ImageViewRuleStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-highlight.msft.png "Рисунок 2: Просмотр таблицы стилей, в которой определено правило"  
[ImageComputedTab]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-h1.msft.png "Рисунок 3: вычисляемая вкладка"  
[ImageBoxModel]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-h1-2.msft.png "Рисунок 4: Схема модели Box"  
[ImageStylesFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-color.msft.png "Рисунок 5: Фильтрация вкладки "стили""  
[ImageComputerFilter]: /microsoft-edge/devtools-guide-chromium/media/css-elements-computed-filter-100.msft.png "Рисунок 6: Фильтрация вычисляемой вкладки"  
[ImagePseudoClass]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-hov-hover.msft.png "Рисунок 7: переключение: псевдо-класс "наведение""  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-coverage.msft.png "Рисунок 8: Открытие вкладки «покрытие» из меню команд"  
[ImageCoverageEmpty]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-empty.msft.png "Рисунок 9: вкладка "покрытие""  
[ImageCoverageOverview]: /microsoft-edge/devtools-guide-chromium/media/css-console-qs-coverage-run.msft.png "Рисунок 10: Общие сведения о том, сколько CSS (и JavaScript) используется и неиспользуемо"  
[ImageCoverageDetail]: /microsoft-edge/devtools-guide-chromium/media/css-sources-css-coverage.msft.png "Рисунок 11: разбиение по строкам использованной и неиспользуемой CSS"  
[ImageInlineDeclarations]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-margin-top-background-color.msft.png "Рисунок 12: Добавление встроенных объявлений"  
[ImageAddDeclarationExistingRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style.msft.png "Рисунок 13: Добавление объявления к правилу стиля"  
[ImageAddDeclarationExistingRule2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-border-bottom-style-dropdown.msft.png "Рисунок 14: изменение значения объявления"  
[ImageElementClasses]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-filter-classes.msft.png "Рис. 15: область «классы элементов»"  
[ImageStyleRule]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new.msft.png "Рисунок 16: Добавление нового правила стиля"  
[ImageChooseStylesheet]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-style-new-select-exisiting.msft.png "Рисунок 17: Выбор таблицы стилей"  
[ImageInsertStyleRuleBelow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-insert-style-rule-below.msft.png "Рисунок 18: Вставка правила стиля ниже"  
[ImageRevealMore]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-new-rule-styles.msft.png "На рисунке 19 показано, как Показать дополнительные действия."  
[ImageInsertStyleRuleBelow2]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-more-options-insert-style-rule-below.msft.png "Рисунок 20: панель инструментов "другие действия""  
[ImageToggleDeclaration]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-deactivated.msft.png "Рисунок 21: переключение объявления"  
[ImageAddBackgroundColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-background-color.msft.png "Рисунок 22: Добавление цвета фона"  
[ImageAddColor]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-color.msft.png "Рисунок 23: Добавление цвета"  
[ImageAddBoxShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-box-shadow.msft.png "Рисунок 24: Добавление тени поля"  
[ImageAddTextShadow]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-add-text-shadow.msft.png "Рисунок 25: Добавление тени текста"  
[ImageColorPreview]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-overlay-color-box.msft.png "Рисунок 26: предварительный просмотр цвета"  
[ImageColorPicker]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker.msft.png "Рисунок 27: палитра цветов"  
[ImageColorPickerAnnotated]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-rule-color-picker-annotated.msft.png "Рис. 28: палитра цветов с аннотированием"  
[ImageUsingEyedropper]: /microsoft-edge/devtools-guide-chromium/media/css-color-picker-eye-dropper.msft.png "Рис. 29: Использование пипетки"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  
[DevToolsCSSGetStartedAddPseudoState]: /microsoft-edge/devtools-guide-chromium/css/index#add-a-pseudostate-to-a-class "Добавление PseudoState в класс — начало работы с просмотром и изменением CSS"  
[DevToolsCSSGetStartedTutorial]: /microsoft-edge/devtools-guide-chromium/css/index#view-the-css-for-an-element "Просмотр CSS для элемента — начало работы с просмотром и изменением CSS"  
[DevToolsCssPrintPreview]: /microsoft-edge/devtools-guide-chromium/css/print-preview "Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS)"  
[DevToolsJavascriptReferenceFormat]: /microsoft-edge/devtools-guide-chromium/javascript/reference#make-a-minified-file-readable "Создание доступного для чтения файла minified-справочника по отладке JavaScript"  

[MaterialDesignColorSystem]: https://material.io/guidelines/style/color.html#color-color-palette "Макет "Цветовая система-материал""  
[MDNBoxModel]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Box_model "Модель Box | MDN"  
[MDNSelectorTypes]: https://developer.mozilla.org/docs/Web/CSS/Specificity#Selector_Types "Типы выбора — "конкретное |" MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
