---
title: Общие сведения о проблемах с безопасностью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 05112d5270f41ce83daa935b8137c4a773ad25a0
ms.sourcegitcommit: 4c24edbd1c591914cb4109511534851570a614cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611912"
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





# <span data-ttu-id="38884-103">Общие сведения о проблемах с безопасностью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="38884-103">Understand Security Issues With Microsoft Edge DevTools</span></span>   

  

<!--Use the **Security** Panel in [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to make sure HTTPS is properly implemented on a page.  See **Why HTTPS Matters** to learn why every website should be protected with HTTPS, even sites that do not handle sensitive user data.  -->  

<!--todo: add section when why-https is available -->  

## <span data-ttu-id="38884-104">Открытие панели безопасности</span><span class="sxs-lookup"><span data-stu-id="38884-104">Open the Security panel</span></span>   

<span data-ttu-id="38884-105">Панель **безопасности** — это основное место в DevTools для проверки безопасности страницы.</span><span class="sxs-lookup"><span data-stu-id="38884-105">The **Security** panel is the main place in DevTools for inspecting the security of a page.</span></span>  

1.  <span data-ttu-id="38884-106">[Откройте DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="38884-106">[Open DevTools][DevToolsOpen].</span></span>  

1.  <span data-ttu-id="38884-107">Щелкните вкладку " **Безопасность** ", чтобы открыть панель " **Безопасность** ".</span><span class="sxs-lookup"><span data-stu-id="38884-107">Click the **Security** tab to open the **Security** panel.</span></span>  
    
    > ##### <span data-ttu-id="38884-108">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="38884-108">Figure 1</span></span>  
    > <span data-ttu-id="38884-109">Панель "безопасность"</span><span class="sxs-lookup"><span data-stu-id="38884-109">The Security panel</span></span>  
    > ![Панель "безопасность"][ImageSecurityPanel]  
    
## <span data-ttu-id="38884-111">Распространенные проблемы</span><span class="sxs-lookup"><span data-stu-id="38884-111">Common problems</span></span>   

### <span data-ttu-id="38884-112">Небезопасные основные источники</span><span class="sxs-lookup"><span data-stu-id="38884-112">Non-secure main origins</span></span>   

<span data-ttu-id="38884-113">Если основной источник страницы небезопасен, в **обзоре безопасности** указано, что **Эта страница не является безопасной**.</span><span class="sxs-lookup"><span data-stu-id="38884-113">When the main origin of a page is not secure, the **Security Overview** says **This page is not secure**.</span></span>  

> ##### <span data-ttu-id="38884-114">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="38884-114">Figure 2</span></span>  
> <span data-ttu-id="38884-115">Небезопасная страница</span><span class="sxs-lookup"><span data-stu-id="38884-115">A non-secure page</span></span>  
> ![Небезопасная страница][ImageNonSecurePage]  

<span data-ttu-id="38884-117">Эта проблема возникает, когда ваш URL-адрес, который вы посещали, запрашивался по протоколу HTTP.</span><span class="sxs-lookup"><span data-stu-id="38884-117">This problem occurs when the URL that you visited was requested over HTTP.</span></span>  <span data-ttu-id="38884-118">Для обеспечения безопасности необходимо запросить его по протоколу HTTPS.</span><span class="sxs-lookup"><span data-stu-id="38884-118">To make it secure you need to request it over HTTPS.</span></span>  <span data-ttu-id="38884-119">Например, если вы посмотрите на URL-адрес в адресной строке, скорее всего, он выглядит примерно так `http://example.com` .</span><span class="sxs-lookup"><span data-stu-id="38884-119">For example, if you look at the URL in your address bar, it probably looks similar to `http://example.com`.</span></span>  <span data-ttu-id="38884-120">Чтобы защитить этот URL-адрес, сделайте это `https://example.com` .</span><span class="sxs-lookup"><span data-stu-id="38884-120">To make it secure the URL should be `https://example.com`.</span></span>  

<span data-ttu-id="38884-121">Если вы уже настроили HTTPS на сервере, все, что нужно сделать, чтобы устранить эту проблему, — настроить сервер для перенаправления всех HTTP-запросов на HTTPS.</span><span class="sxs-lookup"><span data-stu-id="38884-121">If you already set up HTTPS on your server, all you need to do to fix this problem is configure your server to redirect all HTTP requests to HTTPS.</span></span>  

<span data-ttu-id="38884-122">Если вы не настроили HTTPS на сервере, [давайте шифрованием][LetsEncrypt] обеспечивается бесплатный и достаточно простой способ запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="38884-122">If you have not set up HTTPS on your server, [Let's Encrypt][LetsEncrypt] provides a free and relatively-easy way to start the process.</span></span>  <span data-ttu-id="38884-123">Вы также можете размещать сайт в сети CDN.</span><span class="sxs-lookup"><span data-stu-id="38884-123">Or, you might consider hosting your site on a CDN.</span></span>  <span data-ttu-id="38884-124">По умолчанию в настоящее время используются наиболее важные сайты узлов сети CDN на HTTPS.</span><span class="sxs-lookup"><span data-stu-id="38884-124">Most major CDNs host sites on HTTPS by default now.</span></span>  

> [!TIP]
> <span data-ttu-id="38884-125">Использование подсказки по [протоколу HTTPS][WebhintUseHttps] в этой [подсказке][Webhint] может помочь автоматизировать процесс, чтобы все HTTP-запросы направлялись на HTTPS.</span><span class="sxs-lookup"><span data-stu-id="38884-125">The [Use HTTPS][WebhintUseHttps] hint in [webhint][Webhint] may help automate the process of making sure that all HTTP requests are directed to HTTPS.</span></span>  

### <span data-ttu-id="38884-126">Смешанное содержимое</span><span class="sxs-lookup"><span data-stu-id="38884-126">Mixed content</span></span>   

<span data-ttu-id="38884-127">**Смешанное содержимое** указывает на то, что основной источник страницы является безопасным, но страница запрашивает ресурсы из незащищенных источников.</span><span class="sxs-lookup"><span data-stu-id="38884-127">**Mixed content** means that the main origin of a page is secure, but the page requested resources from non-secure origins.</span></span>  <span data-ttu-id="38884-128">Смешанные страницы содержимого защищены только частично, так как содержимое HTTP доступно для прослушивания и уязвимо для атак "злоумышленник в середине".</span><span class="sxs-lookup"><span data-stu-id="38884-128">Mixed content pages are only partially protected because the HTTP content is accessible to sniffers and vulnerable to man-in-the-middle attacks.</span></span>  

> ##### <span data-ttu-id="38884-129">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="38884-129">Figure 3</span></span>  
> <span data-ttu-id="38884-130">Смешанное содержимое</span><span class="sxs-lookup"><span data-stu-id="38884-130">Mixed content</span></span>  
> ![Смешанное содержимое][ImageMixedContent]  

<span data-ttu-id="38884-132">На [рис. 3](#figure-3)щелкните **Просмотреть 1 запрос на панели "сеть** ", чтобы открыть панель " **сеть** " и применить `mixed-content:displayed` фильтр, чтобы в **журнале сети** отображались только небезопасные ресурсы.</span><span class="sxs-lookup"><span data-stu-id="38884-132">In [Figure 3](#figure-3), click **View 1 request in Network panel** to open the **Network** panel and apply the `mixed-content:displayed` filter so that the **Network Log** only shows non-secure resources.</span></span>  

> ##### <span data-ttu-id="38884-133">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="38884-133">Figure 4</span></span>  
> <span data-ttu-id="38884-134">Смешанные ресурсы в сетевом журнале</span><span class="sxs-lookup"><span data-stu-id="38884-134">Mixed resources in the Network Log</span></span>  
> ![Смешанные ресурсы в сетевом журнале][ImageMixedResourcesNetworkLog]  

## <span data-ttu-id="38884-136">Просмотреть подробные сведения</span><span class="sxs-lookup"><span data-stu-id="38884-136">View details</span></span>   

### <span data-ttu-id="38884-137">Просмотр сертификата основного источника</span><span class="sxs-lookup"><span data-stu-id="38884-137">View main origin certificate</span></span>   

<span data-ttu-id="38884-138">В разделе " **Общие сведения о безопасности**" щелкните ссылку **Просмотр сертификата** для быстрого проверки сертификата для основного источника.</span><span class="sxs-lookup"><span data-stu-id="38884-138">From the **Security Overview**, click **View certificate** to quickly inspect the certificate for the main origin.</span></span>  

> ##### <span data-ttu-id="38884-139">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="38884-139">Figure 5</span></span>  
> <span data-ttu-id="38884-140">Основной сертификат источника</span><span class="sxs-lookup"><span data-stu-id="38884-140">A main origin certificate</span></span>  
> ![Основной сертификат источника][ImageCertificate]  

### <span data-ttu-id="38884-142">Просмотр сведений об источнике</span><span class="sxs-lookup"><span data-stu-id="38884-142">View origin details</span></span>   

<span data-ttu-id="38884-143">Щелкните одну из записей на левой панели навигации, чтобы просмотреть подробные сведения об источнике.</span><span class="sxs-lookup"><span data-stu-id="38884-143">Click one of the entries in the left-hand nav to view the details of the origin.</span></span>  <span data-ttu-id="38884-144">На странице сведения вы можете просмотреть сведения о подключении и сертификате.</span><span class="sxs-lookup"><span data-stu-id="38884-144">From the details page you are able to view connection and certificate information.</span></span>  <span data-ttu-id="38884-145">Информация о прозрачности сертификата также отображается, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="38884-145">Certificate transparency information is also shown when available.</span></span>  

> ##### <span data-ttu-id="38884-146">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="38884-146">Figure 6</span></span>  
> <span data-ttu-id="38884-147">Сведения о главном источнике</span><span class="sxs-lookup"><span data-stu-id="38884-147">Main origin details</span></span>  
> ![Сведения о главном источнике][ImageOriginDetails]  

 



<!-- image links -->  

[ImageSecurityPanel]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure.msft.png "Рисунок 1: панель "безопасность""  
[ImageNonSecurePage]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-non-secure.msft.png "Рисунок 2: небезопасная страница"  
[ImageMixedContent]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure.msft.png "Рисунок 3: смешанное содержимое"  
[ImageMixedResourcesNetworkLog]: /microsoft-edge/devtools-guide-chromium/media/security-network-filter.msft.png "Рисунок 4: смешанные ресурсы в сетевом журнале"  
[ImageCertificate]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-secure-view-certificate.msft.png "Рисунок 5: сертификат основного источника"  
[ImageOriginDetails]: /microsoft-edge/devtools-guide-chromium/media/security-security-overview-mixed-secure-main-origin.msft.png "Рисунок 6: сведения о главном источнике"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Открыть Microsoft Edge DevTools"  


[LetsEncrypt]: https://letsencrypt.org "Шифрование-бесплатные сертификаты SSL/TLS"  

[Webhint]: https://webhint.io "Подсказка"  
[WebhintUseHttps]: https://webhint.io/docs/user-guide/hints/hint-https-only "Использование HTTPS | Документация по подсказкам"  

<!--[mixed]: /web/fundamentals/security/prevent-mixed-content/what-is-mixed-content ""  -->

> [!NOTE]
> <span data-ttu-id="38884-160">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="38884-160">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="38884-161">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/security/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="38884-161">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/security/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="38884-163">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="38884-163">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
