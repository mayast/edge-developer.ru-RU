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





# <span data-ttu-id="c414f-103">Отладка фоновых служб с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c414f-103">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c414f-104">Раздел " **фоновые службы** " Microsoft Edge DevTools — это набор средств для API JavaScript, который позволяет веб-сайту отправлять и получать обновления даже в том случае, если ваш веб-сайт не открыт.</span><span class="sxs-lookup"><span data-stu-id="c414f-104">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="c414f-105">Фоновая служба функционально напоминает [фоновый процесс] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="c414f-105">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="c414f-106">Microsoft Edge DevTools считает каждый из указанных ниже API фоновой службой.</span><span class="sxs-lookup"><span data-stu-id="c414f-106">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="c414f-107">Фоновая выборка</span><span class="sxs-lookup"><span data-stu-id="c414f-107">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="c414f-108">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="c414f-108">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="c414f-109">Уведомления</span><span class="sxs-lookup"><span data-stu-id="c414f-109">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="c414f-110">Push-сообщения</span><span class="sxs-lookup"><span data-stu-id="c414f-110">Push Messages</span></span>](#push-messages)  

<span data-ttu-id="c414f-111">Microsoft Edge DevTools может записывать события фоновой службы в течение 3 дней, даже если DevTools не открыт.</span><span class="sxs-lookup"><span data-stu-id="c414f-111">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="c414f-112">Это поможет вам убедиться в том, что события отправляются и принимаются должным образом.</span><span class="sxs-lookup"><span data-stu-id="c414f-112">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="c414f-113">Вы также можете просмотреть сведения о каждом событии.</span><span class="sxs-lookup"><span data-stu-id="c414f-113">You can also inspect the details of each event.</span></span>  

> ##### <span data-ttu-id="c414f-114">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="c414f-114">Figure 1</span></span>  
> <span data-ttu-id="c414f-115">Просмотр сведений о событии в области Push-сообщений</span><span class="sxs-lookup"><span data-stu-id="c414f-115">Viewing the details of an event in the Push Messaging pane</span></span>  
> ![Просмотр сведений о событии в области Push-сообщений][PushDetails]  

## <span data-ttu-id="c414f-117">Фоновая выборка</span><span class="sxs-lookup"><span data-stu-id="c414f-117">Background Fetch</span></span>   

<span data-ttu-id="c414f-118">*Интерфейс API фоновой выборки*\* позволяет **сотруднику службы** надежно загружать большие ресурсы, например фильмы и подкасты, в качестве фоновой службы.</span><span class="sxs-lookup"><span data-stu-id="c414f-118">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="c414f-119">Для записи события фоновой выборки в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="c414f-119">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="c414f-120">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c414f-120">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c414f-121">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="c414f-121">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c414f-122">Открытие области " **Фоновая выборка** ".</span><span class="sxs-lookup"><span data-stu-id="c414f-122">Open the **Background Fetch** pane.</span></span>  
    
    > ##### <span data-ttu-id="c414f-123">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="c414f-123">Figure 2</span></span>  
    > <span data-ttu-id="c414f-124">Область "Фоновая выборка"</span><span class="sxs-lookup"><span data-stu-id="c414f-124">The Background Fetch pane</span></span>  
    > ![Область "Фоновая выборка"][FetchEmpty]  
    
