---
title: Контроль значений выражений JavaScript в режиме реального времени с помощью выражений в реальном масштабе
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: c388e44ca5507dd88ad9ad7b7ee985e658dfc569
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601742"
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





# Контроль значений выражений JavaScript в режиме реального времени с помощью выражений в реальном масштабе   

  

Если вы обнаружите, что один и тот же выражение JavaScript будет вводиться повторно в консоль, возможно, вам будет проще создать **выражение в реальном времени**.  С помощью **выражений в реальном времени** вы вводите выражение один раз, а затем закрепите его в верхней части консоли.  Значение выражения обновляется почти в режиме реального времени.  

## Создание выражения в реальном времени   

1.  [Открытие консоли][DevToolsConsoleReferenceOpenConsole].  
1.  Щелкните создать выражение для создания **динамического выражения** ![ ][ImageCreateLiveExpressionIcon] .  Появится текстовое поле " **выражение в реальном времени** ".  
    
    > ##### Рис. 1  
    > Ввод `document.activeElement` текста в текстовое поле " **интерактивное выражение** "  
    > ![Ввод данных Document. activeElement в текстовое поле "Интерактивное выражение"][ImageLiveExpressionTextbox]  
    
1.  Введите `Control` + `Enter` \ (Windows \) или `Command` + `Enter` \ (macOS \), чтобы сохранить выражение, или щелкните любое место за пределами текстового поля **Live Expression** .  

<!--todo: add reference open console (open the console) section when available  -->  

 



<!-- image links -->  

[ImageCreateLiveExpressionIcon]: /microsoft-edge/devtools-guide-chromium/media/create-live-expression-icon.msft.png  

[ImageLiveExpressionTextbox]: /microsoft-edge/devtools-guide-chromium/media/console-create-live-expression.msft.png "Рисунок 1: ввод данных Document. activeElement в текстовое поле "Интерактивное выражение""  

<!-- links -->  

[DevToolsConsoleReferenceOpenConsole]: /microsoft-edge/devtools-guide-chromium/console/reference#open-the-console "Открытие ссылки на консоль консоли"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/live-expressions) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
