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





# <span data-ttu-id="f1e58-103">Просмотр и изменение IndexedDBных данных с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f1e58-103">View And Change IndexedDB Data With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="f1e58-104">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра и изменения [IndexedDB][MDNIndexedDBAPI] данных.</span><span class="sxs-lookup"><span data-stu-id="f1e58-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view and change [IndexedDB][MDNIndexedDBAPI] data.</span></span>  <span data-ttu-id="f1e58-105">Предполагается, что вы знакомы с DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1e58-105">It assumes you are familiar with DevTools.</span></span>  <span data-ttu-id="f1e58-106">Кроме того, предполагается, что вы знакомы с IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="f1e58-106">It also assumes you are familiar with IndexedDB.</span></span>  <span data-ttu-id="f1e58-107">В противном случае ознакомьтесь [с разIndexedDB][MDNUsingIndexedDB].</span><span class="sxs-lookup"><span data-stu-id="f1e58-107">If not, see [Using IndexedDB][MDNUsingIndexedDB].</span></span>  

## <span data-ttu-id="f1e58-108">Просмотр данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f1e58-108">View IndexedDB data</span></span>   

1.  <span data-ttu-id="f1e58-109">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="f1e58-109">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="f1e58-110">Обычно область **манифеста** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f1e58-110">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="f1e58-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="f1e58-111">Figure 1</span></span>  
    > <span data-ttu-id="f1e58-112">Область «манифест»</span><span class="sxs-lookup"><span data-stu-id="f1e58-112">The Manifest pane</span></span>  
    > ![Область «манифест»][ImageManifest]  

1.  <span data-ttu-id="f1e58-114">Разверните меню **IndexedDB** , чтобы узнать, какие базы данных доступны.</span><span class="sxs-lookup"><span data-stu-id="f1e58-114">Expand the **IndexedDB** menu to see which databases are available.</span></span>  
    
    > ##### <span data-ttu-id="f1e58-115">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="f1e58-115">Figure 2</span></span>  
    > <span data-ttu-id="f1e58-116">Меню **IndexedDB**</span><span class="sxs-lookup"><span data-stu-id="f1e58-116">The **IndexedDB** menu</span></span>  
    > ![Меню IndexedDB][ImageIndexedDBMenu]  
    
    *   ![<span data-ttu-id="f1e58-118">Значок базы данных ][ImageDatabaseIcon] `notes - https://mdn.github.io` представляет базу данных, где `notes` — это имя базы данных, а `https://mdn.github.io` также источник, который получает доступ к базе данных.</span><span class="sxs-lookup"><span data-stu-id="f1e58-118">Database icon][ImageDatabaseIcon] `notes - https://mdn.github.io` represents a database, where `notes` is the name of the database and `https://mdn.github.io` is the origin that accesses the database.</span></span>  
    *   ![<span data-ttu-id="f1e58-119">Значок "хранилище объектов" ][ImageObjectStoreIcon] `notes` — это хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="f1e58-119">Object Store icon][ImageObjectStoreIcon] `notes` is an object store.</span></span>  
    *   <span data-ttu-id="f1e58-120">**заголовок** и **текст** — это [индексы][MDNUsingIndexedDBUsingIndex].</span><span class="sxs-lookup"><span data-stu-id="f1e58-120">**title** and **body** are [indexes][MDNUsingIndexedDBUsingIndex].</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f1e58-121">**Известное ограничение**  Сторонние базы данных не видны.</span><span class="sxs-lookup"><span data-stu-id="f1e58-121">**Known Limitation**  Third-party databases are not visible.</span></span>  <span data-ttu-id="f1e58-122">Например, если вы используете `<iframe>` для внедрения баннера на странице, а в вашей рекламной сети используется IndexedDB, данные IndexedDB для вашей рекламной сети не будут видны.</span><span class="sxs-lookup"><span data-stu-id="f1e58-122">For example, if you use an `<iframe>` to embed an ad on your page, and your ad network uses IndexedDB, the IndexedDB data for your ad network is not be visible.</span></span>  <span data-ttu-id="f1e58-123">Просмотреть [#943770 вопросов][ChromiumIssue943770].</span><span class="sxs-lookup"><span data-stu-id="f1e58-123">See [issue #943770][ChromiumIssue943770].</span></span>  
    
