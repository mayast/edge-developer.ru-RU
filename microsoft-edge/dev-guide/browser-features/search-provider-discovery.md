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
# Обнаружение поставщика поиска


Расширенная интеграция поиска встроена в адресную строку Microsoft EDGE, в том числе варианты поиска, результаты из Интернета, журнал браузера и Избранное. Microsoft Edge использует спецификацию [OpenSearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) для поиска и использования веб-служб поиска. Если вы являетесь поставщиком услуг поиска, убедитесь в том, что Microsoft EDGE поддерживает вашу службу.

**Для обеспечения безопасности и конфиденциальности для пользователей Microsoft Edge требует, чтобы все поиски выполнялись по протоколу SSL.** Следующие ресурсы должны быть указаны как `https` URL-адреса, чтобы включить Microsoft Edge Integration поисковой системы:
* Сайт, содержащий ссылку на документ описания
* URL-адрес самого документа описания
* Шаблон запроса "Поиск" 

1.  Предоставьте файл описания OpenSearch, содержащий имя службы поиска, и шаблон, который будет использоваться для создания поиска. Пример документа:

    ```html
    <?xml version="1.0" encoding="UTF-8"?> 
    <OpenSearchDescription xmlns="http://a9.com/-/spec/opensearch/1.1/">
        <ShortName>Contoso Search</ShortName>
        <Url type="text/html" template="https://www.contoso.com/?query={searchTerms}"/> 
    </OpenSearchDescription>
    ```

2.  Включите ссылку на файл описания OpenSearch в раздел верхнего колонтитула страницы (обычно сюда будет содержаться Домашняя страница сайта и страницы результатов поиска), например:

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

Когда пользователь переходит к службе поиска, описание OpenSearch будет автоматически отобрано и сохранено для дальнейшего использования. Пользователь сможет перейти к параметрам Microsoft EDGE и добавить службу поиска в свой список служб поиска для адресной строки Microsoft Edge.

Более подробную информацию о создании вашего документа с описанием OpenSearch вы увидите в спецификации [opensearch 1,1](https://go.microsoft.com/fwlink/p/?LinkID=208582) .
