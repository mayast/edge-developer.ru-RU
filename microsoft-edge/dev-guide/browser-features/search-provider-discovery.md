---
ms.assetid: f74760f5-061c-494d-b096-9fb6ecb71a16
description: Если вы являетесь поставщиком поиска, ознакомьтесь со сведениями о том, как обеспечить поддержку службой Microsoft Edge поддержки вашей услуги.
title: Руководство по разработке — обнаружение поставщика поиска
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: ac23c2c62d436d5772b498208a56ad306eb8cb3c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570899"
---
# <span data-ttu-id="6d0dc-104">Обнаружение поставщика поиска</span><span class="sxs-lookup"><span data-stu-id="6d0dc-104">Search provider discovery</span></span>


<span data-ttu-id="6d0dc-105">Расширенная интеграция поиска встроена в адресную строку Microsoft EDGE, в том числе варианты поиска, результаты из Интернета, журнал браузера и Избранное.</span><span class="sxs-lookup"><span data-stu-id="6d0dc-105">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span> <span data-ttu-id="6d0dc-106">Microsoft Edge использует спецификацию [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) для поиска и использования веб-служб поиска.</span><span class="sxs-lookup"><span data-stu-id="6d0dc-106">Microsoft Edge follows the [OpenSearch 1.1](https://go.microsoft.com/fwlink/p/?LinkID=208582) specification to discover and use web search providers.</span></span> <span data-ttu-id="6d0dc-107">Если вы являетесь поставщиком услуг поиска, убедитесь в том, что Microsoft EDGE поддерживает вашу службу.</span><span class="sxs-lookup"><span data-stu-id="6d0dc-107">If you are a search provider, here's how to ensure that Microsoft Edge supports your service.</span></span>

**<span data-ttu-id="6d0dc-108">Для обеспечения безопасности и конфиденциальности для пользователей Microsoft Edge требует, чтобы все поиски выполнялись по протоколу SSL.</span><span class="sxs-lookup"><span data-stu-id="6d0dc-108">For user security and privacy, Microsoft Edge requires all searches be conducted over SSL.</span></span>** <span data-ttu-id="6d0dc-109">Следующие ресурсы должны быть указаны как `https` URL-адреса, чтобы включить Microsoft Edge Integration поисковой системы:</span><span class="sxs-lookup"><span data-stu-id="6d0dc-109">The following resources must be specified as `https` URLs to enable Microsoft Edge integration of your search engine:</span></span>
* <span data-ttu-id="6d0dc-110">Сайт, содержащий ссылку на документ описания</span><span class="sxs-lookup"><span data-stu-id="6d0dc-110">The site that contains the reference to the description document</span></span>
* <span data-ttu-id="6d0dc-111">URL-адрес самого документа описания</span><span class="sxs-lookup"><span data-stu-id="6d0dc-111">The URL to the description document itself</span></span>
* <span data-ttu-id="6d0dc-112">Шаблон запроса "Поиск"</span><span class="sxs-lookup"><span data-stu-id="6d0dc-112">The search query template</span></span> 

1.  <span data-ttu-id="6d0dc-113">Предоставьте файл описания OpenSearch, содержащий имя службы поиска, и шаблон, который будет использоваться для создания поиска.</span><span class="sxs-lookup"><span data-stu-id="6d0dc-113">Provide an OpenSearch description file, which contains the name of the search provider, and the template to use to construct the search.</span></span> <span data-ttu-id="6d0dc-114">Пример документа:</span><span class="sxs-lookup"><span data-stu-id="6d0dc-114">Here is an example document:</span></span>

    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```

2.  <span data-ttu-id="6d0dc-115">Включите ссылку на файл описания OpenSearch в раздел верхнего колонтитула страницы (обычно сюда будет содержаться Домашняя страница сайта и страницы результатов поиска), например:</span><span class="sxs-lookup"><span data-stu-id="6d0dc-115">Include a reference to your OpenSearch description file in the header section of your pages (typically this would include your site home page and search result pages), for example:</span></span>

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

<span data-ttu-id="6d0dc-116">Когда пользователь переходит к службе поиска, описание OpenSearch будет автоматически отобрано и сохранено для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="6d0dc-116">When a user browses to your search service, your OpenSearch description will be automatically picked up and saved for later use.</span></span> <span data-ttu-id="6d0dc-117">Пользователь сможет перейти к параметрам Microsoft EDGE и добавить службу поиска в свой список служб поиска для адресной строки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6d0dc-117">The user will then be able to go to Microsoft Edge settings and choose to add your search service to his or her list of search providers for the Microsoft Edge address bar.</span></span>

<span data-ttu-id="6d0dc-118">Более подробную информацию о создании вашего документа с описанием OpenSearch вы увидите в спецификации [opensearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) .</span><span class="sxs-lookup"><span data-stu-id="6d0dc-118">See the [OpenSearch 1.1](https://go.microsoft.com/fwlink/p/?LinkID=208582) specification for further details on creating your OpenSearch description document.</span></span>
