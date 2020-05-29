---
title: Обзор палитры «источники»
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: c61d1bda030ce729b0b217b95a9143508d1f51f8
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601910"
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
   limitations under the License. -->






# Обзор палитры «источники» 



С помощью панели DevTools **источники** Microsoft EDGE Вы можете:

*   [Просмотр файлов](#view-files).  
*   [Редактирование CSS и JavaScript](#edit-css-and-javascript).  
*   [Создавайте и сохраняйте **фрагменты кода** JavaScript](#create-save-and-run-snippets), которые можно запускать на любой странице.  **Фрагменты** аналогичны кнопкам для закладок.  
*   [Отладка JavaScript](#debug-javascript).  
*   [Настройте рабочую область](#set-up-a-workspace), чтобы изменения, внесенные в DevTools, сохранялись в коде в файловой системе.  

## Просмотр файлов 

Используйте область **страниц** для просмотра всех ресурсов, загруженных страницей.

> ##### Рис. 1  
> Область **страницы**  
> ![Рисунок 1: область страницы][ImageSourcesPagePane]  

Упорядочение области **страницы** .  
*   Верхний уровень, например `top` на [**рис. 1**](#figure-1), представляет [рамку HTML][W3CHtml4Frames].  Найдите `top` на каждой странице, которую вы посещаете. `top` представляет рамку основного документа.  
*   Второй уровень, например `docs.microsoft.com` на [**рисунке 1**](#figure-1), представляет [источник][HtmlstandardOrigin].  
*   Третий уровень, четвертый уровень и т. д. — каталоги и ресурсы, загруженные из этого источника.  Например, на [**рисунке 1**](#figure-1) полный путь `devtools-guide-chromium` к ресурсу `docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium`  

Щелкните файл в области **страницы** , чтобы просмотреть содержимое в области " **Редактор** ".  Вы можете просматривать файлы любого типа. Для изображений вы видите изображение для предварительного просмотра.  

> ##### Рисунок 2  
> Просмотр содержимого `a4d10f71.index-docs.js` в области " **Редактор** "  
> ![Рисунок 2. Просмотр содержимого файла a4d10f71. index-docs. js в области "редактор"][ImageSourcesEditorPane]  

## Редактирование CSS и JavaScript 

Для изменения CSS и JavaScript используйте область " **Редактор** ".  DevTools обновляет страницу, чтобы выполнить новый код. Например, если вы изменяете CSS-файл, добавив правило стиля ниже:

```css
.metadata.page-metadata {
    color: red;
}
```

Вы увидите, что изменения вступают в силу немедленно.

> ##### Рисунок3  
> Редактирование CSS на панели « **Редактор** » для изменения цвета текста подзаголовка на красный  
> ![Рисунок 3. Редактирование CSS на панели «редактор» для изменения цвета текста подзаголовка на красный][ImageEditCSS]  

Изменения в CSS вступают в силу немедленно, сохранение не требуется. Чтобы изменения в JavaScript вступили в силу, нажмите клавиши `Control` + `S` \ (Windows \) или `Command` + `S` \ (macOS \). DevTools не выполняет повторно сценарий, поэтому изменения, которые вступают в силу, выполняются только в рамках функций.  Например, на [**рисунке 4**](#figure-4) Обратите внимание на `console.log('A')` то, что не выполняется, в то время как оно `console.log('B')` делает. Если после внесения изменений DevTools повторно запустили весь сценарий, он `A` будет записан в журнал на **консоли**.  

> ##### Рисунок4  
> Редактирование JavaScript в области " **Редактор** "  
> ![Рисунок 4. Редактирование JavaScript в области "редактор"][ImageEditJS]  

DevTools удаляет изменения стилей CSS и JavaScript при повторной загрузке страницы. Сведения о том, как сохранить изменения в файловой системе, можно найти в разделе [Настройка рабочей области](#set-up-a-workspace) .  

## Создание, сохранение и запуск фрагментов 

Фрагменты — это сценарии, которые можно запускать на любой странице. Предположим, что вы повторно вводите на **консоли**следующий код, чтобы вставить библиотеку jQuery на страницу, чтобы можно было запускать команды jQuery из **консоли**:  

```javascript
let script = document.createElement('script');
script.src = 'https://code.jquery.com/jquery-3.2.1.min.js';
script.crossOrigin = 'anonymous';
script.integrity = 'sha256-hwg4gsxgFZhOsEEamdOYGBf13FyQuiTwlAQgxVSNgt4=';
document.head.appendChild(script);
```  

Вместо этого вы можете сохранить этот код во **фрагменте** и выполнить его с помощью нескольких нажатий кнопки, когда вам понадобится.  DevTools сохранит **фрагмент** в файловой системе.  

> ##### Рисунок 5  
> **Фрагмент кода** , который вставляет библиотеку jQuery на страницу  
> ![Рисунок 5. Фрагмент кода, который вставляет библиотеку jQuery на страницу][ImageSnippet]  

Чтобы выполнить **фрагмент кода**, выполните указанные ниже действия.

*   Откройте файл с помощью панели **фрагментов** **и нажмите кнопку выполнить** ![ ][ImageRunIcon] .  
*   Откройте **[меню команд][DevtoolsGuideChromiumCommandMenuIndex]**, удалите `>` символ, введите `!` его имя, а затем нажмите клавишу **Snippet** `Enter` .  

Дополнительные сведения можно найти в разделе [выполнение фрагментов кода на любой странице][DevtoolsGuideChromiumJavascriptSnippets] .


## Отладка JavaScript 

Вместо того `console.log()` , чтобы использовать для определения того, где произошел сбой JavaScript, рекомендуется использовать инструменты отладки Microsoft Edge DevTools. Общая идея состоит в том, чтобы установить точку останова, которая является умышленно остановленным местом в вашем коде, и пошаговое руководство по коду — по одной строке за раз. По мере выполнения кода вы можете просматривать и изменять значения всех текущих заданных свойств и переменных, запускать JavaScript на **консоли**и т. д.

Сведения об отладке в DevTools можно найти в статье Начало [работы с отладкой JavaScript][DevtoolsGuideChromiumJavascriptIndex] .

> ##### Рисунок6  
> Отладка JavaScript  
> ![Рисунок 6. Отладка JavaScript][ImageDebugging]  

## Настройка рабочей области 

По умолчанию при редактировании файла на панели « **источники** » эти изменения теряются при повторной загрузке страницы.  **Рабочие области** позволяют сохранить изменения, внесенные в DevTools, в файловую систему.  По сути, это позволяет использовать DevTools в качестве редактора кода.

Чтобы приступить к работе, ознакомьтесь со статьей [изменение файлов с помощью рабочих областей][DevtoolsGuideChromiumWorkspacesIndex] .

 



<!-- image links -->  

[ImageRunIcon]: /microsoft-edge/devtools-guide-chromium/media/run-snippet-icon.msft.png  

[ImageSourcesPagePane]: /microsoft-edge/devtools-guide-chromium/media/sources-page-pane.msft.png "Рисунок 1: область страницы"  
[ImageSourcesEditorPane]: /microsoft-edge/devtools-guide-chromium/media/sources-editor-pane.msft.png "Рисунок 2: Просмотр содержимого файла a4d10f71. index-docs. js в области "редактор""  
[ImageEditCSS]: /microsoft-edge/devtools-guide-chromium/media/edit-css.msft.png "Рисунок 3: Редактирование CSS на панели "редактор" для изменения цвета текста подзаголовка на красный"  
[ImageEditJS]: /microsoft-edge/devtools-guide-chromium/media/edit-js.msft.png "Рисунок 4: Редактирование JavaScript в области "редактор""  
[ImageSnippet]: /microsoft-edge/devtools-guide-chromium/media/snippet.msft.png "Рисунок 5: фрагмент, который вставляет библиотеку jQuery на страницу"  
[ImageDebugging]: /microsoft-edge/devtools-guide-chromium/media/debugging.msft.png "Рисунок 6: Отладка JavaScript"  

<!-- links -->  

[DevtoolsGuideChromiumCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptIndex]: /microsoft-edge/devtools-guide-chromium/javascript/index "Начало работы с отладкой JavaScript в Microsoft Edge DevTools"  
[DevtoolsGuideChromiumJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools"  
[DevtoolsGuideChromiumWorkspacesIndex]: /microsoft-edge/devtools-guide-chromium/workspaces/index "Редактирование файлов с помощью рабочих областей"  

[HtmlstandardOrigin]: https://html.spec.whatwg.org/multipage/origin.html#origin "Современный: HTML Standard"  

[W3CHtml4Frames]: https://w3.org/TR/html401/present/frames.html "Кадры | PNG"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/sources) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
