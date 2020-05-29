---
title: Просмотр данных кэша приложения с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 6ce3087e9c719efbcf4d9ebceb860edd0ed0c3b6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612097"
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





# Просмотр данных кэша приложения с помощью Microsoft Edge DevTools   



> [!WARNING]
> API кэша приложения [удаляется с веб-платформы][HTMLStandardOfflineWebApplications].  

В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки ресурсов [кэша приложения][MDNWebAPIsWindowApplicationCache] .  

## Просмотр данных кэша приложения   

1.  Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".  Обычно область **манифеста** открывается по умолчанию.  
    
    > ##### Рис. 1  
    > Область «манифест»  
    > ![Область «манифест»][ImageManifestPane]  

1.  Разверните раздел **кэш приложений** и щелкните кэш для просмотра ресурсов.  
    
    > ##### Рисунок 2  
    > Область кэша приложения  
    > ![Область кэша приложения][ImageApplicationCachePane]  

Каждая строка таблицы представляет собой кэшируемый ресурс.  

Столбец **Type** представляет [категорию ресурса][MDNHTMLResourcesInAnApplicationCache].  

| Категория | Сведения |  
|:--- |:--- |  
| `Explicit` | Этот ресурс явно указан в манифесте. |  
| `Fallback` | URL-адрес является резервным для другого ресурса.  URL-адрес другого ресурса не указан в DevTools. |  
| `Master` | `manifest`Атрибут ресурса указывает на то, что этот кэш является родительским для ресурса. |  
| `Network` | Манифест, который должен поступать этим ресурсом из сети. |  

В нижней части таблицы находятся значки состояния, обозначающие сетевое соединение и состояние кэша приложения.  В кэше приложения могут находиться указанные ниже состояния.  

| Состояние | Сведения |  
|:--- |:--- |  
| `CHECKING` | Манифест извлекается и проверяется на наличие обновлений. |  
| `DOWNLOADING` | Ресурсы добавляются в кэш. |  
| `IDLE` | В кэше нет новых изменений. |  
| `OBSOLETE` | Кэш удаляется. |  
| `UPDATEREADY` |  Доступна новая версия кэша. |  

<!--   -->  



<!-- image links -->  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Рисунок 1: область манифеста"  
[ImageApplicationCachePane]: /microsoft-edge/devtools-guide-chromium/media/storage-cache-pane-cache-storage-resources.msft.png "Рисунок 2: область кэша приложения"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Автономные веб-приложения: HTML Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ресурсы в кэше приложения | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-Web API | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
