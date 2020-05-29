---
title: Переопределение строки агента пользователя из Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 376e1550d0dc31f3b47b6badd6970076a8c13f91
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607309"
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





# <span data-ttu-id="ca7f0-103">Переопределение строки агента пользователя из Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="ca7f0-103">Override The User Agent String From Microsoft Edge DevTools</span></span>   



<span data-ttu-id="ca7f0-104">Чтобы переопределить строку [агента пользователя][MDNUserAgent] из Microsoft Edge DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="ca7f0-104">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="ca7f0-105">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="ca7f0-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="ca7f0-106">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="ca7f0-106">Figure 1</span></span>  
    > <span data-ttu-id="ca7f0-107">Меню команд</span><span class="sxs-lookup"><span data-stu-id="ca7f0-107">The Command Menu</span></span>  
    > ![Меню команд][ImageCommandMenu]  
    
1.  <span data-ttu-id="ca7f0-109">Введите и `network conditions` выберите **Показывать условия сети**, а затем `Enter` откройте вкладку **условия сети** .</span><span class="sxs-lookup"><span data-stu-id="ca7f0-109">Type `network conditions`, select **Show Network conditions**, and press `Enter` to open the **Network conditions** tab.</span></span>  
1.  <span data-ttu-id="ca7f0-110">В разделе **Агент пользователя** отключите флажок **выбрать автоматически** .</span><span class="sxs-lookup"><span data-stu-id="ca7f0-110">In the **User agent** section, disable the **Select automatically** checkbox.</span></span>  
    
    > ##### <span data-ttu-id="ca7f0-111">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="ca7f0-111">Figure 2</span></span>  
    > <span data-ttu-id="ca7f0-112">Отключение **Select автоматически**</span><span class="sxs-lookup"><span data-stu-id="ca7f0-112">Disabling **Select automatically**</span></span>  
    > ![Отключение Select автоматически][ImageUserAgentDisableSelectAutomatically]  
    
1.  <span data-ttu-id="ca7f0-114">Выберите строку агента пользователя из списка или введите собственную настраиваемую строку.</span><span class="sxs-lookup"><span data-stu-id="ca7f0-114">Select a user agent string from the list, or enter your own custom string.</span></span>  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Рисунок 1: меню команд"  
[ImageUserAgentDisableSelectAutomatically]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png "Рисунок 2: отключение Select автоматически"  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Агент пользователя | MDN"  

> [!NOTE]
> <span data-ttu-id="ca7f0-118">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ca7f0-118">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="ca7f0-119">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="ca7f0-119">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="ca7f0-121">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="ca7f0-121">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
