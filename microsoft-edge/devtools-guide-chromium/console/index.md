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





# <span data-ttu-id="ab0ae-103">Обзор консоли</span><span class="sxs-lookup"><span data-stu-id="ab0ae-103">Console Overview</span></span>   

  

<span data-ttu-id="ab0ae-104">На этой странице объясняется, как консоль Microsoft Edge DevTools упрощает разработку веб-страниц.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-104">This page explains how the Microsoft Edge DevTools Console makes it easier to develop web pages.</span></span>  <span data-ttu-id="ab0ae-105">У консоли есть 2 основного использования: [Просмотр сообщений, записанных в журнал](#viewing-logged-messages) , и [запуск JavaScript](#running-javascript).</span><span class="sxs-lookup"><span data-stu-id="ab0ae-105">The Console has 2 main uses: [viewing logged messages](#viewing-logged-messages) and [running JavaScript](#running-javascript).</span></span>  

## <span data-ttu-id="ab0ae-106">Просмотр записанных сообщений</span><span class="sxs-lookup"><span data-stu-id="ab0ae-106">Viewing logged messages</span></span>   

<span data-ttu-id="ab0ae-107">Веб-разработчики часто записывает сообщения на консоль, чтобы убедиться в том, что их JavaScript работает должным образом.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-107">Web developers often log messages to the Console to make sure that their JavaScript is working as expected.</span></span>  <span data-ttu-id="ab0ae-108">Чтобы записать сообщение в журнал, вставьте выражение, например, `console.log('Hello, Console!')` в сценарий JavaScript.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-108">To log a message, you insert an expression like `console.log('Hello, Console!')` into your JavaScript.</span></span>  <span data-ttu-id="ab0ae-109">Когда браузер запускает JavaScript и видит такое выражение, оно заносит сообщение в консоль.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-109">When the browser runs your JavaScript and sees an expression like that, it logs the message to the Console.</span></span>  <span data-ttu-id="ab0ae-110">Например, предположим, что вы пишете HTML и JavaScript для страницы:</span><span class="sxs-lookup"><span data-stu-id="ab0ae-110">For example, suppose that you are writing the HTML and JavaScript for a page:</span></span>  

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

