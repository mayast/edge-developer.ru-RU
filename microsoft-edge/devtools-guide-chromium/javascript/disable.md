---
title: Отключение JavaScript с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: f3838b4e8eccf83aaa71be35ff477ec56cbe7455
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581812"
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





# <span data-ttu-id="95395-103">Отключение JavaScript с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="95395-103">Disable JavaScript With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="95395-104">Чтобы просмотреть, как выглядит веб-страница и использует ее при отключении JavaScript, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="95395-104">To see how a web page looks and behaves when JavaScript is disabled:</span></span>  

1.  <span data-ttu-id="95395-105">[Откройте Microsoft Edge DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="95395-105">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="95395-106">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="95395-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="95395-107">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="95395-107">Figure 1</span></span>  
    > <span data-ttu-id="95395-108">Меню команд</span><span class="sxs-lookup"><span data-stu-id="95395-108">The Command Menu</span></span>  
    > ![Меню команд][ImageCommandMenu]  
    
1.  <span data-ttu-id="95395-110">Начните вводить текст, нажмите кнопку `javascript` **отключить JavaScript**, а затем нажмите `Enter` , чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="95395-110">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="95395-111">JavaScript теперь отключен.</span><span class="sxs-lookup"><span data-stu-id="95395-111">JavaScript is now disabled.</span></span>  
    
    > ##### <span data-ttu-id="95395-112">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="95395-112">Figure 2</span></span>  
    > <span data-ttu-id="95395-113">Выбор пункта " **отключить JavaScript** " в меню команд</span><span class="sxs-lookup"><span data-stu-id="95395-113">Selecting **Disable JavaScript** in the Command Menu</span></span>  
    > ![Выбор пункта "отключить JavaScript" в меню команд][ImageDisableJS]  
    
    <span data-ttu-id="95395-115">Значок желтого предупреждения рядом с последующими **источниками** напоминает, что JavaScript отключен.</span><span class="sxs-lookup"><span data-stu-id="95395-115">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    > ##### <span data-ttu-id="95395-116">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="95395-116">Figure 3</span></span>  
    > <span data-ttu-id="95395-117">Значок предупреждения рядом с пунктом « **источники** »</span><span class="sxs-lookup"><span data-stu-id="95395-117">The warning icon next to **Sources**</span></span>  
    > ![Значок предупреждения рядом с пунктом «источники»][ImageDisableJSWarning]  

<span data-ttu-id="95395-119">JavaScript останется отключенным на этой вкладке столько, сколько открыто DevTools.</span><span class="sxs-lookup"><span data-stu-id="95395-119">JavaScript remains disabled in this tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="95395-120">Возможно, потребуется перезагрузить страницу, чтобы проверить, зависит ли страница от JavaScript во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="95395-120">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="95395-121">Чтобы повторно включить JavaScript, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="95395-121">To re-enable JavaScript:</span></span>  

*   <span data-ttu-id="95395-122">Снова откройте **меню команд** и выполните `Enable JavaScript` команду.</span><span class="sxs-lookup"><span data-stu-id="95395-122">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="95395-123">Закройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="95395-123">Close DevTools.</span></span>  

## <span data-ttu-id="95395-124">Отзыв</span><span class="sxs-lookup"><span data-stu-id="95395-124">Feedback</span></span>   



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command.msft.png "Рисунок 1: меню команд"  
[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command-javascript.msft.png "Рисунок 2: выбор пункта "отключить JavaScript" в меню команд"  
[ImageDisableJSWarning]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-javascript-disabled-warning.msft.png "Рисунок 3: значок "предупреждение" рядом с пунктом "источники""  

<!-- links -->  

[DevToolsOpen]: ../open.md "Открыть Microsoft Edge DevTools"  

> [!NOTE]
> <span data-ttu-id="95395-129">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="95395-129">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="95395-130">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="95395-130">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="95395-132">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="95395-132">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
