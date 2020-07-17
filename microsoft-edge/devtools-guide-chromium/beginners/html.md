---
title: 'DevTools для начинающих: Приступая к работе с HTML и моделью DOM'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: d992a6ca68de07c879ca8e319ee6c22782924a6b
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882732"
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

# DevTools для начинающих: Приступая к работе с HTML и моделью DOM   

Это первый из ряда учебников, в котором изучаются основы разработки веб-приложений.  Кроме того, вы узнаете о наборе средств для веб-разработчиков, именуемых Microsoft Edge DevTools, которые могут повысить производительность.  

В этом конкретном учебнике вы узнаете о HTML и модели DOM.  HTML — это одна из основных методик разработки веб-приложений.  Это язык, управляющий структурой и содержимым веб-страниц.  Модель DOM также связана со структурой и контентом веб-страниц, но вы узнаете об этом позже.  

## Цели   

Вы собираетесь познакомиться с веб-разработкой, завершив создание собственного веб-сайта.  Завершив все учебные курсы в серии *DevTools для начинающих* , ваш готовый веб-сайт будет выглядеть так, как **показано на рисунке 1**.  

> ##### Рис. 1  
> Готовый сайт  
> ![Готовый сайт][ImageHtmlFinished]  

В конце этого учебника вы узнаете:  

*   Как HTML и DOM создают содержимое, которое отображается на веб-страницах.  
*   Как Microsoft Edge DevTools помогает экспериментировать с изменениями HTML и DOM.  
*   Разница между HTML и DOM.  

У тебя также есть реальный веб-сайт!  Вы можете использовать этот сайт для размещения резюме или блога.  

## Предварительные условия   

Прежде чем приступить к работе с учебником, выполните следующие требования:  

*   Если вы не знакомы с форматом HTML, ознакомьтесь с разделом начало [работы с HTML][MDNGettingStartedHtml].  
*   Скачайте веб-браузер [Microsoft Edge][MicrosoftEdgeInsider] .  В этом учебнике используется набор средств разработки веб-приложений, которые называются Microsoft Edge DevTools, которые встроены в Microsoft Edge.  

## Настройка кода   

Вы собираетесь создать сайт в редакторе кода на веб-сайте с именем "сбой".  

1.  Откройте [Исходный код][GlitchAlluringShockIndex].  Эта вкладка будет называться **вкладкой "редактор"** в рамках этого учебника.  
    > ##### Рисунок 2  
    > Вкладка "редактор"  
    > ![Вкладка "редактор"][ImageHtmlSetup1]  

1.  Щелкните **alluring-удар**.  В левом верхнем углу откроется меню "Параметры проекта".  
    
    > #### Рисунок3  
    > Меню "Параметры проекта"  
    > ![Меню "Параметры проекта"][ImageHtmlSetup2]  
    
1.  Щелкните **Remix Project (проект**).  При возникновении недостаточной версии создается копия проекта, которую можно редактировать и случайным образом создает новое имя для проекта.  Содержимое будет таким же, как и раньше.  
    
    > ##### Рисунок4  
    > Смешанный проект  
    > ![Смешанный проект][ImageHtmlSetup3]  
    
1.  Если вы планируете выполнить следующий учебник в этой серии, нажмите **Вход** и войдите в систему, чтобы завершить работу с учетной записью GitHub или Facebook.  Если вы не входите в свою учетную запись, то после закрытия вкладки Правка вы потеряли возможность изменить этот проект.  
1.  Нажмите кнопку **Показать** и выберите **в новом окне**.  Откроется новая вкладка, на которой отображается активная страница.  Эта вкладка будет называться на **вкладке динамический** в рамках этого учебника.  
    
    > ##### Рисунок 5  
    > Вкладка "динамический"  
    > ![Вкладка "динамический"][ImageHtmlSetup4]  
    
## Добавление содержимого   

Ваш сайт совершенно пуст.  Чтобы добавить содержимое, выполните указанные ниже действия.  

1.  На **вкладке "редактор"** замените `<!-- You're "About Me" will go here.  -->` на `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
            </main>
            ...
        ...
    ...
    ```  
    
    > ##### Рисунок6  
    > На вкладке "редактор" выделена новая программа  
    > ![На вкладке "редактор" выделена новая программа][ImageHtmlAdd1]  
    
1.  Просмотрите изменения на **вкладке "живые"**.  Текст `About Me` будет отображаться на странице.  Он больше, чем оставшаяся часть текста, так как `<h1>` элемент представляет заголовок раздела.  В веб-браузере стили заголовков автоматически заменяются на более крупные размеры шрифта.  
    
    > ##### Рисунок7  
    > Новый заголовок отображается на вкладке "живые"  
    > ![Новый заголовок отображается на вкладке "живые"][ImageHtmlAdd2]  
    
