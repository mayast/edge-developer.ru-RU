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





# Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)   



По умолчанию DevTools закрепляется справа от окна просмотра.  Вы также можете закрепить нижнюю границу, закрепить слева или отстыковать DevTools в отдельном окне.  

> ##### Рис. 1  
> Закрепить слева  
> ![Закрепить слева][ImageDockLeft]  

> ##### Рисунок 2  
> Закрепить в нижней части экрана  
> ![Закрепить в нижней части экрана][ImageDockBottom]  

> ##### Рисунок3  
> Браузер в отдельном окне  
> ![Браузер в отдельном окне][ImageUndockBrowser]  

> ##### Рисунок4  
> Незакрепленные DevTools в отдельном окне  
> ![Незакрепленные DevTools в отдельном окне][ImageUndockDevTools]  

## Изменение положения в главном меню   

1.  Нажмите кнопку **Настройка DevTools** `...` и выберите команду **открепить в отдельном окне** , а затем закрепите ![ ][ImageUndockIcon] **на нижней** панели ![ ][ImageBottomIcon] или **закрепите** влево ![ ][ImageLeftIcon] .  
    
    > ##### Рисунок 5  
    > Выбор пункта " **открепить в отдельном окне** "  
    > ![Выбор пункта "Открепить в отдельном окне"][ImageUndockSettings]  
    
## Изменение положения в меню команд   

1.  [Открытие меню команд][DevtoolsCommandMenu].  
1.  Выполните одну из указанных ниже `Dock To Bottom` команд. `Undock Into Separate Window`  В настоящее время нет команды для закрепления слева, но вы можете получить доступ к ней из [главного меню](#change-placement-from-the-main-menu).  
    
    > ##### Рисунок6  
    > Команда "отменить закрепление"  
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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/customize/placement) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
