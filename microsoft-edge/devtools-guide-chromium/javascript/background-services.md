---
title: Отладка фоновых служб с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 1fecd6f9c1dceb39482bf8c4ade71918e32dec00
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983314"
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





# <span data-ttu-id="c7d26-103">Отладка фоновых служб с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="c7d26-103">Debug Background Services With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="c7d26-104">Раздел " **фоновые службы** " Microsoft Edge DevTools — это набор средств для API JavaScript, который позволяет веб-сайту отправлять и получать обновления даже в том случае, если ваш веб-сайт не открыт.</span><span class="sxs-lookup"><span data-stu-id="c7d26-104">The **Background Services** section of Microsoft Edge DevTools is a collection of tools for the JavaScript APIs that enables your website to send and receive updates even when a user does not have your website open.</span></span>  
<span data-ttu-id="c7d26-105">Фоновая служба функционально напоминает [фоновый процесс] [WikiBackgroundProcess].</span><span class="sxs-lookup"><span data-stu-id="c7d26-105">A background service is functionally similar to a [background process][WikiBackgroundProcess].</span></span>  
<span data-ttu-id="c7d26-106">Microsoft Edge DevTools считает каждый из указанных ниже API фоновой службой.</span><span class="sxs-lookup"><span data-stu-id="c7d26-106">Microsoft Edge DevTools considers each of the following APIs to be a background service:</span></span>  