1.  Вернувшись на **вкладку Редактор**, вставьте `<p>I am learning HTML.  Recent accomplishments:</p>` строку под тем местом, где они просто размещены `<h1>About Me</h1>` .  
    
    ```html
    ...
        ...
        <body>
            <p> Your site!</p>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
            </main>
            ...
        ...
    ...
    ```  

    > ##### Рисунок8  
    > На вкладке "редактор" выделена новая программа  
    > ![На вкладке "редактор" выделена новая программа][ImageHtmlAdd3]  
    
1.  Просмотрите изменения на **вкладке "живые"**.  
1.  Вернитесь на **вкладку Редактор**и добавьте список ваших достижений.  
    
    ```html
    ...
        ...
            ...
            <p>I am learning web development.  Recent accomplishments:</p>
            <ul>
                <li>Learned how to set up my code in Glitch.</li>
                <li>Added content to my HTML.</li>
                <li>TODO: Learn how to use Microsoft Edge DevTools to experiment with content changes.</li>
                <li>TODO: Learn the difference between HTML and the DOM.</li>
            </ul>
            ...
        ...
    ...
    ```  
    
    > ##### Рисунок9  
    > На вкладке "редактор" выделена новая программа  
    > ![На вкладке "редактор" выделена новая программа][ImageHtmlAdd4]  
    
1.  Опять же, вернитесь на **вкладку динамический** , чтобы убедиться, что новое содержимое отображается правильно.  
    
    > ##### Рисунок 10  
    > Новый список отображается на вкладке "живые"  
    > ![Новый список отображается на вкладке "живые"][ImageHtmlAdd5]  
    
## Поэкспериментировать с изменениями содержимого в Microsoft Edge DevTools   

Если вы разрабатываете большую страницу с большим количеством HTML-файлов, вы можете представить, что она может быть довольно утомительной, чтобы просматривать изменения, особенно если вы не уверены, что нужно сделать, чтобы они были размещены на странице.  Microsoft Edge DevTools поможет вам поэкспериментировать с изменениями содержимого, не выходя из вкладки Live.  

### Сведения о различиях между HTML и DOM   

Перед тем как приступить к редактированию содержимого в Microsoft Edge DevTools, полезно понять разницу между HTML и DOM.  Лучший способ освоить это можно, например:  

1.  Перейдите на **вкладку динамический**.  В нижней части страницы отображается текст `A new element!?!` .  
    
    > ###### Рисунок11  
    > В нижней части страницы `A new element!?!` можно видеть текст  
    > ![В нижней части страницы текст — это новый элемент!?! может отображаться][ImageHtmlDom1]  
    
1.  Вернитесь на **вкладку Редактор** и попробуйте найти этот текст в `index.html` .  Это не так!  
    
    > ##### Рисунок12  
    > Текст загадкы `A new element!?!` не удается найти в `index.html`  
    > ![Текст "Загадка" — новый элемент!?! не удается найти в index.html][ImageHtmlDom2]  
    
1.  Вернитесь на **вкладку динамический**, щелкните правой кнопкой мыши `A new element!?!` и выберите команду **проверить**.  
    
    > ##### Рисунок13  
    > Проверка текста  
    > ![Проверка текста][ImageHtmlDom3]  
    
    DevTools открывается вместе со страницей.  `<div>A new element!?!</div>` выделяется синим цветом.  Несмотря на то, что структура в DevTools выглядит так же, как и у вашего HTML-кода, она действительно является **деревом DOM**.  
    
    > ##### Рисунок14  
    > DevTools открывается вместе со страницей  
    > ![DevTools открывается вместе со страницей][ImageHtmlDom4]  
    
При загрузке страницы браузер использует HTML для создания *начального* содержимого страницы.  Модель DOM представляет *Текущее* содержимое страницы, которое может изменяться с течением времени.  Содержимое Mysterious `<div>A new element!?!</div>` будет добавлено на страницу из `<script src="new.js"></script>` -за тега в нижней части HTML.  Этот тег вызывает выполнение кода JavaScript.  Более подробно о JavaScript можно узнать в более подробном учебнике, но теперь его можно рассматривать как язык программирования, который может изменить содержимое страницы.  В этом конкретном случае код JavaScript добавляется `<div>A new element!?!</div>` на страницу.  Причина в том, что этот загадкный текст отображается на живой странице, но не в HTML.  

### Редактирование модели DOM   

Если вы хотите быстро поэкспериментировать с изменениями содержимого, не выходя из вкладки Live, попробуйте DevTools.  

