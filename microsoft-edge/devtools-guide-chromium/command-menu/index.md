---
title: Выполнение команд с помощью командного меню Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 748008b347a3498008748b9c3f9ecc1445c47f12
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601749"
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





# <span data-ttu-id="09dda-103">Выполнение команд с помощью командного меню Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="09dda-103">Run Commands With The Microsoft Edge DevTools Command Menu</span></span>   

  

<span data-ttu-id="09dda-104">Меню команд предоставляет быстрый способ навигации по пользовательскому интерфейсу Microsoft Edge DevTools и выполнения стандартных задач, таких как [Отключение JavaScript][JavascriptDisable].</span><span class="sxs-lookup"><span data-stu-id="09dda-104">The Command Menu provides a fast way to navigate the Microsoft Edge DevTools UI and accomplish common tasks, such as [disabling JavaScript][JavascriptDisable].</span></span>  <span data-ttu-id="09dda-105">Возможно, вы знакомы с аналогичной функцией в коде Visual Studio, которая называется [палитрой команд][VisualStudioCodeUICommandPalette], которая была первоначальной для меню команд.</span><span class="sxs-lookup"><span data-stu-id="09dda-105">You may be familiar with a similar feature in Visual Studio Code called the [Command Palette][VisualStudioCodeUICommandPalette], which was the original inspiration for the Command Menu.</span></span>  

> ##### <span data-ttu-id="09dda-106">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="09dda-106">Figure 1</span></span>  
> <span data-ttu-id="09dda-107">Отключение JavaScript с помощью меню команд</span><span class="sxs-lookup"><span data-stu-id="09dda-107">Using the Command Menu to disable JavaScript</span></span>  
> ![Отключение JavaScript с помощью меню команд][ImageDisableJS]  

## <span data-ttu-id="09dda-109">Открытие меню команд</span><span class="sxs-lookup"><span data-stu-id="09dda-109">Open the Command Menu</span></span>   

<span data-ttu-id="09dda-110">Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="09dda-110">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\).</span></span> <span data-ttu-id="09dda-111">Или нажмите кнопку **Настройка DevTools** `...` и выберите **команду выполнить**.</span><span class="sxs-lookup"><span data-stu-id="09dda-111">Or click **Customize And Control DevTools** `...` and then select **Run Command**.</span></span>  

> ##### <span data-ttu-id="09dda-112">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="09dda-112">Figure 2</span></span>  
> <span data-ttu-id="09dda-113">Команда "выполнить"</span><span class="sxs-lookup"><span data-stu-id="09dda-113">Run Command</span></span>  
> ![Команда "выполнить"][ImageRunCommand]  

## <span data-ttu-id="09dda-115">Просмотр других доступных действий</span><span class="sxs-lookup"><span data-stu-id="09dda-115">See other available actions</span></span>   

<span data-ttu-id="09dda-116">Если вы используете рабочий процесс, описанный в разделе [Открыть меню команд](#open-the-command-menu), откроется меню команд с `>` символом, добавленным к текстовому полю меню команд.</span><span class="sxs-lookup"><span data-stu-id="09dda-116">If you use the workflow outlined in [Open the Command Menu](#open-the-command-menu), the Command Menu opens with a `>` character prepended to the Command Menu text box.</span></span>  

> ##### <span data-ttu-id="09dda-117">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="09dda-117">Figure 3</span></span>  
> <span data-ttu-id="09dda-118">Символ команды</span><span class="sxs-lookup"><span data-stu-id="09dda-118">The command character</span></span>  
> ![Символ команды][ImageCommandCharacter]  

<span data-ttu-id="09dda-120">Удалите `>` символ и введите текст `?` , чтобы просмотреть другие действия, доступные в меню команд.</span><span class="sxs-lookup"><span data-stu-id="09dda-120">Delete the `>` character and type `?` to see other actions that are available from the Command Menu.</span></span>  

> ##### <span data-ttu-id="09dda-121">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="09dda-121">Figure 4</span></span>  
> <span data-ttu-id="09dda-122">Другие доступные действия</span><span class="sxs-lookup"><span data-stu-id="09dda-122">Other available actions</span></span>  
> ![Другие доступные действия][ImageActions]  

 



<!-- image links -->  

[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command-java.msft.png "Рисунок 1: использование командного меню для отключения JavaScript"  
[ImageRunCommand]: /microsoft-edge/devtools-guide-chromium/media/command-menu-options-run-command.msft.png "Рисунок 2: команда "выполнить""  
[ImageCommandCharacter]: /microsoft-edge/devtools-guide-chromium/media/command-menu-run-command.msft.png "Рисунок 3: символ команды"  
[ImageActions]: /microsoft-edge/devtools-guide-chromium/media/command-menu-help.msft.png "Рисунок 4: другие доступные действия"  

<!-- links -->  

[JavascriptDisable]: /microsoft-edge/devtools-guide-chromium/javascript/disable "Отключение JavaScript с помощью Microsoft Edge DevTools"  

[VisualStudioCodeUICommandPalette]: https://code.visualstudio.com/docs/getstarted/userinterface#_command-palette "Палитра команд — пользовательский интерфейс кода Visual Studio"  

> [!NOTE]
> <span data-ttu-id="09dda-130">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="09dda-130">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="09dda-131">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="09dda-131">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="09dda-133">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="09dda-133">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
