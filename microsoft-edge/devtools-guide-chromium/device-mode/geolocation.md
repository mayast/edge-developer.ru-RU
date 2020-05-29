---
title: Переопределение географического положения с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/26/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 307064bedf992e528b6d79eed3a2ade3367830d4
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607442"
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





# Переопределение географического положения с помощью Microsoft Edge DevTools   



Многие веб-сайты имеют преимущество для предоставления пользователям более подходящих возможностей.  Например, на веб-сайте Weather может отображаться локальный прогноз в области пользователя, после того как пользователь выдает разрешение веб-сайту на доступ к текущему расположению пользователя.  

<!--todo: add link to user location section when available -->  

Если вы создаете пользовательский интерфейс, который изменяется в зависимости от того, где находится пользователь, возможно, вы захотите убедиться в том, что сайт правильно работает в разных местах по всему миру.  Чтобы переопределить географическое положение в Microsoft Edge DevTools, выполните указанные ниже действия.  

1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).  
    
    > ##### Рис. 1  
    > Меню команд  
    > ![Меню команд][ImageCommandMenu]  
    
1.  Введите текст `sensors` , установите флажок **Показать датчики**и нажмите клавишу `Enter` .  Вкладка **датчики** откроется в нижней части окна DevTools.  
1.  В списке **географическое положение** выберите один из готовых городов `Tokyo` или выберите **другое расположение** , чтобы указать пользовательские координаты долготы и широты, или выберите пункт **расположение недоступно** , чтобы увидеть, как работает сайт, когда его расположение недоступно.  
    
    > ##### Рисунок 2  
    > Выбор `Tokyo` из списка **географического расположения**  
    > ![Выбор в Токио из списка географического расположения][ImageGeolocationTokyo]  
    
<!--## Feedback   

  -->  

<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-command-menu.msft.png "Рисунок 1: меню команд"  
[ImageGeolocationTokyo]: /microsoft-edge/devtools-guide-chromium/media/device-mode-console-sensors-geolocation-tokyo.msft.png "Рисунок 2: выбор в Токио из списка географического расположения"  

<!-- links -->  

<!--[WebFundamentalsNativeHardwareUserLocationIndex]: /web/fundamentals/native-hardware/user-location/index "User Location"  -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/geolocation) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
