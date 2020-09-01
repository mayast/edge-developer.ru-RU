---
title: Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 3a5ae986e3080a0b6a8b1bf34b0e0efc44c90303
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982033"
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



Если вы обнаружите, что один и тот же код запускается повторно на [консоли][DevtoolsConsoleIndex] , попробуйте сохранить его как фрагмент кода.  Фрагменты — это сценарии, созданные вами на панели « [источники][DevToolsSourcesPanel] ».  У них есть доступ к контексту JavaScript на странице, и вы можете запускать их на любой странице.  Фрагменты — это альтернатива для [Закладка][WikiBookmarklet].  
В Firefox DevTools есть функция, похожая на фрагменты, которые называются [блокнотом][MDNScratchpad].  

Например, на приведенном ниже рисунке показана домашняя страница DevTools слева и фрагмент исходного кода справа.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen.msft.png" alt-text="Вид страницы перед выполнением фрагмента" lightbox="../media/javascript-sources-snippets-split-screen.msft.png":::
   Вид страницы перед выполнением фрагмента  
:::image-end:::  

Исходный код фрагмента на предыдущем рисунке.  

```javascript
console.log('Hello, Snippets!');
document.body.innerHTML = '';
var p = document.createElement('p');
p.textContent = 'Hello, Snippets!';
document.body.appendChild(p);
```  

На рисунке ниже показана страница после выполнения фрагмента.  Во всплывающем **ящике консоли** выводится `Hello, Snippets!` сообщение о том, что журналы фрагментов, и содержимое страницы полностью меняются.  

:::image type="complex" source="../media/javascript-sources-snippets-split-screen-after.msft.png" alt-text="Вид страницы после выполнения фрагмента" lightbox="../media/javascript-sources-snippets-split-screen-after.msft.png":::
   Вид страницы после выполнения фрагмента  
:::image-end:::  

## Открытие области "фрагменты кода"   

На панели **фрагментов** перечислены ваши фрагменты.  Если вы хотите изменить фрагмент, необходимо открыть его из области **фрагментов** .  

:::image type="complex" source="../media/javascript-sources-snippets-pane.msft.png" alt-text="Область фрагментов" lightbox="../media/javascript-sources-snippets-pane.msft.png":::
   Область **фрагментов**  
:::image-end:::  

### Открытие области фрагментов с помощью мыши   

1.  Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".  Обычно область **страницы** открывается по умолчанию.  
    
    :::image type="complex" source="../media/javascript-sources-page-pane.msft.png" alt-text="Панель «источники» с открытой областью страницы в левой части экрана" lightbox="../media/javascript-sources-page-pane.msft.png":::
       Панель « **источники** » с открытой областью **страницы** в левой части экрана  
    :::image-end:::  
    
1.  Перейдите на вкладку **фрагменты кода** , чтобы открыть область **фрагменты** .  **More Tabs** ![ ][ImageMoreTabsIcon] Для доступа к параметру **фрагментов** может потребоваться нажать кнопку Другие вкладки \ (другие вкладки \).  
    
### Открытие области фрагментов с помощью меню команд   

1.  Сфокусировать указатель мыши в DevTools.  
1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).  
1.  Начните вводить текст `Snippets` , нажмите кнопку **Показать фрагменты**и нажмите клавишу `Enter` для запуска команды.  
    
    :::image type="complex" source="../media/javascript-search-show-snippets.msft.png" alt-text="Команда «Показать фрагменты»" lightbox="../media/javascript-search-show-snippets.msft.png":::
       Команда « **Показать фрагменты** »  
    :::image-end:::  
    
## Создание фрагментов кода   

### Создание фрагмента с помощью панели «источники»   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Нажмите кнопку **создать фрагмент**.  
1.  Введите имя для фрагмента, а затем нажмите `Enter` для сохранения.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-naming.msft.png" alt-text="Присвоение имени фрагменту" lightbox="../media/javascript-sources-snippets-naming.msft.png":::
       Присвоение имени фрагменту  
    :::image-end:::  
    
### Создание фрагмента с помощью меню команд   

1.  Сфокусировать указатель мыши в DevTools.  
1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).  
1.  Начните вводить текст `Snippet` , выберите **создать новый фрагмент**, а затем нажмите, `Enter` чтобы выполнить команду.  
    
    :::image type="complex" source="../media/javascript-search-create-new-snippet.msft.png" alt-text="Команда для создания нового фрагмента." lightbox="../media/javascript-search-create-new-snippet.msft.png":::
       Команда для создания нового фрагмента.  
    :::image-end:::  
    
Если вы хотите присвоить новому фрагменту настраиваемое имя, просмотрите [фрагменты Rename](#rename-snippets) .  

## Редактирование фрагментов   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  В области **фрагменты** щелкните имя фрагмента, который вы хотите изменить, чтобы открыть его в **редакторе кода**.  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-saved.msft.png" alt-text="Редактор кода" lightbox="../media/javascript-sources-snippets-editor-saved.msft.png":::
       **Редактор кода**  
    :::image-end:::  
    
1.  С помощью **редактора кода** добавьте JavaScript в сниппет.  
1.  Если рядом с именем фрагмента появится звездочка, это означает, что у вас есть несохраненный код. Чтобы сохранить, нажмите клавиши `Control` + `S` \ (Windows \) или `Command` + `S` \ (macOS \).  
    
    :::image type="complex" source="../media/javascript-sources-snippets-editor-unsaved.msft.png" alt-text="Звездочка рядом с именем фрагмента, обозначающее несохраненный код." lightbox="../media/javascript-sources-snippets-editor-unsaved.msft.png":::
       Звездочка рядом с именем фрагмента, обозначающее несохраненный код.  
    :::image-end:::  
    
## Выполнение фрагментов кода   

### Выполнение фрагмента на панели «источники»   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Щелкните имя фрагмента, который вы хотите выполнить.  Фрагмент откроется в **редакторе кода**.  
1.  Выберите команду **выполнить фрагмент** \ ( ![ выполнить фрагмент \ ][ImageRunSnippetIcon] ) или нажмите клавиши `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \).  
    
### Выполнение фрагмента с помощью меню команд   

1.  Сфокусировать указатель мыши в DevTools.  
1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).  
1.  Удалите `>` символ и введите символ, а `!` затем имя фрагмента, который вы хотите выполнить.  
    
    :::image type="complex" source="../media/javascript-search-run-command.msft.png" alt-text="Выполнение фрагмента из меню команд" lightbox="../media/javascript-search-run-command.msft.png":::
       Выполнение фрагмента из **меню команд**  
    :::image-end:::  
    
1.  Нажмите, `Enter` чтобы запустить фрагмент.  

## Переименование фрагментов   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Переименовать**.  
    
## Удаление фрагментов   

1.  [Открытие области **фрагментов** ](#open-the-snippets-pane).  
1.  Щелкните имя фрагмента правой кнопкой мыши и выберите команду **Удалить**.  
    
<!--  
 


-->  

<!-- image links -->  

[ImageMoreTabsIcon]: ../media/more-tabs-icon.msft.png  
[ImageRunSnippetIcon]: ../media/run-snippet-icon.msft.png  

<!-- links -->  

[DevtoolsConsoleIndex]: ../console/index.md "Обзор консоли | Документы Microsoft"  
[DevToolsSourcesPanel]: ../sources.md "Обзор панели «источники» | Документы Microsoft"  

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