1.  В DevTools щелкните правой кнопкой мыши `Your site!` и выберите команду **изменить в HTML**.  

    > ##### Рисунок15  
    > Редактирование узла в формате HTML  
    > ![Редактирование узла в формате HTML][ImageHtmlEdit1]  
    
1.  Замените `<p>Your site!</p>` на код ниже.  
    
    ```html
    ...
        ...
            ...
            <header>
                <p><b>Welcome to my site!</b></p>
                <button>Download my resume</button>
            </header>
            ...
        ...
    ...
    ```  
    
    > ##### Рисунок16  
    > Редактирование узла в формате HTML  
    > ![Редактирование узла в формате HTML][ImageHtmlEdit2]  
    
1.  Нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \), чтобы сохранить изменения, или щелкните любое место за пределами поля.  Изменения автоматически отображаются в режиме реального времени на странице.  Текст `Your site!` заменен новым содержимым.  
    
    > ##### Рисунок17  
    > Новое содержимое немедленно появляется на странице  
    > ![Новое содержимое немедленно появляется на странице][ImageHtmlEdit3]  
    
Этот рабочий процесс хорошо подходит только для экспериментов с изменениями контента.  Если вы перезагрузите страницу или закроете ее, ваши изменения будут потеряны.  Если вы используете этот рабочий процесс и хотите сохранить изменения, вам потребуется вручную скопировать эти изменения на HTML-код.  В следующей паре разделов показаны другие способы изменения контента из дерева DOM.  

## Изменение порядка узлов   

Вы также можете изменить порядок узлов DOM.  Например, на веб-странице в нижней части окна находится меню навигации.  Чтобы переместить элемент в начало страницы, выполните указанные ниже действия.  

1.  Найдите `<nav>` узел в **дереве DOM** DevTools.  
    
    > ##### Рис. 18  
    > Узел навигации выделяется синим цветом в DevTools  
    > ![Узел навигации выделяется синим цветом в DevTools][ImageHtmlReorder1]  
    
1.  Перетащите `<nav>` узел в верхнюю части экрана, чтобы он был первым дочерним `<body>` узлом узла.  
    > ##### На рисунке 19  
    > Перетаскивание узла навигации в начало  
    > ![Перетаскивание узла навигации в начало][ImageHtmlReorder2]  
    
    `<nav>`Теперь узел отображается в верхней части страницы.  
    
    > ##### Рис. 20  
    > Узел навигации находится в верхней части страницы  
    > ![Узел навигации находится в верхней части страницы][ImageHtmlReorder3]  
    
### Удаление узла   

Вы также можете удалить узлы из дерева DOM.  

1.  В **дереве DOM**щелкните `<div>A new element!?!</div>` .  DevTools выделяет узел синим цветом.  
    
    > ##### Рисунок 21  
    > Выбор узла для удаления  
    > ![Выбор узла для удаления][ImageHtmlDelete1]  
    
1.  Нажмите клавишу `Delete` на клавиатуре.  `<div>A new element!?!</div>`Узел удаляется из дерева DOM.  
    
    > ##### Рис. 22  
    > Узел удален  
    > ![Узел удален][ImageHtmlDelete2]  
    
## Копирование изменений   

Почти все готово.  Вы внесли несколько изменений на странице в DevTools, но они еще не сохранились в исходном коде.  

1.  Обновите **вкладку Live**.  Изменения, внесенные в дереве DOM, исчезнут.  В частности, текст `Your site!` возвращается в верхней части страницы, а текст `A new element!?!` возвращается в нижнюю часть.  
    
    > ##### Рис. 23  
    > Внесенные вами изменения исчезли  
    > ![Внесенные вами изменения исчезли][ImageHtmlCopy1]  

1.  Скопируйте приведенный ниже код.  
    
    ```html
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <meta charset="utf-8">
            <meta http-equiv="X-UA-Compatible" content="IE=edge">
            <meta name="viewport" content="width=device-width, initial-scale=1">
        </head>
        <body>
            <header>
                <p>Welcome to my site!</p>
            </header>
            <nav>
                <ul>
                    <li><a href="/">Home</a></li>
                    <li><a href="/contact.html">Contact</a></li>
                </ul>
            </nav>
            <main>
                <h1>About Me</h1>
                <p>I am learning web development.  Recent accomplishments:</p>
                <ul>
                    <li>Learned how to set up my code in Glitch.</li>
                    <li>Added content to my HTML.</li>
                    <li>Learned how to use Microsoft Edge DevTools to experiment with content changes.</li>
                    <li>Learned the difference between HTML and the DOM.</li>
                </ul>
            </main>
        </body>
    </html>
    ```  
      
