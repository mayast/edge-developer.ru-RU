---
title: Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/25/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: ebb8ae15a6888ce2227ec1dc18f307b03ddf9319
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601721"
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





# <span data-ttu-id="fe6aa-103">Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="fe6aa-103">Find Unused JavaScript And CSS Code With The Coverage Tab In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="fe6aa-104">Вкладка "покрытие" в Microsoft Edge DevTools помогает найти неиспользуемый код JavaScript и CSS.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-104">The Coverage tab in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="fe6aa-105">Удаление неиспользуемого кода может ускорить загрузку страницы и сохранить мобильные данные мобильных пользователей.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-105">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

> ##### <span data-ttu-id="fe6aa-106">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="fe6aa-106">Figure 1</span></span>  
> <span data-ttu-id="fe6aa-107">Анализ объема протестированного кода</span><span class="sxs-lookup"><span data-stu-id="fe6aa-107">Analyzing code coverage</span></span>  
> ![Анализ объема протестированного кода][ImageExample]  

> [!WARNING]
> <span data-ttu-id="fe6aa-109">Найти неиспользуемый код довольно просто.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-109">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="fe6aa-110">Но рефакторинг базы кода таким образом, чтобы каждая страница расгрузка только JavaScript и CSS может быть сложной.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-110">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="fe6aa-111">Это руководство не содержит сведения о том, как оптимизировать базу кода, чтобы избежать неиспользуемого кода, поскольку эти данные фактов сильно зависят от вашего стека технологий.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-111">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <span data-ttu-id="fe6aa-112">Обзор</span><span class="sxs-lookup"><span data-stu-id="fe6aa-112">Overview</span></span>   

<span data-ttu-id="fe6aa-113">При отправке неиспользуемого сценария JavaScript или CSS часто возникают проблемы с веб-разработкой.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-113">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="fe6aa-114">Например, предположим, что вы хотите использовать [компонент кнопки начальной загрузки][BootstrapButtons] на странице.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-114">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="fe6aa-115">Чтобы использовать компонент Button, необходимо добавить ссылку на таблицу параметров начальной загрузки в HTML-коде, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-115">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="fe6aa-116">Эта таблица стилей не только содержит код для компонента Button.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-116">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="fe6aa-117">Она включает CSS для **всех** компонентов начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-117">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="fe6aa-118">Но вы не используете никакие другие компоненты начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-118">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="fe6aa-119">Таким образом, страница загружается с ненужным набором CSS.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-119">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="fe6aa-120">Эта дополнительная таблица CSS является проблемой по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-120">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="fe6aa-121">Дополнительный код замедляет загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-121">The extra code slows down your page load.</span></span>  <!--See [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="fe6aa-122">Если пользователь получает доступ к странице на мобильном устройстве, в дополнительном коде используются данные сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-122">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  

<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <span data-ttu-id="fe6aa-123">Открытие вкладки "покрытие"</span><span class="sxs-lookup"><span data-stu-id="fe6aa-123">Open the Coverage tab</span></span>   

