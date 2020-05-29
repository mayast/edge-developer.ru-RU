---
title: Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: f0be6243d4780e4ed49428ebaf2b6b37d9da323e
ms.sourcegitcommit: 67ce64f810afdb304844bae0f3918d4e9108dcec
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2020
ms.locfileid: "10601348"
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





# <span data-ttu-id="5e1bb-103">Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)</span><span class="sxs-lookup"><span data-stu-id="5e1bb-103">Change Microsoft Edge DevTools Placement (Undock, Dock To Bottom, Dock To Left)</span></span>   



<span data-ttu-id="5e1bb-104">По умолчанию DevTools закрепляется справа от окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="5e1bb-104">By default DevTools is docked to the right of your viewport.</span></span>  <span data-ttu-id="5e1bb-105">Вы также можете закрепить нижнюю границу, закрепить слева или отстыковать DevTools в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="5e1bb-105">You may also dock to bottom, dock to left, or undock the DevTools to a separate window.</span></span>  

> ##### <span data-ttu-id="5e1bb-106">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="5e1bb-106">Figure 1</span></span>  
> <span data-ttu-id="5e1bb-107">Закрепить слева</span><span class="sxs-lookup"><span data-stu-id="5e1bb-107">Dock To Left</span></span>  
> ![Закрепить слева][ImageDockLeft]  

> ##### <span data-ttu-id="5e1bb-109">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="5e1bb-109">Figure 2</span></span>  
> <span data-ttu-id="5e1bb-110">Закрепить в нижней части экрана</span><span class="sxs-lookup"><span data-stu-id="5e1bb-110">Dock To Bottom</span></span>  
> ![Закрепить в нижней части экрана][ImageDockBottom]  

> ##### <span data-ttu-id="5e1bb-112">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="5e1bb-112">Figure 3</span></span>  
> <span data-ttu-id="5e1bb-113">Браузер в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="5e1bb-113">Browser in separate window</span></span>  
> ![Браузер в отдельном окне][ImageUndockBrowser]  

> ##### <span data-ttu-id="5e1bb-115">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="5e1bb-115">Figure 4</span></span>  
> <span data-ttu-id="5e1bb-116">Незакрепленные DevTools в отдельном окне</span><span class="sxs-lookup"><span data-stu-id="5e1bb-116">Undocked DevTools in separate window</span></span>  
> ![Незакрепленные DevTools в отдельном окне][ImageUndockDevTools]  

## <span data-ttu-id="5e1bb-118">Изменение положения в главном меню</span><span class="sxs-lookup"><span data-stu-id="5e1bb-118">Change placement from the main menu</span></span>   

1.  <span data-ttu-id="5e1bb-119">Нажмите кнопку **Настройка DevTools** `...` и выберите команду **открепить в отдельном окне** , а затем закрепите ![ ][ImageUndockIcon] **на нижней** панели ![ ][ImageBottomIcon] или **закрепите** влево ![ ][ImageLeftIcon] .</span><span class="sxs-lookup"><span data-stu-id="5e1bb-119">Click **Customize And Control DevTools** `...` and select **Undock Into Separate Window** ![Undock][ImageUndockIcon], **Dock To Bottom** ![Dock To Bottom][ImageBottomIcon], or **Dock To Left** ![Dock To Left][ImageLeftIcon].</span></span>  
    
    > ##### <span data-ttu-id="5e1bb-120">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="5e1bb-120">Figure 5</span></span>  
    > <span data-ttu-id="5e1bb-121">Выбор пункта " **открепить в отдельном окне** "</span><span class="sxs-lookup"><span data-stu-id="5e1bb-121">Selecting **Undock Into Separate Window**</span></span>  
    > ![Выбор пункта "Открепить в отдельном окне"][ImageUndockSettings]  
    
## <span data-ttu-id="5e1bb-123">Изменение положения в меню команд</span><span class="sxs-lookup"><span data-stu-id="5e1bb-123">Change placement from the Command Menu</span></span>   

1.  <span data-ttu-id="5e1bb-124">[Открытие меню команд][DevtoolsCommandMenu].</span><span class="sxs-lookup"><span data-stu-id="5e1bb-124">[Open the Command Menu][DevtoolsCommandMenu].</span></span>  
1.  <span data-ttu-id="5e1bb-125">Выполните одну из указанных ниже `Dock To Bottom` команд. `Undock Into Separate Window`</span><span class="sxs-lookup"><span data-stu-id="5e1bb-125">Run one of the following commands: `Dock To Bottom`, `Undock Into Separate Window`.</span></span>  <span data-ttu-id="5e1bb-126">В настоящее время нет команды для закрепления слева, но вы можете получить доступ к ней из [главного меню](#change-placement-from-the-main-menu).</span><span class="sxs-lookup"><span data-stu-id="5e1bb-126">Currently there is no command for docking to left, but you may access it from the [main menu](#change-placement-from-the-main-menu).</span></span>  
    
    > ##### <span data-ttu-id="5e1bb-127">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="5e1bb-127">Figure 6</span></span>  
    > <span data-ttu-id="5e1bb-128">Команда "отменить закрепление"</span><span class="sxs-lookup"><span data-stu-id="5e1bb-128">The undock command</span></span>  
    > ![Команда "отменить закрепление"][ImageUndockCommand]  

 



<!-- image links -->  

[ImageUndockIcon]: /microsoft-edge/devtools-guide-chromium/media/undock-icon.msft.png  
[ImageBottomIcon]: /microsoft-edge/devtools-guide-chromium/media/bottom-icon.msft.png  
[ImageLeftIcon]: /microsoft-edge/devtools-guide-chromium/media/left-icon.msft.png  

[ImageDockLeft]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-right-docked.msft.png "Рисунок 1: закрепление влево"  
[ImageDockBottom]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-bottom-docked.msft.png "Рисунок 2: закрепить в нижней части экрана"  
[ImageUndockBrowser]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-browser.msft.png "Рисунок 3: браузер в отдельном окне"  
[ImageUndockDevTools]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight-devtools.msft.png "Рисунок 4: незакрепленный DevTools в отдельном окне"  
[ImageUndockSettings]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-options-dock-side-highlight.msft.png "Рисунок 5: выбор пункта "Открепить в отдельном окне""  
[ImageUndockCommand]: /microsoft-edge/devtools-guide-chromium/media/customize-elements-styles-command-menu-undo.msft.png "Рисунок 6: команда "Открепить""  

<!-- links -->  

[DevtoolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="5e1bb-137">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5e1bb-137">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5e1bb-138">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/customize/placement) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5e1bb-138">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/customize/placement) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5e1bb-140">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5e1bb-140">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
