---
title: Приступая к просмотру и изменению модели DOM
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 4dee8b4e3ea927e72c0f98517f264b2c1d453013
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607449"
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





# Приступая к просмотру и изменению модели DOM   



Заполните эти интерактивные учебники, чтобы ознакомиться с основными принципами просмотра и изменения модели DOM на странице с помощью Microsoft Edge DevTools.  

В этом руководстве предполагается, что вы знаете разницу между DOM и HTML.  Ознакомьтесь с приложением [: HTML и модель DOM](#appendix-html-versus-the-dom) для объяснения.  

## Примеры открытых DOM  

1.  Удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \) и щелкните **примеры DOM** , чтобы открыть ее на новой вкладке.  
    
    [Примеры DOM][GlitchDomExamples]  
    
## Просмотр узлов DOM   

На панели "элементы" в дереве DOM можно выполнить все действия, связанные с DOM, в DevTools.  

### Проверка узла   

Если вы заинтересованы в определенном узле DOM, **Проверьте** , как быстро открыть DevTools и проанализировать этот узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **Проверка узла**щелкните правой кнопкой мыши **Michelangelo** и выберите команду **проверить**.  
    
    > ##### Рис. 1  
    > Проверка узла  
    > ![Проверка узла][ImageInspectingNode]  
    
    1.  Откроется панель " **элементы** " DevTools.  `<li>Michelangelo</li>` в **дереве DOM**выделено.  
        
        > ##### Рисунок 2  
        > Выделение узла Michelangelo  
        > ![Выделение узла Michelangelo][ImageHighlightingMichelangeloNode]  
        
        1.  Щелкните значок **проверки** ![ проверки ][ImageInspectIcon] в левом верхнем углу DevTools.  
            
            > ##### Рисунок3  
            > Значок проверки  
            > ![Значок проверки][ImageInspect]  
            
1.  В разделе **Проверка узла**щелкните текст в **Токио** .  Теперь `<li>Tokyo</li>` выделена в дереве DOM.  

Проверка узла также является первым шагом в направлении просмотра и изменения стилей узла.  Ознакомьтесь [со статьей начало работы с помощью просмотра и изменения CSS][DevToolsCssGetStarted].  

### Навигация по дереву DOM с помощью клавиатуры   

После того как вы выбрали узел в дереве DOM, вы можете перемещаться по дереву DOM с помощью клавиатуры.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **Навигация по дереву DOM с помощью клавиатуры**щелкните правой кнопкой мыши **Ringo** и выберите команду **проверить**.  `<li>Ringo</li>` выбрано в дереве DOM.  
    
    > ##### Рисунок4  
    > Проверка узла Ringo  
    > ![Проверка узла Ringo][ImageInspectingRingoNode]  
    
    1.  Нажимайте клавишу `Up` стрелка 2.  `<ul>` .  
        
        > ##### Рисунок 5  
        > Проверка узла UL  
        > ![Проверка узла UL][ImageInspectingUlNode]  
        
    1.  Нажмите клавишу `Left` со стрелкой.  `<ul>`Список сворачивается.  
    1.  Снова нажмите клавишу `Left` со стрелкой.  Выбран родительский элемент `<ul>` узла.  В этом случае это `<div>` идентификатор `navigate-the-dom-tree-with-a-keyboard-1` .  
    1.  Нажимайте клавишу `Down` стрелка 2, чтобы повторно выбрать `<ul>` только что свернутый список.  Это должно выглядеть следующим образом. `<ul>... </ul>`  
    1.  Нажмите клавишу `Right` со стрелкой.  Список будет развернут.  

### Прокрутка представления   

