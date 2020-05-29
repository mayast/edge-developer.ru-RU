---
title: Помечайте сценарии содержимого как код библиотеки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: fe34d8f2fb656283b1821441162b93d47d51d24e
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581791"
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





# Помечайте сценарии содержимого как код библиотеки   



При использовании панели **Sources (источники** данных) Microsoft Edge DevTools для [перехода по коду][DevToolsJavascriptStepThroughCode], иногда наведите указатель мыши на код, который вы не знаете.  Возможно, вы приостановили код для одного из установленных расширений Microsoft Edge.  Выполните указанные ниже действия, чтобы не приостанавливаться на коде расширения.  

1.  Откройте DevTools, выберите пункт **Настройка DevTools и управление** `...` **параметрами**.  Вы также можете открыть **Параметры** , нажав клавишу `F1` .  

1.  Откройте вкладку **код библиотеки** , которая открывает раздел **код библиотеки Framework** **параметров**.  
1.  Установите флажок **помечать сценарии содержимого как библиотечный код** .  
    
    > ##### Рис. 1  
    > Флажок " **помечать сценарии содержимого как библиотеку кода** "  
    > ![Флажок "помечать сценарии содержимого как библиотеку кода"][ImageMarkContentScriptsLibraryCode]  

<!--## Feedback   -->  



<!-- image links -->  

[ImageMarkContentScriptsLibraryCode]: /microsoft-edge/devtools-guide-chromium/media/javascript-settings-library-code-mark-content-scripts-library-code.msft.png "Рисунок 1: флажок "помечать сценарии содержимого как библиотеку кода""  

<!-- links -->  

[DevToolsJavascriptStepThroughCode]: ../index.md#step-4-step-through-the-code "Шаг 4: пошаговое руководство по написанию кода — начало работы с отладкой JavaScript в Microsoft Edge DevTools"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/guides/blackbox-chrome-extension-scripts) и [Kayce Basques][KayceBasques] \ (технический писатель, хром DevTools & Lighthouse).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
