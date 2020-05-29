---
title: Просмотр данных из веб-SQL с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 7a1e3e47f6761cfdb23488683107ed0df6a8f4e2
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612062"
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





# Просмотр данных из веб-SQL с помощью Microsoft Edge DevTools   



> [!WARNING]
> Спецификация веб-SQL [не поддерживается][W3CWebSQLStatus].  

В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных в веб-приложении SQL.  

## Просмотр данных в веб-SQL   

1.  Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".  Обычно область **манифеста** открывается по умолчанию.  
    
    > ##### Рис. 1  
    > Область «манифест»  
    > ![Область «манифест»][ImageManifestPane]  
    
1.  Разверните раздел **веб-SQL** , чтобы просмотреть базы данных и таблицы.  На [рис. 2](#figure-2) ниже **html5meetup** база данных, а **комнаты** — таблица.  
    
    > ##### Рисунок 2  
    > Область "веб-SQL"  
    > ![Область "веб-SQL"][ImageWebSQLPane]  

1.  Выберите таблицу, чтобы просмотреть данные для этой таблицы.  
    
    > ##### Рисунок3  
    > Просмотр данных таблицы веб-SQL **комнат**  
    > ![Просмотр данных таблицы веб-SQL][ImageWebSQLTable]  

## Изменение данных в веб-SQL   

Вы не можете редактировать данные веб-SQL при просмотре таблицы веб-SQL (например, на **рис. 3** выше).  Но вы можете запускать на веб-сайте SQL инструкции для редактирования и удаления таблиц.  Дополнительные сведения: [запуск запросов Web SQL](#run-web-sql-queries).  

## Выполнение запросов на веб-SQL   

1.  Выберите базу данных, чтобы открыть для нее консоль.  

1.  Введите инструкцию веб-SQL и нажмите `Enter` для ее запуска.  
    
    > ##### Рисунок4  
    > Использование веб-консоли SQL для удаления строки из таблицы " **комнаты** "  
    > ![Удаление строки из таблицы с помощью веб-консоли SQL][ImageWebSQLEdit]  

## Обновление таблицы веб-SQL   

DevTools не обновляет таблицы в режиме реального времени.  Чтобы обновить данные в таблице, выполните указанные ниже действия.  

1.  [Просмотр данных в таблице веб-SQL](#view-web-sql-data).  
1.  Нажмите кнопку **Обновить** ![ Обновление ][ImageRefreshIcon] .  

## Фильтрация столбцов в таблице веб-SQL   

1.  [Просмотр данных в таблице веб-SQL](#view-web-sql-data).  
1.  С помощью текстового поля **видимые столбцы** можно указать, какие столбцы вы хотите отобразить.  Укажите имена столбцов в виде CSV-списка.  
    
    > ##### Рисунок 5  
    > Использование текстового поля " **видимые столбцы** " для отображения `room_name` только `last_updated` столбцов  
    > ![Использование текстового поля "видимые столбцы" для уменьшения количества отображаемых столбцов][ImageWebSQLFilter]  

## Удаление всех данных из веб-SQL   

1.  Открытие области **очистки хранилища** .  
1.  Убедитесь, что установлен флажок **веб-SQL** .  
    
    > ##### Рисунок6  
    > Флажок " **веб-SQL** "  
    > ![Флажок "веб-SQL"][ImageWebSQLCheckbox]  

1.  Нажмите кнопку **Очистить данные сайта**.  
    
    > ##### Рисунок7  
    > Кнопка " **Очистить данные сайта** "  
    > ![Кнопка "очистить данные сайта"][ImageClearWebSQL]  

 



<!-- image links -->  

[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  

[ImageManifestPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Рисунок 1: область манифеста"  
[ImageWebSQLPane]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql.msft.png "Рисунок 2: область "веб-SQL""  
[ImageWebSQLTable]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-1.msft.png "Рисунок 3: Просмотр данных таблицы веб-SQL"  
[ImageWebSQLEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-commands.msft.png "Рисунок 4: использование консоли веб-SQL для удаления строки из таблицы"  
[ImageWebSQLFilter]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-web-sql-html5meetup-rooms-2.msft.png "Рисунок 5: использование текстового поля "видимые столбцы" для уменьшения количества отображаемых столбцов"  
[ImageWebSQLCheckbox]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-web-sql.msft.png "Рисунок 6: флажок "веб-SQL""  
[ImageClearWebSQL]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-clear-site-data-button.msft.png "Рис. 7: кнопка "очистить данные сайта""  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

[W3CWebSQLStatus]: https://w3.org/TR/webdatabase/#status-of-this-document "База данных веб-SQL | PNG"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/websql) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
