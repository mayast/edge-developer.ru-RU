---
title: Обзор консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 6062afb929a5d763c095d4915a2960993bc5ab4c
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601790"
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





# Обзор консоли   

  

На этой странице объясняется, как консоль Microsoft Edge DevTools упрощает разработку веб-страниц.  У консоли есть 2 основного использования: [Просмотр сообщений, записанных в журнал](#viewing-logged-messages) , и [запуск JavaScript](#running-javascript).  

## Просмотр записанных сообщений   

Веб-разработчики часто записывает сообщения на консоль, чтобы убедиться в том, что их JavaScript работает должным образом.  Чтобы записать сообщение в журнал, вставьте выражение, например, `console.log('Hello, Console!')` в сценарий JavaScript.  Когда браузер запускает JavaScript и видит такое выражение, оно заносит сообщение в консоль.  Например, предположим, что вы пишете HTML и JavaScript для страницы:  

```html
<!doctype html>
<html>
  <head>
    <title>Console Demo</title>
  </head>
  <body>
    <h1>Hello, World!</h1>
    <script>
      console.log('Loading!');
      const h1 = document.querySelector('h1');
      console.log(h1.textContent);
      console.assert(document.querySelector('h2'), 'h2 not found!');
      const artists = [
        {
          first: 'René',
          last: 'Magritte'
        },
        {
          first: 'Chaim',
          last: 'Soutine'
        },
        {
          first: 'Henri',
          last: 'Matisse'
        }
      ];
      console.table(artists);
      setTimeout(() => {
        h1.textContent = 'Hello, Console!';
        console.log(h1.textContent);
      }, 3000);
    </script>
  </body>
</html>
```  

[На рисунке 1](#figure-1) показано, как выглядит консоль после загрузки страницы и ожидания 3 секунды.  Попробуйте узнать, какие строки кода привели к тому, что браузер зарегистрирует сообщения.  

> ##### Рис. 1  
> Панель консоли  
> ![Панель консоли][ImageConsole]  

Веб-разработчики могут регистрировать сообщения по двум основным причинам.  

*   Убедитесь в том, что код выполняется в нужном порядке.  
*   Проверка значений переменных в определенный момент времени.  

В разделе Начало работы [с сообщениями для ведения журнала][DevtoolsConsoleLoggingMessages] вы можете получить практический опыт по ведению журнала.  Полный список методов можно найти в [справочнике по API консоли][DevToolsConsoleAPI] `console` .  Основным различием между методами является способ отображения данных в журнале.  

## Выполнение JavaScript   

Консоль также является [REPL][WikiREPLoop].  Вы можете запустить JavaScript на консоли для взаимодействия с проверяемой страницей.  Например, [на рисунке 2](#figure-2) показана консоль рядом с домашней страницей DevTools, а [на рисунке 3](#figure-3) показана эта же страница после использования консоли для изменения верхнего заголовка страницы.  

> ##### Рисунок 2  
> Панель консоли рядом с домашней страницей DevTools  
> ![Панель консоли рядом с домашней страницей DevTools][ImageConsoleOverview]  

> ##### Рисунок3  
> Использование консоли для изменения верхнего заголовка страницы  
> ![Использование консоли для изменения верхнего заголовка страницы][ImageConsoleChangeTitle]  

Изменение страницы на консоли возможно из-за того, что консоль имеет полный доступ к [окну][MDNWindow] страницы.  В DevTools есть несколько удобных функций, которые облегчают изучение страницы.  Например, предположим, что ваш сценарий JavaScript содержит функцию с именем `hideModal` .  Выполнение `debug(hideModal)` программы приостанавливает код на первой строке при `hideModal` следующем запуске.  Полный список служебных функций можно найти в [справочнике API для консольных утилит][DevtoolsConsoleUtilitiesDebug] .  

При запуске JavaScript вам не нужно взаимодействовать со страницей.  Вы можете использовать консоль, чтобы попробовать новый код, не связанный со страницей.  Например, предположим, что вы только что узнали о встроенном методе [Map ()][MDNMap] для массивов JavaScript () и хотите поэкспериментировать с ним.  
**Консоль** — это хорошее место для повторения функции.  

Чтобы получить практический опыт выполнения JavaScript на консоли, ознакомьтесь [со статьей начало работы с JavaScript][ImageConsoleChangeTitle] .  

   

  

<!-- image links -->  

[ImageConsole]: /microsoft-edge/devtools-guide-chromium/media/console-console-demo.msft.png "Рисунок 1: панель консоли"  
[ImageConsoleChangeTitle]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-h1-changed.msft.png "Рисунок 3: использование консоли для изменения верхнего заголовка страницы"  
[ImageConsoleOverview]: /microsoft-edge/devtools-guide-chromium/media/devtools-console-empty.msft.png "Рисунок 2: панель консоли рядом с домашней страницей DevTools"  

<!-- links -->  

[DevToolsConsoleAPI]: /microsoft-edge/devtools-guide-chromium/console/api "Справочник по API консоли"  
[DevtoolsConsoleLoggingMessages]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с сообщениями журнала на консоли"  
[DevtoolsConsoleRunningJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Начало работы с JavaScript на консоли"  
[DevtoolsConsoleUtilitiesDebug]: /microsoft-edge/devtools-guide-chromium/console/utilities#debug "Справочник по API служебных программ для консоли отладки"  

[MDNMap]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/map "Array. prototype. Map () | MDN"  
[MDNWindow]: https://developer.mozilla.org/docs/Web/API/Window "Окно | MDN"  

[WikiREPLoop]: https://en.wikipedia.org/wiki/Read%E2%80%93eval%E2%80%93print_loop "Read – eval — цикл печати — Википедии"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
