---
description: Процесс распространения расширения по механизму, отличному от проверенных хранилищ
title: Альтернативный способ распространения расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: e28a84fd75ad1ac0be2000a22c26371ca73d0293
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015697"
---
# Альтернативный способ распространения расширения  

Если вы являетесь разработчиком, которому нужно распространить расширение в рамках процесса установки другого программного обеспечения или администратор сети, которому нужно распространить расширение по всей Организации, Microsoft EDGE поддерживает следующие методы установки расширения:  

*   **Использование реестра Windows \ (только для Windows)**  

Microsoft EDGE поддерживает установку расширения, размещенного на `update_URL` .  В Windows `update_URL` необходимо указывать на каталог надстроек Microsoft Edge \ (надстройки Microsoft EDGE), где должно быть размещено расширение.  

> [!NOTE]
> Внешняя Установка расширения с помощью JSON-файла настроек для macOS <!--and Linux--> еще не поддерживаются.  Поддержка этих функций скоро будет доступна.

## Использование реестра Windows  

Сначала опубликуйте расширение в надстройках Microsoft EDGE или упакуйте файл a. CRX и убедитесь, что он успешно установлен.  

Для установки расширения через реестр в Windows можно выполнить следующие действия:  

*   Найдите или создайте в реестре следующий раздел:  
    *   32 — разрядная версия Windows:  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   64 — разрядная версия Windows:  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   Создайте новый ключ \ (Folder \) в разделе Extensions с тем же именем, что и идентификатор расширения, (например, `aaaaaaaaaabbbbbbbbbbcccccccccc` \).  
*   В ключе расширения создайте свойство `update_url` и задайте для него значение: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (это указывает на CRX расширения в надстройках Microsoft Edge \). Если вы хотите установить расширение из веб-магазина Chrome, укажите URL-адрес веб-магазина Chrome Update `https://clients2.google.com/service/update2/crx` .  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   Запустите браузер и перейдите к нему, и `edge://extensions` вы увидите расширение в списке.  

## Обновление и удаление  

Microsoft Edge проверяет записи метаданных в реестре каждый раз при запуске браузера и вносит необходимые изменения во внешние расширения.  

Чтобы обновить расширение до новой версии, обновите файл и обновите версию в реестре.  

Чтобы удалить расширение (например, если оно удалено), удалите файл параметров \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) или метаданные из реестра.  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> [Здесь](https://developer.chrome.com/apps/external_extensions)будет найдена исходная страница.  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
