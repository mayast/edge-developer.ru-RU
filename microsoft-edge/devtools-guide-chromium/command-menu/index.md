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





# Выполнение команд с помощью командного меню Microsoft Edge DevTools   

  

Меню команд предоставляет быстрый способ навигации по пользовательскому интерфейсу Microsoft Edge DevTools и выполнения стандартных задач, таких как [Отключение JavaScript][JavascriptDisable].  Возможно, вы знакомы с аналогичной функцией в коде Visual Studio, которая называется [палитрой команд][VisualStudioCodeUICommandPalette], которая была первоначальной для меню команд.  

> ##### Рис. 1  
> Отключение JavaScript с помощью меню команд  
> ![Отключение JavaScript с помощью меню команд][ImageDisableJS]  

## Открытие меню команд   

Нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \). Или нажмите кнопку **Настройка DevTools** `...` и выберите **команду выполнить**.  

> ##### Рисунок 2  
> Команда "выполнить"  
> ![Команда "выполнить"][ImageRunCommand]  

## Просмотр других доступных действий   

Если вы используете рабочий процесс, описанный в разделе [Открыть меню команд](#open-the-command-menu), откроется меню команд с `>` символом, добавленным к текстовому полю меню команд.  

> ##### Рисунок3  
> Символ команды  
> ![Символ команды][ImageCommandCharacter]  

Удалите `>` символ и введите текст `?` , чтобы просмотреть другие действия, доступные в меню команд.  

> ##### Рисунок4  
> Другие доступные действия  
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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/command-menu/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
