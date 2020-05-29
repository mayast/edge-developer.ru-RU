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





# <span data-ttu-id="eb0c9-103">Руководство по сетевым проблемам</span><span class="sxs-lookup"><span data-stu-id="eb0c9-103">Network Issues Guide</span></span>   




<span data-ttu-id="eb0c9-104">В этом руководстве показано, как определить сетевые проблемы или возможности оптимизации на панели "сеть" Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-104">This guide shows you how to detect network issues or optimization opportunities in the Network panel of Microsoft Edge DevTools.</span></span>  

<span data-ttu-id="eb0c9-105">Ознакомьтесь со [статьей][NetworkPerformance] "Начало работы", чтобы ознакомиться с основными понятиями панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="eb0c9-105">See [Get Started][NetworkPerformance] to learn the basics of the Network panel.</span></span>  

## <span data-ttu-id="eb0c9-106">Запросы, поставленные в очередь или остановленные</span><span class="sxs-lookup"><span data-stu-id="eb0c9-106">Queued or stalled requests</span></span>   

### <span data-ttu-id="eb0c9-107">Симптомы</span><span class="sxs-lookup"><span data-stu-id="eb0c9-107">Symptoms</span></span>  

<span data-ttu-id="eb0c9-108">Шесть запросов загружаются одновременно.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-108">Six requests are downloading simultaneously.</span></span>  <span data-ttu-id="eb0c9-109">После этого серии запросов будут помещены в очередь или остановлены.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-109">After that, a series of requests are queued or stalled.</span></span>  <span data-ttu-id="eb0c9-110">После завершения одного из шести первых запросов запускается один из запросов в очереди.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-110">Once one of the first six requests finishes, one of the requests in the queue starts.</span></span>  