1.  Вернитесь на **вкладку Редактор** и замените содержимое `index.html` файла кодом, который вы только что скопировали.  
    
    > ##### Рисунок 24  
    > Как `index.html` должен выглядеть файл  
    > ![Как должен выглядеть файл index.html][ImageHtmlCopy2]  
    
## Дальнейшие действия   

*   Чтобы узнать, как изменить стиль страницы и поэкспериментировать с изменениями стиля в Microsoft Edge DevTools, выполните следующие шаги в этой серии. Приступая к [работе с CSS][DevToolsBeginnersCss].  
*   Ознакомьтесь [с введением в DOM][MDNIntroductionDom] , чтобы узнать больше об DOM.  
*   Ознакомьтесь с курсом, например [Знакомство с веб-разработкой][CourseraIntroductionToWebDevelopment] , чтобы получить больше возможностей для веб-разработки.  

<!--- image links --->  

[ImageHtmlFinished]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-finished.msft.png "Рисунок 1: готовый веб-сайт"  
[ImageHtmlSetup1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup1.msft.png "Рисунок 2: вкладка "редактор""  
[ImageHtmlSetup2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup2.msft.png "Рисунок 3: меню "Параметры проекта""  
[ImageHtmlSetup3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup3.msft.png "Рисунок 4: смешанный проект"  
[ImageHtmlSetup4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-setup4.msft.png "Рисунок 5. Вкладка "динамический""  
[ImageHtmlAdd1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add1.msft.png "Рисунок 6: на вкладке "редактор" выделена новая программа"  
[ImageHtmlAdd2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add2.msft.png "Рисунок 7: новый заголовок отображается на вкладке "живые""  
[ImageHtmlAdd3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add3.msft.png "Рисунок 8: на вкладке "редактор" выделена новая программа"  
[ImageHtmlAdd4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add4.msft.png "На рисунке 9: на вкладке "редактор" выделена кнопка "создать код"."  
[ImageHtmlAdd5]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-add5.msft.png "Рисунок 10: новый список отображается на вкладке "живые""  
[ImageHtmlDom1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom1.msft.png "На рисунке 11: в нижней части страницы текст — это новый элемент!?! может отображаться"  
[ImageHtmlDom2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom2.msft.png "Рисунок 12: текст "Загадка" — новый элемент!?! не удается найти в index.html"  
[ImageHtmlDom3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom3.msft.png "Рисунок 13: проверка текста"  
[ImageHtmlDom4]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-dom4.msft.png "Рисунок 14: DevTools открывается вместе со страницей"  
[ImageHtmlEdit1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit1.msft.png "Рисунок 15: Редактирование узла в формате HTML"  
[ImageHtmlEdit2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit2.msft.png "Рисунок 16: Редактирование узла в формате HTML"  
[ImageHtmlEdit3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-edit3.msft.png "Рисунок 17: новое содержимое немедленно появляется на странице"  
[ImageHtmlReorder1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder1.msft.png "Рисунок 18: узел навигации выделен синим цветом в DevTools"  
[ImageHtmlReorder2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder2.msft.png "На рисунке 19 показано, как перетащить узел навигации в начало."  
[ImageHtmlReorder3]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-reorder3.msft.png "Рисунок 20: узел навигации находится в верхней части страницы."  
[ImageHtmlDelete1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete1.msft.png "Рисунок 21: Выбор узла для удаления"  
[ImageHtmlDelete2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-delete2.msft.png "Рис. 22: узел удален"  
[ImageHtmlCopy1]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy1.msft.png "Рис. 23: изменения, внесенные вами, исчезли"  
[ImageHtmlCopy2]: /microsoft-edge/devtools-guide-chromium/media/beginners-html-copy2.msft.png "Рисунок 24: способ просмотра файла index.html"  

<!--- links --->  

[DevToolsBeginnersCss]: /microsoft-edge/devtools-guide-chromium/beginners/css "DevTools для начинающих: Приступая к работе с CSS"  

[MicrosoftEdgeInsider]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  

[CourseraIntroductionToWebDevelopment]: https://www.coursera.org/learn/web-development "Общие сведения о веб-разработке | Coursera"  

[GlitchAlluringShockIndex]: https://glitch.com/edit/#!/alluring-shock?path=index.html "index.html-alluring-удар | Цепь"  

[MDNGettingStartedHtml]: https://developer.mozilla.org/docs/Learn/HTML/Introduction_to_HTML/Getting_started "Начало работы с HTML | MDN"  
[MDNIntroductionDom]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/beginners/html) и [Katherine Джексон][KatherineJackson] \ (помощник службы технической поддержки, Chrome DevTools \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[KatherineJackson]: https://developers.google.com/web/resources/contributors/katjackson  