1.  <span data-ttu-id="fe6aa-124">[Открытие меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="fe6aa-124">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="fe6aa-125">Начните вводить текст `coverage` , выберите команду **Показать покрытие** , а затем нажмите `Enter` , чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-125">Start typing `coverage`, select the **Show Coverage** command, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="fe6aa-126">В **денежном ящике**откроется вкладка **покрытие** .</span><span class="sxs-lookup"><span data-stu-id="fe6aa-126">The **Coverage** tab opens in the **Drawer**.</span></span>  

    > ##### <span data-ttu-id="fe6aa-127">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="fe6aa-127">Figure 2</span></span>  
    > <span data-ttu-id="fe6aa-128">Вкладка " **покрытие** "</span><span class="sxs-lookup"><span data-stu-id="fe6aa-128">The **Coverage** tab</span></span>  
    > ![Вкладка "покрытие"][ImageCoverage]  

## <span data-ttu-id="fe6aa-130">Запись покрытия кода</span><span class="sxs-lookup"><span data-stu-id="fe6aa-130">Record code coverage</span></span>   

1.  <span data-ttu-id="fe6aa-131">На вкладке **покрытие** нажмите одну из указанных ниже кнопок.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-131">Click one of the following buttons in the **Coverage** tab:</span></span>  
    *   <span data-ttu-id="fe6aa-132">Нажмите кнопку **Запуск инструментирования и перезагрузка страницы** , ![ ][ImageReloadIcon] чтобы просмотреть код, необходимый для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-132">Click **Start Instrumenting Coverage And Reload Page** ![Start Instrumenting Coverage And Reload Page][ImageReloadIcon] if you want to see what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="fe6aa-133">**Instrument Coverage** ![ ][ImageRecordIcon] Если вы хотите узнать, какой код используется после взаимодействия со страницей, щелкните покрытие инструментированного покрытия.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-133">Click **Instrument Coverage** ![Instrument Coverage][ImageRecordIcon] if you want to see what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="fe6aa-134">Нажмите кнопку **остановить покрытие и выводит результаты** ![ остановить инструментирование и показать результаты, ][ImageStopIcon] когда необходимо остановить запись покрытия кода.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-134">Click **Stop Instrumenting Coverage And Show Results** ![Stop Instrumenting Coverage And Show Results][ImageStopIcon] when you want to stop recording code coverage.</span></span>  

## <span data-ttu-id="fe6aa-135">Анализ объема протестированного кода</span><span class="sxs-lookup"><span data-stu-id="fe6aa-135">Analyze code coverage</span></span>   

<span data-ttu-id="fe6aa-136">В таблице на вкладке **покрытие** показано, какие ресурсы были проанализированы, и сколько кода используется в каждом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-136">The table in the **Coverage** tab shows you what resources were analyzed, and how much code is used within each resource.</span></span> <span data-ttu-id="fe6aa-137">Щелкните строку, чтобы открыть ресурс на панели « **источники** » и просмотреть разбиение по строкам используемого кода и неиспользуемый код.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-137">Click a row to open that resource in the **Sources** panel and see a line-by-line breakdown of used code and unused code.</span></span>  

> ##### <span data-ttu-id="fe6aa-138">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="fe6aa-138">Figure 3</span></span>  
> <span data-ttu-id="fe6aa-139">Отчет о покрытии кода</span><span class="sxs-lookup"><span data-stu-id="fe6aa-139">A code coverage report</span></span>  
> ![Отчет о покрытии кода][ImageExample]  

*   <span data-ttu-id="fe6aa-141">Столбец **URL** — это URL-адрес анализируемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-141">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="fe6aa-142">Столбец **Type (тип** ) показывает, содержит ли ресурс CSS, JavaScript или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-142">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="fe6aa-143">Столбец **Total Bytes** — это общий размер ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-143">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="fe6aa-144">Столбец **неиспользованных байтов** — это количество байтов, которые не использовались.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-144">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="fe6aa-145">Последний безымянный столбец — это визуализация общего числа столбцов в **байтах** и **неиспользуемых байтах** .</span><span class="sxs-lookup"><span data-stu-id="fe6aa-145">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="fe6aa-146">Красная область на панели содержит неиспользуемые байты.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-146">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="fe6aa-147">Зеленый раздел используется в байтах.</span><span class="sxs-lookup"><span data-stu-id="fe6aa-147">The green section is used bytes.</span></span>  

 



<!-- image links -->  

[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  
[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  
[ImageStopIcon]: /microsoft-edge/devtools-guide-chromium/media/stop-icon.msft.png  

[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage.msft.png "Рисунок 1: анализ объема протестированного кода"  
[ImageCoverage]: /microsoft-edge/devtools-guide-chromium/media/coverage-console-drawer-coverage-empty.msft.png "Рисунок 2: вкладка "покрытие""  
[ImageExample]: /microsoft-edge/devtools-guide-chromium/media/coverage-sources-resource-drawer-coverage-selected.msft.png "Рисунок 3: отчет о покрытии кода"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Кнопки для загрузки"  

> [!NOTE]
> <span data-ttu-id="fe6aa-153">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fe6aa-153">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="fe6aa-154">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/coverage/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="fe6aa-154">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="fe6aa-156">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="fe6aa-156">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
