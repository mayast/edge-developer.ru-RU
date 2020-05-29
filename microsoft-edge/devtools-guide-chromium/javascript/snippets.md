---
title: Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: aa9f7e96c7e379c1fe537ffba730e08990e0c20a
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581819"
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





# Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools   



Если вы обнаружите, что один и тот же код запускается повторно на [консоли][DevtoolsConsoleIndex] , попробуйте сохранить его как фрагмент кода.  Фрагменты — это сценарии, созданные вами на [панели « **источники** »][DevToolsSourcesPanel].  У них есть доступ к контексту JavaScript на странице, и вы можете запускать их на любой странице.  Фрагменты — это альтернатива для [Закладка][WikiBookmarklet].  
В Firefox DevTools есть функция, похожая на фрагменты, которые называются [блокнотом][MDNScratchpad].  

Например, на [**рисунке 1**](#figure-1) показана домашняя страница DevTools слева и фрагмент исходного кода справа.  

> ##### Рис. 1  
> Вид страницы перед выполнением фрагмента  
> ![Вид страницы перед выполнением фрагмента][ImageSnippetSplitScreen]  

Исходный код фрагмента на [**рисунке 1**](#figure-1):  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

[**На рисунке 2**](#figure-2) показано, как выглядит страница после выполнения фрагмента.  Во всплывающем **ящике консоли** выводится `Hello, Snippets!` сообщение о том, что журналы фрагментов, и содержимое страницы полностью меняются.  

> ##### Рисунок 2  
> Вид страницы после выполнения фрагмента  
> ![Вид страницы после выполнения фрагмента][ImageSnippetSplitScreenAfter]  

## Открытие области "фрагменты кода"   

На панели **фрагментов** перечислены ваши фрагменты.  Если вы хотите изменить фрагмент, необходимо открыть его из области **фрагментов** .  

> ##### Рисунок3  
> Область **фрагментов**  
> ![Область фрагментов][ImageSnippetsPane]  

### Открытие области фрагментов с помощью мыши   

1.  Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".  Обычно область **страницы** открывается по умолчанию.  

    > ##### Рисунок4  
    > Панель « **источники** » с открытой областью **страницы** в левой части экрана  
    > ![Панель «источники» с открытой областью страницы в левой части экрана][ImageSourcesPageEmpty]  

1.  Перейдите на вкладку **фрагменты кода** , чтобы открыть область **фрагменты** .  **More Tabs** ![ ][ImageMoreTabsIcon] Для доступа к параметру **фрагментов** может потребоваться нажать кнопку Другие вкладки.  

### Открытие области фрагментов с помощью меню команд   

1.  Сфокусировать указатель мыши в DevTools.  
1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).  
1.  Начните вводить текст `Snippets` , нажмите кнопку **Показать фрагменты**и нажмите клавишу `Enter` для запуска команды.  

    > ##### Рисунок 5  
    > Команда « **Показать фрагменты** »  
    > ![Команда «Показать фрагменты»][ImageShowSnippetsSearch]  

## Создание фрагментов кода   

### Создание фрагмента с помощью панели «источники»   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Нажмите кнопку **создать фрагмент**.  
1.  Введите имя для фрагмента, а затем нажмите `Enter` для сохранения.  

    > ##### Рисунок6  
    > Присвоение имени фрагменту  
    > ![Присвоение имени фрагменту][ImageSnippetName]  

### Создание фрагмента с помощью меню команд   

1.  Сфокусировать указатель мыши в DevTools.  
1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).  
1.  Начните вводить текст `Snippet` , выберите **создать новый фрагмент**, а затем нажмите, `Enter` чтобы выполнить команду.  

    > ##### Рисунок7  
    > Команда для создания нового фрагмента.  
    > ![Команда для создания нового фрагмента.][ImageCreateSnippetSearch]  

Если вы хотите присвоить новому фрагменту настраиваемое имя, просмотрите [фрагменты Rename](#rename-snippets) .  

## Редактирование фрагментов   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  В области **фрагменты** щелкните имя фрагмента, который вы хотите изменить, чтобы открыть его в **редакторе кода**.  

    > ##### Рисунок8  
    > Редактор кода  
    > ![Редактор кода][ImageSnippetEditor]  

1.  С помощью **редактора кода** добавьте JavaScript в сниппет.  
1.  Если рядом с именем фрагмента появится звездочка, это означает, что у вас есть несохраненный код. Чтобы сохранить, нажмите клавиши `Control` + `S` \ (Windows \) или `Command` + `S` \ (macOS \).  

    > ##### Рисунок9  
    > Звездочка рядом с именем фрагмента, обозначающее несохраненный код.  
    > ![Звездочка рядом с именем фрагмента, обозначающее несохраненный код.][ImageUnsavedSnippet]  

## Выполнение фрагментов кода   

### Выполнение фрагмента на панели «источники»   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Щелкните имя фрагмента, который вы хотите выполнить.  Фрагмент откроется в **редакторе кода**.  
1.  Выберите команду **выполнить** фрагмент. ![ запустите фрагмент ][ImageRunSnippetIcon] или нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \).  

### Выполнение фрагмента с помощью меню команд   

1.  Сфокусировать указатель мыши в DevTools.  
1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).  
1.  Удалите `>` символ и введите символ, а `!` затем имя фрагмента, который вы хотите выполнить.  

    > ##### Рисунок 10  
    > Выполнение фрагмента из меню команд  
    > ![Выполнение фрагмента из меню команд][ImageRunSnippetCommand]  

1.  Нажмите, `Enter` чтобы запустить фрагмент.  

## Переименование фрагментов   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Переименовать**.  

## Удаление фрагментов   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Удалить**.  

 



<!-- image links -->  

[ImageMoreTabsIcon]: /microsoft-edge/devtools-guide-chromium/media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSnippetSplitScreen]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen.msft.png "На рисунке 1 показано, как выглядит страница перед выполнением фрагмента."  
[ImageSnippetSplitScreenAfter]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-split-screen-after.msft.png "Рисунок 2: вид страницы после выполнения фрагмента."  
[ImageSnippetsPane]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-pane.msft.png "Рисунок 3: область фрагментов"  
[ImageSourcesPageEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-page-pane.msft.png "Рисунок 4: панель «источники» с открытой областью страниц в левой части экрана"  
[ImageShowSnippetsSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-show-snippets.msft.png "Рисунок 5: команда «Показать фрагменты»"  
[ImageSnippetName]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-naming.msft.png "Рисунок 6: именование фрагмента"  
[ImageCreateSnippetSearch]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-create-new-snippet.msft.png "Рисунок 7: команда для создания нового фрагмента кода"  
[ImageSnippetEditor]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-saved.msft.png "Рисунок 8: редактор кода"  
[ImageUnsavedSnippet]: /microsoft-edge/devtools-guide-chromium/media/javascript-sources-snippets-editor-unsaved.msft.png "Рисунок 9: звездочка рядом с именем фрагмента, указывающая на несохраненный код."  
[ImageRunSnippetCommand]: /microsoft-edge/devtools-guide-chromium/media/javascript-search-run-command.msft.png "Рисунок 10: запуск фрагмента из меню команд"  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли"  
[DevToolsSourcesPanel]: ../sources.md "Обзор палитры «источники»"  

[MDNScratchpad]: https://developer.mozilla.org/docs/Tools/Scratchpad "Пометок | MDN"  
[WikiBookmarklet]: https://en.wikipedia.org/wiki/Bookmarklet "Кнопка-«Википедии»"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/snippets) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
