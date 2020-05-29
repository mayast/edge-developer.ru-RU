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





# <span data-ttu-id="cb95b-103">Просмотр данных кэша приложения с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="cb95b-103">View Application Cache Data With Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="cb95b-104">API кэша приложения [удаляется с веб-платформы][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="cb95b-104">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="cb95b-105">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки ресурсов [кэша приложения][MDNWebAPIsWindowApplicationCache] .</span><span class="sxs-lookup"><span data-stu-id="cb95b-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="cb95b-106">Просмотр данных кэша приложения</span><span class="sxs-lookup"><span data-stu-id="cb95b-106">View Application Cache Data</span></span>   

1.  <span data-ttu-id="cb95b-107">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="cb95b-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="cb95b-108">Обычно область **манифеста** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="cb95b-108">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="cb95b-109">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="cb95b-109">Figure 1</span></span>  
    > <span data-ttu-id="cb95b-110">Область «манифест»</span><span class="sxs-lookup"><span data-stu-id="cb95b-110">The Manifest pane</span></span>  
    > ![Область «манифест»][ImageManifestPane]  

1.  <span data-ttu-id="cb95b-112">Разверните раздел **кэш приложений** и щелкните кэш для просмотра ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cb95b-112">Expand the **Application Cache** section and click a cache to view the resources.</span></span>  
    
    > ##### <span data-ttu-id="cb95b-113">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="cb95b-113">Figure 2</span></span>  
    > <span data-ttu-id="cb95b-114">Область кэша приложения</span><span class="sxs-lookup"><span data-stu-id="cb95b-114">The Application Cache pane</span></span>  
    > ![Область кэша приложения][ImageApplicationCachePane]  

<span data-ttu-id="cb95b-116">Каждая строка таблицы представляет собой кэшируемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="cb95b-116">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="cb95b-117">Столбец **Type** представляет [категорию ресурса][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="cb95b-117">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="cb95b-118">Категория</span><span class="sxs-lookup"><span data-stu-id="cb95b-118">Category</span></span> | <span data-ttu-id="cb95b-119">Сведения</span><span class="sxs-lookup"><span data-stu-id="cb95b-119">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="cb95b-120">Этот ресурс явно указан в манифесте.</span><span class="sxs-lookup"><span data-stu-id="cb95b-120">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="cb95b-121">URL-адрес является резервным для другого ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb95b-121">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="cb95b-122">URL-адрес другого ресурса не указан в DevTools.</span><span class="sxs-lookup"><span data-stu-id="cb95b-122">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="cb95b-123">`manifest`Атрибут ресурса указывает на то, что этот кэш является родительским для ресурса.</span><span class="sxs-lookup"><span data-stu-id="cb95b-123">The `manifest` attribute on the resource indicated that this cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="cb95b-124">Манифест, который должен поступать этим ресурсом из сети.</span><span class="sxs-lookup"><span data-stu-id="cb95b-124">The manifest specified that this resource must come from the network.</span></span> |  

<span data-ttu-id="cb95b-125">В нижней части таблицы находятся значки состояния, обозначающие сетевое соединение и состояние кэша приложения.</span><span class="sxs-lookup"><span data-stu-id="cb95b-125">At the bottom of the table there are status icons indicating your network connection and the status of the Application Cache.</span></span>  <span data-ttu-id="cb95b-126">В кэше приложения могут находиться указанные ниже состояния.</span><span class="sxs-lookup"><span data-stu-id="cb95b-126">The Application Cache may have the following states.</span></span>  

| <span data-ttu-id="cb95b-127">Состояние</span><span class="sxs-lookup"><span data-stu-id="cb95b-127">State</span></span> | <span data-ttu-id="cb95b-128">Сведения</span><span class="sxs-lookup"><span data-stu-id="cb95b-128">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="cb95b-129">Манифест извлекается и проверяется на наличие обновлений.</span><span class="sxs-lookup"><span data-stu-id="cb95b-129">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="cb95b-130">Ресурсы добавляются в кэш.</span><span class="sxs-lookup"><span data-stu-id="cb95b-130">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="cb95b-131">В кэше нет новых изменений.</span><span class="sxs-lookup"><span data-stu-id="cb95b-131">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="cb95b-132">Кэш удаляется.</span><span class="sxs-lookup"><span data-stu-id="cb95b-132">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="cb95b-133">Доступна новая версия кэша.</span><span class="sxs-lookup"><span data-stu-id="cb95b-133">A new version of the cache is available.</span></span> |  

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
> <span data-ttu-id="cb95b-140">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cb95b-140">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="cb95b-141">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="cb95b-141">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="cb95b-143">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="cb95b-143">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
