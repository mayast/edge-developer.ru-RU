---
title: Редактирование файлов с помощью рабочих областей
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8a31dd9fbfe492cf8eaacc654f7d501925f730f2
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942180"
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
> Цель этого учебника — предоставить на практические практические задачи по настройке и использованию рабочих областей, чтобы вы сможете использовать рабочие области в собственных проектах.  Вы можете сохранить изменения в исходном коде на локальном компьютере, которые были сделаны в DevTools после включения рабочих областей.  

> [!IMPORTANT]
> **Предварительные предварительные проверки:** прежде чем приступать к учебнику, необходимо узнать, как выполнить следующие действия.  
> 
> *   [Создание веб-страниц с помощью html, CSS и JavaScript][MDNWebGettingStarted]  
> *   [Внесение основных изменений в CSS с помощью Средств разработки][DevToolsCssIndex]  
> *   [Запуск локального HTTP-сервера][MDNSimpleLocalHTTPServer]  

## Обзор  

Рабочие области дают возможность сохранить изменения, внесенные в Devtools, в локальную копию файла на компьютере.  В этом учебнике у вас должны быть следующие параметры компьютера:  

*   У вас есть исходный код сайта на вашем компьютере.  
*   Вы запускаете локальный веб-сервер из исходного каталога кодов, чтобы сайт был доступен самого `localhost:8080` языка.  
*   Вы открывали `localhost:8080` в Microsoft Edge и используете средства разработчиков для изменения CSS-сайта.  

Если включена поддержка рабочих областей, изменения, внесенные в DevTools, сохраняются в исходном коде на рабочем столе.  

## Ограничения  

Если вы используете современной структуру, вероятно, исходный код из формата, который проще сохранять в формат, оптимизированный для работы как можно быстрее.  

Обычно рабочие области можно сопоставить оптимизированный код с исходным кодом с помощью исходных [карт.][TreehouseBlogSourceMaps]  Однако между структурами используется множество вариантов, которые используются в каждой из них.  Дисперсии просто поддерживают все варианты.  

Рабочие области не совместимо с приведенной ниже таблицей.  

*   Создать редактироваемое приложение  

    <!-- If you run into issues while using Workspaces with your framework of choice, or you get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  
    
## Дополнительные функции: локальные переопределения  

**Локальный переопределение —** это еще один компонент DevTools, аналогичная рабочей области.  Используйте локальные переопределения, если вы хотите экспертировать с изменениями на странице и вам нужно просматривать изменения на странице, но не беспокойтесь об изменениях исходного кода страницы.  

<!--Todo: add section when content is ready  -->  

## Шаг 1. Настройка  

Выполните указанные ниже действия, чтобы повысить эффективность работы с рабочими областями.  

### Настройка демонстрации  

1.  [Открыть демонстрацию.][GlitchWorkspacesDemo]  <!--In the top-left of the editor, a randomly-generated project name is displayed.  -->  
    
    :::image type="complex" source="../media/workspaces-glitch-workspaces-demo-source.msft.png" alt-text="Проект в glitch-проекте" lightbox="../media/workspaces-glitch-workspaces-demo-source.msft.png":::
       Проект в glitch-проекте  
    :::image-end:::  
    
    <!--1.  Choose the project name.  -->  
    <!--1.  Select **Advanced Options** > **Download Project**.  
    
    :::image type="complex" source="../media/workspaces-glitch-advanced-options-download-project.msft.png" alt-text="The Download Project button" lightbox="../media/workspaces-glitch-advanced-options-download-project.msft.png":::
       The Download Project button  
    :::image-end:::  

    -->  
    <!--1.  Close the tab.  -->  
    <!--1.  Unzip the source code and move the unzipped `app` directory to your desktop.  For the rest of this tutorial the unzipped directory is referred to as `~/Desktop/app`.  -->  
    
