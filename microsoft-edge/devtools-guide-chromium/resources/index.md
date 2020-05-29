---
title: Просмотр ресурсов страницы с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 0977d0a9132c19742c3337f9dc0c3e1240508a3d
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611919"
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





# Просмотр ресурсов страницы с помощью Microsoft Edge DevTools   

  

В этом руководстве рассказывается, как использовать Microsoft Edge DevTools для просмотра ресурсов веб-страницы.  Ресурсы — это файлы, необходимые для правильного отображения страницы.  Примеры ресурсов включают CSS, JavaScript и HTML-файлы, а также изображения.  

В этом руководстве предполагается, что вы знакомы с основами [веб-разработки][MDNLearnWebDevelopment] и [Microsoft Edge DevTools][MicrosoftEdgeDevTools].  

## Открытие ресурсов   

Если вы знаете имя ресурса, который вы хотите проверить, **меню команд** предоставляет быстрый способ открытия ресурса.  

1.  Нажмите клавиши `Control` + `P` \ (Windows \) или `Command` + `P` \ (macOS \).  Откроется диалоговое окно **Открытие файла** .  
    
    > ##### Рис. 1  
    > Диалоговое окно « **Открытие файла** »  
    > ![Диалоговое окно «Открытие файла»][ImageOpenFile]  
    
1.  Выберите файл из раскрывающегося списка или введите имя файла и нажмите `Enter` один раз, чтобы выделить его в поле "Автозаполнение".  
    
    > ##### Рисунок 2  
    > Ввод имени файла в диалоговом окне " **Открытие файла** "  
    > ![Ввод имени файла в диалоговом окне "Открытие файла"][ImageFileSearch]  
    
### Открытие ресурсов на панели "сеть"   

Ознакомьтесь [с подробными сведениями о ресурсе][DevtoolsNetworkInspectDetailsResource].  

> ##### Рисунок3  
> Проверка ресурса на панели "сеть"  
> ![Проверка ресурса на панели "сеть"][ImageNetworkResponse]  

### Показать ресурсы на панели "сеть" с других панелей   

