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





# <span data-ttu-id="5647b-103">Просмотр данных из веб-SQL с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="5647b-103">View Web SQL Data With Microsoft Edge DevTools</span></span>   



> [!WARNING]
> <span data-ttu-id="5647b-104">Спецификация веб-SQL [не поддерживается][W3CWebSQLStatus].</span><span class="sxs-lookup"><span data-stu-id="5647b-104">The Web SQL specification is [not being maintained][W3CWebSQLStatus].</span></span>  

<span data-ttu-id="5647b-105">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для проверки данных в веб-приложении SQL.</span><span class="sxs-lookup"><span data-stu-id="5647b-105">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to inspect Web SQL data.</span></span>  

## <span data-ttu-id="5647b-106">Просмотр данных в веб-SQL</span><span class="sxs-lookup"><span data-stu-id="5647b-106">View Web SQL Data</span></span>   

1.  <span data-ttu-id="5647b-107">Перейдите на вкладку **источники** , чтобы открыть панель " **источники** ".</span><span class="sxs-lookup"><span data-stu-id="5647b-107">Select the **Sources** tab to open the **Sources** panel.</span></span>  <span data-ttu-id="5647b-108">Обычно область **манифеста** открывается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5647b-108">The **Manifest** pane usually opens by default.</span></span>  
    
    > ##### <span data-ttu-id="5647b-109">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="5647b-109">Figure 1</span></span>  
    > <span data-ttu-id="5647b-110">Область «манифест»</span><span class="sxs-lookup"><span data-stu-id="5647b-110">The Manifest pane</span></span>  
    > ![Область «манифест»][ImageManifestPane]  
    
