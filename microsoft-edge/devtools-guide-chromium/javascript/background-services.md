---
title: Отладка фоновых служб с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 0ac2a057307a939069cbb3b48ecd38c9de71e5db
ms.sourcegitcommit: ecdc4287fa25a18cb4ddcaf43fcce3b396c3314c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/17/2020
ms.locfileid: "10581833"
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





# Отладка фоновых служб с помощью Microsoft Edge DevTools   



Раздел " **фоновые службы** " Microsoft Edge DevTools — это набор средств для API JavaScript, который позволяет веб-сайту отправлять и получать обновления даже в том случае, если ваш веб-сайт не открыт.  
Фоновая служба функционально напоминает [фоновый процесс] [WikiBackgroundProcess].  
Microsoft Edge DevTools считает каждый из указанных ниже API фоновой службой.  

*   [Фоновая выборка](#background-fetch)  
*   [Фоновая синхронизация](#background-sync)  
*   [Уведомления](#notifications)  
*   [Push-сообщения](#push-messages)  

Microsoft Edge DevTools может записывать события фоновой службы в течение 3 дней, даже если DevTools не открыт.  
Это поможет вам убедиться в том, что события отправляются и принимаются должным образом.  Вы также можете просмотреть сведения о каждом событии.  

> ##### Рис. 1  
> Просмотр сведений о событии в области Push-сообщений  
> ![Просмотр сведений о событии в области Push-сообщений][PushDetails]  

## Фоновая выборка   

*Интерфейс API фоновой выборки** позволяет **сотруднику службы** надежно загружать большие ресурсы, например фильмы и подкасты, в качестве фоновой службы.  Для записи события фоновой выборки в течение 3 дней, даже если DevTools не открыт:  

<!--Todo: add background fetch api section when available -->  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте панель **приложения** .  
1.  Открытие области " **Фоновая выборка** ".  
    
    > ##### Рисунок 2  
    > Область "Фоновая выборка"  
    > ![Область "Фоновая выборка"][FetchEmpty]  
    
1.  Нажмите **кнопку запись** ![ ][ImageRecordIcon] .  
   После запуска некоторых операций фоновой выборки DevTools регистрирует события в таблице.  
    
    > ##### Рисунок3  
    > Журнал событий в области "Фоновая выборка"  
    > ![Журнал событий в области "Фоновая выборка"][FetchLog]  
    
1.  Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.  
    
    > ##### Рисунок4  
    > Просмотр сведений о событии в области "Фоновая выборка"  
    > ![Просмотр сведений о событии в области "Фоновая выборка"][FetchDetails]  

## Фоновая синхронизация   

**API фоновой синхронизации** позволяет автономному **рабочему специалисту** отправлять данные на сервер после повторного установления надежного Интернет-соединения.  Чтобы записать события фоновой синхронизации в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.  

<!--Todo: add background sync api section when available -->  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте панель **приложения** .  
1.  Откройте область **фоновая синхронизация** .  
    
    > ##### Рисунок 5  
    > Область "фоновая синхронизация"  
    > ![Область "фоновая синхронизация"][SyncEmpty]  
    
1.  Нажмите **кнопку запись** ![ ][ImageRecordIcon] .  
   После запуска некоторых операций синхронизации в фоновом режиме DevTools регистрирует события в таблице.  
    
    > ##### Рисунок6  
    > Журнал событий в области "фоновая синхронизация"  
    > ![Журнал событий в области "фоновая синхронизация"][SyncLog]  
    
1.  Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.  
    
    > ##### Рисунок7  
    > Просмотр сведений о событии в области "фоновая синхронизация"  
    > ![Просмотр сведений о событии в области "фоновая синхронизация"][SyncDetails]  
    
## Уведомления 

После того как **сотрудник службы** получил [Push-сообщение][MDNPush] с сервера, сотрудник службы использует [API уведомлений][MDNNotifications] для отображения данных для пользователя.  Для ведения журнала уведомлений в течение 3 дней, даже если DevTools не открыт:  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте панель **приложения** .  
1.  Открытие области **уведомлений** .  
    
    > ##### Рисунок8  
    > Область уведомлений  
    > ![Область уведомлений][NotificationsEmpty]  
    
1.  Нажмите **кнопку запись** ![ ][ImageRecordIcon] .  
   После запуска некоторых действий с уведомлениями DevTools регистрирует события в таблице.  
    
    > ##### Рисунок9  
    > Журнал событий в области уведомлений  
    > ![Журнал событий в области уведомлений][NotificationsLog]  
    
1.  Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.  
    
    > ##### Рисунок 10  
    > Просмотр сведений о событии в области уведомлений  
    > ![Просмотр сведений о событии в области уведомлений][NotificationsDetails]  
    
## Push-сообщения 

Чтобы отобразить push-уведомление для пользователя, **сотрудник службы** должен сначала использовать [API Push-сообщений][MDNPush] для получения данных с сервера.  Когда сотрудник службы готов отобразить уведомление, он использует [API уведомлений][MDNNotifications].  Чтобы регистрировать push-сообщения в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.  

1.  [Откройте DevTools][OpenDevTools].  
1.  Откройте панель **приложения** .  
1.  Открыть область **Push-сообщений** .  
    
    > ##### Рисунок11  
    > Область Push-сообщений  
    > ![Область Push-сообщений][PushEmpty]  

1.  Нажмите **кнопку запись** ![ ][ImageRecordIcon] .  
    После запуска некоторых действий Push-сообщений DevTools регистрирует события в таблице.  
    
    > ##### Рисунок12  
    > Журнал событий в области Push-сообщений  
    > ![Журнал событий в области Push-сообщений][PushLog]  

1.  Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.  
    
    > ##### Рисунок13  
    > Просмотр сведений о событии в области Push-сообщений  
    > ![Просмотр сведений о событии в области Push-сообщений][PushDetails2]  
    
 



<!-- image links -->  

[ImageRecordIcon]: /microsoft-edge/devtools-guide-chromium/media/record-icon.msft.png  

[PushDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Рисунок 1: Просмотр сведений о событии в области Push-сообщений"  
[FetchEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-empty.msft.png "Рисунок 2: область "Фоновая выборка""  
[FetchLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch.msft.png "Рисунок 3: журнал событий в области "Фоновая выборка""  
[FetchDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-fetch-details.msft.png "Рисунок 4: Просмотр сведений о событии в области "Фоновая выборка""  
[SyncEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-empty.msft.png "Рисунок 5: область "фоновая синхронизация""  
[SyncLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync.msft.png "Рисунок 6: журнал событий в области "фоновая синхронизация""  
[SyncDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-background-sync-details.msft.png "Рисунок 7: Просмотр сведений о событии в области "фоновая синхронизация""  
[NotificationsEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-empty.msft.png "Рисунок 8: область уведомлений"  
[NotificationsLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications.msft.png "Рисунок 9: журнал событий в области уведомлений"  
[NotificationsDetails]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-notifications-details.msft.png "Рисунок 10: Просмотр сведений о событии в области уведомлений"  
[PushEmpty]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-empty.msft.png "Рисунок 11: область Push-сообщений"  
[PushLog]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging.msft.png "Рисунок 12: журнал событий в области Push-сообщений"  
[PushDetails2]: /microsoft-edge/devtools-guide-chromium/media/javascript-application-background-services-push-messaging-details.msft.png "Рисунок 13: Просмотр сведений о событии в области Push-сообщений"  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Средства разработчика Open Microsoft EDGE (Chromium)"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API push-уведомлений | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "фоновый процесс — Википедии"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
