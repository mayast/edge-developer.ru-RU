---
title: Редактирование файлов с помощью рабочих областей
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 612e85b8b00a78a40e53ac5c33d187fdae174024
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601854"
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







# Редактирование файлов с помощью рабочих областей   



> [!NOTE]
> Цель этого учебника — предоставить практические рекомендации по настройке и использованию рабочих областей, чтобы можно было использовать рабочие области в своих проектах.  Вы можете сохранить изменения в исходном коде на локальном компьютере, который вы сделали в DevTools после включения рабочих областей.  

> [!CAUTION]
> **Предварительные условия**: перед началом работы с этим учебником следует знать, как это сделать:  
> *   [Создание веб-страниц с помощью HTML, CSS и JavaScript][MDNWebGettingStarted]  
> *   [Использование DevTools для внесения основных изменений в CSS][DevToolsCssIndex]  
> *   [Запуск локального веб-сервера HTTP][MDNSimpleLocalHTTPServer]  

## Обзор   

Рабочие области позволяют сохранить изменения, внесенные в Devtools, в локальную копию того же файла на компьютере.  Например, предположим, что:  

*   У вас есть исходный код для вашего сайта на рабочем столе.  
*   Вы запускаете локальный веб-сервер из каталога исходного кода, чтобы сайт был доступен по адресу `localhost:8080` .  
*   Вы открыли `localhost:8080` приложение Microsoft EDGE и используете DevTools для изменения CSS-сайта.  

После включения рабочих областей изменения в CSS, внесенные в DevTools, сохраняются в исходном коде на рабочем столе.  

## Ограничения   

При использовании современной платформы, скорее всего, она преобразует исходный код из формата, который легко поддерживать в формате, который оптимизирован для выполнения как можно быстрее.  
В рабочих областях обычно можно сопоставить оптимизированный код с первоначальным исходным кодом с помощью [карт исходного][TreehouseBlogSourceMaps]кода.  Однако между платформами есть множество вариантов использования карт исходного кода.  Devtools просто поддерживает все варианты.  

Рабочие области не работают с этими платформами:  

*   Приложение "Создание реагируй"  

<!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

## Связанная функция: локальные переопределения   

**Локальные переопределения** — это еще одна функция DevTools, похожая на рабочие области.  Используйте локальные переопределения, если вы хотите поэкспериментировать с изменениями на странице, и вам нужно увидеть эти изменения при загрузке страницы, но вы не хотите сопоставлять изменения в исходном коде страницы.  

<!--Todo: add section when content is ready  -->  

## Действие 1: Настройка   

Следуйте этим учебником, чтобы получить практические навыки работы с рабочими областями.  

### Настройка ролика   

1.  [Откройте демонстрацию][GlitchWorkspacesDemo].  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    > ##### Рис. 1  
    > Проект с сбоев ![][ImageGlitchProject]  
    
    <!--1.  Click the project name.  -->
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    > ##### Figure 2  
    > The Download Project button  
    > ![The Download Project button][ImageDownloadProjectButton]  
    -->
    <!--1.  Close the tab.  -->
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial this directory is referred to as `~/Desktop/app`.  -->  
    
1.  Создайте `app` каталог на рабочем столе.  Сохраняйте копии файлов в `workspaces-demo` каталоге.  В оставшейся части этого учебника этот каталог называется `~/Desktop/app` .  
1.  Запустите локальный веб-сервер в `~/Desktop/app` .  Ниже приведен пример кода для запуска `SimpleHTTPServer` , но вы можете использовать любой предпочитаемый сервер.  
    
    ```bash
    cd ~/Desktop/app
    python -m SimpleHTTPServer # Python 2
    ```  
    
    ```bash
    cd ~/Desktop/app
    python -m http.server # Python 3
    ```  
    
1.  Откройте вкладку в Microsoft EDGE и перейдите на веб-сайт с локально размещенной версией.  Доступ к ней можно получить с помощью URL-адреса, например `localhost:8080` или `http://0.0.0.0:8080` .  Точный [номер порта][WikiPortURLs] может отличаться от остальных.  
    
    > ##### Рисунок 2  
    > Демонстрация  
    > ! [Демонстрация] [ImageDemo]  

### Настройка DevTools   

1.  Нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \), чтобы открыть панель **консоли** DevTools.  
    
    > ##### Рисунок3  
    > Панель **консоли**  
    > ! [Панель консоли] [ImageConsolePanel]  

1.  Откройте вкладку **источники** .  
1.  Откройте вкладку **FileSystem (файловая система** ).  
    
    > ##### Рисунок4  
    > Вкладка " **Файловая система** "  
    > ! [Вкладка FileSystem] [ImageFilesystem]  