1.  Создайте каталог `app` на компьютере.  Сохраняйте копии файлов из `workspaces-demo` каталога в `app` каталог.  Для остального учебника каталог называется `~/Desktop/app` каталогом.  
1.  Запустите локальный веб-сервер `~/Desktop/app` в.  Ниже приведен пример кода для запуска, но вы можете использовать то, что `SimpleHTTPServer` вы хотите использовать.  
    
    :::row:::
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m SimpleHTTPServer # Python 2
          ```  
       :::column-end:::  
       :::column span="":::
          ```bash
          cd ~/Desktop/app
          python -m http.server # Python 3
          ```  
       :::column-end:::
    :::row-end:::  
    
1.  Откройте вкладку в Microsoft Edge и перейдите к версии сайта, размещенной локально.  Вы должны иметь доступ по URL-адресу, такому `localhost:8080` как. `http://0.0.0.0:8080`  Точный [номер порта][WikiPortURLs] может быть другим.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo.msft.png" alt-text="Демонстрация" lightbox="../media/workspaces-workspaces-demo.msft.png":::
       Демонстрация  
    :::image-end:::  
    
### Настройка DevTools  

1.  Выберите `Control` + `Shift` + `J` \(Windows\) `Command` + `Option` + `J` или \(macOS\), чтобы открыть **панель консоли** devTools.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-console.msft.png" alt-text="Панель консоли" lightbox="../media/workspaces-workspaces-demo-console.msft.png":::
       Панель **консоли**  
    :::image-end:::  
    
1.  Откройте **вкладку "Источники".**  
1.  Откройте **вкладку Filesystem.**  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem.msft.png" alt-text="Вкладка "Файловая система"" lightbox="../media/workspaces-workspaces-demo-sources-filesystem.msft.png":::
       Вкладка **"Файловая система"**  
    :::image-end:::  
    
1.  Выберите **команду "Добавить папку в рабочую область".**  
1.  Введите `~/Desktop/app`.  
1.  Выберите **"Разрешить",** чтобы предоставить devTools разрешение на чтение и запись в каталог.  
    На **вкладке "Файлная** система" рядом с ней появится зеленая `index.html` `script.js` пунктирная линия, а также зеленая `styles.css` пунктирная линия.  Эти зеленые точки означали, что DevTools установил сопоставленное сопоставленное сопоставление между сетевыми ресурсами страницы и `~/Desktop/app` файлами.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png" alt-text="На вкладке "Файлная система" отображается сопоставление между локальными файлами и сетью" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-folder.msft.png":::
       На **вкладке "Файлная** система" отображается сопоставление между локальными файлами и сетью  
    :::image-end:::  
    
## Шаг 2. Сохранение изменения CSS на диск  

1.  `styles.css`Откройте.  
    
    > [!NOTE]
    > Для `color` свойства `h1` элементов задано значение `fuchsia` ..  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png" alt-text="Просмотр стилей.css в текстовом редакторе" lightbox="../media/workspaces-workspaces-demo-sources-filesystem-css.msft.png":::
       Просмотр `styles.css` в текстовом редакторе  
    :::image-end:::  
    
1.  Откройте **вкладку "Элементы".**  
1.  Измените значение `color` свойства `<h1>` элемента на избранный цвет.  
    Помните, что чтобы правила CSS применены к этому представлению, необходимо выбрать элемент в дереве DOM, чтобы отобразить примененные к нему правила `<h1>` CSS в **области "Стили".** **DOM Tree**  Зеленая точка рядом с значками, с которыми `styles.css:1` вы вносите `~/Desktop/app/styles.css` изменения.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-css.msft.png" alt-text="Зеленый индикатор связывания файла" lightbox="../media/workspaces-workspaces-demo-elements-styles-css.msft.png":::
       Зеленый индикатор связывания файла  
    :::image-end:::  
    
1.  Снова `styles.css` откройте его в текстовом редакторе.  Теперь `color` для свойства будет настроен ваш избранный цвет.  
1.  Обновите страницу.  Цвет элемента `<h1>` по-прежнему имеет избранный цвет.  Изменения остаются в обновлении, так как при внесении изменений средств разработчиков сохраняются изменения, сохраненные на диск.  После этого при обновлении страницы измененная копия файла с диска.  
    
## Шаг 3. Сохранение изменения В ФОРМАТе HTML на диск  

### Изменение HTML-кода из панели элементов  

Html можно вносить изменения в html-файл из панели элементов, но изменения в дереве DOM не сохраняются на диске и влияют только на текущий сеанс браузера.  

Дерево DOM не является html.  

<!--### Try changing HTML from the Elements panel  

> [!WARNING]
> The workflow that you are about to try does not work.  You are trying it now so that you do not waste time later trying to figure out why it is not working.  

