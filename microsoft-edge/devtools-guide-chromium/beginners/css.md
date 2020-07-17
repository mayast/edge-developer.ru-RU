---
title: 'DevTools для начинающих: Приступая к работе с CSS'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: fba049a20a7b5f981130b4d9e60c37b07dc7e092
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882739"
---
<!-- Copyright Katherine Jackson 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->

# DevTools для начинающих: Приступая к работе с CSS   

В этом учебнике вы узнаете, как использовать CSS для стиля веб-страницы.  Кроме того, вы узнаете, как использовать Microsoft Edge DevTools для экспериментов с изменениями CSS.  

Это второй учебник из ряда учебников, в котором рассказывается о том, что такое веб-разработка и Microsoft Edge DevTools.  Вы получаете практический опыт, завершив создание собственного веб-сайта.  Вам не нужно выполнять первый учебник, прежде чем делать это.  Здесь вы можете приступить к работе.  [Настройка кода](#set-up-your-code) показывает, как это сделать.  

> [!NOTE]
> Этот учебник предназначен для абсолютных новичков и специализируется на **основах разработки веб-приложений** и основах использования DevTools для экспериментов с CSS.  Если вам нужен учебник, который фокусируется только на DevTools, ознакомьтесь [со статьей Приступая к просмотру и изменению CSS][DevtoolsCssIndex].  

На данный момент ваш веб-сайт выглядит следующим образом:  

> ##### Рис. 1  
> Как выглядит ваш веб-сайт  
> ![Как выглядит ваш веб-сайт][ImageCssIntro1]  

После завершения работы с учебником он будет выглядеть примерно так:  

> ##### Рисунок 2  
> Как будет выглядеть ваш веб-сайт в конце учебника  
> ![Как будет выглядеть ваш веб-сайт в конце учебника][ImageCssIntro2]  

## Цели   

В конце этого учебника вы узнаете:  

*   Использование CSS для стиля веб-страницы.  
*   Использование Microsoft Edge DevTools для экспериментов с CSS.  
*   Разница между платформами CSS и CSS.  

У тебя также есть реальный веб-сайт!  

## Предварительные условия   

Прежде чем приступить к работе с учебником, выполните следующие требования:  

*   Закончите [работу с HTML и моделью DOM][DevToolsBeginnersHtml] или убедитесь в том, что вы знаете HTML и модель DOM, похожую на то, что научились в этом учебнике.  
*   Скачайте веб-браузер [Microsoft Edge][MicrosoftEdgeInsider] .  В этом учебнике используется набор средств разработки веб-приложений, которые называются Microsoft Edge DevTools, которые встроены в Microsoft Edge.  

## Настройка кода   

Чтобы приступить к созданию сайта, вам нужно настроить код:  

1.  **Если вы уже завершили первый учебник в этой серии, пропустите этот раздел.  Продолжайте использовать код из последнего учебника, Приступая к [работе с HTML и DOM][DevToolsBeginnersHtml].**  
1.  Откройте [Исходный код][GlitchCookedAmphibianIndex].  Эта вкладка браузера будет называться **вкладкой "Редактирование"**.  
    
    > ##### Рисунок3  
    > Вкладка "Редактирование"  
    > ![Вкладка "Редактирование"][ImageCssSetup1]  
    
1.  Щелкните **готовил-amphibian**.  Всплывающее меню.  
    
    > ##### Рисунок4  
    > Меню "Параметры проекта"  
    > ![Меню "Параметры проекта"][ImageCssSetup2]  

1.  Щелкните **Remix Project (проект**).  Сбой создает копию проекта, которую можно изменить.  
    
    > [!NOTE]
    > Сбой генерирует случайное имя для нового проекта.  
    
1.  Нажмите кнопку **Показать** и выберите **в новом окне**.  Откроется другая вкладка с активным представлением сайта.  Эта вкладка браузера будет называться **вкладкой Быстрая**.  
    
    > ##### Рисунок 5  
    > Вкладка "динамический"  
    > ![Вкладка "динамический"][ImageCssSetup3]  

## Общие сведения о CSS   

**CSS** — это язык компьютера, который определяет макет и стиль веб-страниц.  Например, вот абзац с границей:  

> ##### Рисунок6  
> Этот стиль помечен с помощью CSS  
> ![Этот стиль помечен с помощью CSS][ImageCssStyled]  

Ниже приведен код HTML и CSS, который используется для создания абзаца.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

`style="border: 1px dashed red; padding: 5px;"` возможно, вам покажется, что у вас новый.  Остальные должны выглядеть знакомым.  Если это не так, сначала приступайте [к работе с помощью HTML и DOM][DevToolsBeginnersHtml] перед тем, как попытаться воспользоваться этим учебником.  

## Добавление встроенных стилей   

Используйте **встроенные стили** , если вы хотите применить стили к одному элементу.  Попробуйте вот так:  

1.  Вернитесь на вкладку Правка и откройте окно `index.html` .  
    
    > ##### Рисунок7  
    > `index.html`  
    > ![index.html][ImageCssInline1]  

1.  Добавить `style="background-color: aliceblue;"` в `<nav>` .  В блоке кода, приведенном ниже, четвертая строка кода имеет тот же адрес, который нужно изменить.  Вот и все! вы можете сделать так, чтобы в нужном окне вы могли поместить новый код в нужное место.  
    
    ```html
    ...
        ...
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav style="background-color: aliceblue;">
                <ul>
                    <li><a href="/">Home</a></li>
                    ...
                ...
            ...
        ...
    ...
    ```  

1.  Перейдите на **вкладку динамический** , чтобы увидеть изменения.  `<nav>`Теперь фон раздела синего цвета.  
    
    > ##### Рисунок8  
    > Цвет фона, который находится за домашней страницей и ссылками на контакты, стал синей  
    > ![Цвет фона, который находится за домашней страницей и ссылками на контакты, стал синей][ImageCssInline2]  

## Повторное использование стилей на одной странице с внутренними таблицами стилей   

Ранее вы увидели встроенный стиль, который применяет стиль для одного тега, `<p>` как показано ниже.  

```html
<p style="border: 1px dashed red; padding: 5px;">
    This has been styled with CSS.
</p>
```  

Что делать, если вы хотите `<p>` , чтобы все элементы на веб-странице были применены таким же образом?  Вам потребуется скопировать код и вставить его в каждый один `<p>` тег на вашем сайте.  Это не слишком много времени и сил.  Если вы хотите внести изменения, вам придется заново изменить каждый из тегов.  **Внутренние таблицы стилей** позволяют создавать CSS один раз, чтобы она применялась к нескольким элементам.  Попробуйте вот так:  

1.  На вкладке динамический щелкните **контакт** , чтобы перейти на страницу контакта.  Обратите внимание на шрифт **домашних** и **контактных**данных.  
    
    > ##### Рисунок9  
    > Страница "контакт"  
    > ![Страница "контакт"][ImageCssInternal1]  

1.  На **вкладке "редактор**" перейдите в раздел `contact.html` .  
1.  Добавьте следующий код `contact.html` .  Помните, что вам нужно добавить строки, начинающиеся с `<style>` и заканчивая данными `</style>` .  Другой код — это только то, что вы знаете, где разместить новый код.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <style>
                li a {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        </head>
        ...
    ...
    ```  
    
1.  Вернитесь на **вкладку динамический**.  
1.  Нажмите кнопку " **контакт** ", чтобы вернуться на страницу контакта.  Изменился шрифт " **Главная** " и " **контакт** ".  
    
    > ##### Рисунок 10  
    > Изменен шрифт ссылок на домашнюю страницу и контакт контакта  
    > ![Изменен шрифт ссылок на домашнюю страницу и контакт контакта][ImageCssInternal2]  
    
### Общие сведения о внутренних таблицах стилей   

Внутренние таблицы стилей. Примените стили с помощью **селекторов**.  Селекторы — это шаблоны, которые могут применяться к одному или нескольким элементам HTML.  Например, в предыдущем коде выполните указанные ниже действия.  

```html
...
    ...
        ...
        <style>
            li a {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

`li a` — Это селектор, который преобразуется в "Any `<li>` , которая содержит `<a>` ".  Браузер изменит шрифт **домашних** и **контактных** ссылок, так как они соответствуют этому шаблону.  

```html
...
    ...
        ...
            ...
                <li><a href="/">Home</a></li>
                <li><a href="/contact.html">Contact</a></li>
                ...
            ...
        ...
    ...
...
```  

`font-family: 'Courier New', Courier, serif` является **объявлением**.  Объявление состоит из двух частей: **Свойства** и **значения**.  `font-family` является свойством и `'Courier New', Courier, serif` является значением этого свойства.  Свойство описывает общий способ изменения стиля элемента, а также указывает, как именно оно должно изменяться.  Например, `font-family: 'Courier New', Courier, serif` предоставляет браузеру следующую инструкцию: "Установка шрифта элементов, которые соответствуют шаблону `li a` `'Courier New'` .  Если этот шрифт недоступен, используйте `Courier` .  Если это недоступно, используйте `serif` ".  

### Добавление нескольких селекторов в набор правил   

Блок кода CSS вроде того, что вы видите ниже, называется набором **правил**.  

```css
li a {
  font-family: 'Courier New', Courier, monospace;
}
```  

Используйте запятые, чтобы добавить в набор правил несколько селекторов.  Попробуйте вот так:  

1.  На **вкладке Редактор**откройте `contact.html` .  
1.  После `li a` ввода `, h1` .  

    ```html
    ...
        ...
            ...
            <style>
                li a, h1 {
                  font-family: 'Courier New', Courier, Serif;
                }
            </style>
            ...
        ...
    ...
    ```  

    Таким образом браузер применяет `<h1>` элементы стиля так же, как и элементы, которые соответствуют шаблону `li a` .  
    
1.  Перейдите на **вкладку динамический**.  
1.  Щелкните ссылку **контакт** , чтобы вернуться на страницу контакта.  Теперь **свяжитесь со мной!** имеет тот же шрифт, что и ссылки для навигации.  
    
    > ##### Рисунок11  
    > Текст "контактные данные!" Теперь тот же шрифт, что и ссылки на домашнюю и контактный  
    > ![Текстовые контакты!  Теперь тот же шрифт, что и ссылки на домашнюю и контактный][ImageCssMultiple1]  

## Поэкспериментировать с DevTools   

По мере того как вы продолжите путешествие в главную веб-разработку, вы обнаружите, что эта таблица CSS может быть сложной.  Вы пишете некоторые стили CSS и ожидаете, что они будут отображаться одним из них, но браузер делает что-то совершенно другое.  Microsoft Edge DevTools упрощает эксперименты с изменениями и немедленно показывает, как эти изменения влияют на страницу.  

### Добавление объявления к существующему правилу в DevTools   

Если вы хотите выполнить итерацию по стилю существующего элемента, добавьте объявление к существующему набору правил.  Попробуйте вот так:  

1.  Щелкните ссылку " **Домашняя страница** " правой кнопкой мыши и выберите команду " **проверить**".  
    
    > ##### Рисунок12  
    > Проверка ссылки на домашнюю страницу  
    > ![Проверка ссылки на домашнюю страницу][ImageCssAdd1]  
    
    DevTools открывается вместе со страницей.  Код, представляющий ссылку на домашнюю страницу, `<a href="/">Home</a>` выделяется синим цветом в дереве DOM.  Это должно быть знакомо с тем, как начать [работу с HTML и DOM][DevToolsBeginnersHtml].  На вкладке " **стили** " под деревом DOM вы видите `font-family: 'Courier New', Courier, serif` объявление, которое вы добавили `contact.html` раньше.  
    
    > ##### Рисунок13  
    > Вкладка "стили" находится под деревом DOM  
    > ![Вкладка "стили" находится под деревом DOM][ImageCssAdd2]  
    
    Если окно DevTools является широкой страницей, вкладка стили находится справа от дерева DOM.  
    
    > ##### Рисунок14  
    > Вкладка "стили" справа от дерева DOM  
    > ![Вкладка "стили" справа от дерева DOM][ImageCssAdd3]  
    
1.  Щелкните пробел ниже, `font-family: 'Courier New', Courier, Serif` чтобы добавить новое объявление.  
    
    > ##### Рисунок15  
    > Добавление нового объявления  
    > ![Добавление нового объявления][ImageCssAdd4]  
    
1.  Введите текст `color` и нажмите клавишу `Enter` .  Пользовательский интерфейс автозаполнения предлагает параметры по мере ввода.  
    
    > ##### Рисунок16  
    > Ввод с клавиатуры `color`  
    > ![Цвет текста][ImageCssAdd5]  

1.  Введите текст `magenta` и нажмите `Enter` еще раз.  Весь текст на странице контакта стал пурпурным.  
    
    > ##### Рисунок17  
    > Ввод с клавиатуры `magenta`  
    > ![Ввод пурпурного][ImageCssAdd6]  
    
### Изменение объявления в DevTools   

Вы также можете изменить существующие объявления в DevTools.  Попробуйте вот так:  

1.  Щелкните пурпурный квадрат рядом с `magenta` .  Появится палитра выбора цвета.  
    
    > ##### Рис. 18  
    > Выбор цвета  
    > ![Выбор цвета][ImageCssEdit1]  
    
1.  С помощью средства выбора цвета измените текст шрифта на нужный цвет.  
    
    > ##### На рисунке 19  
    > Изменение цвета шрифта на фиолетовый с помощью средства выбора цвета  
    > ![Изменение цвета шрифта на фиолетовый с помощью средства выбора цвета][ImageCssEdit2]  

### Добавление нового набора правил в DevTools   

Вы также можете добавлять новые наборы правил в DevTools.  Попробуйте вот так:  

1.  Нажмите **новое правило стиля** ![ новое правило стиля ][ImageNewStyleRuleIcon] , которое находится рядом с полем **CLS**.  В качестве Selector появится пустой набор правил `a` .  
    
    > ##### Рис. 20  
    > Добавление нового правила  
    > ![Добавление нового правила][ImageCssRule1]  
    
1.  Заменить `a` на `a:hover` .  
    
    > ##### Рисунок 21  
    > Замена `a` на `a:hover`  
    > ![Замена в a:hover][ImageCssRule2]  
    
    `:hover` является **псевдо-классом**.  Используйте псевдо-классы для стиля элементов при вводе специальных состояний.  Например, `a:hover` стиль вступает в силу только при наведении указателя мыши на `<a>` элемент.  
    
1.  Щелкните между скобками, чтобы добавить новое объявление.  
1.  Введите `background-color` имя объявления и нажмите клавишу `Enter` .  
    
    > ##### Рис. 22  
    > Ввод с клавиатуры `background-color`  
    > ![Ввод цвета фона][ImageCssRule3]  
    
1.  Введите `green` значение объявления и нажмите клавишу `Enter` .  
    
    > ##### Рис. 23  
    > Ввод с клавиатуры `green`  
    > ![Ввод зеленого][ImageCssRule4]  
    
1.  Наведите указатель мыши на ссылку " **Домашняя страница** ".  Фон ссылки становится зеленым.  
    
    > ##### Рисунок 24  
    > Наведите указатель мыши на домашнюю ссылку, чтобы отобразить зеленый фон.  
    > ![Наведите указатель мыши на домашнюю ссылку, чтобы отобразить зеленый фон.][ImageCssRule5]  
    
## Повторное использование стилей на разных страницах с внешними таблицами стилей   

Ранее вы добавили эту внутреннюю таблицу стилей в `contact.html` :  

```html
...
    ...
        ...
        <style>
            li a, h1 {
              font-family: 'Courier New', Courier, Serif;
            }
        </style>
        ...
    ...
...
```  

Что делать, если вы захотите стиль `index.html` одинаково?  Что делать, если у вас *тысячи* страниц и вы хотите применить эти стили ко всем из них?  Вам потребуется скопировать и вставить этот внутренний набор таблиц в каждую веб-страницу на сайте.  **Внешние таблицы стилей** позволяют создавать CSS, пока они применены к нескольким страницам.  Попробуйте вот так:  

1.  Сначала перезагрузите вкладку Live, чтобы удалить изменения, внесенные в DevTools.  
    
    > ##### Рис. 25  
    >  После перезагрузки страницы изменения, внесенные в DevTools, исчезают  
    > ![ После перезагрузки страницы изменения, внесенные в DevTools, исчезают][ImageCssExternal01]  
    
1.  Вернитесь на **вкладку Редактор** и откройте ее `contact.html` .  
    
    > ##### Рис. 26  
    > `contact.html`  
    > ![contact.html][ImageCssExternal02]  
    
1.  Удалить все между `<style>` и `</style>` , включая `<style>` и `</style>` .  
    
    > ##### На рисунке 27  
    > Тег Style был удален  
    > ![Тег Style был удален][ImageCssExternal03]  
    
1.  Перейдите к `index.html` тегу и удалите `style="background-color: aliceblue;"` его `<nav>` .  Теперь вы удалили все CSS-таблицы, которые вы ранее добавили на сайт.  
    
    > ##### Рис. 28  
    > Встроенный стиль удален из элемента навигации  
    > ![Встроенный стиль удален из элемента навигации][ImageCssExternal04]  

1.  Нажмите кнопку **создать файл**.  
    
    > ##### Рис. 29  
    > Диалоговое окно "Создание файла"  
    > ![Диалоговое окно "Создание файла"][ImageCssExternal05]  
    
1.  Замените `cool-file.js` на `style.css` и нажмите кнопку **Добавить файл**.  
    
    > ##### Рис. 30  
    > Ввод с клавиатуры `style.css`  
    > ![Ввод Style. CSS][ImageCssExternal06]  
    
1.  Вставьте этот код в `style.css` :  
    
    ```css
    li a, h1 {
      font-family: 'Courier New', Courier, Serif;
    }
    a:hover {
      background-color: green;
    }
    nav {
      background-color: aliceblue;
    }
    ```  
    
    > ##### На рисунке 31  
    > Добавление кода в `style.css`  
    > ![Добавление кода в Style. CSS][ImageCssExternal07]  
    
    На этом этапе вы создали внешнюю таблицу стилей, но ваш HTML-код еще не знает, что он существует.  
    
1.  Open (открыть) `index.html` .  
1.  Добавьте `<link rel="stylesheet" href="style.css">` в свой HTML-код.  
    
    ```html
    ...
        <head>
            ...
            <meta name="viewport" content="width=device-width, initial-scale=1">
            <link rel="stylesheet" href="style.css">
        </head>
        ...
    ...
    ```  

    > ##### Рисунок 32  
    > Связывание с `style.css`  
    > ![Связывание с Style. CSS][ImageCssExternal08]  

1.  Перейдите к разделу `contact.html` и добавьте в него ссылку.  
    
    > ##### Рисунок 33  
    > Связывание `style.css` в `contact.html`  
    > ![Связывание со стилем Style. CSS в contact.html][ImageCssExternal09]  

1.  Перейдите на **вкладку динамический**.  Домашняя страница теперь имеет тот же шрифт, что и в последнем разделе, и в синем разделе навигации.  
    
    > ##### Рисунок 34  
    > Домашняя страница  
    > ![Домашняя страница][ImageCssExternal10]  
    
1.  Щелкните ссылку **контакт** , чтобы перейти на страницу контакта.  Страница контакта имеет тот же формат, что и домашняя страница.  
    
    > ##### Рисунок 35  
    > Страница "контакт"  
    > ![Страница "контакт"][ImageCssExternal11]  
    
## Использование платформы CSS   

**Платформы CSS** — это коллекции стилей, разработанных другими разработчиками, которые упрощают создание привлекательных веб-сайтов.  Вместо того чтобы определять стили самостоятельно, платформа предоставляет коллекцию стилей, которые можно использовать в элементах страницы.  

1.  Скопируйте приведенный ниже код.  
    
    ```html
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.1.1/css/bootstrap.min.css">
    ```  
    
1.  Перейдите на вкладку Правка и вставьте код в `contact.html` .  
    
    > ##### Рисунок 36  
    > Связывание с платформой в `contact.html`  
    > ![Связывание с платформой в contact.html][ImageCssFramework1]  
    
1.  Также вставьте код в `index.html` .  
    
    > ##### Рисунок 37  
    > Связывание с платформой в `index.html`  
    > ![Связывание с платформой в index.html][ImageCssFramework2]  
    
1.  Вернитесь на вкладку динамический, чтобы просмотреть изменения.  Несмотря на то, что цвет фона `<nav>` и шрифт элементов совпадают `li a` , изменился шрифт других элементов.  
    
    > ##### Рисунок 38  
    > Некоторые шрифты на домашней странице изменились из-за платформы  
    > ![Некоторые шрифты на домашней странице изменились из-за платформы][ImageCssFramework3]  

### Использование класса   

В последнем разделе вы добавили начальную загрузку на веб-страницы, которая изменила шрифты для некоторых элементов на вашем сайте.  Структуры CSS помогают вносить существенные изменения на странице с помощью очень небольшого количества кода.  Попробуйте выполнить его прямо сейчас, изменив верхний колонтитул:  

1.  Скопируйте этот код:  
    
    ```html
    class="jumbotron jumbotron-fluid"  
    ```  
    
1.  Добавьте этот код в `<header>` тег в `index.html` .  
    
    > ##### Рисунок 39  
    > Добавление классов в `index.html`  
    > ![Добавление классов в index.html][ImageCssJumbotron1]  
    
1.  Добавьте код в `<header>` тег `contact.html` .  
    
    > ##### Рисунок 40  
    > Добавление классов в `contact.html`  
    > ![Добавление классов в contact.html][ImageCssJumbotron2]  
    
1.  Просмотрите изменения на вкладке "живые".  На вашем заголовке есть большое затененное поле.  
    
    > ##### Рисунок 41  
    > Теперь верхний колонтитул имеет большой серый прямоугольник вокруг него.  
    > ![Теперь верхний колонтитул имеет большой серый прямоугольник вокруг него.][ImageCssJumbotron3]  
    
### Общие сведения о классах   

Классы позволяют назначать коллекции стилей произвольным элементам.  Например, установка `class` атрибута `<header>` тегов для `jumbotron` применения к ним указанных ниже стилей.  

```css
.jumbotron {
  padding: 2rem 1rem;
  margin-bottom: 2rem;
  background-color: #e9ecef;
  border-radius: .3rem;
}
```  

Одно из преимуществ классов состоит в том, что они позволяют применять стили к любым нужным элементам.  Например, предположим, что вы хотите установить для *некоторых* `<p>` элементов цвет фона, который будет фиолетовым, но не *всеми* .  Вы можете определить стиль в классе.  

```css
.custom-background {
  background-color: purple;
}
```  

А затем примените этот класс только к `<p>` элементам, которые вы хотите отформатировать:  

```html
...
    ...
        ...
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        <p>This won't be purple.</p>
        <p class="custom-background">This will be purple.</p>
        ...
    ...
...
```  

### Выравнивание элементов   

Начальная загрузка также предоставляет классы для выравнивания элементов.  Попробуйте вот так:  

1.  Вернитесь на вкладку Редактор и откройте ее `index.html` .  
1.  Добавьте `class="container-fluid"` в свой `<body>` тег.  
    
    > ##### Рисунок 42  
    > Добавление `container-fluid` класса  
    > ![Добавление класса Container-жидкости][ImageCssAlign1]  

1.  Обтекание `<nav>` `<main>` элементов `<div class="row">` .  `</div>`Чтобы правильно закрыть новый тег, убедитесь в том, что вы хотите сделать `</main>` это.  
    
    > ##### Рисунок 43  
    > Добавление строки  
    > ![Добавление строки][ImageCssAlign2]  
    
1.  Добавьте `class="col-3"` теги в тег `<nav>` и `class="col-9"` в `<main>` тег.  
    
    > ##### Рисунок 44  
    > Добавление `col-3` и использование `col-9` классов  
    > ![Добавление классов Col-3 и Col-9][ImageCssAlign3]  
    
1.  Просмотрите изменения на вкладке "живые".  
    
    > ##### Рисунок 45  
    > Содержимое элемента навигации теперь находится слева от основного содержимого.  
    > ![Содержимое элемента навигации теперь находится слева от основного содержимого.][ImageCssAlign4]  
    
## Дальнейшие действия   

Поздравляем!  Готово!  

*   Лучший способ улучшить качество веб-приложений — создать дополнительные сайты.  Не беспокойтесь о нарушениях.  Просто восприяты и намерены очень удобно.  
*   Ознакомьтесь со статьей [Введение в CSS][MDNCssFirstSteps] , чтобы узнать больше о стилях веб-страниц.  
*   Узнайте больше о том, как можно использовать DevTools для экспериментов с CSS [-таблицей][DevtoolsCssIndex] .  

<!--- image links --->  

[ImageNewStyleRuleIcon]: /microsoft-edge/devtools-guide-chromium/media/new-style-rule-icon.msft.png  

[ImageCssIntro1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro1.msft.png "Рисунок 1: как выглядит ваш сайт"  
[ImageCssIntro2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-intro2.msft.png "На рисунке 2 показано, как будет выглядеть ваш сайт в конце учебника."  
[ImageCssSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup1.msft.png "Рисунок 3: вкладка "Редактирование""  
[ImageCssSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup2.msft.png "Рисунок 4: меню "Параметры проекта""  
[ImageCssSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-setup3.msft.png "Рисунок 5. Вкладка "динамический""  
[ImageCssStyled]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-red_paragraph.msft.png "Рисунок 6: этот стиль помечен с помощью CSS"  
[ImageCssInline1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline1.msft.png "Рисунок 7: index.html"  
[ImageCssInline2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-inline2.msft.png "Рисунок 8: цвет фона, на котором находятся ссылки на домашнюю и контактный, теперь синего цвета"  
[ImageCssInternal1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal1.msft.png "Рисунок 9: страница "контакт""  
[ImageCssInternal2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-internal2.msft.png "Рисунок 10: изменен шрифт ссылок на домашнюю и контактный"  
[ImageCssMultiple1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-multiple1.msft.png "Рисунок 11: текст "контактные данные" теперь имеет тот же шрифт, что и ссылки на домашнюю и контактный."  
[ImageCssAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add1.msft.png "Рисунок 12: Проверка ссылки на домашнюю страницу"  
[ImageCssAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add2.msft.png "Рисунок 13. Вкладка "стили" находится под деревом DOM"  
[ImageCssAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add3.msft.png "Рисунок 14: вкладка "стили" справа от дерева DOM"  
[ImageCssAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add4.msft.png "Рисунок 15: Добавление нового объявления"
[ImageCssAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add5.msft.png "Рисунок 16: ввод цвета"  
[ImageCssAdd6]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-add6.msft.png "Рисунок 17: ввод пурпурного"  
[ImageCssEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit1.msft.png "Рисунок 18: палитра цветов"  
[ImageCssEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-edit2.msft.png "На рисунке 19 показано, как изменить цвет шрифта на фиолетовый с помощью палитры цветов."  
[ImageCssRule1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule1.msft.png "Рисунок 20: Добавление нового правила"  
[ImageCssRule2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule2.msft.png "Рисунок 21: Замена a на a:hover"  
[ImageCssRule3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule3.msft.png "Рисунок 22: ввод цвета фона"  
[ImageCssRule4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule4.msft.png "Рисунок 23: ввод зеленого"  
[ImageCssRule5]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-rule5.msft.png "Рис. 24: наведение указателя мыши на домашнюю ссылку для отображения зеленого фона"  
[ImageCssExternal01]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external1.msft.png "Рис. 25: после перезагрузки страницы изменения, внесенные в DevTools, исчезают"  
[ImageCssExternal02]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external2.msft.png "Рисунок 26: contact.html"  
[ImageCssExternal03]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external3.msft.png "Рисунок 27: тег Style был удален"  
[ImageCssExternal04]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external4.msft.png "Рис. 28: встроенный стиль удален из элемента навигации."  
[ImageCssExternal05]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external5.msft.png "Рис. 29: диалоговое окно "Создание файла""  
[ImageCssExternal06]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external6.msft.png "Рисунок 30: ввод Style. CSS"  
[ImageCssExternal07]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external7.msft.png "Рисунок 31: Добавление кода в Style. CSS"  
[ImageCssExternal08]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external8.msft.png "Рисунок 32: связывание со стилем Style. CSS"  
[ImageCssExternal09]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external9.msft.png "Рисунок 33: связывание со стилем Style. CSS в contact.html"  
[ImageCssExternal10]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external10.msft.png "Рисунок 34: Главная страница"  
[ImageCssExternal11]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-external11.msft.png "Рисунок 35: страница контакта"  
[ImageCssFramework1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework1.msft.png "Рисунок 36: связывание с платформой в contact.html"  
[ImageCssFramework2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework2.msft.png "Рисунок 37: связывание с платформой в index.html"  
[ImageCssFramework3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-framework3.msft.png "Рисунок 38: некоторые шрифты на домашней странице изменились из-за платформы"  
[ImageCssJumbotron1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron1.msft.png "Рисунок 39: Добавление классов в index.html"  
[ImageCssJumbotron2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron2.msft.png "Рисунок 40: Добавление классов в contact.html"  
[ImageCssJumbotron3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-jumbotron3.msft.png "Рисунок 41: теперь верхний колонтитул имеет большой серый прямоугольник вокруг него."  
[ImageCssAlign1]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align1.msft.png "Рисунок 42: Добавление класса Container-жидкостный"  
[ImageCssAlign2]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align2.msft.png "Рисунок 43: Добавление строки"  
[ImageCssAlign3]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align3.msft.png "Рисунок 44: Добавление классов Col-3 и Col-9"  
[ImageCssAlign4]: /microsoft-edge/devtools-guide-chromium/media/beginners-css-align4.msft.png "Рисунок 45: содержимое элемента навигации теперь находится слева от основного содержимого."  

<!--- links  --->  

[DevToolsBeginnersHtml]: html.md "DevTools для начинающих: Приступая к работе с HTML и моделью DOM"  
[DevtoolsCssIndex]: ../css/index.md "Приступая к просмотру и изменению каскадных таблиц стилей"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  

[GlitchCookedAmphibianIndex]: https://glitch.com/edit/#!/cooked-amphibian?path=index.html "index.html-готовил-amphibian | Цепь"  

[MDNCssFirstSteps]: https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS "Первые шаги CSS | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/css) и [Katherine Джексон][KatherineJackson] \ (помощник службы технической поддержки, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
