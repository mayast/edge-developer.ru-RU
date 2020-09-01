---
title: Переопределение строки агента пользователя из Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 0ffea8f515a2d4ba0fa16b447a7d204c335dc7bb
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10984998"
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





# <span data-ttu-id="a7452-103">Переопределение строки агента пользователя из Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a7452-103">Override the user agent string from Microsoft Edge DevTools</span></span>   



<span data-ttu-id="a7452-104">Чтобы переопределить строку [агента пользователя][MDNUserAgent] из Microsoft Edge DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="a7452-104">To override the [user agent][MDNUserAgent] string from Microsoft Edge DevTools:</span></span>  

1.  <span data-ttu-id="a7452-105">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="a7452-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-command-menu.msft.png":::
       <span data-ttu-id="a7452-107">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="a7452-107">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a7452-108">Введите и `network conditions` выберите **Показывать условия сети**, а затем `Enter` откройте вкладку **условия сети** .</span><span class="sxs-lookup"><span data-stu-id="a7452-108">Type `network conditions`, select **Show Network conditions**, and press `Enter` to open the **Network conditions** tab.</span></span>  
1.  <span data-ttu-id="a7452-109">В разделе **Агент пользователя** отключите флажок **выбрать автоматически** .</span><span class="sxs-lookup"><span data-stu-id="a7452-109">In the **User agent** section, disable the **Select automatically** checkbox.</span></span>  
    
    :::image type="complex" source="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png" alt-text="Отключить функцию "выбрать автоматически"" lightbox="../media/device-mode-console-network-conditions-user-agent-select-automatically-deselected.msft.png":::
       <span data-ttu-id="a7452-111">Отключить функцию " **выбрать автоматически** "</span><span class="sxs-lookup"><span data-stu-id="a7452-111">Disable **Select automatically**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="a7452-112">Выберите строку агента пользователя из списка или введите собственную настраиваемую строку.</span><span class="sxs-lookup"><span data-stu-id="a7452-112">Select a user agent string from the list, or enter your own custom string.</span></span>  
    
<!--  
## Feedback   


-->  

<!-- links -->  

[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Агент пользователя | MDN"  

> [!NOTE]
> <span data-ttu-id="a7452-114">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a7452-114">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a7452-115">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a7452-115">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/override-user-agent) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a7452-117">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a7452-117">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
