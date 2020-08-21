---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Если вы являетесь поставщиком поиска, узнайте, как проверить, поддерживает ли Microsoft Edge службу.
title: Обнаружение поставщика услуг поиска — руководство по разработке
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 4ac8ea966e9c4736834a0be1130a8c2a8dfb2614
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941967"
---
# <span data-ttu-id="249e6-104">Обнаружение службы поиска</span><span class="sxs-lookup"><span data-stu-id="249e6-104">Search provider discovery</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="249e6-105">Интеграция с поддержкой поиска встроена в адресную строку Microsoft Edge, включая предложения для поиска, результаты из Интернета, журнал браузера и избранное.</span><span class="sxs-lookup"><span data-stu-id="249e6-105">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="249e6-106">Microsoft Edge использует [спецификацию OpenSearch 1.1,](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) чтобы найти и использовать поставщики поиска в Интернете.</span><span class="sxs-lookup"><span data-stu-id="249e6-106">Microsoft Edge follows the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification to discover and use web search providers.</span></span>  <span data-ttu-id="249e6-107">Если вы являетесь поставщиком поиска, вот как можно проверить, поддерживает ли Microsoft Edge вашу службу.</span><span class="sxs-lookup"><span data-stu-id="249e6-107">If you are a search provider, here's how to ensure that Microsoft Edge supports your service.</span></span>  

> <span data-ttu-id="249e6-108">[ВАЖНО] Для обеспечения безопасности и конфиденциальности Microsoft Edge требует ся все поисковые запросы по SSL.</span><span class="sxs-lookup"><span data-stu-id="249e6-108">[IMPORTANT] For user security and privacy, Microsoft Edge requires all searches be conducted over SSL.</span></span>  

<span data-ttu-id="249e6-109">Чтобы включить интеграцию Microsoft Edge с поисковой `https` поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой</span><span class="sxs-lookup"><span data-stu-id="249e6-109">The following resources must be specified as `https` URLs to enable Microsoft Edge integration of your search engine:</span></span>  

*   <span data-ttu-id="249e6-110">Сайт, содержащий ссылку на документ описания</span><span class="sxs-lookup"><span data-stu-id="249e6-110">The site that contains the reference to the description document</span></span>  
*   <span data-ttu-id="249e6-111">URL-адрес самого документа описания</span><span class="sxs-lookup"><span data-stu-id="249e6-111">The URL to the description document itself</span></span>  
*   <span data-ttu-id="249e6-112">Шаблон поисковых запросов</span><span class="sxs-lookup"><span data-stu-id="249e6-112">The search query template</span></span>  

1.  <span data-ttu-id="249e6-113">Укажите OpenSearch файла описания, содержащий имя поставщика поиска и шаблон, на основе которого нужно строить поиск.</span><span class="sxs-lookup"><span data-stu-id="249e6-113">Provide an OpenSearch description file, which contains the name of the search provider, and the template to use to construct the search.</span></span>  <span data-ttu-id="249e6-114">Вот пример документа:</span><span class="sxs-lookup"><span data-stu-id="249e6-114">Here is an example document:</span></span>  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  <span data-ttu-id="249e6-115">Вставьте ссылку на файл описания OpenSearch в верхний колонтитул страниц (обычно это может быть домашняя страница сайта и страницы результатов поиска):</span><span class="sxs-lookup"><span data-stu-id="249e6-115">Include a reference to your OpenSearch description file in the header section of your pages (typically this would include your site home page and search result pages), for example:</span></span>  
    
    ```html
    <html>
        <head>
            <link rel="search" 
                type="application/opensearchdescription+xml"  
                href="https://contoso.com/content-search.xml" 
                title="Contoso search" /> 
        </head> 
        <body> 
        ...
    ```  
    
<span data-ttu-id="249e6-116">Когда пользователь просматривает свою службу поиска, OpenSearch описание автоматически будит при этом для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="249e6-116">When a user browses to your search service, your OpenSearch description will be automatically picked up and saved for later use.</span></span>  <span data-ttu-id="249e6-117">После этого пользователь сможет перейти в параметры Microsoft Edge и добавить службу поиска в свой список поставщиков службы поиска адресной строки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="249e6-117">The user will then be able to go to Microsoft Edge settings and choose to add your search service to his or her list of search providers for the Microsoft Edge address bar.</span></span>  

<span data-ttu-id="249e6-118">Дополнительные OpenSearch сведения о создании документа OpenSearch [описания](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) см. в спецификации OpenSearch Description.</span><span class="sxs-lookup"><span data-stu-id="249e6-118">See the [OpenSearch 1.1](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) specification for further details on creating your OpenSearch description document.</span></span>  
