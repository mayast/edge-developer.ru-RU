---
title: Просмотр данных кэша приложения с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/14/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: fc1800fc54e5fb0d7998c62ce163ece7a461dd82
ms.sourcegitcommit: 054ad92f0b8f9a15da1e3aed32e8f4379b10860f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "10931217"
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

# <span data-ttu-id="28148-103">Просмотр данных кэша приложения с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="28148-103">View Application Cache data with Microsoft Edge DevTools</span></span>  

> [!WARNING]
> <span data-ttu-id="28148-104">API кэша приложения [удаляется с веб-платформы][HTMLStandardOfflineWebApplications].</span><span class="sxs-lookup"><span data-stu-id="28148-104">The Application Cache API is [being removed from the web platform][HTMLStandardOfflineWebApplications].</span></span>  

<span data-ttu-id="28148-105">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки ресурсов [кэша приложения][MDNWebAPIsWindowApplicationCache] .</span><span class="sxs-lookup"><span data-stu-id="28148-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect [Application Cache][MDNWebAPIsWindowApplicationCache] resources.</span></span>  

## <span data-ttu-id="28148-106">Просмотр данных кэша приложения</span><span class="sxs-lookup"><span data-stu-id="28148-106">View Application Cache data</span></span>  

1.  <span data-ttu-id="28148-107">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="28148-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="28148-108">Обычно область **манифеста** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="28148-108">The **Manifest** pane usually opens by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="28148-110">Область « **Манифест** »</span><span class="sxs-lookup"><span data-stu-id="28148-110">The **Manifest** pane</span></span>  
    :::image-end:::  

1.  <span data-ttu-id="28148-111">Разверните раздел **кэш приложения** и выберите кэш для просмотра ресурсов.</span><span class="sxs-lookup"><span data-stu-id="28148-111">Expand the **Application Cache** section and choose a cache to view the resources.</span></span>  
    
    :::image type="complex" source="../media/storage-cache-pane-cache-storage-resources.msft.png" alt-text="Область кэша приложения" lightbox="../media/storage-cache-pane-cache-storage-resources.msft.png":::
       <span data-ttu-id="28148-113">Область **кэша приложения**</span><span class="sxs-lookup"><span data-stu-id="28148-113">The **Application Cache** pane</span></span>  
    :::image-end:::  

<span data-ttu-id="28148-114">Каждая строка таблицы представляет собой кэшируемый ресурс.</span><span class="sxs-lookup"><span data-stu-id="28148-114">Each row of the table represents a cached resource.</span></span>  

<span data-ttu-id="28148-115">Столбец **Type** представляет [категорию ресурса][MDNHTMLResourcesInAnApplicationCache].</span><span class="sxs-lookup"><span data-stu-id="28148-115">The **Type** column represents the [category of the resource][MDNHTMLResourcesInAnApplicationCache].</span></span>  

| <span data-ttu-id="28148-116">Категория</span><span class="sxs-lookup"><span data-stu-id="28148-116">Category</span></span> | <span data-ttu-id="28148-117">Сведения</span><span class="sxs-lookup"><span data-stu-id="28148-117">Details</span></span> |  
|:--- |:--- |  
| `Explicit` | <span data-ttu-id="28148-118">Этот ресурс явно указан в манифесте.</span><span class="sxs-lookup"><span data-stu-id="28148-118">This resource was explicitly listed in the manifest.</span></span> |  
| `Fallback` | <span data-ttu-id="28148-119">URL-адрес является резервным для другого ресурса.</span><span class="sxs-lookup"><span data-stu-id="28148-119">The URL is a fallback for another resource.</span></span>  <span data-ttu-id="28148-120">URL-адрес другого ресурса не указан в DevTools.</span><span class="sxs-lookup"><span data-stu-id="28148-120">The URL of the other resource is not listed in DevTools.</span></span> |  
| `Master` | <span data-ttu-id="28148-121">`manifest`Атрибут ресурса указывает на то, что кэш является родительским для ресурса.</span><span class="sxs-lookup"><span data-stu-id="28148-121">The `manifest` attribute on the resource indicates that the cache is the parent of the resource.</span></span> |  
| `Network` | <span data-ttu-id="28148-122">Манифест, который указывает, что ресурс должен поступать из сети.</span><span class="sxs-lookup"><span data-stu-id="28148-122">The manifest specified that the resource must come from the network.</span></span> |  

<!--todo:  replace "Master" phrasing if possible.  -->  

<span data-ttu-id="28148-123">В нижней части таблицы находятся значки состояния, обозначающие сетевое соединение и состояние **кэша приложения**.</span><span class="sxs-lookup"><span data-stu-id="28148-123">At the bottom of the table there are status icons indicating your network connection and the status of the **Application Cache**.</span></span>  <span data-ttu-id="28148-124">В **кэше приложения** могут находиться указанные ниже состояния.</span><span class="sxs-lookup"><span data-stu-id="28148-124">The **Application Cache** may have the following states.</span></span>  

| <span data-ttu-id="28148-125">Состояние</span><span class="sxs-lookup"><span data-stu-id="28148-125">State</span></span> | <span data-ttu-id="28148-126">Сведения</span><span class="sxs-lookup"><span data-stu-id="28148-126">Details</span></span> |  
|:--- |:--- |  
| `CHECKING` | <span data-ttu-id="28148-127">Манифест извлекается и проверяется на наличие обновлений.</span><span class="sxs-lookup"><span data-stu-id="28148-127">The manifest is being fetched and checked for updates.</span></span> |  
| `DOWNLOADING` | <span data-ttu-id="28148-128">Ресурсы добавляются в кэш.</span><span class="sxs-lookup"><span data-stu-id="28148-128">Resources are being added to the cache.</span></span> |  
| `IDLE` | <span data-ttu-id="28148-129">В кэше нет новых изменений.</span><span class="sxs-lookup"><span data-stu-id="28148-129">The cache has no new changes.</span></span> |  
| `OBSOLETE` | <span data-ttu-id="28148-130">Кэш удаляется.</span><span class="sxs-lookup"><span data-stu-id="28148-130">The cache is being deleted.</span></span> |  
| `UPDATEREADY` |  <span data-ttu-id="28148-131">Доступна новая версия кэша.</span><span class="sxs-lookup"><span data-stu-id="28148-131">A new version of the cache is available.</span></span> |  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[HTMLStandardOfflineWebApplications]: https://html.spec.whatwg.org/multipage/offline.html#offline "Автономные веб-приложения: HTML Standard"  

[MDNHTMLResourcesInAnApplicationCache]: https://developer.mozilla.org/docs/Web/HTML/Using_the_application_cache#Resources_in_an_application_cache "Ресурсы в кэше приложения | MDN"  
[MDNWebAPIsWindowApplicationCache]: https://developer.mozilla.org/docs/Web/API/Window/applicationCache "Window. applicationCache-Web API | MDN"  

> [!NOTE]
> <span data-ttu-id="28148-136">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="28148-136">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="28148-137">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="28148-137">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/applicationcache) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="28148-139">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="28148-139">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