1.  <span data-ttu-id="f1e58-124">Выберите базу данных, чтобы увидеть источник и номер версии.</span><span class="sxs-lookup"><span data-stu-id="f1e58-124">Select a database to see the origin and version number.</span></span>  
    
    > ##### <span data-ttu-id="f1e58-125">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="f1e58-125">Figure 3</span></span>  
    > <span data-ttu-id="f1e58-126">База данных **Notes**</span><span class="sxs-lookup"><span data-stu-id="f1e58-126">The **notes** database</span></span>  
    > ![База данных Notes][ImageIndexedDBDatabase]  
    
1.  <span data-ttu-id="f1e58-128">Выберите хранилище объектов для просмотра пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="f1e58-128">Select an object store to see the key-value pairs.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="f1e58-129">Данные IndexedDB не обновляются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="f1e58-129">IndexedDB data does not update in real-time.</span></span>  <span data-ttu-id="f1e58-130">Смотрите раздел [Обновление данных IndexedDB](#refresh-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="f1e58-130">See [Refresh IndexedDB data](#refresh-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="f1e58-131">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="f1e58-131">Figure 4</span></span>  
    > <span data-ttu-id="f1e58-132">Хранилище объектов " **заметки** "</span><span class="sxs-lookup"><span data-stu-id="f1e58-132">The **notes** object store</span></span>  
    > ![Хранилище объектов "Заметки"][ImageIndexedDBObjectStore]  

    *   <span data-ttu-id="f1e58-134">**Всего элементов** — общее количество пар "ключ-значение" в хранилище объектов.</span><span class="sxs-lookup"><span data-stu-id="f1e58-134">**Total entries** is the total number of key-value pairs in the object store.</span></span>  
    *   <span data-ttu-id="f1e58-135">**Значение ключевого генератора** — это следующий доступный ключ.</span><span class="sxs-lookup"><span data-stu-id="f1e58-135">**Key generator value** is the next available key.</span></span>  <span data-ttu-id="f1e58-136">Это поле отображается только при использовании [генераторов ключей][MDNBasicConceptsKeyGenerator].</span><span class="sxs-lookup"><span data-stu-id="f1e58-136">This field is only shown when using [key generators][MDNBasicConceptsKeyGenerator].</span></span>  

1.  <span data-ttu-id="f1e58-137">Выберите ячейку в столбце **значение** , чтобы развернуть это значение.</span><span class="sxs-lookup"><span data-stu-id="f1e58-137">Select a cell in the **Value** column to expand that value.</span></span>  
    
    > ##### <span data-ttu-id="f1e58-138">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="f1e58-138">Figure 5</span></span>  
    > <span data-ttu-id="f1e58-139">Просмотр значения IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f1e58-139">Viewing an IndexedDB value</span></span>  
    > ![Просмотр значения IndexedDB][ImageIndexedBDValue]  
    
1.  <span data-ttu-id="f1e58-141">Выберите индекс (например, **заголовок** или **текст** ) на [рисунке 6](#figure-6), чтобы отсортировать хранилище объектов согласно значениям этого индекса.</span><span class="sxs-lookup"><span data-stu-id="f1e58-141">Select an index, such as **title** or **body** in [Figure 6](#figure-6), to sort the object store according to the values of that index.</span></span>  
   
    > ##### <span data-ttu-id="f1e58-142">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="f1e58-142">Figure 6</span></span>  
    > <span data-ttu-id="f1e58-143">Хранилище объектов, отсортированное в алфавитном порядке по ключу **заголовка**</span><span class="sxs-lookup"><span data-stu-id="f1e58-143">An object store that is sorted alphabetically according to the **title** key</span></span>  
    > ![Сортировка хранилища объектов по индексу][ImageIndexedDBIndex]  

## <span data-ttu-id="f1e58-145">Обновление данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f1e58-145">Refresh IndexedDB data</span></span>   

<span data-ttu-id="f1e58-146">Значения IndexedDB на панели **приложения** не обновляются в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="f1e58-146">IndexedDB values in the **Application** panel do not update in real-time.</span></span>  <span data-ttu-id="f1e58-147">Выберите **Обновить** ![ Обновление ][ImageReloadIcon] при просмотре хранилища объектов, чтобы обновить данные, или просмотрите базу данных и нажмите **обновить базу данных** , чтобы обновить все данные.</span><span class="sxs-lookup"><span data-stu-id="f1e58-147">Select **Refresh** ![Refresh][ImageReloadIcon] when viewing an object store to refresh the data, or view a database and click **Refresh database** to refresh all data.</span></span>  

> ##### <span data-ttu-id="f1e58-148">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="f1e58-148">Figure 7</span></span>  
> <span data-ttu-id="f1e58-149">Просмотр базы данных</span><span class="sxs-lookup"><span data-stu-id="f1e58-149">Viewing a database</span></span>  
> ![Просмотр базы данных][ImageIndexedDBDatabase2]  

## <span data-ttu-id="f1e58-151">Изменить данные IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f1e58-151">Edit IndexedDB data</span></span>   

<span data-ttu-id="f1e58-152">IndexedDB ключи и значения не подлежат редактированию на панели **приложения** .</span><span class="sxs-lookup"><span data-stu-id="f1e58-152">IndexedDB keys and values are not editable from the **Application** panel.</span></span>  <span data-ttu-id="f1e58-153">Так как DevTools имеет доступ к контексту страницы, вы можете выполнить код JavaScript в DevTools для редактирования IndexedDB данных.</span><span class="sxs-lookup"><span data-stu-id="f1e58-153">Since DevTools has access to page context, however, you may run JavaScript code within DevTools to edit IndexedDB data.</span></span>  

### <span data-ttu-id="f1e58-154">Редактирование данных IndexedDB с помощью фрагментов</span><span class="sxs-lookup"><span data-stu-id="f1e58-154">Edit IndexedDB data with Snippets</span></span>   

<span data-ttu-id="f1e58-155">[Фрагменты][DevtoolsJavascriptSnippets] — это способ хранения и выполнения блоков кода JavaScript в DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1e58-155">[Snippets][DevtoolsJavascriptSnippets] are a way to store and run blocks of JavaScript code within DevTools.</span></span>  <span data-ttu-id="f1e58-156">При выполнении фрагмента на **консоль**выписывается результат.</span><span class="sxs-lookup"><span data-stu-id="f1e58-156">When you run a Snippet, the result is logged to the **Console**.</span></span>  <span data-ttu-id="f1e58-157">Вы можете использовать сниппет для выполнения кода JavaScript, чтобы изменить базу данных IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="f1e58-157">You may use a Snippet to run JavaScript code to edit an IndexedDB database.</span></span>  

> ##### <span data-ttu-id="f1e58-158">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="f1e58-158">Figure 8</span></span>  
> <span data-ttu-id="f1e58-159">Использование фрагмента для взаимодействия с IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f1e58-159">Using a Snippet to interact with IndexedDB</span></span>  
> ![Использование фрагмента для взаимодействия с IndexedDB][ImageIndexedDBSnippet]  

## <span data-ttu-id="f1e58-161">Удаление данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f1e58-161">Delete IndexedDB data</span></span>   

### <span data-ttu-id="f1e58-162">Удаление пары ключ-значение IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f1e58-162">Delete an IndexedDB key-value pair</span></span>   

1.  <span data-ttu-id="f1e58-163">[Просмотр хранилища объектов IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="f1e58-163">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
1.  <span data-ttu-id="f1e58-164">Выберите пару "ключ-значение", которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="f1e58-164">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="f1e58-165">DevTools выделит ее, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="f1e58-165">DevTools highlights it to indicate that it is selected.</span></span>  
    
    > ##### <span data-ttu-id="f1e58-166">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="f1e58-166">Figure 9</span></span>  
    > <span data-ttu-id="f1e58-167">Выбор пары "ключ-значение" для ее удаления</span><span class="sxs-lookup"><span data-stu-id="f1e58-167">Selecting a key-value pair in order to delete it</span></span>  
    > ![Выбор пары "ключ-значение" для ее удаления][ImageIndexedDBKeyValuePair]  

1.  <span data-ttu-id="f1e58-169">Нажмите клавишу `Delete` или выберите команду **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="f1e58-169">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  
    
    > ##### <span data-ttu-id="f1e58-170">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="f1e58-170">Figure 10</span></span>  
    > <span data-ttu-id="f1e58-171">Как выглядит хранилище объектов после удаления пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="f1e58-171">How the object store looks after the key-value pair has been deleted</span></span>  
    > ![Как выглядит хранилище объектов после удаления пары "ключ-значение"][ImageIndexedDBKeyValuePairDeleted]  

### <span data-ttu-id="f1e58-173">Удаление всех пар "ключ-значение" в хранилище объектов</span><span class="sxs-lookup"><span data-stu-id="f1e58-173">Delete all key-value pairs in an object store</span></span>   

1.  <span data-ttu-id="f1e58-174">[Просмотр хранилища объектов IndexedDB](#view-indexeddb-data).</span><span class="sxs-lookup"><span data-stu-id="f1e58-174">[View an IndexedDB object store](#view-indexeddb-data).</span></span>  
    
    > ##### <span data-ttu-id="f1e58-175">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="f1e58-175">Figure 11</span></span>  
    > <span data-ttu-id="f1e58-176">Просмотр хранилища объектов</span><span class="sxs-lookup"><span data-stu-id="f1e58-176">Viewing an object store</span></span>  
    > ![Просмотр хранилища объектов][ImageIndexedDBObjectStore]  

1.  <span data-ttu-id="f1e58-178">Выберите **Очистить хранилище объектов** ![ Очистить хранилище объектов ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="f1e58-178">Select **Clear object store** ![Clear object store][ImageClearIcon].</span></span>  

### <span data-ttu-id="f1e58-179">Удаление базы данных IndexedDB</span><span class="sxs-lookup"><span data-stu-id="f1e58-179">Delete an IndexedDB database</span></span>   

1.  <span data-ttu-id="f1e58-180">[Просмотрите базу данных IndexedDB](#view-indexeddb-data) , которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="f1e58-180">[View the IndexedDB database](#view-indexeddb-data) that you want to delete.</span></span>  
1.  <span data-ttu-id="f1e58-181">Выберите команду **Удалить базу данных**.</span><span class="sxs-lookup"><span data-stu-id="f1e58-181">Select **Delete database**.</span></span>  
    
    > ##### <span data-ttu-id="f1e58-182">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="f1e58-182">Figure 12</span></span>  
    > <span data-ttu-id="f1e58-183">Кнопка " **Удалить базу данных** "</span><span class="sxs-lookup"><span data-stu-id="f1e58-183">The **Delete database** button</span></span>  
    > ![Кнопка "удалить базу данных"][ImageIndexedDBDatabase]  

### <span data-ttu-id="f1e58-185">Удаление всех IndexedDB хранилища</span><span class="sxs-lookup"><span data-stu-id="f1e58-185">Delete all IndexedDB storage</span></span>   

1.  <span data-ttu-id="f1e58-186">Открытие области **очистки хранилища** .</span><span class="sxs-lookup"><span data-stu-id="f1e58-186">Open the **Clear storage** pane.</span></span>  

1.  <span data-ttu-id="f1e58-187">Убедитесь, что флажок **IndexedDB** установлен.</span><span class="sxs-lookup"><span data-stu-id="f1e58-187">Make sure that the **IndexedDB** checkbox is enabled.</span></span>  

1.  <span data-ttu-id="f1e58-188">Нажмите кнопку **Очистить данные сайта**.</span><span class="sxs-lookup"><span data-stu-id="f1e58-188">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="f1e58-189">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="f1e58-189">Figure 13</span></span>  
    > <span data-ttu-id="f1e58-190">Область **очистки** области "Очистка хранилища ![ "][ImageIndexedDBClearStorage]</span><span class="sxs-lookup"><span data-stu-id="f1e58-190">The **Clear storage** pane ![The Clear storage pane][ImageIndexedDBClearStorage]</span></span>  

 



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
> <span data-ttu-id="f1e58-211">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f1e58-211">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f1e58-212">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f1e58-212">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/indexeddb) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f1e58-214">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f1e58-214">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
