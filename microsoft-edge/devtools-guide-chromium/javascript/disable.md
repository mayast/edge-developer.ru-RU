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





# Отключение JavaScript с помощью Microsoft Edge DevTools   



Чтобы просмотреть, как выглядит веб-страница и использует ее при отключении JavaScript, выполните указанные ниже действия.  

1.  [Откройте Microsoft Edge DevTools][DevToolsOpen].  
1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).  
    
    > ##### Рис. 1  
    > Меню команд  
    > ![Меню команд][ImageCommandMenu]  
    
1.  Начните вводить текст, нажмите кнопку `javascript` **отключить JavaScript**, а затем нажмите `Enter` , чтобы выполнить команду.  JavaScript теперь отключен.  
    
    > ##### Рисунок 2  
    > Выбор пункта " **отключить JavaScript** " в меню команд  
    > ![Выбор пункта "отключить JavaScript" в меню команд][ImageDisableJS]  
    
    Значок желтого предупреждения рядом с последующими **источниками** напоминает, что JavaScript отключен.  
    
    > ##### Рисунок3  
    > Значок предупреждения рядом с пунктом « **источники** »  
    > ![Значок предупреждения рядом с пунктом «источники»][ImageDisableJSWarning]  

JavaScript останется отключенным на этой вкладке столько, сколько открыто DevTools.  

Возможно, потребуется перезагрузить страницу, чтобы проверить, зависит ли страница от JavaScript во время загрузки.  

Чтобы повторно включить JavaScript, выполните указанные ниже действия.  

*   Снова откройте **меню команд** и выполните `Enable JavaScript` команду.  
*   Закройте DevTools.  

## Отзыв   



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command.msft.png "Рисунок 1: меню команд"  
[ImageDisableJS]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-command-javascript.msft.png "Рисунок 2: выбор пункта "отключить JavaScript" в меню команд"  
[ImageDisableJSWarning]: /microsoft-edge/devtools-guide-chromium/media/javascript-console-javascript-disabled-warning.msft.png "Рисунок 3: значок "предупреждение" рядом с пунктом "источники""  

<!-- links -->  

[DevToolsOpen]: ../open.md "Открыть Microsoft Edge DevTools"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/disable) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