1.  <span data-ttu-id="5647b-112">Разверните раздел **веб-SQL** , чтобы просмотреть базы данных и таблицы.</span><span class="sxs-lookup"><span data-stu-id="5647b-112">Expand the **Web SQL** section to view databases and tables.</span></span>  <span data-ttu-id="5647b-113">На [рис. 2](#figure-2) ниже **html5meetup** база данных, а **комнаты** — таблица.</span><span class="sxs-lookup"><span data-stu-id="5647b-113">In [Figure 2](#figure-2) below **html5meetup** is a database and **rooms** is a table.</span></span>  
    
    > ##### <span data-ttu-id="5647b-114">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="5647b-114">Figure 2</span></span>  
    > <span data-ttu-id="5647b-115">Область "веб-SQL"</span><span class="sxs-lookup"><span data-stu-id="5647b-115">The Web SQL pane</span></span>  
    > ![Область "веб-SQL"][ImageWebSQLPane]  

1.  <span data-ttu-id="5647b-117">Выберите таблицу, чтобы просмотреть данные для этой таблицы.</span><span class="sxs-lookup"><span data-stu-id="5647b-117">Select a table to view the data for that table.</span></span>  
    
    > ##### <span data-ttu-id="5647b-118">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="5647b-118">Figure 3</span></span>  
    > <span data-ttu-id="5647b-119">Просмотр данных таблицы веб-SQL **комнат**</span><span class="sxs-lookup"><span data-stu-id="5647b-119">Viewing the data of the **rooms** Web SQL table</span></span>  
    > ![Просмотр данных таблицы веб-SQL][ImageWebSQLTable]  

## <span data-ttu-id="5647b-121">Изменение данных в веб-SQL</span><span class="sxs-lookup"><span data-stu-id="5647b-121">Edit Web SQL data</span></span>   

<span data-ttu-id="5647b-122">Вы не можете редактировать данные веб-SQL при просмотре таблицы веб-SQL (например, на **рис. 3** выше).</span><span class="sxs-lookup"><span data-stu-id="5647b-122">You are not able to edit Web SQL data when viewing a Web SQL table, such as in **Figure 3** above.</span></span>  <span data-ttu-id="5647b-123">Но вы можете запускать на веб-сайте SQL инструкции для редактирования и удаления таблиц.</span><span class="sxs-lookup"><span data-stu-id="5647b-123">But you may run statements from the Web SQL Console that edit or delete tables.</span></span>  <span data-ttu-id="5647b-124">Дополнительные сведения: [запуск запросов Web SQL](#run-web-sql-queries).</span><span class="sxs-lookup"><span data-stu-id="5647b-124">See [Run Web SQL queries](#run-web-sql-queries).</span></span>  

## <span data-ttu-id="5647b-125">Выполнение запросов на веб-SQL</span><span class="sxs-lookup"><span data-stu-id="5647b-125">Run Web SQL queries</span></span>   

1.  <span data-ttu-id="5647b-126">Выберите базу данных, чтобы открыть для нее консоль.</span><span class="sxs-lookup"><span data-stu-id="5647b-126">Select a database to open a console for that database.</span></span>  

1.  <span data-ttu-id="5647b-127">Введите инструкцию веб-SQL и нажмите `Enter` для ее запуска.</span><span class="sxs-lookup"><span data-stu-id="5647b-127">Type a Web SQL statement, then press `Enter` to run it.</span></span>  
    
    > ##### <span data-ttu-id="5647b-128">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="5647b-128">Figure 4</span></span>  
    > <span data-ttu-id="5647b-129">Использование веб-консоли SQL для удаления строки из таблицы " **комнаты** "</span><span class="sxs-lookup"><span data-stu-id="5647b-129">Using the Web SQL Console to delete a row from the **rooms** table</span></span>  
    > ![Удаление строки из таблицы с помощью веб-консоли SQL][ImageWebSQLEdit]  

## <span data-ttu-id="5647b-131">Обновление таблицы веб-SQL</span><span class="sxs-lookup"><span data-stu-id="5647b-131">Refresh a Web SQL table</span></span>   

<span data-ttu-id="5647b-132">DevTools не обновляет таблицы в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="5647b-132">DevTools does not update tables in real-time.</span></span>  <span data-ttu-id="5647b-133">Чтобы обновить данные в таблице, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5647b-133">To update the data in a table:</span></span>  

1.  <span data-ttu-id="5647b-134">[Просмотр данных в таблице веб-SQL](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="5647b-134">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="5647b-135">Нажмите кнопку **Обновить** ![ Обновление ][ImageRefreshIcon] .</span><span class="sxs-lookup"><span data-stu-id="5647b-135">Select **Refresh** ![Refresh][ImageRefreshIcon].</span></span>  

## <span data-ttu-id="5647b-136">Фильтрация столбцов в таблице веб-SQL</span><span class="sxs-lookup"><span data-stu-id="5647b-136">Filter out columns in a Web SQL table</span></span>   

1.  <span data-ttu-id="5647b-137">[Просмотр данных в таблице веб-SQL](#view-web-sql-data).</span><span class="sxs-lookup"><span data-stu-id="5647b-137">[View the data in a Web SQL table](#view-web-sql-data).</span></span>  
1.  <span data-ttu-id="5647b-138">С помощью текстового поля **видимые столбцы** можно указать, какие столбцы вы хотите отобразить.</span><span class="sxs-lookup"><span data-stu-id="5647b-138">Use the **Visible columns** text box to specify what columns you want to show.</span></span>  <span data-ttu-id="5647b-139">Укажите имена столбцов в виде CSV-списка.</span><span class="sxs-lookup"><span data-stu-id="5647b-139">Provide the column names as a CSV list.</span></span>  
    
    > ##### <span data-ttu-id="5647b-140">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="5647b-140">Figure 5</span></span>  
    > <span data-ttu-id="5647b-141">Использование текстового поля " **видимые столбцы** " для отображения `room_name` только `last_updated` столбцов</span><span class="sxs-lookup"><span data-stu-id="5647b-141">Using the **Visible Columns** text box to only show the `room_name` and `last_updated` columns</span></span>  
    > ![Использование текстового поля "видимые столбцы" для уменьшения количества отображаемых столбцов][ImageWebSQLFilter]  

## <span data-ttu-id="5647b-143">Удаление всех данных из веб-SQL</span><span class="sxs-lookup"><span data-stu-id="5647b-143">Delete all Web SQL data</span></span>   

1.  <span data-ttu-id="5647b-144">Открытие области **очистки хранилища** .</span><span class="sxs-lookup"><span data-stu-id="5647b-144">Open the **Clear Storage** pane.</span></span>  
1.  <span data-ttu-id="5647b-145">Убедитесь, что установлен флажок **веб-SQL** .</span><span class="sxs-lookup"><span data-stu-id="5647b-145">Make sure that the **Web SQL** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="5647b-146">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="5647b-146">Figure 6</span></span>  
    > <span data-ttu-id="5647b-147">Флажок " **веб-SQL** "</span><span class="sxs-lookup"><span data-stu-id="5647b-147">The **Web SQL** checkbox</span></span>  
    > ![Флажок "веб-SQL"][ImageWebSQLCheckbox]  

1.  <span data-ttu-id="5647b-149">Нажмите кнопку **Очистить данные сайта**.</span><span class="sxs-lookup"><span data-stu-id="5647b-149">Select **Clear site data**.</span></span>  
    
    > ##### <span data-ttu-id="5647b-150">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="5647b-150">Figure 7</span></span>  
    > <span data-ttu-id="5647b-151">Кнопка " **Очистить данные сайта** "</span><span class="sxs-lookup"><span data-stu-id="5647b-151">The **Clear Site Data** button</span></span>  
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
> <span data-ttu-id="5647b-162">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5647b-162">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5647b-163">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/websql) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5647b-163">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/websql) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5647b-165">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5647b-165">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
