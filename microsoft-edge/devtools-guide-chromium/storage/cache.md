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





# <span data-ttu-id="8d5ae-103">Просмотр данных кэша с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="8d5ae-103">View Cache Data With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="8d5ae-104">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных [кэша][MDNCache] .</span><span class="sxs-lookup"><span data-stu-id="8d5ae-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Cache][MDNCache] data.</span></span>  

<span data-ttu-id="8d5ae-105">Если вы пытаетесь проверить данные [кэша HTTP][MDNHTTPCaching] , это не значит, что вам нужно.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-105">If you are trying to inspect [HTTP cache][MDNHTTPCaching] data, this is not the guide you want.</span></span>  
<span data-ttu-id="8d5ae-106">Найдите данные в столбце " **Размер** " в **сетевом журнале**.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-106">Look for the information in the **Size** column of the **Network Log**.</span></span>  <span data-ttu-id="8d5ae-107">Просмотр [журнала активности сети][DevtoolsNetworkLogActivity].</span><span class="sxs-lookup"><span data-stu-id="8d5ae-107">See [Log network activity][DevtoolsNetworkLogActivity].</span></span>  

## <span data-ttu-id="8d5ae-108">Просмотр данных кэша</span><span class="sxs-lookup"><span data-stu-id="8d5ae-108">View cache data</span></span>   

1.  <span data-ttu-id="8d5ae-109">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="8d5ae-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="8d5ae-110">Обычно область **манифеста** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="8d5ae-111">Figure 1</span></span>  
    > <span data-ttu-id="8d5ae-112">Область «манифест»</span><span class="sxs-lookup"><span data-stu-id="8d5ae-112">The Manifest pane</span></span>  
    > ![Область «манифест»][ImageManifestPane]  

1.  <span data-ttu-id="8d5ae-114">Разверните раздел **хранилище кэша** , чтобы просмотреть доступные кэши.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-114">Expand the **Cache Storage** section to view available caches.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-115">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="8d5ae-115">Figure 2</span></span>  
    > <span data-ttu-id="8d5ae-116">Доступные кэши</span><span class="sxs-lookup"><span data-stu-id="8d5ae-116">Available caches</span></span>  
    > ![Доступные кэши][ImageCache]  

1.  <span data-ttu-id="8d5ae-118">Выберите кэш, чтобы просмотреть его содержимое.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-118">Select a cache to view the contents.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-119">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="8d5ae-119">Figure 3</span></span>  
    > <span data-ttu-id="8d5ae-120">Просмотр содержимого кэша</span><span class="sxs-lookup"><span data-stu-id="8d5ae-120">Viewing the contents of a cache</span></span>  
    > ![Просмотр содержимого кэша][ImageCacheView]  

1.  <span data-ttu-id="8d5ae-122">Выберите ресурс для просмотра заголовков HTTP в разделе под таблицей.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-122">Select a resource to view the HTTP headers in the section below the table.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-123">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="8d5ae-123">Figure 4</span></span>  
    > <span data-ttu-id="8d5ae-124">Просмотр заголовков HTTP ресурса</span><span class="sxs-lookup"><span data-stu-id="8d5ae-124">Viewing the HTTP headers of a resource</span></span>  
    > ![Просмотр заголовков HTTP ресурса][ImageViewCacheResource]  

1.  <span data-ttu-id="8d5ae-126">Нажмите кнопку **Предварительный просмотр** , чтобы просмотреть содержимое ресурса.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-126">Select **Preview** to view the content of a resource.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-127">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="8d5ae-127">Figure 5</span></span>  
    > <span data-ttu-id="8d5ae-128">Просмотр содержимого ресурса</span><span class="sxs-lookup"><span data-stu-id="8d5ae-128">Viewing the content of a resource</span></span>  
    > ![Просмотр содержимого ресурса][ImageCacheContent]  

## <span data-ttu-id="8d5ae-130">Обновление ресурса</span><span class="sxs-lookup"><span data-stu-id="8d5ae-130">Refresh a resource</span></span>   

