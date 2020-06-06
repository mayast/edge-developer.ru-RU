---
title: Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 659120414597273b15657377c33c800e0c83b7cb
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601840"
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





# Принудительная установка Microsoft Edge DevTools в режиме предварительного просмотра (тип носителя для печати CSS)   



[Запрос на печать][MDNUsingMediaQueries] позволяет управлять тем, как выглядит страница после печати.  Чтобы перевести страницу в режим предварительного просмотра, выполните указанные ниже действия.  

1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).  
    
    > ##### Рис. 1  
    > **Меню команд**  
    > ![Меню команд][ImageCommandMenu]  
    
1.  Введите `rendering` команду **Показать рендеринг**и нажмите клавишу `Enter` .  
1.  В разделе **Эмуляция мультимедиа в CSS** выберите **Печать**.  
    
    > ##### Рисунок 2  
    > Режим предварительного просмотра  
    > ![Режим предварительного просмотра][ImagePrintMode]  
    
Отсюда вы можете просматривать и изменять CSS, как и любую другую веб-страницу.  Ознакомьтесь [со статьей начало работы с помощью просмотра и изменения CSS][DevToolsCSSGetStarted].  

 



<!-- image links -->  

[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/css-console-command-menu-rendering.msft.png "Рисунок 1: меню команд"  
[ImagePrintMode]: /microsoft-edge/devtools-guide-chromium/media/css-elements-styles-qs-rendering-emulate-css-media-print.msft.png "Рисунок 2: режим предварительного просмотра"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevToolsCSSGetStarted]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  

[MDNUsingMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries/Using_media_queries "Использование мультимедийных запросов | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/css/print-preview) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  