---
title: Просмотр данных кэша с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 82356777f209b86f88de1ee53b212947d969ff8a
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612076"
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





# Просмотр данных кэша с помощью Microsoft Edge DevTools   



В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных [кэша][MDNCache] .  

Если вы пытаетесь проверить данные [кэша HTTP][MDNHTTPCaching] , это не значит, что вам нужно.  
Найдите данные в столбце " **Размер** " в **сетевом журнале**.  Просмотр [журнала активности сети][DevtoolsNetworkLogActivity].  

## Просмотр данных кэша   

1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Обычно область **манифеста** открывается по умолчанию.  
    
    > ##### Рис. 1  
    > Область «манифест»  
    > ![Область «манифест»][ImageManifestPane]  

1.  Разверните раздел **хранилище кэша** , чтобы просмотреть доступные кэши.  
    
    > ##### Рисунок 2  
    > Доступные кэши  
    > ![Доступные кэши][ImageCache]  

1.  Выберите кэш, чтобы просмотреть его содержимое.  
    
    > ##### Рисунок3  
    > Просмотр содержимого кэша  
    > ![Просмотр содержимого кэша][ImageCacheView]  

1.  Выберите ресурс для просмотра заголовков HTTP в разделе под таблицей.  
    
    > ##### Рисунок4  
    > Просмотр заголовков HTTP ресурса  
    > ![Просмотр заголовков HTTP ресурса][ImageViewCacheResource]  

1.  Нажмите кнопку **Предварительный просмотр** , чтобы просмотреть содержимое ресурса.  
    
    > ##### Рисунок 5  
    > Просмотр содержимого ресурса  
    > ![Просмотр содержимого ресурса][ImageCacheContent]  

## Обновление ресурса   

1.  [Просмотр данных для кэша](#view-cache-data).  
1.  Выберите ресурс, который вы хотите обновить.  DevTools выделит ее, чтобы показать, что она выбрана.  
    
    > ##### Рисунок6  
    > Выбор ресурса  
    > ![Выбор ресурса][ImageCacheSelected]  

1.  Нажмите кнопку **Обновить** ![ Обновление ][ImageRefreshIcon] .  

## Фильтрация ресурсов   

1.  [Просмотр данных для кэша](#view-cache-data).  
1.  С помощью текстового поля **Фильтр по пути** можно отфильтровать ресурсы, которые не соответствуют указанному вами пути.  
    
    > ##### Рисунок7  
    > Фильтрация ресурсов, не соответствующих указанному пути  
    > ![Фильтрация ресурсов, не соответствующих указанному пути][ImageCacheFilter]  

## Удаление ресурса   

1.  [Просмотр данных для кэша](#view-cache-data).  
1.  Выберите ресурс, который вы хотите удалить.  DevTools выделит ее, чтобы показать, что она выбрана.  
    
    > ##### Рисунок8  
    > Выбор ресурса  
    > ![Выбор ресурса][ImageCacheSelected2]  

1.  Выберите команду **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] .  

## Удаление всех данных из кэша   

1.  Откройте **приложение**  >  , чтобы**Очистить хранилище**.  
1.  Убедитесь, что флажок **хранилище кэша** включен.  
    
    > ##### Рисунок9  
    > Флажок " **хранилище кэша** "  
    > ![Флажок "хранилище кэша"][ImageCacheCheckbox]  

1.  Нажмите кнопку **Очистить данные сайта**.  
    
    > ##### Рисунок 10  
    > Кнопка " **Очистить данные сайта** "  
    > ![Кнопка "очистить данные сайта"][ImageCacheClearSite]  

<!--  -->  



<!-- image links -->  

[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Рисунок 1: область манифеста"  
[ImageCache]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage.msft.png "Рисунок 2: доступные кэши"  
[ImageCacheView]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-root-headers.msft.png "Рисунок 3: Просмотр содержимого кэша"  
[ImageViewCacheResource]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-index-headers.msft.png "Рисунок 4: Просмотр заголовков HTTP ресурса"  
[ImageCacheContent]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-js-preview.msft.png "Рисунок 5: Просмотр содержимого ресурса"  
[ImageCacheSelected]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-domain-refresh.msft.png "Рисунок 6. Выбор ресурса"  
[ImageCacheFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-filter.msft.png "Рис. 7: Фильтрация ресурсов, не соответствующих указанному пути"  
[ImageCacheSelected2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-cache-storage-delete-selected.msft.png "Рисунок 8: Выбор ресурса"  
[ImageCacheCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox.msft.png "Рисунок 9: флажок хранилища кэша"  
[ImageCacheClearSite]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-cache-storage-checkbox-clear-site-data-button.msft.png "Рисунок 10: кнопка "очистить данные сайта""  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevtoolsNetworkLogActivity]: /microsoft-edge/network/index#log-network-activity  "Регистрация активности в сети"  

[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNHTTPCaching]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэширование HTTP | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/cache) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