В разделе [Обзор ресурсов](#browse-resources) ниже показано, как просматривать ресурсы из различных частей пользовательского интерфейса DevTools.  Если вы когда-нибудь хотите просмотреть ресурс на панели **сеть** , щелкните ресурс правой кнопкой мыши и выберите пункт **Показать на панели "сеть**".  

> ##### Рисунок4  
> Параметр « **Показать в сети»**  
> ![Панель "Показать в сети"][ImageRevealNetwork]  

## Просмотр ресурсов   

### Просмотр ресурсов на панели «Сеть»   

Просмотр [журнала активности сети][DevtoolsNetworkLogActivity].  

> ##### Рисунок 5  
> Ресурсы страницы в журнале сети  
> ![Ресурсы страницы в журнале сети][ImageNetworkLog]  

### Просмотр по каталогу   

Чтобы просмотреть ресурсы на странице, упорядоченные по каталогу, выполните указанные ниже действия.  

1.  Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".  
1.  Щелкните вкладку **страницы** , чтобы показать ресурсы страницы.  Откроется область **страница** .  
    
    > ##### Рисунок6  
    > Область **страницы**  
    > ![Область страницы][ImagePage]  
    
    Ниже приведено разделение элементов, не являющихся очевидными, на [рисунке 6](#figure-6).  
    
    | Элемент страницы | Описание |  
    |:--- |:--- |  
    | `top` | Основной [контекст обзора][MDNInlineFrame]документов. |  
    | `airhorner.com` | Домен.  Все ресурсы, вложенные в него, поступают из этого домена.  Например, может быть задан полный URL-адрес `comlink.global.j` файла `https://airhorner.com/scripts/comlink.global.js` . |  
    | `scripts` | Каталог. |  
    | `(index)` | Основной HTML-документ. |  
    | `sw.js` | Контекст среды выполнения рабочего процесса службы. |  
    
1.  Щелкните ресурс, чтобы просмотреть его в **редакторе**.  
    
    > ##### Рисунок7  
    > Просмотр файла в **редакторе**  
    > ![Просмотр файла в редакторе][ImageSourcesView]  
    
### Просмотр по имени файла   

По умолчанию в области **страницы** ресурсы группируются по каталогам.  Чтобы отключить эту группировку и просмотреть ресурсы для каждого домена в виде плоского списка, выполните указанные ниже действия.  

1.  Открытие области **страницы** .  Просмотр [по каталогу](#browse-by-directory).  
1.  Нажмите кнопку **Дополнительные параметры** `...` и отключите функцию **Группировка по папкам**.  
    
    > ##### Рисунок8  
    > Параметр **Группировка по папке**  
    > ![Параметр Группировка по папке][ImageGroupByFolder]  
    
    Ресурсы упорядочены по типам файлов.  В каждом типе файла ресурсы упорядочены по алфавиту.  
    
    > ##### Рисунок9  
    > Область **страницы** после отключения **группировки по папке**  
    > ![Область страницы после отключения группировки по папке][ImageFileNames]  
    
### Просмотр по типу файла   

Чтобы сгруппировать ресурсы в зависимости от типа файла:  

1.  Откройте вкладку **приложение** .  Откроется панель **приложения** .  По умолчанию область **манифеста** обычно открывается в первую очередь.  
    
    > ##### Рисунок 10  
    > Панель **приложения**  
    > ![Панель приложения][ImageApplication]  
    
1.  Прокрутите страницу вниз до области **рамок** .  
    
    > ##### Рисунок11  
    > Область **рамок**  
    > ![Область рамок][ImageFrames]  
    
1.  Разверните разделы, в которых вы заинтересованы.  
1.  Щелкните ресурс, чтобы просмотреть его.  
    
    > ##### Рисунок12  
    > Просмотр ресурса на панели « **приложение** »  
    > ![Просмотр ресурса на панели «приложение»][ImageApplicationView]  

#### Просмотр файлов по типу на панели «Сеть»   

Просмотреть [Фильтр по типу ресурсов][DevtoolsNetworkFilterByResourceType].  

> ##### Рисунок13  
> Фильтрация для CSS в сетевом журнале  
> ![Фильтрация для CSS в сетевом журнале][ImageCSS]  

<!--  -->  



<!-- image links -->  

[ImageOpenFile]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-empty.msft.png "Рисунок 1: диалоговое окно "открыть файл""  
[ImageFileSearch]: /microsoft-edge/devtools-guide-chromium/media/resources-command-menu-file-search.msft.png "Рисунок 2: ввод имени файла в диалоговом окне "Открытие файла""  
[ImageNetworkResponse]: /microsoft-edge/devtools-guide-chromium/media/resources-network-response.msft.png "Рисунок 3: Проверка ресурса на панели * * Network * *"  
[ImageRevealNetwork]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-reveal-in-network-panel.msft.png "Рисунок 4: Показать на панели "сеть""  
[ImageNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources.msft.png "Рисунок 5: ресурсы страницы в журнале сети"  
[ImagePage]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-empty.msft.png "Рисунок 6: область страницы"  
[ImageSourcesView]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource.msft.png "Рис. 7: Просмотр файла в редакторе"  
[ImageGroupByFolder]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resource-group-by-folder.msft.png "Рисунок 8: параметр группировка по папке"  
[ImageFileNames]: /microsoft-edge/devtools-guide-chromium/media/resources-sources-page-resources-empty-not-grouped-by-folder.msft.png "Рисунок 9: область страницы после отключения группы по папке"  
[ImageApplication]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner.msft.png "Рисунок 10: панель приложения"  
[ImageFrames]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-frames-expanded.msft.png "Рисунок 11: область рамок"  
[ImageApplicationView]: /microsoft-edge/devtools-guide-chromium/media/resources-application-mainfest-airhorner-expanded-resources.msft.png "Рисунок 12: Просмотр ресурса на панели «приложение»"  
[ImageCSS]: /microsoft-edge/devtools-guide-chromium/media/resources-network-resources-filter-css.msft.png "Рисунок 13: Фильтрация CSS в сетевом журнале"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevtoolsNetworkFilterByResourceType]: /microsoft-edge/devtools-guide-chromium/network/index#filter-by-resource-type "Фильтрация по типу ресурсов: Проверка активности сети в Microsoft Edge DevTools"  
[DevtoolsNetworkInspectDetailsResource]: /microsoft-edge/devtools-guide-chromium/network/index#inspect-the-details-of-the-resource "Просмотрите сведения об активности в сети для проверки ресурсов в Microsoft Edge DevTools"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/devtools-guide-chromium/network/index#log-network-activity "Регистрация активности сети — проверка активности сети в Microsoft Edge DevTools"  

[MDNInlineFrame]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> IFRAME: элемент встроенной рамки | MDN"  
[MDNLearnWebDevelopment]: https://developer.mozilla.org/docs/Learn "Знакомство с веб-разработкой | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/resources/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
