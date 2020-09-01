---
title: Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1c03140199b26bca39e69cdfbe33cd1c524257fe
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10981878"
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





# <span data-ttu-id="f0b84-103">Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f0b84-103">Find Unused JavaScript And CSS Code With The Coverage Tab In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="f0b84-104">Вкладка "покрытие" в Microsoft Edge DevTools помогает найти неиспользуемый код JavaScript и CSS.</span><span class="sxs-lookup"><span data-stu-id="f0b84-104">The Coverage tab in Microsoft Edge DevTools helps you find unused JavaScript and CSS code.</span></span>  <span data-ttu-id="f0b84-105">Удаление неиспользуемого кода может ускорить загрузку страницы и сохранить мобильные данные мобильных пользователей.</span><span class="sxs-lookup"><span data-stu-id="f0b84-105">Removing unused code may speed up your page load and save your mobile users cellular data.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage.msft.png" alt-text="Анализ объема протестированного кода" lightbox="../media/coverage-sources-resource-drawer-coverage.msft.png":::
   <span data-ttu-id="f0b84-107">Анализ объема протестированного кода</span><span class="sxs-lookup"><span data-stu-id="f0b84-107">Analyzing code coverage</span></span>  
:::image-end:::  

> [!WARNING]
> <span data-ttu-id="f0b84-108">Найти неиспользуемый код довольно просто.</span><span class="sxs-lookup"><span data-stu-id="f0b84-108">Finding unused code is relatively easy.</span></span>  <span data-ttu-id="f0b84-109">Но рефакторинг базы кода таким образом, чтобы каждая страница расгрузка только JavaScript и CSS может быть сложной.</span><span class="sxs-lookup"><span data-stu-id="f0b84-109">But refactoring a codebase so that each page only ships the JavaScript and CSS that it needs may be difficult.</span></span>  <span data-ttu-id="f0b84-110">Это руководство не содержит сведения о том, как оптимизировать базу кода, чтобы избежать неиспользуемого кода, поскольку эти данные фактов сильно зависят от вашего стека технологий.</span><span class="sxs-lookup"><span data-stu-id="f0b84-110">This guide does not cover how to refactor a codebase to avoid unused code because these refactors depend highly on your technology stack.</span></span>  

## <span data-ttu-id="f0b84-111">Обзор</span><span class="sxs-lookup"><span data-stu-id="f0b84-111">Overview</span></span>   

<span data-ttu-id="f0b84-112">При отправке неиспользуемого сценария JavaScript или CSS часто возникают проблемы с веб-разработкой.</span><span class="sxs-lookup"><span data-stu-id="f0b84-112">Shipping unused JavaScript or CSS is a common problem in web development.</span></span>  <span data-ttu-id="f0b84-113">Например, предположим, что вы хотите использовать [компонент кнопки начальной загрузки][BootstrapButtons] на странице.</span><span class="sxs-lookup"><span data-stu-id="f0b84-113">For example, suppose that you want to use [Bootstrap button component][BootstrapButtons] on your page.</span></span>  <span data-ttu-id="f0b84-114">Чтобы использовать компонент Button, необходимо добавить ссылку на таблицу параметров начальной загрузки в HTML-коде, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="f0b84-114">To use the button component you need to add a link to the Bootstrap stylesheet in your HTML, like this:</span></span>  

```html
...
<head>
    ...
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">
    ...
</head>
...
```  

<span data-ttu-id="f0b84-115">Эта таблица стилей не только содержит код для компонента Button.</span><span class="sxs-lookup"><span data-stu-id="f0b84-115">This stylesheet does not just include the code for the button component.</span></span>  <span data-ttu-id="f0b84-116">Она включает CSS для **всех** компонентов начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="f0b84-116">It contains the CSS for **all** of the Bootstrap components.</span></span>  <span data-ttu-id="f0b84-117">Но вы не используете никакие другие компоненты начальной загрузки.</span><span class="sxs-lookup"><span data-stu-id="f0b84-117">But you are not using any of the other Bootstrap components.</span></span>  <span data-ttu-id="f0b84-118">Таким образом, страница загружается с ненужным набором CSS.</span><span class="sxs-lookup"><span data-stu-id="f0b84-118">So your page is downloading a bunch of CSS that it does not need.</span></span>  <span data-ttu-id="f0b84-119">Эта дополнительная таблица CSS является проблемой по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="f0b84-119">This extra CSS is a problem for the following reasons.</span></span>  

