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
# Обнаружение службы поиска  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

Интеграция с поддержкой поиска встроена в адресную строку Microsoft Edge, включая предложения для поиска, результаты из Интернета, журнал браузера и избранное.  Microsoft Edge использует [спецификацию OpenSearch 1.1,](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) чтобы найти и использовать поставщики поиска в Интернете.  Если вы являетесь поставщиком поиска, вот как можно проверить, поддерживает ли Microsoft Edge вашу службу.  

> [ВАЖНО] Для обеспечения безопасности и конфиденциальности Microsoft Edge требует ся все поисковые запросы по SSL.  

Чтобы включить интеграцию Microsoft Edge с поисковой `https` поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой поисковой  

*   Сайт, содержащий ссылку на документ описания  
*   URL-адрес самого документа описания  
*   Шаблон поисковых запросов  

1.  Укажите OpenSearch файла описания, содержащий имя поставщика поиска и шаблон, на основе которого нужно строить поиск.  Вот пример документа:  
    
    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```  
    
1.  Вставьте ссылку на файл описания OpenSearch в верхний колонтитул страниц (обычно это может быть домашняя страница сайта и страницы результатов поиска):  
    
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
    
Когда пользователь просматривает свою службу поиска, OpenSearch описание автоматически будит при этом для дальнейшего использования.  После этого пользователь сможет перейти в параметры Microsoft Edge и добавить службу поиска в свой список поставщиков службы поиска адресной строки Microsoft Edge.  

Дополнительные OpenSearch сведения о создании документа OpenSearch [описания](https://github.com/dewitt/opensearch/blob/master/opensearch-1-1-draft-6.md) см. в спецификации OpenSearch Description.  
