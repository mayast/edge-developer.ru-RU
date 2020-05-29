---
description: Проверка веб-хранилища, IndexedDB, файлов cookie и кэша запросов и ответов с помощью панели хранилища
title: DevTools — хранилище
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, веб-хранилище, локальное хранилище, хранилище сеанса, IndexedDB, файлы cookie, сотрудник службы, кэш
ms.custom: seodec18
ms.openlocfilehash: 8de6e1f90f86fa09b116646918c6be1d8cfb0a72
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571722"
---
# <span data-ttu-id="5eb51-104">Хранилище</span><span class="sxs-lookup"><span data-stu-id="5eb51-104">Storage</span></span>

<span data-ttu-id="5eb51-105">С помощью панели " **хранилище** " можно проверять различные данные, хранящиеся на локальном компьютере, и управлять ими, в том числе:</span><span class="sxs-lookup"><span data-stu-id="5eb51-105">Use the **Storage** panel to inspect and manage various locally cached data, including:</span></span>

 - <span data-ttu-id="5eb51-106">Пары ключей и значений в [веб-хранилище](#local-and-session-storage-managers) (*Локальное* и хранилище *сеансов* )</span><span class="sxs-lookup"><span data-stu-id="5eb51-106">[Web storage](#local-and-session-storage-managers) (*Local* and *Session* storage) key/values pairs</span></span>
 - <span data-ttu-id="5eb51-107">Структурированные данные с [индексированной базой](#indexeddb-manager) данных</span><span class="sxs-lookup"><span data-stu-id="5eb51-107">[Indexed DB](#indexeddb-manager) structured data</span></span>
 - <span data-ttu-id="5eb51-108">[Файлы cookie](#cookies-list) для домена</span><span class="sxs-lookup"><span data-stu-id="5eb51-108">[Cookies](#cookies-list) for the domain</span></span>
 - <span data-ttu-id="5eb51-109">[Кэш](#cache-manager) (пары запросов и ответов) для отладки рабочего процесса службы</span><span class="sxs-lookup"><span data-stu-id="5eb51-109">[Cache](#cache-manager) (request/response pairs) for service worker debugging</span></span>

<span data-ttu-id="5eb51-110">Разверните любую из этих категорий и щелкните дочерний элемент, чтобы открыть вкладку "Диспетчер ресурсов".</span><span class="sxs-lookup"><span data-stu-id="5eb51-110">Expand any of those categories and click on a child entry to open its resource manager tab.</span></span>

## <span data-ttu-id="5eb51-111">Локальные и Диспетчеры хранилища сеанса</span><span class="sxs-lookup"><span data-stu-id="5eb51-111">Local and Session storage managers</span></span>

<span data-ttu-id="5eb51-112">С помощью *локального диспетчера хранилища* и *диспетчера хранилища сеанса* просмотрите веб-хранилище для своей страницы и управляйте им.</span><span class="sxs-lookup"><span data-stu-id="5eb51-112">Use the *Local Storage manager* and *Session Storage manager* to inspect and manage the web storage for  your page.</span></span> 

<span data-ttu-id="5eb51-113">Папки " **Локальное хранилище** " и " **хранилище сеанса** " в [*средстве выбора ресурсов*](./debugger.md#resource-picker) панели хранилища выводят список источников для страницы.</span><span class="sxs-lookup"><span data-stu-id="5eb51-113">The **Local Storage** and **Session Storage** folders inside the Storage panel's [*Resource picker*](./debugger.md#resource-picker) display a list of origins for the page.</span></span> <span data-ttu-id="5eb51-114">При выборе одной из этих рамок открывается редактируемая таблица текущих пар ключ-значение, заданных с помощью [Window. localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) или [Window. sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), соответственно (и/или непосредственно из [списка хранилищ](#storage-list)DevTools).</span><span class="sxs-lookup"><span data-stu-id="5eb51-114">Selecting one of these frames opens up an editable table of the current key/value pairs set via [Window.localStorage](https://developer.mozilla.org/docs/Web/API/Window/localStorage) or [Window.sessionStorage](https://developer.mozilla.org/docs/Web/API/Window/sessionStorage), respectively (and/or set directly from the  DevTools [Storage list](#storage-list)).</span></span>

![Диспетчер DevTools cookies](./media/storage_web_storage.png)

<span data-ttu-id="5eb51-116">На вкладках *Локальное хранилище* и *хранилище сеансов* можно выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5eb51-116">From the *Local Storage* and *Session Storage* tabs you can:</span></span>

 - <span data-ttu-id="5eb51-117">**Refresh** ( `Ctrl+F5` ) [список хранилищ](#cookies-list) для просмотра текущего набора пар "ключ-значение" для данного домена.</span><span class="sxs-lookup"><span data-stu-id="5eb51-117">**Refresh** (`Ctrl+F5`) the [storage list](#cookies-list) to see the current set of key/values pairs for the given domain.</span></span> <span data-ttu-id="5eb51-118">(Список не обновляется автоматически при обновлении сценария.)</span><span class="sxs-lookup"><span data-stu-id="5eb51-118">(The list does not auto-refresh upon script updates.)</span></span>
 - <span data-ttu-id="5eb51-119">**Имитация ограничения размера хранилища** для веб-хранилища Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5eb51-119">**Simulate reaching the storage limit** for Microsoft Edge web storage.</span></span> <span data-ttu-id="5eb51-120">У каждого домена и дочернего домена есть своя область хранения, но есть Объединенные ограничения.</span><span class="sxs-lookup"><span data-stu-id="5eb51-120">Each domain and subdomain has its own storage area, however there is a combined limit:</span></span>
    - <span data-ttu-id="5eb51-121">**Дочерние домены:** до 5 МБ свободного места</span><span class="sxs-lookup"><span data-stu-id="5eb51-121">**Subdomains:** up to 5 MBs of space</span></span>
    - <span data-ttu-id="5eb51-122">**Домены:** до 10 МБ свободного места</span><span class="sxs-lookup"><span data-stu-id="5eb51-122">**Domains:** up to 10 MBs of space</span></span>
    - <span data-ttu-id="5eb51-123">**Общее количество для всех доменов:** до 50 МБ свободного места</span><span class="sxs-lookup"><span data-stu-id="5eb51-123">**Total for all domains:** up to 50 MBs of space</span></span>

   <span data-ttu-id="5eb51-124">Хранилище сеанса очищается, как только вкладка последнего браузера, ссылающаяся на ее источник, будет закрыта.</span><span class="sxs-lookup"><span data-stu-id="5eb51-124">Session storage is cleared as soon as the last browser tab referencing its origin is closed.</span></span> <span data-ttu-id="5eb51-125">Записи локального хранилища остаются неопределенными до тех пор, пока они не будут очищены с помощью страницы вручную или пользователем:</span><span class="sxs-lookup"><span data-stu-id="5eb51-125">Local storage entries persist indefinitely until cleared programmatically by the page or manually by the user:</span></span>

   <span data-ttu-id="5eb51-126">**Параметры**  >  **Очистка данных браузера**  >  **Файлы cookie и сохраненные данные веб-сайтов**</span><span class="sxs-lookup"><span data-stu-id="5eb51-126">**Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

![Очистка обзора данных на панели "параметры Microsoft Edge"](./media/settings_clear_browsing_data.png)

### <span data-ttu-id="5eb51-128">Список хранилищ</span><span class="sxs-lookup"><span data-stu-id="5eb51-128">Storage list</span></span>

<span data-ttu-id="5eb51-129">В таблице *список хранилищ* можно выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5eb51-129">From the *Storage list* table you can:</span></span>

 - <span data-ttu-id="5eb51-130">**Проверьте и отсортируйте** пары "ключ-значение", щелкнув любое имя столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="5eb51-130">**Inspect and sort** your key/value pairs by clicking on either column name in the table.</span></span>
 - <span data-ttu-id="5eb51-131">**Измените** *ключ* и *значение* существующего элемента, щелкнув ячейку.</span><span class="sxs-lookup"><span data-stu-id="5eb51-131">**Edit** the *Key* and *Value* of an existing entry by clicking in the cell.</span></span>
 - <span data-ttu-id="5eb51-132">**Удалить** ( `Del` ). в контекстном меню щелкните правой кнопкой мыши пункт *удалить элемент*.</span><span class="sxs-lookup"><span data-stu-id="5eb51-132">**Delete** (`Del`) an entry from the right-click context menu option, *Delete item*.</span></span>
 - <span data-ttu-id="5eb51-133">**Добавьте** новую пару ключ/значение, щелкнув пустую строку в нижней части таблицы.</span><span class="sxs-lookup"><span data-stu-id="5eb51-133">**Add** a new key/value pair by clicking on the empty row at the bottom of the table.</span></span>


### <span data-ttu-id="5eb51-134">Горячие</span><span class="sxs-lookup"><span data-stu-id="5eb51-134">Shortcuts</span></span>

| <span data-ttu-id="5eb51-135">Действие</span><span class="sxs-lookup"><span data-stu-id="5eb51-135">Action</span></span>              | <span data-ttu-id="5eb51-136">Появивше</span><span class="sxs-lookup"><span data-stu-id="5eb51-136">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="5eb51-137">Обновить</span><span class="sxs-lookup"><span data-stu-id="5eb51-137">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="5eb51-138">Удалить элемент</span><span class="sxs-lookup"><span data-stu-id="5eb51-138">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="5eb51-139">Копирование выделенных элементов</span><span class="sxs-lookup"><span data-stu-id="5eb51-139">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="5eb51-140">Выделить все</span><span class="sxs-lookup"><span data-stu-id="5eb51-140">Select all</span></span>          | `Ctrl` + `A`  |


## <span data-ttu-id="5eb51-141">Менеджер IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5eb51-141">IndexedDB manager</span></span>

<span data-ttu-id="5eb51-142">С помощью вкладки **IndexedDB** можно проверять структурированные данные, хранящиеся на клиентском компьютере, и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="5eb51-142">Use the **IndexedDB** tab to inspect and manage the structured data stored locally on a client machine.</span></span> <span data-ttu-id="5eb51-143">В частности, вы можете проверить или отсортировать и обновить хранилища объектов и индексы, а также удалить отдельные записи ключа.</span><span class="sxs-lookup"><span data-stu-id="5eb51-143">Specifically, you can inspect/sort and refresh your object stores and indices, and also delete individual key-value entries.</span></span>

> [!TIP]
> <span data-ttu-id="5eb51-144">Вы можете использовать нашу демонстрацию [микшера звука](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) для тестирования *IndexedDB Manager* в Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="5eb51-144">You can use our [Audio Mixer](https://developer.microsoft.com/microsoft-edge/testdrive/demos/audiomixer/) demo to test drive the *IndexedDB manager* in Microsoft Edge DevTools.</span></span>

<span data-ttu-id="5eb51-145">Чтобы удалить все данные IndexedDB, сохраненные для текущего пользователя в Microsoft EDGE, используйте меню " *Параметры* Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="5eb51-145">To delete all the IndexedDB data stored for the current user in Microsoft Edge, use the Microsoft Edge *Settings* menu:</span></span>

<span data-ttu-id="5eb51-146">**...** >  **Параметры**  >  **Очистка данных браузера**  >  **Файлы cookie и сохраненные данные веб-сайтов**</span><span class="sxs-lookup"><span data-stu-id="5eb51-146">**...** > **Settings** > **Clear browsing data** > **Cookies and saved website data**</span></span>

<span data-ttu-id="5eb51-147">Папка **IndexedDB** в [*средстве выбора ресурсов*](./debugger.md#resource-picker) отладчика отображает список источников происхождения из ресурсов, загруженных страницей.</span><span class="sxs-lookup"><span data-stu-id="5eb51-147">The **IndexedDB** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="5eb51-148">Любые базы данных IndexedDB (IDB) будут указаны в исходном виде, а также их хранилища объектов.</span><span class="sxs-lookup"><span data-stu-id="5eb51-148">Any IndexedDB (IDB) databases will be listed under the origin, along with their object stores.</span></span> 

![Менеджер DevTools IndexedDB](./media/storage_indexeddb.png)

### <span data-ttu-id="5eb51-150">Панель инструментов IndexedDB</span><span class="sxs-lookup"><span data-stu-id="5eb51-150">IndexedDB Toolbar</span></span>

<span data-ttu-id="5eb51-151">На панели инструментов *IndexedDB* вы можете:</span><span class="sxs-lookup"><span data-stu-id="5eb51-151">From the *IndexedDB* toolbar you can:</span></span>

 - <span data-ttu-id="5eb51-152">**Refresh** ( `Ctrl+F5` ) для просмотра текущих записей в хранилище объектов или индексе базы данных.</span><span class="sxs-lookup"><span data-stu-id="5eb51-152">**Refresh** (`Ctrl+F5`) to see the current entries in the object store or index of your database.</span></span> <span data-ttu-id="5eb51-153">После внесения изменений в базу данных руководитель IndexedDB не будет автоматически обновляться.</span><span class="sxs-lookup"><span data-stu-id="5eb51-153">The IndexedDB manager does not auto-refresh when changes are made to your database.</span></span>

### <span data-ttu-id="5eb51-154">Список записей в хранилище объектов</span><span class="sxs-lookup"><span data-stu-id="5eb51-154">Object store entries list</span></span>

<span data-ttu-id="5eb51-155">Из *хранилища объектов* или таблицы *индексов* можно выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5eb51-155">From the *Object store* or *Index* table you can:</span></span>

 - <span data-ttu-id="5eb51-156">Для **проверки и сортировки** пар "ключ-значение" щелкните любое имя столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="5eb51-156">**Inspect and sort** your key-value pairs by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="5eb51-157">**Refresh** ( `Ctrl+F5` )</span><span class="sxs-lookup"><span data-stu-id="5eb51-157">**Refresh** (`Ctrl+F5`)</span></span>
 - <span data-ttu-id="5eb51-158">**Удалить элемент** ( `Del` ), чтобы удалить выбранный элемент из хранилища объектов или предметного указателя.</span><span class="sxs-lookup"><span data-stu-id="5eb51-158">**Delete item** (`Del`) to remove the selected entry in your object store or index.</span></span> <span data-ttu-id="5eb51-159">Вы также можете сделать это с помощью [контекстного меню](#context-menu) правой кнопкой мыши, а затем *удалить элемент*.</span><span class="sxs-lookup"><span data-stu-id="5eb51-159">You can also do this from the right-click [context menu](#context-menu) option, *Delete item*.</span></span>
 - <span data-ttu-id="5eb51-160">**Копировать выделенные элементы** ( `Ctrl+C` ), чтобы скопировать выделенный элемент в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="5eb51-160">**Copy selected items** (`Ctrl+C`) to copy the selected item to your clipboard.</span></span> <span data-ttu-id="5eb51-161">Вы также можете сделать это с помощью [контекстного меню](#context-menu) правой кнопкой мыши и *выбрать команду Копировать выбранный элемент*.</span><span class="sxs-lookup"><span data-stu-id="5eb51-161">You can also do this from the right-click [context menu](#context-menu) option, *Copy selected item*.</span></span>
 - <span data-ttu-id="5eb51-162">**Выберите все** ( `Ctrl+A` ), чтобы выбрать все записи в хранилище объектов или предметном указателе.</span><span class="sxs-lookup"><span data-stu-id="5eb51-162">**Select all** (`Ctrl+A`) to select all the entries in your object store or index.</span></span> <span data-ttu-id="5eb51-163">Вы также можете сделать это в [контекстном меню](#context-menu) правой кнопкой мыши и *выбрать пункт Все*.</span><span class="sxs-lookup"><span data-stu-id="5eb51-163">You can also do this from the right-click [context menu](#context-menu) option, *Select all*.</span></span>

<span data-ttu-id="5eb51-164">Столбцы в *хранилище объектов* или таблице *индексов* можно сортировать:</span><span class="sxs-lookup"><span data-stu-id="5eb51-164">The columns of the *Object store* or *Index* table are sortable:</span></span>

<span data-ttu-id="5eb51-165">Столбец</span><span class="sxs-lookup"><span data-stu-id="5eb51-165">Column</span></span> | <span data-ttu-id="5eb51-166">Описание</span><span class="sxs-lookup"><span data-stu-id="5eb51-166">Description</span></span>
:------------ | :-------------
<span data-ttu-id="5eb51-167">Раздел</span><span class="sxs-lookup"><span data-stu-id="5eb51-167">Key</span></span> | <span data-ttu-id="5eb51-168">Имя пары "ключ-значение" (то же, что и *первичный ключ*) при итерации по хранилищу объектов; Имя ключа индекса (Текущая клавиша курсора) при итерации по индексу.</span><span class="sxs-lookup"><span data-stu-id="5eb51-168">Name of the key-value pair (same as *Primary Key*) when iterating over an object store; Name of the index key (cursor's current key) when iterating over an index</span></span>
<span data-ttu-id="5eb51-169">Первичный ключ</span><span class="sxs-lookup"><span data-stu-id="5eb51-169">Primary Key</span></span> | <span data-ttu-id="5eb51-170">Имя пары "ключ-значение" (Дополнительные сведения о [ключах](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database)IDB см *MDN в веб-документах* .)</span><span class="sxs-lookup"><span data-stu-id="5eb51-170">Name of the key-value pair (see *MDN web docs* for more on IDB [keys](https://developer.mozilla.org/docs/Web/API/IndexedDB_API/Using_IndexedDB#Structuring_the_database))</span></span>
<span data-ttu-id="5eb51-171">Значение</span><span class="sxs-lookup"><span data-stu-id="5eb51-171">Value</span></span> | <span data-ttu-id="5eb51-172">Значение пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="5eb51-172">Value of the key-value pair</span></span>

<span data-ttu-id="5eb51-173">Узнайте больше о [концепциях и использовании](https://developer.mozilla.org/docs/Web/API/IndexedDB_API) *MDN в веб-документах* для IndexedDB.</span><span class="sxs-lookup"><span data-stu-id="5eb51-173">Check out *MDN web docs* for more on [IndexedDB concepts and usage](https://developer.mozilla.org/docs/Web/API/IndexedDB_API).</span></span>

### <span data-ttu-id="5eb51-174">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="5eb51-174">Context menu</span></span>

<span data-ttu-id="5eb51-175">В дополнение к [панели инструментов *IndexedDB* ](#indexeddb-toolbar)можно также управлять данными в хранилищах объектов или индексами в **контекстном меню** и/или с помощью сочетаний [клавиш](#shortcuts).</span><span class="sxs-lookup"><span data-stu-id="5eb51-175">In addition to the [*IndexedDB* toolbar](#indexeddb-toolbar), you can also manage your data in object stores or indices from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="5eb51-176">Горячие</span><span class="sxs-lookup"><span data-stu-id="5eb51-176">Shortcuts</span></span>

<span data-ttu-id="5eb51-177">Действие</span><span class="sxs-lookup"><span data-stu-id="5eb51-177">Action</span></span> | <span data-ttu-id="5eb51-178">Появивше</span><span class="sxs-lookup"><span data-stu-id="5eb51-178">Shortcut</span></span>
:------------ | :-------------
<span data-ttu-id="5eb51-179">Обновить</span><span class="sxs-lookup"><span data-stu-id="5eb51-179">Refresh</span></span> | `Ctrl` + `F5`
<span data-ttu-id="5eb51-180">Удаление пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="5eb51-180">Delete key-value pair</span></span> | `Del`
<span data-ttu-id="5eb51-181">Копирование выделенных элементов</span><span class="sxs-lookup"><span data-stu-id="5eb51-181">Copy selected items</span></span> | `Ctrl` + `C`
<span data-ttu-id="5eb51-182">Выделить все</span><span class="sxs-lookup"><span data-stu-id="5eb51-182">Select all</span></span> | `Ctrl` + `A`

## <span data-ttu-id="5eb51-183">Диспетчер cookie-файлов</span><span class="sxs-lookup"><span data-stu-id="5eb51-183">Cookies manager</span></span>

<span data-ttu-id="5eb51-184">Используйте *Диспетчер файлов cookie* для проверки и управления файлами cookie для данного домена.</span><span class="sxs-lookup"><span data-stu-id="5eb51-184">Use the *Cookies manager* to inspect and manage the cookies for the given domain.</span></span> 

<span data-ttu-id="5eb51-185">В папке **cookies** в [*средстве выбора ресурсов*](./debugger.md#resource-picker) отладчика отображается список происхождения из ресурсов, загруженных страницей.</span><span class="sxs-lookup"><span data-stu-id="5eb51-185">The **Cookies** folder inside the Debugger's [*Resource picker*](./debugger.md#resource-picker) displays a list of origins from the resources loaded by the page.</span></span> <span data-ttu-id="5eb51-186">При выборе одного из этих фреймов открывается таблица, представляющая текущие файлы cookie, заданные заголовком [http](https://developer.mozilla.org/docs/Web/HTTP/Cookies) или сценарием с помощью [файла Document. cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span><span class="sxs-lookup"><span data-stu-id="5eb51-186">Selecting one of these frames opens up a table representing the current cookies set by either [HTTP](https://developer.mozilla.org/docs/Web/HTTP/Cookies) header or via script with [Document.cookie](https://developer.mozilla.org/docs/Web/API/Document/cookie).</span></span>

![Диспетчер DevTools cookies](./media/storage_cookies.png)

<span data-ttu-id="5eb51-188">На панели инструментов вкладки " *cookie* " можно выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="5eb51-188">From the *Cookies* tab toolbar you can:</span></span>

 - <span data-ttu-id="5eb51-189">**Обновите** ( `Ctrl+F5` ) [список cookies](#cookies-list) , чтобы просмотреть текущий набор cookie-файлов для данного домена.</span><span class="sxs-lookup"><span data-stu-id="5eb51-189">**Refresh** (`Ctrl+F5`) the [Cookies list](#cookies-list) to see the current set of cookies for the given domain.</span></span> <span data-ttu-id="5eb51-190">(Список не обновляется автоматически).</span><span class="sxs-lookup"><span data-stu-id="5eb51-190">(The list does not auto-refresh.)</span></span>
 - <span data-ttu-id="5eb51-191">**Удалите все файлы cookie** ( `Ctrl+Shift+Del` ) (сеанс и постоянный) для пути к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="5eb51-191">**Delete all cookies** (`Ctrl+Shift+Del`) (session and permanent) for the path of the current page.</span></span>
 - <span data-ttu-id="5eb51-192">**Удалите все cookie-файлы сеанса** ( `Ctrl+Del` ) для пути к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="5eb51-192">**Delete all session cookies** (`Ctrl+Del`) for the path of the current page.</span></span>

<span data-ttu-id="5eb51-193">Для полного удаления *списка cookie*-файлов вам может потребоваться **удалить все cookie-файлы для домена** на панели инструментов " [**сеть**](./network.md#toolbar) ".</span><span class="sxs-lookup"><span data-stu-id="5eb51-193">To completely clear your *Cookies list*, you might need to **Clear all cookies for the domain** from the [**Network**](./network.md#toolbar) panel toolbar.</span></span>

### <span data-ttu-id="5eb51-194">Список cookie-файлов</span><span class="sxs-lookup"><span data-stu-id="5eb51-194">Cookies list</span></span>

<span data-ttu-id="5eb51-195">В таблице *cookie List* можно выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5eb51-195">From the *Cookies list* table you can:</span></span>

 - <span data-ttu-id="5eb51-196">**Проанализировать и отсортировать** файлы cookie, щелкнув любое имя столбца в таблице.</span><span class="sxs-lookup"><span data-stu-id="5eb51-196">**Inspect and sort** your cookies by clicking on any column name in the table.</span></span>
 - <span data-ttu-id="5eb51-197">**Измените** *имя* и *значение* существующего файла cookie, щелкнув ячейку.</span><span class="sxs-lookup"><span data-stu-id="5eb51-197">**Edit** the *Name* and *Value* of an existing cookie by clicking in the cell.</span></span>
 - <span data-ttu-id="5eb51-198">**Удалить** ( `Del` ) файл cookie из [контекстного меню](#context-menu) правой кнопкой мыши *удалить файл cookie*.</span><span class="sxs-lookup"><span data-stu-id="5eb51-198">**Delete** (`Del`) a cookie from the right-click [context menu](#context-menu) option, *Delete cookie*.</span></span>
 - <span data-ttu-id="5eb51-199">**Добавьте** новый файл cookie сеанса для указанного *домена или пути* , щелкнув пустую строку в нижней части таблицы.</span><span class="sxs-lookup"><span data-stu-id="5eb51-199">**Add** a new session cookie for the given *Domain/Path* by clicking on the empty row at the bottom of the table.</span></span> <span data-ttu-id="5eb51-200">Это работает только для cookie-файлов сеансов. постоянные файлы cookie (с определенными датами истечения срока действия) должны быть установлены с традиционными методами.</span><span class="sxs-lookup"><span data-stu-id="5eb51-200">This only works for session cookies; permanent cookies (with specific expiry dates) must be set with traditional methods.</span></span> <span data-ttu-id="5eb51-201">Значения *домена* и *пути* автоматически заполняются в соответствии с расположением страницы.</span><span class="sxs-lookup"><span data-stu-id="5eb51-201">The *Domain* and *Path* values are auto-filled according to the location of the page.</span></span>

<span data-ttu-id="5eb51-202">Столбцы в *списке cookie-файлов* доступны для сортировки:</span><span class="sxs-lookup"><span data-stu-id="5eb51-202">The columns of the *Cookies list* are sortable:</span></span>

<span data-ttu-id="5eb51-203">Столбец</span><span class="sxs-lookup"><span data-stu-id="5eb51-203">Column</span></span> | <span data-ttu-id="5eb51-204">Описание</span><span class="sxs-lookup"><span data-stu-id="5eb51-204">Description</span></span>
:------------ | :-------------
<span data-ttu-id="5eb51-205">Name</span><span class="sxs-lookup"><span data-stu-id="5eb51-205">Name</span></span> | <span data-ttu-id="5eb51-206">Имя cookie-файла</span><span class="sxs-lookup"><span data-stu-id="5eb51-206">Name of the cookie</span></span>
<span data-ttu-id="5eb51-207">Значение</span><span class="sxs-lookup"><span data-stu-id="5eb51-207">Value</span></span> | <span data-ttu-id="5eb51-208">Значение cookie-файла</span><span class="sxs-lookup"><span data-stu-id="5eb51-208">Value of the cookie</span></span>
<span data-ttu-id="5eb51-209">Домен</span><span class="sxs-lookup"><span data-stu-id="5eb51-209">Domain</span></span> | <span data-ttu-id="5eb51-210">Имя узла cookie-файла (может быть пустым)</span><span class="sxs-lookup"><span data-stu-id="5eb51-210">Host name of the cookie (may be empty)</span></span>
<span data-ttu-id="5eb51-211">Путь</span><span class="sxs-lookup"><span data-stu-id="5eb51-211">Path</span></span> | <span data-ttu-id="5eb51-212">URL-путь для файла cookie (может быть пустым)</span><span class="sxs-lookup"><span data-stu-id="5eb51-212">URL path for the cookie (may be empty)</span></span>
<span data-ttu-id="5eb51-213">Срок действия истекает</span><span class="sxs-lookup"><span data-stu-id="5eb51-213">Expires</span></span> | <span data-ttu-id="5eb51-214">Максимальное время существования cookie в качестве метки времени HTTP-даты.</span><span class="sxs-lookup"><span data-stu-id="5eb51-214">Maximum lifetime of the cookie as an HTTP-date timestamp.</span></span> <span data-ttu-id="5eb51-215">Если `Expires` значение не `Max-Age` задано, запись считается файлом cookie *сеанса* .</span><span class="sxs-lookup"><span data-stu-id="5eb51-215">If no `Expires` or `Max-Age` was set, the entry is considered a *Session* cookie.</span></span>
<span data-ttu-id="5eb51-216">Только HTTP</span><span class="sxs-lookup"><span data-stu-id="5eb51-216">HTTP only</span></span> | <span data-ttu-id="5eb51-217">Указывает, был ли для файла cookie задана `HttpOnly` директива, указывающая на то, что он недоступен из JavaScript</span><span class="sxs-lookup"><span data-stu-id="5eb51-217">Indicates if the cookie was set with `HttpOnly` directive, indicating that it is inaccessible from JavaScript</span></span>
<span data-ttu-id="5eb51-218">Защита</span><span class="sxs-lookup"><span data-stu-id="5eb51-218">Secure</span></span> | <span data-ttu-id="5eb51-219">Указывает, был ли в качестве файла cookie указана `Secure` директива, указывающая на то, что она будет отправлена на сервер из запроса с помощью SSL и протокола HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5eb51-219">Indicates if the cookie was set with the `Secure` directive, indicating it will only be sent to the server from a request using SSL and the HTTPS protocol.</span></span>

<span data-ttu-id="5eb51-220">Дополнительные сведения о свойствах файлов cookie вы увидите в разделе **MDN Web doc** [Set-cookies](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) .</span><span class="sxs-lookup"><span data-stu-id="5eb51-220">See the **MDN web docs** [Set-Cookie](https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie) reference for further details on cookie properties.</span></span>

### <span data-ttu-id="5eb51-221">Контекстное меню</span><span class="sxs-lookup"><span data-stu-id="5eb51-221">Context menu</span></span>

<span data-ttu-id="5eb51-222">Помимо вкладки *cookies* , вы [toolbar](#cookies-manager)также можете управлять файлами cookie с помощью **контекстного меню** и (или) сочетаний [клавиш](#shortcuts).</span><span class="sxs-lookup"><span data-stu-id="5eb51-222">In addition to the *Cookies* tab [toolbar](#cookies-manager), you can also manage your cookies from the right-click **Context menu** and/or the keyboard [shortcuts](#shortcuts).</span></span>

### <span data-ttu-id="5eb51-223">Горячие</span><span class="sxs-lookup"><span data-stu-id="5eb51-223">Shortcuts</span></span>

| <span data-ttu-id="5eb51-224">Действие</span><span class="sxs-lookup"><span data-stu-id="5eb51-224">Action</span></span>                     | <span data-ttu-id="5eb51-225">Появивше</span><span class="sxs-lookup"><span data-stu-id="5eb51-225">Shortcut</span></span>                 |
|:---------------------------|:-------------------------|
| <span data-ttu-id="5eb51-226">Обновить</span><span class="sxs-lookup"><span data-stu-id="5eb51-226">Refresh</span></span>                    | `Ctrl` + `F5`            |
| <span data-ttu-id="5eb51-227">Удаление файла cookie</span><span class="sxs-lookup"><span data-stu-id="5eb51-227">Delete cookie</span></span>              | `Del`                    |
| <span data-ttu-id="5eb51-228">Удаление всех файлов cookie</span><span class="sxs-lookup"><span data-stu-id="5eb51-228">Delete all cookies</span></span>         | `Ctrl` + `Shift` + `Del` |
| <span data-ttu-id="5eb51-229">Удаление всех файлов cookie сеанса</span><span class="sxs-lookup"><span data-stu-id="5eb51-229">Delete all session cookies</span></span> | `Ctrl` + `Del`           |
| <span data-ttu-id="5eb51-230">Копирование выделенных элементов</span><span class="sxs-lookup"><span data-stu-id="5eb51-230">Copy selected items</span></span>        | `Ctrl` + `C`             |
| <span data-ttu-id="5eb51-231">Выделить все</span><span class="sxs-lookup"><span data-stu-id="5eb51-231">Select all</span></span>                 | `Ctrl` + `A`             |

### <span data-ttu-id="5eb51-232">Диспетчер кэша</span><span class="sxs-lookup"><span data-stu-id="5eb51-232">Cache manager</span></span>

<span data-ttu-id="5eb51-233">При нажатии на определенную запись кэша откроется диспетчер **кэша** рабочих процессов служб, в котором можно проверить и при необходимости удалить записи кэша (пары ключ-значение для*запроса* и *ответа* ).</span><span class="sxs-lookup"><span data-stu-id="5eb51-233">Clicking on a specific cache entry will open up the service worker **Cache** manager, where you can inspect and optionally delete cache entries (*Request* and *Response* key/value pairs):</span></span>

![Диспетчер кэша](./media/storage_cache.png)

### <span data-ttu-id="5eb51-235">Горячие</span><span class="sxs-lookup"><span data-stu-id="5eb51-235">Shortcuts</span></span>

#### <span data-ttu-id="5eb51-236">Диспетчер кэша</span><span class="sxs-lookup"><span data-stu-id="5eb51-236">Cache manager</span></span>

| <span data-ttu-id="5eb51-237">Действие</span><span class="sxs-lookup"><span data-stu-id="5eb51-237">Action</span></span>              | <span data-ttu-id="5eb51-238">Появивше</span><span class="sxs-lookup"><span data-stu-id="5eb51-238">Shortcut</span></span>      |
|:--------------------|:--------------|
| <span data-ttu-id="5eb51-239">Обновить</span><span class="sxs-lookup"><span data-stu-id="5eb51-239">Refresh</span></span>             | `Ctrl` + `F5` |
| <span data-ttu-id="5eb51-240">Удалить элемент</span><span class="sxs-lookup"><span data-stu-id="5eb51-240">Delete item</span></span>         | `Del`         |
| <span data-ttu-id="5eb51-241">Копирование выделенных элементов</span><span class="sxs-lookup"><span data-stu-id="5eb51-241">Copy selected items</span></span> | `Ctrl` + `C`  |
| <span data-ttu-id="5eb51-242">Выделить все</span><span class="sxs-lookup"><span data-stu-id="5eb51-242">Select all</span></span>          | `Ctrl` + `A`  |