1.  Choose the **Elements** tab.  
1.  Choose and edit the text content of the `h1` element, which says `Workspaces Demo`, and replace it with `I ❤️  Cake`.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-change-h1.msft.png" alt-text="Attempt to change html from the DOM Tree of the Elements panel" lightbox="../media/workspaces-workspaces-demo-change-h1.msft.png":::
       Attempt to change html from the DOM Tree of the **Elements** panel  
    :::image-end:::  
    
1.  Open `~/Desktop/app/index.html` in a text editor.  The change that you just made does not appear.  
1.  Refresh the page.  The page reverts to the original title.  
    
#### Optional: Why it is not working  

> [!NOTE]
> This section describes why the workflow from [Try changing html from the Elements panel](#try-changing-html-from-the-elements-panel) does not work.  You should skip this section if you do not care why.  

*   The tree of nodes that you see on the **Elements** panel represents the [DOM][MDNWebAPIsDOM] of the page.  
*   To display a page, a browser fetches html over the network, parses the html, and then converts it into a tree of DOM nodes.  
*   If the page has any JavaScript, that JavaScript may add, delete, or change DOM nodes.  CSS may change the DOM, too, using the [`content`][MDNCSSContent] property.  
*   The browser eventually uses the DOM to determine what content it should present to browser users.  
*   Therefore, the final state of the page that users see may be very different from the html that the browser fetched.  
*   This makes it difficult for DevTools to resolve where a change made in the **Elements** panel should be saved, because the DOM is affected by HTML, JavaScript, and CSS.  

In short, the **DOM Tree** `!==` HTML.  
-->  

### Изменение HTML-кода из панели "Источники"  

Если вы хотите сохранить изменение на HTML-адресстраницы, сделайте это с **помощью панели "Источники".**  

1.  Откройте **вкладку "Источники".**  
1.  Выберите **вкладку Страницы.**  
1.  Выберите **(индекс).**  Откроется HTML-код страницы.  
1.  Замените `<h1>Workspaces Demo</h1>` `<h1>I ❤️  Cake</h1>` их.  См. на следующем рисунке.  
1.  Выберите `Control` + `S` \(Windows\) `Command` + `S` или \(macOS\), чтобы сохранить изменение.  
1.  Обновите страницу.  Элемент `<h1>` по-прежнему отображает новый текст.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-sources-page-h1.msft.png" alt-text="Изменение HTML-кода из панели "Источники"" lightbox="../media/workspaces-workspaces-demo-sources-page-h1.msft.png":::
       Изменение HTML-кода **из панели "Источники"**  
    :::image-end:::  
    
1.  `~/Desktop/app/index.html`Откройте.  Элемент `<h1>` содержит новый текст.  
    
## Шаг 4. Сохранение изменения JavaScript на диск  

В **области "Источники"** также можно вносить изменения в JavaScript.  Но иногда при внесении изменений на сайт необходимо получить доступ к другим панелям, таким как панель "Элементы" или "Консоль", и при внесении изменений на сайт. **Elements** **Console**  Существует способ открыть **панель "Источники"** рядом с другими панелями.  

1.  Откройте **вкладку "Элементы".**  
1.  Выберите `Control` + `Shift` + `P` \(Windows\) `Command` + `Shift` + `P` или \(macOS\).  Откроется **меню** команд.  
1.  Введите `QS` текст, а затем выберите **"Показать экспресс-источник".**  В нижней части окна DevTools теперь находится вкладка **"Быстрый источник".**  Вкладка отображает содержимое `index.html` файла, который вы изменили на **панели "Источники".**  Вкладка **"Быстрый** источник" позволяет редактировать редактор на панели **"Источники",** чтобы можно было редактировать файлы, открыв другие панели.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png" alt-text="Открытие вкладки "Экспресс-источник" с помощью меню команд" lightbox="../media/workspaces-workspaces-demo-search-show-quick-source.msft.png":::
       Открытие **вкладки "Экспресс-источник"** с **помощью меню команд**  
    :::image-end:::  
    
1.  Нажмите `Control` + `P` кнопку \(Windows\) `Command` + `P` или \(macOS\), чтобы открыть **диалоговое окно "Открыть** файл".  См. на следующем рисунке.  
1.  Введите `script` и выберите **приложение/script.js. **  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-search-script.msft.png" alt-text="Открытие script.js с помощью диалогового окна "Открытие файла"" lightbox="../media/workspaces-workspaces-demo-search-script.msft.png":::
       `script.js`Открытие файла с **помощью диалогового окна "Открытие** файла"  
    :::image-end:::  
    
    > [!NOTE]
    > Ссылка `Save Changes To Disk With Workspaces` в демонстрации регулярно применяется к ссылке.  
    
1.  Добавьте следующий код внизу на **вкладкеscript.js"Быстрый** **источник".**  
    
    ```javascript
    console.log('greetings from script.js');
    document.querySelector('a').style = 'font-style:italic';
    ```  
    
1.  Выберите `Control` + `S` \(Windows\) `Command` + `S` или \(macOS\), чтобы сохранить изменение.  
1.  Обновите страницу.  
    
    > [!NOTE]
    > Ссылка на странице теперь выделена курсивом.  
    
    :::image type="complex" source="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png" alt-text="Ссылка на странице теперь выделена курсивом" lightbox="../media/workspaces-workspaces-demo-elements-styles-quick-source-script.msft.png":::
       Ссылка на странице теперь выделена курсивом  
    :::image-end:::  
    
## Дальнейшие действия  

Используйте то, что вы узнали в этом учебнике, чтобы настроить рабочие области в своем проекте.  <!-- If you run into any issues or are able to get it working after some custom configuration, please [start a thread in the mailing list][AlphabetGroupsAlphabetBrowserDevTools] or [ask a question on Stack Overflow][StackOverflowAlphabetBrowserDevTools] to share your knowledge with the rest of the DevTools community.  -->  

<!--  
If you have more feedback on the topics or anything else, please use any of the channels below:  

*   [Mailing List][AlphabetGroupsAlphabetBrowserDevTools]  
*   [Twitter][TwitterAlphabetBrowserDevTools]  
    -->  

<!-- links -->  

[DevToolsCssIndex]: ../css/index.md "Начало работы с просмотром и изменением CSS | Документы Майкрософт"  

<!--[LocalOverrides]: ../whats-new/2018/01/devtools#overrides -->  

<!--[AlphabetGroupsAlphabetBrowserDevTools]: https://groups.alphabet.com/forum/#!forum/alphabet-browser-developer-tools "Alphabet Browser DevTools - Alphabet Groups"  -->  

[GlitchWorkspacesDemo]: https://glitch.com/edit/#!/microsoft-edge-chromium-devtools?path=workspaces-demo/index.html:1:0 "Демонстрация файлов рабочих областей | Глитский"  

[MDNCSSContent]: https://developer.mozilla.org/docs/Web/CSS/content "Содержимое CSS: касание таблиц стилей | MDN"  
[MDNWebGettingStarted]: https://developer.mozilla.org/docs/Learn/Getting_started_with_the_web "Начало работы с Веб-браузером | MDN"  
[MDNSimpleLocalHTTPServer]: https://developer.mozilla.org/docs/Learn/Common_questions/set_up_a_local_testing_server#Running_a_simple_local_HTTP_server "Работа с простой локальным HTTP-сервером | MDN"  
[MDNWebAPIsDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM — веб-API | MDN"  

<!--[StackOverflowAlphabetBrowserDevTools]: https://stackoverflow.com/questions/ask?tags=alphabet-browser-devtools "Alphabet Browser DevTools - Stack Overflow"  -->

[TreehouseBlogSourceMaps]: https://blog.teamtreehouse.com/introduction-source-maps "Общие сведения об исходных картах | Treehouse Blog"  

<!-- [TwitterAlphabetBrowserDevTools]: https://twitter.com/alphabetbrowserdevtools "Alphabet Browser DevTools \(@AlphabetBrowserDevTools\) | Twitter"  -->

[WikiPortURLs]: https://en.wikipedia.org/wiki/Port_(computer_networking)#Use_in_URLs "Порт \(компьютеры\) - Википедия"  

> [!NOTE]
> Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]  
> Исходная страница [here](https://developers.google.com/web/tools/chrome-devtools/workspaces/index) находится на сайте [Kayce Basques][KayceBasques] \(технический автор, Chrome DevTools \& Lighthouse\).  

[![Creative Commons License][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
