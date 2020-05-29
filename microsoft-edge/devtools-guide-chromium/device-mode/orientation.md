---
title: Имитация ориентации устройства с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 9e8115819fa6c3209a6c82940e033113783ece0c
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607322"
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





# <span data-ttu-id="b9f9c-103">Имитация ориентации устройства с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="b9f9c-103">Simulate Device Orientation With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="b9f9c-104">Для имитации разных ориентаций устройства в Microsoft Edge DevTools:</span><span class="sxs-lookup"><span data-stu-id="b9f9c-104">To simulate different device orientations from Microsoft Edge DevTools:</span></span>  

<!--todo: update device orientation section when available -->  

1.  <span data-ttu-id="b9f9c-105">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="b9f9c-105">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="b9f9c-106">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="b9f9c-106">Figure 1</span></span>  
    > <span data-ttu-id="b9f9c-107">Меню команд</span><span class="sxs-lookup"><span data-stu-id="b9f9c-107">The Command Menu</span></span>  
    > ![Меню команд][ImageCommandMenu]  
    
1.  <span data-ttu-id="b9f9c-109">Введите текст `sensors` , установите флажок **Показать датчики**и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="b9f9c-109">Type `sensors`, select **Show Sensors**, and press `Enter`.</span></span>  <span data-ttu-id="b9f9c-110">Вкладка **датчики** откроется в нижней части окна DevTools.</span><span class="sxs-lookup"><span data-stu-id="b9f9c-110">The **Sensors** tab opens at the bottom of your DevTools window.</span></span>  
1.  <span data-ttu-id="b9f9c-111">В списке **ориентация** выберите один из готовых вариантов ориентации, например `Portrait upside down` или **другой** , чтобы задать точную ориентацию.</span><span class="sxs-lookup"><span data-stu-id="b9f9c-111">From the **Orientation** list, select one of the preset orientations, such as `Portrait upside down`, or select **Custom orientation** to provide your own exact orientation.</span></span>  
    
    > ##### <span data-ttu-id="b9f9c-112">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="b9f9c-112">Figure 2</span></span>  
    > <span data-ttu-id="b9f9c-113">Выбор `Portrait upside down` из списка **ориентации**</span><span class="sxs-lookup"><span data-stu-id="b9f9c-113">Selecting `Portrait upside down` from the **Orientation** list</span></span>  
    > ![Выбор книжной стрелки сверху вниз от списка ориентации][ImageOrientationPortraitUpsideDown]  
    
    <span data-ttu-id="b9f9c-115">После выбора **настраиваемой ориентации** `alpha` `beta` `gamma` будут включены поля и и.</span><span class="sxs-lookup"><span data-stu-id="b9f9c-115">After selecting **Custom orientation**, the `alpha`, `beta`, and `gamma` fields are enabled.</span></span>  
    <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how these axes work.  -->  
    <!--todo: update links to alpha, beta, and gamma section when available -->  
    <span data-ttu-id="b9f9c-116">Вы также можете настроить пользовательскую ориентацию, перетащив **модель ориентации**.</span><span class="sxs-lookup"><span data-stu-id="b9f9c-116">You are also able to set a custom orientation by dragging the **Orientation Model**.</span></span>  <span data-ttu-id="b9f9c-117">Удерживайте `Shift` перед перетаскиванием, чтобы повернуть вдоль `alpha` оси.</span><span class="sxs-lookup"><span data-stu-id="b9f9c-117">Hold `Shift` before dragging to rotate along the `alpha` axis.</span></span>  
    
    > ##### <span data-ttu-id="b9f9c-118">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="b9f9c-118">Figure 3</span></span>  
    > <span data-ttu-id="b9f9c-119">**Модель ориентации**</span><span class="sxs-lookup"><span data-stu-id="b9f9c-119">The **Orientation Model**</span></span>  
    > ![Модель ориентации][ImageOrientationModel]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Рисунок 1: меню команд"  
[ImageOrientationPortraitUpsideDown]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png "Рисунок 2: Выбор книжной стрелки сверху вниз от списка ориентации"  
[ImageOrientationModel]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-orientation-custom.msft.png "Рисунок 3: модель ориентации"  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation \& Motion"  -->  

> [!NOTE]
> <span data-ttu-id="b9f9c-124">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b9f9c-124">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="b9f9c-125">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="b9f9c-125">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="b9f9c-127">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="b9f9c-127">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