1.  Нажмите кнопку **Добавить папку в рабочую область**.  
1.  Выберите `~/Desktop/app` .  
1.  Нажмите кнопку **Разрешить** , чтобы предоставить DevTools разрешение на чтение и запись в каталог.  
    На вкладке **FileSystem** теперь есть зеленая точка рядом с `index.html` , `script.js` и `styles.css` .  Эти зеленые точки означают, что в DevTools установлено соответствие между сетевыми ресурсами страницы и файлами в `~/Desktop/app` .  
    
    > ##### Рисунок 5  
    > На вкладке **FileSystem** теперь показано соответствие между локальными и сетевыми файлами.  
    > ! [На вкладке FileSystem теперь отображается соответствие между локальными файлами и сетью] [ImageMapping]  

## Шаг 2: сохранение изменений CSS на диске   

1.  Open (открыть) `styles.css` .  
    
    > [!NOTE]
    >`color` `h1` Для свойства элементы задано значение `fuchsia` .
    
    > ##### Рисунок6  
    > Просмотр `styles.css` в текстовом редакторе  
    > ! [Просмотр стилей. CSS в текстовом редакторе] [ImageStylesFuchsia]  


1.  Откройте вкладку **элементы** .  
1.  Измените значение `color` свойства `<h1>` элемента на предпочтительный цвет.  
    Помните о том, что для `<h1>` просмотра примененных к нему правил CSS в области **стили** необходимо щелкнуть элемент в **дереве DOM** .  Зеленая точка рядом с `styles.css:1` ней означает, что все изменения, внесенные вами, сопоставлены `~/Desktop/app/styles.css` .  
    
    > ##### Рисунок7  
    > Зеленый индикатор, связанный с файлом  
    > ! [Зеленый индикатор, связанный с файлом] [ImageStylesGreen]  

1.  `styles.css`Снова откройте текстовый редактор.  `color`Свойству будет присвоена предпочтительный цвет.  
1.  Перезагрузите страницу.  Цвет `<h1>` элемента по-прежнему установлен на предпочтительный цвет.  Это происходит потому, что после внесения изменений DevTools сохраняет изменения на диск.  А затем, когда вы перезагрузите страницу, локальный сервер сослужил измененную копию файла с диска.  

## Шаг 3: сохранение изменений HTML на диске   

### Изменение HTML на панели "элементы"  

Вы можете внести изменения в HTML-код с панели элементов, но ваши изменения в дереве DOM не сохраняются на диск и влияют только на текущий сеанс браузера.  
Дерево DOM не является HTML-кодом.  

<!--### Try changing HTML from the Elements panel   

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Click the **Elements** tab.  
1.  Double click the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    > ##### Old Figure 9  
    > Attempting to change HTML from the **DOM Tree** of the **Elements** panel  
    > ![Attempting to change HTML from the DOM Tree of the Elements panel][ImageElementsCake]  

1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Reload the page.  The page reverts to its original title.  

#### Optional: Why it is not working   

