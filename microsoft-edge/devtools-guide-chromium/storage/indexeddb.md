---
title: Просмотр и изменение IndexedDBных данных с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 4eca78dcd92048d75f8488fddc7b210da68690df
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612090"
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





# Просмотр и изменение IndexedDBных данных с помощью Microsoft Edge DevTools   

  

В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра и изменения [IndexedDB][MDNIndexedDBAPI] данных.  Предполагается, что вы знакомы с DevTools.  Кроме того, предполагается, что вы знакомы с IndexedDB.  В противном случае ознакомьтесь [с разIndexedDB][MDNUsingIndexedDB].  

## Просмотр данных IndexedDB   

1.  Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .  Обычно область **манифеста** открывается по умолчанию.  
    
    > ##### Рис. 1  
    > Область «манифест»  
    > ![Область «манифест»][ImageManifest]  

1.  Разверните меню **IndexedDB** , чтобы узнать, какие базы данных доступны.  
    
    > ##### Рисунок 2  
    > Меню **IndexedDB**  
    > ![Меню IndexedDB][ImageIndexedDBMenu]  
    
    *   ![Значок базы данных ][ImageDatabaseIcon] `notes - https://mdn.github.io` представляет базу данных, где `notes` — это имя базы данных, а `https://mdn.github.io` также источник, который получает доступ к базе данных.  
    *   ![Значок "хранилище объектов" ][ImageObjectStoreIcon] `notes` — это хранилище объектов.  
    *   **заголовок** и **текст** — это [индексы][MDNUsingIndexedDBUsingIndex].  
    
    > [!NOTE]
    > **Известное ограничение**  Сторонние базы данных не видны.  Например, если вы используете `<iframe>` для внедрения баннера на странице, а в вашей рекламной сети используется IndexedDB, данные IndexedDB для вашей рекламной сети не будут видны.  Просмотреть [#943770 вопросов][ChromiumIssue943770].  
    
1.  Выберите базу данных, чтобы увидеть источник и номер версии.  
    
    > ##### Рисунок3  
    > База данных **Notes**  
    > ![База данных Notes][ImageIndexedDBDatabase]  
    
1.  Выберите хранилище объектов для просмотра пар "ключ-значение".  
    
    > [!NOTE]
    > Данные IndexedDB не обновляются в режиме реального времени.  Смотрите раздел [Обновление данных IndexedDB](#refresh-indexeddb-data).  
    
    > ##### Рисунок4  
    > Хранилище объектов " **заметки** "  
    > ![Хранилище объектов "Заметки"][ImageIndexedDBObjectStore]  

    *   **Всего элементов** — общее количество пар "ключ-значение" в хранилище объектов.  
    *   **Значение ключевого генератора** — это следующий доступный ключ.  Это поле отображается только при использовании [генераторов ключей][MDNBasicConceptsKeyGenerator].  

1.  Выберите ячейку в столбце **значение** , чтобы развернуть это значение.  
    
    > ##### Рисунок 5  
    > Просмотр значения IndexedDB  
    > ![Просмотр значения IndexedDB][ImageIndexedBDValue]  
    
1.  Выберите индекс (например, **заголовок** или **текст** ) на [рисунке 6](#figure-6), чтобы отсортировать хранилище объектов согласно значениям этого индекса.  
   
    > ##### Рисунок6  
    > Хранилище объектов, отсортированное в алфавитном порядке по ключу **заголовка**  
    > ![Сортировка хранилища объектов по индексу][ImageIndexedDBIndex]  

## Обновление данных IndexedDB   

Значения IndexedDB на панели **приложения** не обновляются в режиме реального времени.  Выберите **Обновить** ![ Обновление ][ImageReloadIcon] при просмотре хранилища объектов, чтобы обновить данные, или просмотрите базу данных и нажмите **обновить базу данных** , чтобы обновить все данные.  

> ##### Рисунок7  
> Просмотр базы данных  
> ![Просмотр базы данных][ImageIndexedDBDatabase2]  

## Изменить данные IndexedDB   

IndexedDB ключи и значения не подлежат редактированию на панели **приложения** .  Так как DevTools имеет доступ к контексту страницы, вы можете выполнить код JavaScript в DevTools для редактирования IndexedDB данных.  

### Редактирование данных IndexedDB с помощью фрагментов   

[Фрагменты][DevtoolsJavascriptSnippets] — это способ хранения и выполнения блоков кода JavaScript в DevTools.  При выполнении фрагмента на **консоль**выписывается результат.  Вы можете использовать сниппет для выполнения кода JavaScript, чтобы изменить базу данных IndexedDB.  

> ##### Рисунок8  
> Использование фрагмента для взаимодействия с IndexedDB  
> ![Использование фрагмента для взаимодействия с IndexedDB][ImageIndexedDBSnippet]  

## Удаление данных IndexedDB   

### Удаление пары ключ-значение IndexedDB   

1.  [Просмотр хранилища объектов IndexedDB](#view-indexeddb-data).  
1.  Выберите пару "ключ-значение", которую вы хотите удалить.  DevTools выделит ее, чтобы показать, что она выбрана.  
    
    > ##### Рисунок9  
    > Выбор пары "ключ-значение" для ее удаления  
    > ![Выбор пары "ключ-значение" для ее удаления][ImageIndexedDBKeyValuePair]  

1.  Нажмите клавишу `Delete` или выберите команду **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] .  
    
    > ##### Рисунок 10  
    > Как выглядит хранилище объектов после удаления пары "ключ-значение"  
    > ![Как выглядит хранилище объектов после удаления пары "ключ-значение"][ImageIndexedDBKeyValuePairDeleted]  

### Удаление всех пар "ключ-значение" в хранилище объектов   

1.  [Просмотр хранилища объектов IndexedDB](#view-indexeddb-data).  
    
    > ##### Рисунок11  
    > Просмотр хранилища объектов  
    > ![Просмотр хранилища объектов][ImageIndexedDBObjectStore]  

1.  Выберите **Очистить хранилище объектов** ![ Очистить хранилище объектов ][ImageClearIcon] .  

### Удаление базы данных IndexedDB   

1.  [Просмотрите базу данных IndexedDB](#view-indexeddb-data) , которую вы хотите удалить.  
1.  Выберите команду **Удалить базу данных**.  
    
    > ##### Рисунок12  
    > Кнопка " **Удалить базу данных** "  
    > ![Кнопка "удалить базу данных"][ImageIndexedDBDatabase]  

### Удаление всех IndexedDB хранилища   

1.  Открытие области **очистки хранилища** .  

1.  Убедитесь, что флажок **IndexedDB** установлен.  

1.  Нажмите кнопку **Очистить данные сайта**.  
    
    > ##### Рисунок13  
    > Область **очистки** области "Очистка хранилища ![ "][ImageIndexedDBClearStorage]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDatabaseIcon]: /microsoft-edge/devtools-guide-chromium/media/database-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  
[ImageObjectStoreIcon]: /microsoft-edge/devtools-guide-chromium/media/object-store-icon.msft.png  
[ImageReloadIcon]: /microsoft-edge/devtools-guide-chromium/media/reload-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest-empty.msft.png "Рисунок 1: область манифеста"  
[ImageIndexedDBMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb.msft.png "Рисунок 2: меню IndexedDB"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db.msft.png "Рисунок 3: база данных notes_db"  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os.msft.png "Рисунок 4: notes_osое хранилище объектов"  
[ImageIndexedBDValue]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-edge-chromium.msft.png "Рисунок 5: Просмотр значения IndexedDB"  
[ImageIndexedDBIndex]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-title.msft.png "Рисунок 6: Сортировка хранилища объектов по индексу"  
[ImageIndexedDBDatabase2]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-refresh-database.msft.png "Рисунок 7: Просмотр базы данных"  
[ImageIndexedDBSnippet]: /microsoft-edge/devtools-guide-chromium/media/storage-sources-snippets-indexeddb-output.msft.png "Рисунок 8: использование фрагмента для взаимодействия с IndexedDB"  
[ImageIndexedDBKeyValuePair]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os2.msft.png "Рис. 9: выбор пары "ключ-значение" для ее удаления"  
[ImageIndexedDBKeyValuePairDeleted]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-delete-selected.msft.png "Рисунок 10: внешний вид хранилища объектов после удаления пары "ключ-значение""  
[ImageIndexedDBObjectStore]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-notes_os-clear-object-store.msft.png "Рисунок 11: просмотр хранилища объектов"  
[ImageIndexedDBDatabase]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-indexeddb-notes_db-delete-database.msft.png "Рисунок 12: кнопка "удалить базу данных""  
[ImageIndexedDBClearStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-clear-storage-indexeddb-clear-site-data.msft.png "Рисунок 13: область очистки хранилища"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  
[DevtoolsJavascriptSnippets]: /microsoft-edge/devtools-guide-chromium/javascript/snippets "Выполнение фрагментов кода JavaScript на любой странице с Microsoft Edge DevTools"  

[ChromiumIssue943770]: https://crbug.com/943770 "943770-DevTools: Show IFRAME IndexedDB databases-Chromium-Monorail"  

[MDNBasicConceptsKeyGenerator]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Basic_Concepts_Behind_IndexedDB#gloss_keygenerator "Ключевой генератор — основные принципы | MDN"  
[MDNIndexedDBAPI]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API "API IndexedDB | MDN"  
[MDNUsingIndexedDB]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB "Использование IndexedDB | MDN"  
[MDNUsingIndexedDBUsingIndex]: https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Using_an_index "Использование индекса с помощью IndexedDB | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