<span data-ttu-id="ab0ae-111">[На рисунке 1](#figure-1) показано, как выглядит консоль после загрузки страницы и ожидания 3 секунды.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-111">[Figure 1](#figure-1) shows what the Console looks like after loading the page and waiting 3 seconds.</span></span>  <span data-ttu-id="ab0ae-112">Попробуйте узнать, какие строки кода привели к тому, что браузер зарегистрирует сообщения.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-112">Try to figure out which lines of code caused the browser to log the messages.</span></span>  

> ##### <span data-ttu-id="ab0ae-113">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="ab0ae-113">Figure 1</span></span>  
> <span data-ttu-id="ab0ae-114">Панель консоли</span><span class="sxs-lookup"><span data-stu-id="ab0ae-114">The Console panel</span></span>  
> ![Панель консоли][ImageConsole]  

<span data-ttu-id="ab0ae-116">Веб-разработчики могут регистрировать сообщения по двум основным причинам.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-116">Web developers log messages for 2 general reasons:</span></span>  

*   <span data-ttu-id="ab0ae-117">Убедитесь в том, что код выполняется в нужном порядке.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-117">Making sure that code is running in the right order.</span></span>  
*   <span data-ttu-id="ab0ae-118">Проверка значений переменных в определенный момент времени.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-118">Inspecting the values of variables at a certain moment in time.</span></span>  

<span data-ttu-id="ab0ae-119">В разделе Начало работы [с сообщениями для ведения журнала][DevtoolsConsoleLoggingMessages] вы можете получить практический опыт по ведению журнала.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-119">See [Get Started With Logging Messages][DevtoolsConsoleLoggingMessages] to get hands-on experience with logging.</span></span>  <span data-ttu-id="ab0ae-120">Полный список методов можно найти в [справочнике по API консоли][DevToolsConsoleAPI] `console` .</span><span class="sxs-lookup"><span data-stu-id="ab0ae-120">See the [Console API Reference][DevToolsConsoleAPI] to browse the full list of `console` methods.</span></span>  <span data-ttu-id="ab0ae-121">Основным различием между методами является способ отображения данных в журнале.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-121">The main difference between the methods is how the data being logged is displayed.</span></span>  

## <span data-ttu-id="ab0ae-122">Выполнение JavaScript</span><span class="sxs-lookup"><span data-stu-id="ab0ae-122">Running JavaScript</span></span>   

<span data-ttu-id="ab0ae-123">Консоль также является [REPL][WikiREPLoop].</span><span class="sxs-lookup"><span data-stu-id="ab0ae-123">The Console is also a [REPL][WikiREPLoop].</span></span>  <span data-ttu-id="ab0ae-124">Вы можете запустить JavaScript на консоли для взаимодействия с проверяемой страницей.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-124">You may run JavaScript in the Console to interact with the page being inspected.</span></span>  <span data-ttu-id="ab0ae-125">Например, [на рисунке 2](#figure-2) показана консоль рядом с домашней страницей DevTools, а [на рисунке 3](#figure-3) показана эта же страница после использования консоли для изменения верхнего заголовка страницы.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-125">For example, [Figure 2](#figure-2) shows the Console next to the DevTools homepage, and [Figure 3](#figure-3) shows that same page after using the Console to change the top heading of the page.</span></span>  

> ##### <span data-ttu-id="ab0ae-126">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="ab0ae-126">Figure 2</span></span>  
> <span data-ttu-id="ab0ae-127">Панель консоли рядом с домашней страницей DevTools</span><span class="sxs-lookup"><span data-stu-id="ab0ae-127">The Console panel next to the DevTools homepage</span></span>  
> ![Панель консоли рядом с домашней страницей DevTools][ImageConsoleOverview]  

> ##### <span data-ttu-id="ab0ae-129">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="ab0ae-129">Figure 3</span></span>  
> <span data-ttu-id="ab0ae-130">Использование консоли для изменения верхнего заголовка страницы</span><span class="sxs-lookup"><span data-stu-id="ab0ae-130">Using the Console to change the top heading of the page</span></span>  
> ![Использование консоли для изменения верхнего заголовка страницы][ImageConsoleChangeTitle]  

<span data-ttu-id="ab0ae-132">Изменение страницы на консоли возможно из-за того, что консоль имеет полный доступ к [окну][MDNWindow] страницы.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-132">Modifying the page from the Console is possible because the Console has full access to the [window][MDNWindow] of the page.</span></span>  <span data-ttu-id="ab0ae-133">В DevTools есть несколько удобных функций, которые облегчают изучение страницы.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-133">DevTools has a few convenience functions that make it easier to inspect a page.</span></span>  <span data-ttu-id="ab0ae-134">Например, предположим, что ваш сценарий JavaScript содержит функцию с именем `hideModal` .</span><span class="sxs-lookup"><span data-stu-id="ab0ae-134">For example, suppose that your JavaScript contains a function called `hideModal`.</span></span>  <span data-ttu-id="ab0ae-135">Выполнение `debug(hideModal)` программы приостанавливает код на первой строке при `hideModal` следующем запуске.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-135">Running `debug(hideModal)` pauses your code on the first line of `hideModal` the next time that you run it.</span></span>  <span data-ttu-id="ab0ae-136">Полный список служебных функций можно найти в [справочнике API для консольных утилит][DevtoolsConsoleUtilitiesDebug] .</span><span class="sxs-lookup"><span data-stu-id="ab0ae-136">See [Console Utilities API Reference][DevtoolsConsoleUtilitiesDebug] to see the full list of utility functions.</span></span>  

<span data-ttu-id="ab0ae-137">При запуске JavaScript вам не нужно взаимодействовать со страницей.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-137">When you run JavaScript you do not have to interact with the page.</span></span>  <span data-ttu-id="ab0ae-138">Вы можете использовать консоль, чтобы попробовать новый код, не связанный со страницей.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-138">You may use the Console to try out new code unrelated to the page.</span></span>  <span data-ttu-id="ab0ae-139">Например, предположим, что вы только что узнали о встроенном методе [Map ()][MDNMap] для массивов JavaScript () и хотите поэкспериментировать с ним.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-139">For example, suppose you just learned about the built-in JavaScript Array [map()][MDNMap] method, and you want to experiment with it.</span></span>  
<span data-ttu-id="ab0ae-140">**Консоль** — это хорошее место для повторения функции.</span><span class="sxs-lookup"><span data-stu-id="ab0ae-140">The **Console** is a good place to try out the function.</span></span>  

<span data-ttu-id="ab0ae-141">Чтобы получить практический опыт выполнения JavaScript на консоли, ознакомьтесь [со статьей начало работы с JavaScript][ImageConsoleChangeTitle] .</span><span class="sxs-lookup"><span data-stu-id="ab0ae-141">See [Get Started With Running JavaScript][ImageConsoleChangeTitle] to get hands-on experience with running JavaScript in the Console.</span></span>  

   

  

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
> <span data-ttu-id="ab0ae-152">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ab0ae-152">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ab0ae-153">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ab0ae-153">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ab0ae-155">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ab0ae-155">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