<span data-ttu-id="eb0c9-111">На **каскаде** на [рисунке 1](#figure-1)первые шесть запросов `edge-iconx1024.msft.png` актива запускаются одновременно.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-111">In the **Waterfall** in [Figure 1](#figure-1), the first six requests for the `edge-iconx1024.msft.png` asset start simultaneously.</span></span>  <span data-ttu-id="eb0c9-112">Последующие запросы загружаются до тех пор, пока не завершится один из этих шести первоначальных элементов.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-112">The subsequent requests are stalled until one of the original six finishes.</span></span>  

> ##### <span data-ttu-id="eb0c9-113">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="eb0c9-113">Figure 1</span></span>  
> <span data-ttu-id="eb0c9-114">Пример списка в очереди или остановленного ряда на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="eb0c9-114">An example of a queued or stalled series in the Network panel</span></span>  
> ![Пример списка в очереди или остановленного ряда на панели "сеть"][ImageStalled]  

### <span data-ttu-id="eb0c9-116">Причины</span><span class="sxs-lookup"><span data-stu-id="eb0c9-116">Causes</span></span>  

<span data-ttu-id="eb0c9-117">Слишком много запросов выполняется в одном домене.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-117">Too many requests are being made on a single domain.</span></span>  <span data-ttu-id="eb0c9-118">Для подключений HTTP/1.0 или HTTP/1.1 Microsoft Edge допускает не более шести одновременных подключений TCP на одном узле.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-118">On HTTP/1.0 or HTTP/1.1 connections, Microsoft Edge allows a maximum of six simultaneous TCP connections per host.</span></span>  

### <span data-ttu-id="eb0c9-119">Исправления</span><span class="sxs-lookup"><span data-stu-id="eb0c9-119">Fixes</span></span>  

*   <span data-ttu-id="eb0c9-120">Реализуйте сегментирование доменов, если необходимо использовать HTTP/1.0 или HTTP/1.1.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-120">Implement domain sharding if you must use HTTP/1.0 or HTTP/1.1.</span></span>  
*   <span data-ttu-id="eb0c9-121">Используйте HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-121">Use HTTP/2.</span></span>  <span data-ttu-id="eb0c9-122">Не используйте сегментирование доменов с протоколом HTTP/2.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-122">Do not use domain sharding with HTTP/2.</span></span>  
*   <span data-ttu-id="eb0c9-123">Удалите или отложите ненужные запросы, чтобы загрузить критические запросы.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-123">Remove or defer unnecessary requests so that critical requests download earlier.</span></span>  

## <span data-ttu-id="eb0c9-124">Медленное время до первого байта (TTFB)</span><span class="sxs-lookup"><span data-stu-id="eb0c9-124">Slow Time To First Byte (TTFB)</span></span>   

### <span data-ttu-id="eb0c9-125">Симптомы</span><span class="sxs-lookup"><span data-stu-id="eb0c9-125">Symptoms</span></span>  

<span data-ttu-id="eb0c9-126">Запрос тратит много времени на ожидание получения первого байта с сервера.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-126">A request spends a long time waiting to receive the first byte from the server.</span></span>  

<span data-ttu-id="eb0c9-127">На [рисунке 2](#figure-2)длинная Зеленая цветная полоса в **каскаде** указывает на то, что запрос был выполнен в течение длительного времени.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-127">In [Figure 2](#figure-2), the long, green bar in the **Waterfall** indicates that the request was waiting a long time.</span></span>  <span data-ttu-id="eb0c9-128">Это было смоделировано с помощью профиля, ограничивающего скорость сети и добавляя задержку.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-128">This was simulated using a profile to restrict network speed and add a delay.</span></span>  

> ##### <span data-ttu-id="eb0c9-129">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="eb0c9-129">Figure 2</span></span>  
> <span data-ttu-id="eb0c9-130">Пример запроса с медленным временем до получения первого байта</span><span class="sxs-lookup"><span data-stu-id="eb0c9-130">An example of a request with a slow Time To First Byte</span></span>  
> ![Пример запроса с медленным временем до получения первого байта][ImageSlowTimeToFirstByte]  

### <span data-ttu-id="eb0c9-132">Причины</span><span class="sxs-lookup"><span data-stu-id="eb0c9-132">Causes</span></span>  

*   <span data-ttu-id="eb0c9-133">Соединение между клиентом и сервером происходит медленно.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-133">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="eb0c9-134">Скорость ответа сервера не отвечает.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-134">The server is slow to respond.</span></span>  <span data-ttu-id="eb0c9-135">Разведите сервер на локальный компьютер, чтобы определить, является ли это подключение или медленный сервер.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-135">Host the server locally to determine if it is the connection or server that is slow.</span></span>  <span data-ttu-id="eb0c9-136">Если вы по-прежнему получаете очень много времени на первый байт \ (TTFB \) при доступе к локальному серверу, сервер работает медленно.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-136">If you still get a slow Time To First Byte \(TTFB\) when accessing a local server, then the server is slow.</span></span>  

### <span data-ttu-id="eb0c9-137">Исправления</span><span class="sxs-lookup"><span data-stu-id="eb0c9-137">Fixes</span></span>  

*   <span data-ttu-id="eb0c9-138">Если соединение медленное, разрешите размещение содержимого в сети CDN или изменение поставщиков услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-138">If the connection is slow, consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="eb0c9-139">Если сервер работает медленно, рассматривайте запросы к базе данных, реализуйте кэш или изменяйте конфигурацию сервера.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-139">If the server is slow, consider optimizing database queries, implementing a cache, or modifying your server configuration.</span></span>  

## <span data-ttu-id="eb0c9-140">Медленная загрузка содержимого</span><span class="sxs-lookup"><span data-stu-id="eb0c9-140">Slow content download</span></span>   

### <span data-ttu-id="eb0c9-141">Симптомы</span><span class="sxs-lookup"><span data-stu-id="eb0c9-141">Symptoms</span></span>  

<span data-ttu-id="eb0c9-142">Загрузка запроса занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-142">A request takes a long time to download.</span></span>  

<span data-ttu-id="eb0c9-143">На [рисунке 3](#figure-3)длинная синяя полоса в **каскаде** рядом с форматом PNG означает, что загрузка занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-143">In [Figure 3](#figure-3), the long, blue bar in the **Waterfall** next to the png means it took a long time to download.</span></span>  

> ##### <span data-ttu-id="eb0c9-144">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="eb0c9-144">Figure 3</span></span>  
> <span data-ttu-id="eb0c9-145">Пример запроса, загрузка которого занимает много времени</span><span class="sxs-lookup"><span data-stu-id="eb0c9-145">An example of a request that takes a long time to download</span></span>  
> ![Пример запроса, загрузка которого занимает много времени][ImageSlowContentDownload]  

### <span data-ttu-id="eb0c9-147">Причины</span><span class="sxs-lookup"><span data-stu-id="eb0c9-147">Causes</span></span>  

*   <span data-ttu-id="eb0c9-148">Соединение между клиентом и сервером происходит медленно.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-148">The connection between the client and server is slow.</span></span>  
*   <span data-ttu-id="eb0c9-149">Загружается много контента.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-149">A lot of content is being downloaded.</span></span>  

### <span data-ttu-id="eb0c9-150">Исправления</span><span class="sxs-lookup"><span data-stu-id="eb0c9-150">Fixes</span></span>  

*   <span data-ttu-id="eb0c9-151">Возможно, вы размещаете содержимое в сети CDN или меняете поставщиков услуг размещения.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-151">Consider hosting your content on a CDN or changing hosting providers.</span></span>  
*   <span data-ttu-id="eb0c9-152">Уменьшите количество байтов, оптимизируя запросы.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-152">Send fewer bytes by optimizing your requests.</span></span>  

## <span data-ttu-id="eb0c9-153">Сведения о Contribute</span><span class="sxs-lookup"><span data-stu-id="eb0c9-153">Contribute knowledge</span></span>  

<span data-ttu-id="eb0c9-154">Есть ли у вас сетевая проблема, которая должна быть добавлена в это руководство?</span><span class="sxs-lookup"><span data-stu-id="eb0c9-154">Do you have a network issue that should be added to this guide?</span></span>  

*   <span data-ttu-id="eb0c9-155">Отправить твит на [@EdgeDevTools][MicrosoftEdgeTweet].</span><span class="sxs-lookup"><span data-stu-id="eb0c9-155">Send a tweet to [@EdgeDevTools][MicrosoftEdgeTweet].</span></span>  
*   <span data-ttu-id="eb0c9-156">Нажмите кнопку **Отправить отзыв** ![ отправьте отзыв ][ImageSendFeedbackIcon] в DevTools или нажмите клавиши `Alt` + `Shift` + `I` \ (Windows \) или `Option` + `Shift` + `I` \ (macOS \), чтобы предоставить отзыв или запрос функций.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-156">Select **Send Feedback** ![Send Feedback][ImageSendFeedbackIcon] in the DevTools or press `Alt`+`Shift`+`I` \(Windows\) or `Option`+`Shift`+`I` \(macOS\) to provide feedback or feature requests.</span></span>  
*   <span data-ttu-id="eb0c9-157">[Открыть вопрос][WebFundamentalsIssue] в репозитории документов.</span><span class="sxs-lookup"><span data-stu-id="eb0c9-157">[Open an issue][WebFundamentalsIssue] on the docs repo.</span></span>  

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
> <span data-ttu-id="eb0c9-163">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eb0c9-163">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="eb0c9-164">Исходная страница размещается [здесь](https://developers.google.com/web/tools/chrome-devtools/network/issues) и разрабатывается с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \) и [Джонатан-искаженного][JonathanGarbee] (эксперта Google Developer, для Web Technology).</span><span class="sxs-lookup"><span data-stu-id="eb0c9-164">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/issues) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\) and [Jonathan Garbee][JonathanGarbee] \(Google Developer Expert for Web Technology\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="eb0c9-166">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="eb0c9-166">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
[JonathanGarbee]: https://developers.google.com/web/resources/contributors/jonathangarbee