*   [<span data-ttu-id="c7d26-107">Фоновая выборка</span><span class="sxs-lookup"><span data-stu-id="c7d26-107">Background Fetch</span></span>](#background-fetch)  
*   [<span data-ttu-id="c7d26-108">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="c7d26-108">Background Sync</span></span>](#background-sync)  
*   [<span data-ttu-id="c7d26-109">Уведомления</span><span class="sxs-lookup"><span data-stu-id="c7d26-109">Notifications</span></span>](#notifications)  
*   [<span data-ttu-id="c7d26-110">Push-сообщения</span><span class="sxs-lookup"><span data-stu-id="c7d26-110">Push Messages</span></span>](#push-messages)  
    
<span data-ttu-id="c7d26-111">Microsoft Edge DevTools может записывать события фоновой службы в течение 3 дней, даже если DevTools не открыт.</span><span class="sxs-lookup"><span data-stu-id="c7d26-111">Microsoft Edge DevTools can log background service events for 3 days, even when DevTools is not open.</span></span>  
<span data-ttu-id="c7d26-112">Это поможет вам убедиться в том, что события отправляются и принимаются должным образом.</span><span class="sxs-lookup"><span data-stu-id="c7d26-112">This can help you make sure that events are being sent and received as expected.</span></span>  <span data-ttu-id="c7d26-113">Кроме того, вы можете просмотреть сведения о каждом событии.</span><span class="sxs-lookup"><span data-stu-id="c7d26-113">You may also inspect the details of each event.</span></span>  

:::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
   <span data-ttu-id="c7d26-115">Просмотр сведений о событии в области **Push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="c7d26-115">View the details of an event in the **Push Messaging** pane</span></span>  
:::image-end:::  

## <span data-ttu-id="c7d26-116">Фоновая выборка</span><span class="sxs-lookup"><span data-stu-id="c7d26-116">Background Fetch</span></span>   

<span data-ttu-id="c7d26-117">*Интерфейс API фоновой выборки*\* позволяет **сотруднику службы** надежно загружать большие ресурсы, например фильмы и подкасты, в качестве фоновой службы.</span><span class="sxs-lookup"><span data-stu-id="c7d26-117">The *Background Fetch API*\* enables a **service worker** to reliably download large resources, like movies or podcasts, as a background service.</span></span>  <span data-ttu-id="c7d26-118">Для записи события фоновой выборки в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="c7d26-118">To log Background Fetch event for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background fetch api section when available -->  

1.  <span data-ttu-id="c7d26-119">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c7d26-119">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c7d26-120">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="c7d26-120">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c7d26-121">Открытие области " **Фоновая выборка** ".</span><span class="sxs-lookup"><span data-stu-id="c7d26-121">Open the **Background Fetch** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-empty.msft.png" alt-text="Область "Фоновая выборка"" lightbox="../media/javascript-application-background-services-background-fetch-empty.msft.png":::
       <span data-ttu-id="c7d26-123">Область " **Фоновая выборка** "</span><span class="sxs-lookup"><span data-stu-id="c7d26-123">The **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7d26-124">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c7d26-124">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="c7d26-125">После запуска некоторых операций фоновой выборки DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="c7d26-125">After triggering some Background Fetch activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch.msft.png" alt-text="Журнал событий в области "Фоновая выборка"" lightbox="../media/javascript-application-background-services-background-fetch.msft.png":::
       <span data-ttu-id="c7d26-127">Журнал событий в области " **Фоновая выборка** "</span><span class="sxs-lookup"><span data-stu-id="c7d26-127">A log of events in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7d26-128">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="c7d26-128">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-fetch-details.msft.png" alt-text="Просмотр сведений о событии в области "Фоновая выборка"" lightbox="../media/javascript-application-background-services-background-fetch-details.msft.png":::
       <span data-ttu-id="c7d26-130">Просмотр сведений о событии в области " **Фоновая выборка** "</span><span class="sxs-lookup"><span data-stu-id="c7d26-130">View the details of an event in the **Background Fetch** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c7d26-131">Фоновая синхронизация</span><span class="sxs-lookup"><span data-stu-id="c7d26-131">Background Sync</span></span>   

<span data-ttu-id="c7d26-132">**API фоновой синхронизации** позволяет автономному **рабочему специалисту** отправлять данные на сервер после повторного установления надежного Интернет-соединения.</span><span class="sxs-lookup"><span data-stu-id="c7d26-132">The **Background Sync API** enables an offline **service worker** to send data to a server once it has re-established a reliable internet connection.</span></span>  <span data-ttu-id="c7d26-133">Чтобы записать события фоновой синхронизации в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c7d26-133">To log Background Sync events for 3 days, even when DevTools is not open:</span></span>  

<!--Todo: add background sync api section when available -->  

1.  <span data-ttu-id="c7d26-134">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c7d26-134">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c7d26-135">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="c7d26-135">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c7d26-136">Откройте область **фоновая синхронизация** .</span><span class="sxs-lookup"><span data-stu-id="c7d26-136">Open the **Background Sync** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-empty.msft.png" alt-text="Область "фоновая синхронизация"" lightbox="../media/javascript-application-background-services-background-sync-empty.msft.png":::
       <span data-ttu-id="c7d26-138">Область " **фоновая синхронизация** "</span><span class="sxs-lookup"><span data-stu-id="c7d26-138">The **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7d26-139">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c7d26-139">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="c7d26-140">После запуска некоторых операций синхронизации в фоновом режиме DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="c7d26-140">After triggering some Background Sync activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync.msft.png" alt-text="Журнал событий в области "фоновая синхронизация"" lightbox="../media/javascript-application-background-services-background-sync.msft.png":::
       <span data-ttu-id="c7d26-142">Журнал событий в области " **фоновая синхронизация** "</span><span class="sxs-lookup"><span data-stu-id="c7d26-142">A log of events in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7d26-143">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="c7d26-143">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-background-sync-details.msft.png" alt-text="Просмотр сведений о событии в области фоновой синхронизации" lightbox="../media/javascript-application-background-services-background-sync-details.msft.png":::
       <span data-ttu-id="c7d26-145">Просмотр сведений о событии в области **фоновой синхронизации**</span><span class="sxs-lookup"><span data-stu-id="c7d26-145">View the details of an event in the **Background Sync** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c7d26-146">Уведомления</span><span class="sxs-lookup"><span data-stu-id="c7d26-146">Notifications</span></span> 

<span data-ttu-id="c7d26-147">После того как **сотрудник службы** получил [Push-сообщение][MDNPush] с сервера, сотрудник службы использует [API уведомлений][MDNNotifications] для отображения данных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7d26-147">After a **service worker** has received a [Push Message][MDNPush] from a server, the service worker uses the [Notifications API][MDNNotifications] to display the data to a user.</span></span>  <span data-ttu-id="c7d26-148">Для ведения журнала уведомлений в течение 3 дней, даже если DevTools не открыт:</span><span class="sxs-lookup"><span data-stu-id="c7d26-148">To log Notifications for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="c7d26-149">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c7d26-149">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c7d26-150">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="c7d26-150">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c7d26-151">Открытие области **уведомлений** .</span><span class="sxs-lookup"><span data-stu-id="c7d26-151">Open the **Notifications** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-empty.msft.png" alt-text="Область уведомлений" lightbox="../media/javascript-application-background-services-notifications-empty.msft.png":::
       <span data-ttu-id="c7d26-153">Область **уведомлений**</span><span class="sxs-lookup"><span data-stu-id="c7d26-153">The **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7d26-154">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c7d26-154">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
   <span data-ttu-id="c7d26-155">После запуска некоторых действий с уведомлениями DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="c7d26-155">After triggering some Notifications activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications.msft.png" alt-text="Журнал событий в области уведомлений" lightbox="../media/javascript-application-background-services-notifications.msft.png":::
       <span data-ttu-id="c7d26-157">Журнал событий в области **уведомлений**</span><span class="sxs-lookup"><span data-stu-id="c7d26-157">A log of events in the **Notifications** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7d26-158">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="c7d26-158">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-notifications-details.msft.png" alt-text="Просмотр сведений о событии в области уведомлений" lightbox="../media/javascript-application-background-services-notifications-details.msft.png":::
       <span data-ttu-id="c7d26-160">Просмотр сведений о событии в области **уведомлений**</span><span class="sxs-lookup"><span data-stu-id="c7d26-160">View the details of an event in the **Notifications** pane</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="c7d26-161">Push-сообщения</span><span class="sxs-lookup"><span data-stu-id="c7d26-161">Push Messages</span></span> 

<span data-ttu-id="c7d26-162">Чтобы отобразить push-уведомление для пользователя, **сотрудник службы** должен сначала использовать [API Push-сообщений][MDNPush] для получения данных с сервера.</span><span class="sxs-lookup"><span data-stu-id="c7d26-162">To display a push notification to a user, a **service worker** must first use the [Push Message API][MDNPush] to receive data from a server.</span></span>  <span data-ttu-id="c7d26-163">Когда сотрудник службы готов отобразить уведомление, он использует [API уведомлений][MDNNotifications].</span><span class="sxs-lookup"><span data-stu-id="c7d26-163">When the service worker is ready to display the notification, it uses the [Notifications API][MDNNotifications].</span></span>  <span data-ttu-id="c7d26-164">Чтобы регистрировать push-сообщения в течение 3 дней, даже если DevTools не открыт, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="c7d26-164">To log Push Messages for 3 days, even when DevTools is not open:</span></span>  

1.  <span data-ttu-id="c7d26-165">[Откройте DevTools][OpenDevTools].</span><span class="sxs-lookup"><span data-stu-id="c7d26-165">[Open DevTools][OpenDevTools].</span></span>  
1.  <span data-ttu-id="c7d26-166">Откройте панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="c7d26-166">Open the **Application** panel.</span></span>  
1.  <span data-ttu-id="c7d26-167">Открыть область **Push-сообщений** .</span><span class="sxs-lookup"><span data-stu-id="c7d26-167">Open the **Push Messaging** pane.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-empty.msft.png" alt-text="Область Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-empty.msft.png":::
       <span data-ttu-id="c7d26-169">Область **Push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="c7d26-169">The **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7d26-170">Нажмите **запись** \ ( ![ запись ][ImageRecordIcon] \).</span><span class="sxs-lookup"><span data-stu-id="c7d26-170">Click **Record** \(![Record][ImageRecordIcon]\).</span></span>  
    <span data-ttu-id="c7d26-171">После запуска некоторых действий Push-сообщений DevTools регистрирует события в таблице.</span><span class="sxs-lookup"><span data-stu-id="c7d26-171">After triggering some Push Message activity, DevTools logs the events to the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging.msft.png" alt-text="Журнал событий в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging.msft.png":::
       <span data-ttu-id="c7d26-173">Журнал событий в области Push- **сообщений**</span><span class="sxs-lookup"><span data-stu-id="c7d26-173">A log of events in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="c7d26-174">Щелкните событие, чтобы просмотреть сведения о нем в пространстве под таблицей.</span><span class="sxs-lookup"><span data-stu-id="c7d26-174">Click an event to view its details in the space below the table.</span></span>  
    
    :::image type="complex" source="../media/javascript-application-background-services-push-messaging-details.msft.png" alt-text="Просмотр сведений о событии в области Push-сообщений" lightbox="../media/javascript-application-background-services-push-messaging-details.msft.png":::
       <span data-ttu-id="c7d26-176">Просмотр сведений о событии в области **Push-сообщений**</span><span class="sxs-lookup"><span data-stu-id="c7d26-176">View the details of an event in the **Push Messaging** pane</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageRecordIcon]: ../media/record-icon.msft.png  

<!-- links -->  

<!--[BackgroundFetchAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2018/12/background-fetch.md "Background Fetch API"  -->  
<!--[BackgroundSyncAPI]: ../../../microsoft-edge/devtools-guide-chromium/whats-new/2015/12/background-sync.md  "Background Sync API"  -->

[OpenDevTools]: ../open.md "Открытие средств разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[MDNNotifications]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNPush]: https://developer.mozilla.org/docs/Web/API/Push_API "API push-уведомлений | MDN"  
<!--[ServiceWorkerCacheStorage]: https://alphabet.dev/service-workers-cache-storage "Service workers and the Cache Storage API | alphabet.dev"  -->
[WikiBackgroundProcess]: https://en.wikipedia.org/wiki/Background_process "фоновый процесс — Википедии"  

> [!NOTE]
> <span data-ttu-id="c7d26-181">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c7d26-181">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c7d26-182">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="c7d26-182">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/javascript/background-services) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  
[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="c7d26-184">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c7d26-184">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