*   <span data-ttu-id="f0b84-120">Дополнительный код замедляет загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="f0b84-120">The extra code slows down your page load.</span></span>  <!--See [Render-Blocking CSS][render].  -->  
*   <span data-ttu-id="f0b84-121">Если пользователь получает доступ к странице на мобильном устройстве, в дополнительном коде используются данные сотовой связи.</span><span class="sxs-lookup"><span data-stu-id="f0b84-121">If a user accesses the page on a mobile device, the extra code uses up their cellular data.</span></span>  
    
<!--[render]: /web/fundamentals/performance/critical-rendering-path/render-blocking-css  -->  

## <span data-ttu-id="f0b84-122">Открытие вкладки "покрытие"</span><span class="sxs-lookup"><span data-stu-id="f0b84-122">Open the Coverage tab</span></span>   

1.  <span data-ttu-id="f0b84-123">[Открытие меню команд][DevToolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="f0b84-123">[Open the Command Menu][DevToolsCommandMenu].</span></span>  
1.  <span data-ttu-id="f0b84-124">Начните вводить текст `coverage` , выберите команду **Показать покрытие** , а затем нажмите `Enter` , чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="f0b84-124">Start typing `coverage`, select the **Show Coverage** command, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="f0b84-125">В **денежном ящике**откроется вкладка **покрытие** .</span><span class="sxs-lookup"><span data-stu-id="f0b84-125">The **Coverage** tab opens in the **Drawer**.</span></span>  

    :::image type="complex" source="../media/coverage-console-drawer-coverage-empty.msft.png" alt-text="Вкладка "покрытие"" lightbox="../media/coverage-console-drawer-coverage-empty.msft.png":::
       <span data-ttu-id="f0b84-127">Вкладка " **покрытие** "</span><span class="sxs-lookup"><span data-stu-id="f0b84-127">The **Coverage** tab</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="f0b84-128">Запись покрытия кода</span><span class="sxs-lookup"><span data-stu-id="f0b84-128">Record code coverage</span></span>   

1.  <span data-ttu-id="f0b84-129">На вкладке **покрытие** нажмите одну из указанных ниже кнопок.</span><span class="sxs-lookup"><span data-stu-id="f0b84-129">Click one of the following buttons in the **Coverage** tab:</span></span>  
    *   <span data-ttu-id="f0b84-130">Нажмите кнопку **запустить инструментирование покрытия и перезагрузите страницу** \ ( ![ Запуск инструментированного покрытия и перезагрузка страницы ][ImageReloadIcon] \), если вы хотите узнать, какой код требуется для загрузки страницы.</span><span class="sxs-lookup"><span data-stu-id="f0b84-130">Click **Start Instrumenting Coverage And Reload Page** \(![Start Instrumenting Coverage And Reload Page][ImageReloadIcon]\) if you want to see what code is needed to load the page.</span></span>  
    *   <span data-ttu-id="f0b84-131">**Instrument Coverage** ![ ][ImageRecordIcon] Если вы хотите узнать, какой код используется после взаимодействия со страницей, нажмите кнопку покрытие на инструментальных средствах (покрытие инструментов).</span><span class="sxs-lookup"><span data-stu-id="f0b84-131">Click **Instrument Coverage** \(![Instrument Coverage][ImageRecordIcon]\) if you want to see what code is used after interacting with the page.</span></span>  
1.  <span data-ttu-id="f0b84-132">Чтобы остановить запись, нажмите кнопку **остановить покрытие и показать результаты, а** затем — ![ остановить покрытие инструментирования и показать результаты ][ImageStopIcon] .</span><span class="sxs-lookup"><span data-stu-id="f0b84-132">Click **Stop Instrumenting Coverage And Show Results** \(![Stop Instrumenting Coverage And Show Results][ImageStopIcon]\) when you want to stop recording code coverage.</span></span>  
    
## <span data-ttu-id="f0b84-133">Анализ объема протестированного кода</span><span class="sxs-lookup"><span data-stu-id="f0b84-133">Analyze code coverage</span></span>   

<span data-ttu-id="f0b84-134">В таблице на вкладке **покрытие** показано, какие ресурсы были проанализированы, и сколько кода используется в каждом ресурсе.</span><span class="sxs-lookup"><span data-stu-id="f0b84-134">The table in the **Coverage** tab shows you what resources were analyzed, and how much code is used within each resource.</span></span>  <span data-ttu-id="f0b84-135">Щелкните строку, чтобы открыть ресурс на панели « **источники** » и просмотреть разбиение по строкам используемого кода и неиспользуемый код.</span><span class="sxs-lookup"><span data-stu-id="f0b84-135">Click a row to open that resource in the **Sources** panel and see a line-by-line breakdown of used code and unused code.</span></span>  

:::image type="complex" source="../media/coverage-sources-resource-drawer-coverage-selected.msft.png" alt-text="Отчет о покрытии кода" lightbox="../media/coverage-sources-resource-drawer-coverage-selected.msft.png":::
   <span data-ttu-id="f0b84-137">Отчет о покрытии кода</span><span class="sxs-lookup"><span data-stu-id="f0b84-137">A code coverage report</span></span>  
:::image-end:::  

*   <span data-ttu-id="f0b84-138">Столбец **URL** — это URL-адрес анализируемого ресурса.</span><span class="sxs-lookup"><span data-stu-id="f0b84-138">The **URL** column is the URL of the resource that was analyzed.</span></span>  
*   <span data-ttu-id="f0b84-139">Столбец **Type (тип** ) показывает, содержит ли ресурс CSS, JavaScript или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="f0b84-139">The **Type** column says whether the resource contains CSS, JavaScript, or both.</span></span>  
*   <span data-ttu-id="f0b84-140">Столбец **Total Bytes** — это общий размер ресурса в байтах.</span><span class="sxs-lookup"><span data-stu-id="f0b84-140">The **Total Bytes** column is the total size of the resource in bytes.</span></span>  
*   <span data-ttu-id="f0b84-141">Столбец **неиспользованных байтов** — это количество байтов, которые не использовались.</span><span class="sxs-lookup"><span data-stu-id="f0b84-141">The **Unused Bytes** column is the number of bytes that were not used.</span></span>  
*   <span data-ttu-id="f0b84-142">Последний безымянный столбец — это визуализация общего числа столбцов в **байтах** и **неиспользуемых байтах** .</span><span class="sxs-lookup"><span data-stu-id="f0b84-142">The last, unnamed column is a visualization of the **Total Bytes** and **Unused Bytes** columns.</span></span>  <span data-ttu-id="f0b84-143">Красная область на панели содержит неиспользуемые байты.</span><span class="sxs-lookup"><span data-stu-id="f0b84-143">The red section of the bar is unused bytes.</span></span>  <span data-ttu-id="f0b84-144">Зеленый раздел используется в байтах.</span><span class="sxs-lookup"><span data-stu-id="f0b84-144">The green section is used bytes.</span></span>  
    
<!--  
 


-->  

<!-- image links -->  

[ImageReloadIcon]: ../media/reload-icon.msft.png  
[ImageRecordIcon]: ../media/record-icon.msft.png  
[ImageStopIcon]: ../media/stop-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  

[BootstrapButtons]: https://getbootstrap.com/docs/4.3/components/buttons "Кнопки для загрузки"  

> [!NOTE]
> <span data-ttu-id="f0b84-147">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f0b84-147">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f0b84-148">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/coverage/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f0b84-148">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/coverage/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f0b84-150">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f0b84-150">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
