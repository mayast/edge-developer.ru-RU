---
title: Руководство по сетевым проблемам
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 018a6ef89242d55cefaa974641be456f4501c557
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611807"
---
<!-- Copyright Kayce Basques and Jonathan Garbee

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->





# Руководство по сетевым проблемам   




В этом руководстве показано, как определить сетевые проблемы или возможности оптимизации на панели "сеть" Microsoft Edge DevTools.  

Ознакомьтесь со [статьей][NetworkPerformance] "Начало работы", чтобы ознакомиться с основными понятиями панели "сеть".  

## Запросы, поставленные в очередь или остановленные   

### Симптомы  

Шесть запросов загружаются одновременно.  После этого серии запросов будут помещены в очередь или остановлены.  После завершения одного из шести первых запросов запускается один из запросов в очереди.  

На **каскаде** на [рисунке 1](#figure-1)первые шесть запросов `edge-iconx1024.msft.png` актива запускаются одновременно.  Последующие запросы загружаются до тех пор, пока не завершится один из этих шести первоначальных элементов.  

> ##### Рис. 1  
> Пример списка в очереди или остановленного ряда на панели "сеть"  
> ![Пример списка в очереди или остановленного ряда на панели "сеть"][ImageStalled]  

### Причины  

Слишком много запросов выполняется в одном домене.  Для подключений HTTP/1.0 или HTTP/1.1 Microsoft Edge допускает не более шести одновременных подключений TCP на одном узле.  

### Исправления  

*   Реализуйте сегментирование доменов, если необходимо использовать HTTP/1.0 или HTTP/1.1.  
*   Используйте HTTP/2.  Не используйте сегментирование доменов с протоколом HTTP/2.  
*   Удалите или отложите ненужные запросы, чтобы загрузить критические запросы.  

## Медленное время до первого байта (TTFB)   

### Симптомы  

Запрос тратит много времени на ожидание получения первого байта с сервера.  

На [рисунке 2](#figure-2)длинная Зеленая цветная полоса в **каскаде** указывает на то, что запрос был выполнен в течение длительного времени.  Это было смоделировано с помощью профиля, ограничивающего скорость сети и добавляя задержку.  

> ##### Рисунок 2  
> Пример запроса с медленным временем до получения первого байта  
> ![Пример запроса с медленным временем до получения первого байта][ImageSlowTimeToFirstByte]  

### Причины  

*   Соединение между клиентом и сервером происходит медленно.  
*   Скорость ответа сервера не отвечает.  Разведите сервер на локальный компьютер, чтобы определить, является ли это подключение или медленный сервер.  Если вы по-прежнему получаете очень много времени на первый байт \ (TTFB \) при доступе к локальному серверу, сервер работает медленно.  

### Исправления  

*   Если соединение медленное, разрешите размещение содержимого в сети CDN или изменение поставщиков услуг размещения.  
*   Если сервер работает медленно, рассматривайте запросы к базе данных, реализуйте кэш или изменяйте конфигурацию сервера.  

## Медленная загрузка содержимого   

### Симптомы  

Загрузка запроса занимает много времени.  

На [рисунке 3](#figure-3)длинная синяя полоса в **каскаде** рядом с форматом PNG означает, что загрузка занимает много времени.  

> ##### Рисунок3  
> Пример запроса, загрузка которого занимает много времени  
> ![Пример запроса, загрузка которого занимает много времени][ImageSlowContentDownload]  

### Причины  

*   Соединение между клиентом и сервером происходит медленно.  
*   Загружается много контента.  

### Исправления  

*   Возможно, вы размещаете содержимое в сети CDN или меняете поставщиков услуг размещения.  
*   Уменьшите количество байтов, оптимизируя запросы.  

## Сведения о Contribute  

Есть ли у вас сетевая проблема, которая должна быть добавлена в это руководство?  

*   Отправить твит на [@EdgeDevTools][MicrosoftEdgeTweet].  
*   Нажмите кнопку **Отправить отзыв** ![ отправьте отзыв ][ImageSendFeedbackIcon] в DevTools или нажмите клавиши `Alt` + `Shift` + `I` \ (Windows \) или `Option` + `Shift` + `I` \ (macOS \), чтобы предоставить отзыв или запрос функций.  
*   [Открыть вопрос][WebFundamentalsIssue] в репозитории документов.  

<!--   -->  



<!-- image links -->  

[ImageSendFeedbackIcon]: /microsoft-edge/devtools-guide-chromium/media/smile-icon.msft.png  

[ImageStalled]: /microsoft-edge/devtools-guide-chromium/media/network-network-disabled-cache-resources-queue.msft.png "Рисунок 1: пример последовательности в очереди или на панели "сеть""  
[ImageSlowTimeToFirstByte]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-using-dial-up-profile.msft.png "Рисунок 2: пример запроса с немедленным временем до первого байта"  
[ImageSlowContentDownload]: /microsoft-edge/devtools-guide-chromium/media/network-network-resources-edge-devtools.msft.png "Рисунок 3: пример запроса, загрузка которого занимает много времени"  

<!-- links -->  

[NetworkPerformance]: /microsoft-edge/devtools-guide-chromium/network/index "Проверка активности сети в Microsoft Edge DevTools"  

[MicrosoftEdgeTweet]: https://twitter.com/intent/tweet?text=@EdgeDevTools%20[Network%20Issues%20Guide%20Suggestion]  

[WebFundamentalsIssue]: https://github.com/MicrosoftDocs/edge-developer/issues/new?title=%5BDevTools%20Network%20Issues%20Guide%20Suggestion%5D "Новая ошибка — MicrosoftDocs/Edge-разработчик"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница размещается [здесь](https://developers.google.com/web/tools/chrome-devtools/network/issues) и разрабатывается с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Джонатан-искаженного][JonathanGarbee] (эксперта Google Developer, для Web Technology).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