> [!NOTE]
> This section describes why the workflow from [Try changing HTML from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches HTML over the network, parses the HTML, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the HTML that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->
### Изменение HTML на панели «источники»   

Если вы хотите сохранить изменения в HTML-коде страницы, сделайте это с помощью панели « **источники** ».  

1.  Откройте вкладку **источники** .  
1.  Откройте вкладку **страница** .  
1.  Нажмите кнопку **(указатель)**.  Откроется HTML-код для страницы.  
1.  Заменить `<h1>Workspaces Demo</h1>` на `<h1>I ❤️  Cake</h1>` .  Смотрите [Рисунок 8](#figure-8).  
1.  `Control` + `S` Чтобы сохранить изменения, нажмите клавиши \ (Windows \) или `Command` + `S` \ (macOS \).  
1.  Перезагрузите страницу.  `<h1>`Элемент по-прежнему отображается в новом тексте.  
    
    > ##### Рисунок8  
    > Для строки 12 установлено значение `I ❤️  Cake`  
    > ! [Изменение HTML-кода на панели «источники»] [ImageSourcesCakeHTML]  

1.  Open (открыть) `~/Desktop/app/index.html` .  `<h1>`Элемент включает новый текст.  

## Шаг 4: сохранение изменений JavaScript на диске   

Панель « **источники** » — это также место, где можно вносить изменения в JavaScript.  Но иногда вам нужно получить доступ к другим панелям, таким как панель **элементов** или панель **консоли** , при внесении изменений на сайт.  На панели « **источники** » есть способ открытия рядом с другими панелями.  

1.  Откройте вкладку **элементы** .  
1.  Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).  Откроется **меню команд** .  
1.  Введите текст `QS` и выберите параметр **Показать быстрый источник**.  В нижней части окна DevTools теперь есть вкладка **быстрый источник** .  На вкладке отображается содержимое `index.html` , которое является последним файлом, измененным на панели « **источники** ».  На вкладке **быстрый источник** вы можете открыть редактор из панели **источники** , чтобы можно было редактировать файлы, не открывая другие панели.  
    
    > ##### Рисунок9  
    > Открытие вкладки " **быстрый источник** " с помощью **меню команд**  
    > ! [Открытие вкладки "быстрый источник" с помощью меню "команды"] [ImageCommandMenuQuickSource]  

1.  `Control` + `P` `Command` + `P` Чтобы открыть диалоговое окно " **Открытие файла** ", нажмите клавиши \ (Windows \) или \ (macOS \).  Смотрите [Рисунок 10](#figure-10).  
1.  Введите `script` команду **app/script. js**.  
    
    > ##### Рисунок 10  
    > Открытие `script.js` с помощью диалогового окна " **Открыть файл** "  
    > ! [Открытие сценария. js с помощью диалогового окна "Открытие файла"] [ImageOpenFileDialog]  
    
    > [!NOTE]
    > `Save Changes To Disk With Workspaces`Ссылка в демонстрационной видеоролика будет регулярно применена.  
    
1.  Добавьте следующий код в нижнюю часть **сценария. js** с помощью вкладки " **быстрый источник** ".  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  `Control` + `S` Чтобы сохранить изменения, нажмите клавиши \ (Windows \) или `Command` + `S` \ (macOS \).  
1.  Перезагрузите страницу.  
    
    > [!NOTE]
    > Ссылка на странице теперь будет курсивной.
    
    > ##### Рисунок11  
    > Ссылка на странице теперь курсивом  
    > ! [Ссылка на странице теперь курсивом] [ImageScriptItalic]  

## Дальнейшие действия   

С помощью этого учебника вы можете настроить рабочие области в проекте.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->

 <!--  -->



<!-- 
If you have more feedback on these topics or anything else, please use any of the channels below:
*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
-->

<!-- image links -->  

[ImageGlitchProject]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-workspaces-demo-source.msft.png "Рисунок 1: неработающий проект с именем, созданным случайным образом"  
<!--[ImageDownloadProjectButton]: /microsoft-edge/devtools-guide-chromium/media/workspaces-glitch-advanced-options-download-project.msft.png "old Figure 2: The Download Project button"  -->  
[ImageDemo]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo.MSFT.png "Рисунок 2: демонстрационный ролик"  
[ImageConsolePanel]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Console.MSFT.png "Рисунок 3: панель консоли"  
[ImageFilesystem]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Sources-FileSystem.MSFT.png "Рисунок 4: вкладка" FileSystem ""  
[ImageMapping]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Sources-FileSystem-Folder.MSFT.png "Рисунок 5: теперь на вкладке FileSystem показано соответствие между локальными и сетевыми файлами.  
[ImageStylesFuchsia]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Sources-FileSystem-CSS.MSFT.png "Рисунок 6: Просмотр стилей. CSS в текстовом редакторе"  
[ImageStylesGreen]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Elements-Styles-CSS.MSFT.png "Рисунок 7: зеленый индикатор, связанный с файлом"  
[ImageSourcesCakeHTML]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Sources-Page-H1.MSFT.png "Рисунок 8: изменение HTML на панели" источники "  
<!--[ImageElementsCake]: /microsoft-edge/devtools-guide-chromium/media/workspaces-workspaces-demo-change-h1.msft.png "Old Figure 9: Attempting to change HTML from the DOM Tree of the Elements panel"  -->  
[ImageCommandMenuQuickSource]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Search-Show-Quick-Source.MSFT.png "Рисунок 9: Открытие вкладки" быстрый источник "с помощью командного меню  
[ImageOpenFileDialog]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Search-script.MSFT.png "Рисунок 10: открытие сценария. js с помощью диалогового окна" открыть файл "  
[ImageScriptItalic]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/workspaces-workspaces-Demo-Elements-Styles-Quick-Source-script.MSFT.png "Рисунок 11: ссылка на странице теперь курсивом"  

<!-- links -->  

[DevToolsCssIndex]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Рабочие области — демонстрационные файлы | Цепь"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Content-CSS: Каскадные таблицы стилей | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Начало работы с Интернетом | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Выполнение простого локального HTTP-сервера | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM — веб-API | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Общие сведения о картах исходного кода | Блог Treehouse"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Порт \ (компьютерная сеть \) — Википедии"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