1.  <span data-ttu-id="8d5ae-131">[Просмотр данных для кэша](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="8d5ae-131">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="8d5ae-132">Выберите ресурс, который вы хотите обновить.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-132">Select the resource that you want to refresh.</span></span>  <span data-ttu-id="8d5ae-133">DevTools выделит ее, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-133">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-134">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="8d5ae-134">Figure 6</span></span>  
    > <span data-ttu-id="8d5ae-135">Выбор ресурса</span><span class="sxs-lookup"><span data-stu-id="8d5ae-135">Selecting a resource</span></span>  
    > ![Выбор ресурса][ImageCacheSelected]  

1.  <span data-ttu-id="8d5ae-137">Нажмите кнопку **Обновить** ![ Обновление ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="8d5ae-137">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="8d5ae-138">Фильтрация ресурсов</span><span class="sxs-lookup"><span data-stu-id="8d5ae-138">Filter resources</span></span>   

1.  <span data-ttu-id="8d5ae-139">[Просмотр данных для кэша](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="8d5ae-139">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="8d5ae-140">С помощью текстового поля **Фильтр по пути** можно отфильтровать ресурсы, которые не соответствуют указанному вами пути.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-140">Use the **Filter by Path** text box to filter out any resources that do not match the path that you provide.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-141">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="8d5ae-141">Figure 7</span></span>  
    > <span data-ttu-id="8d5ae-142">Фильтрация ресурсов, не соответствующих указанному пути</span><span class="sxs-lookup"><span data-stu-id="8d5ae-142">Filtering out resources that do not match the specified path</span></span>  
    > ![Фильтрация ресурсов, не соответствующих указанному пути][ImageCacheFilter]  

## <span data-ttu-id="8d5ae-144">Удаление ресурса</span><span class="sxs-lookup"><span data-stu-id="8d5ae-144">Delete a resource</span></span>   

1.  <span data-ttu-id="8d5ae-145">[Просмотр данных для кэша](#view-cache-data).</span><span class="sxs-lookup"><span data-stu-id="8d5ae-145">[View the data for a cache](#view-cache-data).</span></span>  
1.  <span data-ttu-id="8d5ae-146">Выберите ресурс, который вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-146">Select the resource that you want to delete.</span></span>  <span data-ttu-id="8d5ae-147">DevTools выделит ее, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-147">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-148">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="8d5ae-148">Figure 8</span></span>  
    > <span data-ttu-id="8d5ae-149">Выбор ресурса</span><span class="sxs-lookup"><span data-stu-id="8d5ae-149">Selecting a resource</span></span>  
    > ![Выбор ресурса][ImageCacheSelected2]  

1.  <span data-ttu-id="8d5ae-151">Выберите команду **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="8d5ae-151">Select **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="8d5ae-152">Удаление всех данных из кэша</span><span class="sxs-lookup"><span data-stu-id="8d5ae-152">Delete all cache data</span></span>   

1.  <span data-ttu-id="8d5ae-153">Откройте **приложение**  >  , чтобы**Очистить хранилище**.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-153">Open **Application** > **Clear Storage**.</span></span>  
1.  <span data-ttu-id="8d5ae-154">Убедитесь, что флажок **хранилище кэша** включен.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-154">Make sure that the **Cache Storage** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-155">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="8d5ae-155">Figure 9</span></span>  
    > <span data-ttu-id="8d5ae-156">Флажок " **хранилище кэша** "</span><span class="sxs-lookup"><span data-stu-id="8d5ae-156">The **Cache Storage** checkbox</span></span>  
    > ![Флажок "хранилище кэша"][ImageCacheCheckbox]  

1.  <span data-ttu-id="8d5ae-158">Нажмите кнопку **Очистить данные сайта**.</span><span class="sxs-lookup"><span data-stu-id="8d5ae-158">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="8d5ae-159">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="8d5ae-159">Figure 10</span></span>  
    > <span data-ttu-id="8d5ae-160">Кнопка " **Очистить данные сайта** "</span><span class="sxs-lookup"><span data-stu-id="8d5ae-160">The **Clear Site Data** button</span></span>  
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
> <span data-ttu-id="8d5ae-176">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8d5ae-176">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="8d5ae-177">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/cache) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="8d5ae-177">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/cache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="8d5ae-179">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="8d5ae-179">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
