---
title: Имитация ориентации устройства с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: c9a2aecfff1101de532eb59f73da21a32d62c791
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985018"
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





# Имитация ориентации устройства с помощью Microsoft Edge DevTools   



Для имитации разных ориентаций устройства в Microsoft Edge DevTools:  

<!--todo: update device orientation section when available -->  

1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).  
    
    :::image type="complex" source="../media/device-mode-console-command-menu.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-console-command-menu.msft.png":::
       **Меню команд**  
    :::image-end:::  
    
1.  Введите текст `sensors` , установите флажок **Показать датчики**и нажмите клавишу `Enter` .  Вкладка **датчики** откроется в нижней части окна DevTools.  
1.  В списке **ориентация** выберите один из готовых вариантов ориентации, например `Portrait upside down` или **другой** , чтобы задать точную ориентацию.  
    
    :::row:::
       :::column span="":::
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png" alt-text="Выбор книжной ориентации сверху вниз в списке" lightbox="../media/device-mode-console-sensors-orientation-portrait-upside-down.msft.png":::
             Выбор `Portrait upside down` из списка **ориентации**  
          :::image-end:::  
       :::column-end:::
       :::column span="":::
          После выбора **настраиваемой ориентации** `alpha` `beta` поля и "и" `gamma` будут включены.  
          <!--See [Alpha][alpha], [Beta][beta], and [Gamma][gamma] to understand how these axes work.  -->  
          <!--todo: update links to alpha, beta, and gamma section when available -->  
          Вы также можете настроить пользовательскую ориентацию, перетащив **модель ориентации**.  Удерживайте `Shift` перед перетаскиванием, чтобы повернуть вдоль `alpha` оси.  
          
          :::image type="complex" source="../media/device-mode-console-sensors-orientation-custom.msft.png" alt-text="Модель ориентации" lightbox="../media/device-mode-console-sensors-orientation-custom.msft.png":::
             **Модель ориентации**  
          :::image-end:::  
       :::column-end:::
    :::row-end:::
    
<!--  
## Feedback 


-->  

<!-- links -->  

<!--[WebFundamentasNativeHardwareDeviceOrientationIndex]: /web/fundamentals/native-hardware/device-orientation/index "Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexAlpha]: /web/fundamentals/native-hardware/device-orientation/index#alpha "Alpha - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexBeta]: /web/fundamentals/native-hardware/device-orientation/index#beta "Beta - Device Orientation \& Motion"  -->  
<!--[WebFundamentasNativeHardwareDeviceOrientationIndexGamma]: /web/fundamentals/native-hardware/device-orientation/index#gamma "Gamma - Device Orientation \& Motion"  -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/orientation) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