1.  <span data-ttu-id="c414f-126">Нажмите **кнопку запись** ![ ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="c414f-126">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="c414f-127">После запуска некоторых операций фоновой выборки DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="c414f-127">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="c414f-128">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="c414f-128">Figure 3</span></span>  
    > <span data-ttu-id="c414f-129">Журнал событий в области "Фоновая выборка"</span><span class="sxs-lookup"><span data-stu-id="c414f-129">A log of events in the Background Fetch pane</span></span>  
    > ![Журнал событий в области "Фоновая выборка"][FetchLog]  
    
1.  <span data-ttu-id="c414f-131">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="c414f-131">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="c414f-132">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="c414f-132">Figure 4</span></span>  
    > <span data-ttu-id="c414f-133">Просмотр сведений о событии в области "Фоновая выборка"</span><span class="sxs-lookup"><span data-stu-id="c414f-133">Viewing the details of an event in the Background Fetch pane</span></span>  
    > ![Просмотр сведений о событии в области "Фоновая выборка"][FetchDetails]  

## <span data-ttu-id="c414f-135">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="c414f-135">Background Sync</span></span>   

<span data-ttu-id="c414f-136">**API фоновой синхронизации** позволяет автономному **рабочему специалисту** отправлять данные на сервер после повторного установления надежного Интернет-соединения.</span><span class="sxs-lookup"><span data-stu-id="c414f-136">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="c414f-137">Чтобы записать события фоновой синхронизации в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c414f-137">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="c414f-138">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c414f-138">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c414f-139">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="c414f-139">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c414f-140">Откройте область **фоновая синхронизация** .</span><span class="sxs-lookup"><span data-stu-id="c414f-140">Open the **Background Sync** pane.</span></span>  
    
    > ##### <span data-ttu-id="c414f-141">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="c414f-141">Figure 5</span></span>  
    > <span data-ttu-id="c414f-142">Область "фоновая синхронизация"</span><span class="sxs-lookup"><span data-stu-id="c414f-142">The Background Sync pane</span></span>  
    > ![Область "фоновая синхронизация"][SyncEmpty]  
    
1.  <span data-ttu-id="c414f-144">Нажмите **кнопку запись** ![ ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="c414f-144">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="c414f-145">После запуска некоторых операций синхронизации в фоновом режиме DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="c414f-145">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="c414f-146">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="c414f-146">Figure 6</span></span>  
    > <span data-ttu-id="c414f-147">Журнал событий в области "фоновая синхронизация"</span><span class="sxs-lookup"><span data-stu-id="c414f-147">A log of events in the Background Sync pane</span></span>  
    > ![Журнал событий в области "фоновая синхронизация"][SyncLog]  
    
1.  <span data-ttu-id="c414f-149">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="c414f-149">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="c414f-150">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="c414f-150">Figure 7</span></span>  
    > <span data-ttu-id="c414f-151">Просмотр сведений о событии в области "фоновая синхронизация"</span><span class="sxs-lookup"><span data-stu-id="c414f-151">Viewing the details of an event in the Background Sync pane</span></span>  
    > ![Просмотр сведений о событии в области "фоновая синхронизация"][SyncDetails]  
    
## <span data-ttu-id="c414f-153">Уведомления</span><span class="sxs-lookup"><span data-stu-id="c414f-153">Notifications</span></span> 

<span data-ttu-id="c414f-154">После того как **сотрудник службы** получил [Push-сообщение][MDNPush] с сервера, сотрудник службы использует [API уведомлений][MDNNotifications] для отображения данных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c414f-154">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="c414f-155">Для ведения журнала уведомлений в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="c414f-155">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="c414f-156">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c414f-156">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c414f-157">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="c414f-157">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c414f-158">Открытие области **уведомлений** .</span><span class="sxs-lookup"><span data-stu-id="c414f-158">Open the **Notifications** pane.</span></span>  
    
    > ##### <span data-ttu-id="c414f-159">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="c414f-159">Figure 8</span></span>  
    > <span data-ttu-id="c414f-160">Область уведомлений</span><span class="sxs-lookup"><span data-stu-id="c414f-160">The Notifications pane</span></span>  
    > ![Область уведомлений][NotificationsEmpty]  
    
1.  <span data-ttu-id="c414f-162">Нажмите **кнопку запись** ![ ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="c414f-162">Click **Record** ![Record][ImageRecordIcon].</span></span>  
   <span data-ttu-id="c414f-163">После запуска некоторых действий с уведомлениями DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="c414f-163">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="c414f-164">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="c414f-164">Figure 9</span></span>  
    > <span data-ttu-id="c414f-165">Журнал событий в области уведомлений</span><span class="sxs-lookup"><span data-stu-id="c414f-165">A log of events in the Notifications pane</span></span>  
    > ![Журнал событий в области уведомлений][NotificationsLog]  
    
1.  <span data-ttu-id="c414f-167">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="c414f-167">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="c414f-168">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="c414f-168">Figure 10</span></span>  
    > <span data-ttu-id="c414f-169">Просмотр сведений о событии в области уведомлений</span><span class="sxs-lookup"><span data-stu-id="c414f-169">Viewing the details of an event in the Notifications pane</span></span>  
    > ![Просмотр сведений о событии в области уведомлений][NotificationsDetails]  
    
## <span data-ttu-id="c414f-171">Push-сообщения</span><span class="sxs-lookup"><span data-stu-id="c414f-171">Push Messages</span></span> 

<span data-ttu-id="c414f-172">Чтобы отобразить push-уведомление для пользователя, **сотрудник службы** должен сначала использовать [API Push-сообщений][MDNPush] для получения данных с сервера.</span><span class="sxs-lookup"><span data-stu-id="c414f-172">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="c414f-173">Когда сотрудник службы готов отобразить уведомление, он использует [API уведомлений][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="c414f-173">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="c414f-174">Чтобы регистрировать push-сообщения в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c414f-174">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="c414f-175">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c414f-175">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c414f-176">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="c414f-176">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c414f-177">Открыть область **Push-сообщений** .</span><span class="sxs-lookup"><span data-stu-id="c414f-177">Open the **Push Messaging** pane.</span></span>  
    
    > ##### <span data-ttu-id="c414f-178">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="c414f-178">Figure 11</span></span>  
    > <span data-ttu-id="c414f-179">Область Push-сообщений</span><span class="sxs-lookup"><span data-stu-id="c414f-179">The Push Messaging pane</span></span>  
    > ![Область Push-сообщений][PushEmpty]  

1.  <span data-ttu-id="c414f-181">Нажмите **кнопку запись** ![ ][ImageRecordIcon] .</span><span class="sxs-lookup"><span data-stu-id="c414f-181">Click **Record** ![Record][ImageRecordIcon].</span></span>  
    <span data-ttu-id="c414f-182">После запуска некоторых действий Push-сообщений DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="c414f-182">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    > ##### <span data-ttu-id="c414f-183">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="c414f-183">Figure 12</span></span>  
    > <span data-ttu-id="c414f-184">Журнал событий в области Push-сообщений</span><span class="sxs-lookup"><span data-stu-id="c414f-184">A log of events in the Push Messaging pane</span></span>  
    > ![Журнал событий в области Push-сообщений][PushLog]  

1.  <span data-ttu-id="c414f-186">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="c414f-186">Click an event to view its details in the space below the table.</span></span>  
    
    > ##### <span data-ttu-id="c414f-187">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="c414f-187">Figure 13</span></span>  
    > <span data-ttu-id="c414f-188">Просмотр сведений о событии в области Push-сообщений</span><span class="sxs-lookup"><span data-stu-id="c414f-188">Viewing the details of an event in the Push Messaging pane</span></span>  
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
> <span data-ttu-id="c414f-207">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c414f-207">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c414f-208">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c414f-208">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c414f-210">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c414f-210">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