При просмотре дерева DOM может возникнуть интерес к узлу DOM, который в данный момент не находится в окне просмотра.  Например, предположим, что вы прокручивается в нижней части страницы, и вы заинтересованы в `<h1>` узле в верхней части страницы.  **Прокрутка представления** позволяет быстро изменить расположение окна просмотра, чтобы вы могли видеть этот узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **прокрутить представление**щелкните правой кнопкой мыши **Magritte** и выберите команду **проверить**.  
1.  Прокрутите страницу "примеры DOM" до конца.  
1.  Этот `<li>Magritte</li>` узел по-прежнему должен быть выбран в дереве DOM.  В противном случае вернитесь на [страницу Просмотр](#scroll-into-view) и начните заново.  
1.  Щелкните правой кнопкой мыши `<li>Magritte</li>` узел и выберите **прокрутить до представления**.  Ваше окно просмотра будет прокручено, чтобы вы могли видеть узел **Magritte** .  Если вы не видите параметр **прокрутить в представлении** , вы можете просмотреть [Приложение: отсутствующие параметры](#appendix-missing-options) .
    
    > ##### Рисунок6  
    > Прокрутка представления  
    > ![Прокрутка представления][ImageScrollView]  

### Поиск узлов   

Вы можете выполнить поиск по дереву DOM по строке, селектору CSS или селектору XPath.  

1.  Сосредоточьте указатель мыши на панели " **элементы** ".  
1.  Нажмите клавиши `Control` + `F` \ (Windows \) или `Command` + `F` \ (macOS \).  Строка поиска откроется в нижней части дерева DOM.  
1.  Введите `The Moon is a Harsh Mistress`.  Последнее предложение выделено в дереве DOM.  
    
    > ##### Рисунок7  
    > Выделение запроса в строке поиска  
    > ![Выделение запроса в строке поиска][ImageHighlightingQuerySearchBar]  
    
Как упоминалось выше, строка поиска также поддерживает селекторы CSS и XPath.  

## Редактирование модели DOM   

Вы можете изменить модель DOM на лету и посмотреть, как эти изменения влияют на страницу.  

### Редактирование контента   

Чтобы изменить содержимое узла, дважды щелкните его содержимое в дереве DOM.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **изменить содержимое**щелкните правой кнопкой мыши **Мишель** и выберите команду **проверить**.  
    1.  В дереве DOM дважды щелкните `Michelle` .  Другими словами, дважды щелкните текст между `<li>` and `</li>` .  Текст будет выделено, чтобы показать, что он выделен.  
        
        > ##### Рисунок8  
        > Редактирование текста  
        > ![Редактирование текста][ImageEditingText]  
        
    1.  Удалить `Michelle` , введите `Leela` и нажмите кнопку, `Enter` чтобы подтвердить изменение.  Текст в DOM изменится с **Мишель** на **Leela**.  

### Изменение атрибутов   

Чтобы изменить атрибуты, дважды щелкните имя или значение атрибута.  Следуйте инструкциям, чтобы научиться добавлять атрибуты на узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **изменить атрибуты**щелкните правой кнопкой мыши **Говард** и выберите команду **проверить**.  

1.  Дважды щелкните `<li>` .  Текст будет выделено, чтобы показать, что выбран узел.  
    
    > ##### Рисунок9  
    > Редактирование узла  
    > ![Редактирование узла][ImageEditingNode]  
    
1.  Нажимайте клавишу `Right` со стрелкой, добавьте пробел, введите текст `style="background-color:gold"` и нажмите клавишу `Enter` .  Цвет фона узла изменится на Золотой.  
    
    > ##### Рисунок 10  
    > Добавление атрибута стиля на узел  
    > ![Добавление атрибута стиля на узел][ImageAddingStyleAttributeNode]  
    
### Изменить тип узла   

Чтобы изменить тип узла, дважды щелкните его, а затем введите новый тип.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **изменить тип узла**щелкните правой кнопкой мыши **Hank** и выберите команду **проверить**.  
    1.  Дважды щелкните `<li>` .  Текст `li` будет выделен.  
    1.  Удалить `li` , введите `button` и нажмите клавишу `Enter` .  `<li>`Узел изменится на `<button>` узел.  
        
        > ##### Рисунок11  
        > Изменение типа узла на кнопку  
        > ![Изменение типа узла на кнопку][ImageChangingNodeButton]  
        
### Изменение порядка узлов DOM   

Перетащите узлы, чтобы изменить их порядок.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **изменение порядка узлов DOM**щелкните **Elvis Presley** правой кнопкой мыши и выберите команду **проверить**.  
    
    > [!NOTE]
    > Это последний элемент в списке.  
    
    1.  В дереве DOM перетащите указатель `<li>Elvis Presley</li>` в верхнюю часть списка.  
        
        > ##### Рисунок12  
        > Перетаскивание узла в верхнюю часть списка  
        > ![Перетаскивание узла в верхнюю часть списка][ImageDraggingNodeTopList]  
        
### Принудительное состояние   

Вы можете принудительно оставлять узлы в состоянии, в том числе,,, `:active` `:hover` `:focus` `:visited` и `:focus-within` .  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **принудительное состояние**наведите указатель мыши на **Lord летит**.  Цвет фона становится оранжевым.  
    1.  Щелкните **Lord летит** правой кнопкой мыши и выберите команду **проверить**.  
    1.  Щелкните правой кнопкой мыши `<li class="demo--hover">The Lord of the Flies</li>` и выберите **принудительное состояние**  >  **: наведение**.  Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .  Цвет фона остается оранжевым, несмотря на то что вы не наводите указатель мыши на узел.  

### Скрытие узла   

Нажмите `H` , чтобы скрыть узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **скрыть узел**щелкните правой кнопкой мыши **звезду назначения** и выберите команду **проверить**.  
    1.  Нажмите клавишу `H` .  Узел скрыт.  
        
        > ##### Рисунок13  
        > Как выглядит узел в дереве DOM после его скрытия  
        > ![Как выглядит узел в дереве DOM после его скрытия][ImageNodeDomTreeAfterHidden]  
        
    1.  Снова нажмите клавишу `H` .  Узел снова появится.  

### Удаление узла   

Нажмите `Delete` , чтобы удалить узел.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **Удаление узла**щелкните правой кнопкой мыши элемент **Foundation** и выберите команду **проверить**.  
    1.  Нажмите клавишу `Delete` .  Узел удален.  
    1.  Нажмите клавиши `Control` + `Z` \ (Windows \) или `Command` + `Z` \ (macOS \).  Последнее действие отменено, и узел появится снова.  

## Узлы Access на консоли   

DevTools предоставляет несколько сочетаний клавиш для доступа к узлам DOM из консоли или получения ссылок JavaScript на каждую из них.  

### Ссылка на узел, выбранный в настоящее время с помощью $0   

Когда вы просматриваете узел, `== $0` текст рядом с узлом означает, что вы можете добавить ссылку на этот узел в консоль с переменной `$0` .  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **ссылка на узел, выбранный в $0**, щелкните правой кнопкой мыши **в левой части экрана** , а затем выберите команду **проверить**.  
    1.  Нажмите клавишу, `Escape` чтобы открыть консольный ящик.  
    1.  Введите текст и нажмите клавишу ВВОД `$0` `Enter` .  Результат выражения показывает, что выражение `$0` имеет значение `<li>The Left Hand of Darkness</li>` .  
        
        > ##### Рисунок14  
        > Результат первого `$0` выражения в консоли  
        > ![Результат первого выражения $0 в консоли][ImageFirstConsole]  
        
    1.  Наведите указатель мыши на результат.  Узел выделится в окне просмотра.  
    1.  Щелкните `<li>Dune</li>` дерево DOM, введите `$0` консоль еще раз, а затем нажмите `Enter` еще раз.  Теперь `$0` оценивается `<li>Dune</li>` .  
        
        > ##### Рисунок15  
        > Результат второго `$0` выражения на консоли — ![ результат второго выражения $0 в консоли.][ImageSecondConsole]  
        
### Сохранить как глобальную переменную   

Если необходимо повторно сослаться на узел, сохраните его как глобальную переменную.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **Сохранить как глобальную переменную**щелкните правой кнопкой мыши **в большом спящем режиме** и выберите **проверить**.  
    1.  Щелкните правой кнопкой мыши `<li>The Big Sleep</li>` дерево DOM и выберите **Сохранить как глобальную переменную**.  Если вы не видите этот параметр, просмотрите [Приложение: отсутствующие параметры](#appendix-missing-options) .  
    1.  Введите текст `temp1` на консоли и нажмите клавишу `Enter` .  Результат выражения показывает, что переменная является узлом.  
        
        > ##### Рисунок16  
        > Результат выражения temp1  
        > ![Результат выражения temp1][ImageResultTemp1]  
        
### Скопировать путь к JS   

Скопируйте путь JavaScript на узел, если вам нужно сослаться на него в автоматическом тесте.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **скопировать путь к каталогу**щелкните правой кнопкой мыши **братьев Karamazov** и выберите команду **проверить**.  
    1.  Щелкните правой кнопкой мыши `<li>The Brothers Karamazov</li>` дерево DOM и выберите команду **Копировать**  >  **путь к каталогу**.  `document.querySelector()`Выражение, которое разрешается в узел, копируется в буфер обмена.  
    1.  `Control` + `V` Чтобы вставить выражение на консоль, нажмите клавиши \ (Windows \) или `Command` + `V` \ (macOS \).  
    1.  Нажмите `Enter` , чтобы вычислить выражение.
        
        > ##### Рисунок17  
        > Результат выражения Copy JS Path  
        > ![Результат выражения Copy JS Path][ImageResultCopyJSPath]  
        
## Прерывание изменений DOM   

DevTools позволяет приостановить JavaScript на странице, когда JavaScript изменит модель DOM.  

### Прерывание изменений атрибутов   

Используйте точки останова по изменению атрибутов, если требуется приостановить JavaScript, который приводит к изменению любого атрибута узла.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **прервать на странице "изменения атрибутов**" щелкните правой кнопкой мыши **Sauerkraut** и выберите команду **проверить**.  
    1.  В дереве DOM щелкните правой кнопкой мыши `<li id="target">Sauerkraut</li>` и выберите команду **прервать для**  >  **изменений атрибутов**.  Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .
        
        > ##### Рис. 18  
        > Прерывание изменений атрибутов  
        > ![Прерывание изменений атрибутов][ImageBreakAttributeModification]  
        
    1.  На следующем этапе вы будете получать инструкции по нажатию кнопки, которая приостанавливает код страницы.  После того как страница приостановлена, прокрутка страницы больше недоступна.  **Resume Script** ![ ][ImageResumeScriptIcon] Чтобы снова выполнить прокрутку страницы, необходимо выбрать команду возобновить сценарий возобновления.
        
        > ##### На рисунке 19  
        > Как возобновить выполнение сценария  
        > ![Как возобновить выполнение сценария][ImageResumeScript]  
        
    1.  Нажмите кнопку " **настроить фон** ".  Таким образом, `style` для атрибута узла будет задано значение `background-color:thistle` .  DevTools приостанавливает страницу и выделяет код, который привел к изменению атрибута.  
    1.  Нажмите кнопку **возобновить** сценарий ![ резюме ][ImageResumeScriptIcon] , как упоминалось ранее.  
    
### Прерывание при удалении узла   

Если вы хотите приостановить работу при удалении определенного узла, используйте точки останова удаления узла.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **прервать удаление узла**щелкните правой кнопкой мыши **Neuromancer** и выберите команду **проверить**.  
    1.  В дереве DOM щелкните правой кнопкой мыши `<li id="target">Neuromancer</li>` и выберите команду **прервать при**  >  **удалении узла**.  Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .  
    1.  Нажмите кнопку " **Удалить** ".  DevTools приостанавливает страницу и выделяет код, вызвавший удаление узла.  
    1.  Нажмите кнопку **возобновить** сценарий ![ возобновления ][ImageResumeScriptIcon] .  
    
### Прерывание при изменении поддерева   

После того как вы добавите на узел точку останова изменения поддерева, DevTools приостанавливает страницу при добавлении или удалении любого потомка узла.  

1.  [Откройте примеры DOM](#open-dom-examples).  
1.  В разделе **прервать при изменении поддерева**щелкните правой кнопкой мыши значок **Fire** и выберите пункт **проверить**.  
    1.  В дереве DOM щелкните правой кнопкой мыши расположенный `<ul id="target">` выше узел `<li>A Fire Upon the Deep</li>` и выберите команду **приостановить**  >  **изменение поддерева**.  Если вы не видите этот параметр, ознакомьтесь со статьей [Приложение: отсутствующие параметры](#appendix-missing-options) .  
    1.  Нажмите кнопку **Добавить ребенка**.  Код приостанавливается, так как `<li>` узел был добавлен в список.  
    1.  Нажмите кнопку **возобновить** сценарий ![ возобновления ][ImageResumeScriptIcon] .  
    
## Дальнейшие действия   

, Которая охватывает большую часть функций, связанных с DOM, в DevTools.  Вы можете найти остальные элементы, щелкнув правой кнопкой мыши узлы в дереве DOM и экспериментируя с другими параметрами, которые не были рассмотрены в этом учебнике.  Вы также можете просмотреть [сочетания клавиш для панели элементов][DevToolsShortcutsElements].  

Ознакомьтесь с [домашней страницей Microsoft Edge DevTools][MicrosoftEdgeDevTools] , чтобы найти все, что вы можете делать с DevTools.  

<!--See [Community](../index#community) if you want to contact the DevTools team or get help from the DevTools community.  -->  



## Приложение: HTML и модель DOM   

В этом разделе приводится описание различий между HTML и DOM.  

При использовании веб-браузера для запроса страницы сервер возвращает HTML-код следующим образом:  

```html
<!doctype html>
<html>
  <head>
    <title>Hello, world!</title>
  </head>
  <body>
    <h1>Hello, world!</h1>
    <p>This is a hypertext document on the World Wide Web.</p>
    <script src="/script.js" async></script>
  </body>
</html>
```  

Браузер анализирует HTML-код и создает дерево объектов, как показано ниже.  

```dom
html
  head
    title
  body
    h1
    p
    script
```  

Это дерево объектов или узлов, представляющее содержимое страницы, называется DOM.  Теперь он выглядит так же, как HTML, но предположим, что сценарий, указанный в нижней части HTML, выполняет этот код:  

```javascript
const h1 = document.querySelector('h1');
h1.parentElement.removeChild(h1);
const p = document.createElement('p');
p.textContent = 'Wildcard!';
document.body.appendChild(p);
```  

Этот код удаляет `h1` узел и добавляет еще один `p` узел в модель DOM.  Полная модель DOM теперь выглядит следующим образом:  

```dom
html
  head
    title
  body
    p
    script
    p
```  

HTML-код страницы теперь отличается от модели DOM.  Другими словами, HTML представляет начальное содержимое страницы, а модель DOM — текущее содержимое страницы.  Когда JavaScript добавляет, удаляет или редактирует узлы, модель DOM становится отличной от HTML.  

Дополнительные сведения можно найти в разделе [Введение в модель DOM][MDNIntroductionToDOM] .  

<!--
## Appendix: Scroll into view   

This is a continuation of the [Scroll into view](#scroll-into-view) section.  Follow the instructions below to complete the section.  

1.  The `<li>Magritte</li>` node should still be selected in your DOM Tree.  If not, go back to [Scroll into view](#scroll-into-view) and start over.  
1.  Right-click the `<li>Magritte</li>` node and select **Scroll into view**.  Your viewport scrolls back up so that you may see the **Magritte** node.  See [Appendix: Missing options](#appendix-missing-options) if you are not able to see the **Scroll into view** option.
    
    > ##### Figure 19  
    > Scroll into view  
    > ![Scroll into view][ImageScrollView]  
    -->  

## Приложение: отсутствующие параметры   

Многие инструкции, описанные в этом руководстве, помогут вам щелкнуть правой кнопкой мыши узел в дереве DOM и выбрать нужный вариант в контекстном меню.  Если указанный параметр не отображается в контекстном меню, попробуйте щелкнуть правой кнопкой мыши за пределами текста узла.  

> ##### Рис. 20  
> Выбор варианта, если вы не видите все параметры  
> ![Выбор варианта, если вы не видите все параметры][ImageNotSeeingAllOptions]  

<!-- image links -->  

[ImageInspectIcon]: /microsoft-edge/devtools-guide-chromium/media/inspect-icon.msft.png  
[ImageResumeScriptIcon]: /microsoft-edge/devtools-guide-chromium/media/resume-script-icon.msft.png  

[ImageInspectingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-inspect.msft.png "Рисунок 1: Проверка узла"  
[ImageHighlightingMichelangeloNode]: /microsoft-edge/devtools-guide-chromium/media/dom-glitch-dom-examples-michelangelo-elements-highlighted.msft.png "Рисунок 2: выделение узла Michelangelo"  
[ImageInspect]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-select-element-page-inspect.msft.png "Рисунок 3: значок проверки"  
[ImageInspectingRingoNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ringo.msft.png "Рисунок 4: Проверка узла Ringo"  
[ImageInspectingUlNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-navigate-dom-tree-keyboard-ul.msft.png "Рисунок 5: Проверка узла UL"  
[ImageScrollView]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-scroll-into-view-dropdown.msft.png "Рисунок 6: прокрутка представления"  
[ImageHighlightingQuerySearchBar]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-search-nodes-highlight.msft.png "Рисунок 7: выделение запроса в строке поиска"  
[ImageEditingText]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-content.msft.png "Рисунок 8: Редактирование текста"  
[ImageEditingNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-highlighted.msft.png "Рисунок 9: Редактирование узла"  
[ImageAddingStyleAttributeNode]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-attributes-inline-css.msft.png "Рисунок 10: Добавление атрибута стиля на узел"  
[ImageChangingNodeButton]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-edit-node-type-button.msft.png "Рисунок 11. изменение типа узла на кнопку"  
[ImageDraggingNodeTopList]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-reorder-dom-nodes.msft.png "Рисунок 12: перетаскивание узла в верхнюю часть списка"  
[ImageNodeDomTreeAfterHidden]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-hide-a-node.msft.png "Рис. 13: вид узла в дереве DOM после того, как он скрыт"  
[ImageFirstConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-1.msft.png "Рисунок 14: результат первого выражения $0 в консоли"  
[ImageSecondConsole]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-reference-currently-selected-node-console-2.msft.png "Рисунок 15: результат второго выражения $0 в консоли"  
[ImageResultTemp1]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-store-global-variable-console-temp1.msft.png "Рисунок 16: результат выражения temp1"  
[ImageResultCopyJSPath]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-copy-js-path-console-query-selector.msft.png "Рис. 17: результат выражения Copy JS Path"  
[ImageBreakAttributeModification]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-break-attribute-modifications-break-on-attribute-modifications.msft.png "Рисунок 18: прерывание изменений атрибутов"  
[ImageResumeScript]: /microsoft-edge/devtools-guide-chromium/media/dom-break-attribute-modifications-sources-paused-on.msft.png "На рисунке 19 показано, как возобновить выполнение сценария."  
[ImageNotSeeingAllOptions]: /microsoft-edge/devtools-guide-chromium/media/dom-elements-highlighted-right-click-right-side.msft.png "Рисунок 20: где щелкнуть, если вы не видите все параметры"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft Edge \ (Chromium \)"  
[DevToolsCssGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  
[DevToolsShortcutsElements]: /microsoft-edge/devtools-guide-chromium/shortcuts#elements-panel-keyboard-shortcuts "Сочетания клавиш для панели элементов — сочетания клавиш в Microsoft Edge DevTools"  

[GlitchDomExamples]: https://microsoft-edge-chromium-devtools.glitch.me/static/dom "Пример Microsoft EDGE (Chromium) DevTools DOM | Цепь"

[MDNIntroductionToDOM]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model/Introduction "Общие сведения об DOM | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/dom/index) и [Kayce Basques][KayceBasques] \ (технический писатель, хром DevTools & Lighthouse).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
