---
title: Отключение JavaScript с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 829902ddd76800bb8d36268cb07a61361aa1a159
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986117"
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

# <span data-ttu-id="51721-103">Отключение JavaScript с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="51721-103">Disable JavaScript With Microsoft Edge DevTools</span></span>  

<span data-ttu-id="51721-104">Выполните описанные ниже действия, чтобы увидеть, как выглядит веб-страница и использует ее при отключении JavaScript.</span><span class="sxs-lookup"><span data-stu-id="51721-104">Complete the following actions to see how a web page looks and behaves when JavaScript is disabled.</span></span>  

1.  <span data-ttu-id="51721-105">[Откройте Microsoft Edge DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="51721-105">[Open Microsoft Edge DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="51721-106">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="51721-106">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command.msft.png" alt-text="Меню команд" lightbox="../media/javascript-console-command.msft.png":::
       <span data-ttu-id="51721-108">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="51721-108">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="51721-109">Начните вводить текст, нажмите кнопку `javascript` **отключить JavaScript**, а затем нажмите `Enter` , чтобы выполнить команду.</span><span class="sxs-lookup"><span data-stu-id="51721-109">Start typing `javascript`, select **Disable JavaScript**, and then press `Enter` to run the command.</span></span>  <span data-ttu-id="51721-110">JavaScript теперь отключен.</span><span class="sxs-lookup"><span data-stu-id="51721-110">JavaScript is now disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-command-javascript.msft.png" alt-text="Выбор пункта "отключить JavaScript" в меню команд" lightbox="../media/javascript-console-command-javascript.msft.png":::
       <span data-ttu-id="51721-112">Выбор пункта " **отключить JavaScript** " в **меню команд**</span><span class="sxs-lookup"><span data-stu-id="51721-112">Select **Disable JavaScript** in the **Command Menu**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="51721-113">Значок желтого предупреждения рядом с последующими **источниками** напоминает, что JavaScript отключен.</span><span class="sxs-lookup"><span data-stu-id="51721-113">The yellow warning icon next to **Sources** reminds you that JavaScript is disabled.</span></span>  
    
    :::image type="complex" source="../media/javascript-console-javascript-disabled-warning.msft.png" alt-text="Значок предупреждения рядом с пунктом «источники»" lightbox="../media/javascript-console-javascript-disabled-warning.msft.png":::
       <span data-ttu-id="51721-115">Значок предупреждения рядом с пунктом « **источники** »</span><span class="sxs-lookup"><span data-stu-id="51721-115">The warning icon next to **Sources**</span></span>  
    :::image-end:::  
    
<span data-ttu-id="51721-116">JavaScript остается отключенным на вкладке столько, сколько открыто DevTools.</span><span class="sxs-lookup"><span data-stu-id="51721-116">JavaScript remains disabled in the tab for as long as you have DevTools open.</span></span>  

<span data-ttu-id="51721-117">Возможно, потребуется перезагрузить страницу, чтобы проверить, зависит ли страница от JavaScript во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="51721-117">You may want to reload the page to see if and how the page depends on JavaScript while loading.</span></span>  

<span data-ttu-id="51721-118">Чтобы повторно включить JavaScript, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="51721-118">To re-enable JavaScript, complete the following actions.</span></span>  

*   <span data-ttu-id="51721-119">Снова откройте **меню команд** и выполните `Enable JavaScript` команду.</span><span class="sxs-lookup"><span data-stu-id="51721-119">Open the **Command Menu** again and run the `Enable JavaScript` command.</span></span>  
*   <span data-ttu-id="51721-120">Закройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="51721-120">Close DevTools.</span></span>  

## <span data-ttu-id="51721-121">Знакомство с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="51721-121">Getting in touch with the Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../includes/contact-devtools-team-note.md)]  

<!-- links -->  

[DevToolsOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  

> [!NOTE]
> <span data-ttu-id="51721-123">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51721-123">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="51721-124">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="51721-124">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="51721-126">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="51721-126">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
